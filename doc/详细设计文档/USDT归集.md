# usdt归集流程

## 1 usdt抵押赎回

#### 1.1 usdt归集主流程图
```mermaid
graph TD
    A[开始]--> B(定时任务 检测用户钱包余额)
    B --> C{归集金额是否大于限定值}
    C -->|是| F{判断归集比例}
    C -->|否| D{是否存在待归集列表中}
    D -->|是| F
    D -->|否| B
    F -->|热钱包比例小于5%| G[归集到热钱包]
    F -->|热钱包比例大于5%| H[归集到冷钱包]
    H --> I[结束]
    G --> I[结束]
```
<center>usdt归集主流程图</center>

#### 1.2 usdt归集流程图
```mermaid
graph LR
    A[开始]--> B(系统归集)
    B --> C{钱包余额是否大于归集限定值}
    C -->|是| D(加入归集队列.修改帐号归集金额)
    C -->|否| F{判断系统内外转账}
    F -->|转账到系统外| G{判断钱包余额是否足够}
    F -->|转账到系统内| O{被归集金额是否足够}
    O -->|足够| P(修改双方帐号金额.归集金额)
    O -->|不足| Q(归集清零.再修改双方帐号金额.归集金额)
    P --> Z[结束]
    Q --> Z[结束]
    G -->|余额足够| H{判断是否正在被归集.确认数不足}
    H -->|是| J{判断归集金额是否足够}
    J -->|是| L(走系统热钱包转账.不归集)
    J -->|否| N(归集清零.在走系统热钱包转账)
    L --> Z[结束]
    N --> Z[结束]
    H -->|否| K(帐号钱包转账.不归集)
    K --> Z[结束]
    G -->|余额不足| M(加入归集队列.先归集.先修改帐号归集金额.系统热钱包转账)
    M --> Z
    D --> Z[结束]

```
<center>usdt归集流程图</center>

## 附：
1. 钱包余额 = 帐号可用金额 + 冻结金额 + 抵押金额 - 被系统归集金额 - 帐号转出金额(包括系统内，系统外转账)
2. 转账申请总金额 = 冻结金额
3. 发起提现申请时可提现金额 <= 帐号可用金额
4. 提现审批时可转账金额 <= 帐号被冻结的金额

