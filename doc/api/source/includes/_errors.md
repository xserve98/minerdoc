# 业务错误码说明

业务错误码存储于 Response body 中的Json 结构的"code"中，目前已定义的业务错误码如下：

| 错误码 | 描述 | 备注 |
| :------ | :------ | :------ |	
| 0 | UNKNOWN | zh : 未知错误<br> |
| 1 | DB | zh : 数据库操作错误<br> |
| 2 | REDIS | zh : redis操作错误<br> |
| 3 | DECODE_FAILED | zh : 解码失败<br> |
| 4 | GEN_ID | zh : 生成唯一标识失败<br> |
| 5 | PARAM_FAILED | zh : 获取参数失败<br> |
| 6 | ENCODE_FAILED | zh : 编码失败<br> |
| 200 | SUCCESS |  |
| 201 | NO_LOGIN | zh : 请先登录<br> |
| 202 | PARAMS_ERROR | zh : 参数错误<br> |
| 203 | NO_USER | zh : 用户不存在<br> |
| 204 | CAPTCHA_ERR | zh : 验证码错误<br> |
| 205 | SMS_ERR | zh : 短信验证码错误<br> |
| 206 | MOBILE_ERR | zh : 手机号错误<br> |
| 207 | SMS_SEND_FAIL | zh : 短信验证码发送失败<br> |
| 208 | SMS_VERIFY_FAIL_TOO_MATH | zh : 短信验证码验证失败次数太多，请重新获取短信<br> |
| 209 | TOKEN_ERR | zh : Token生成失败<br> |
| 210 | CLIENT_TYPE_UNKOWN | zh : 客户端类型未知<br> |
| 211 | NO_AUTH | zh : 没有权限<br> |
| 212 | USER_NO_ACTIVE | zh : 用户未激活<br> |
| 213 | TOKEN_VERIFY_ERR | zh : 登录TOKEN验证失败，请重新登录<br> |
| 214 | SIGNATURE_VERIFY_ERR | zh : 登录签名认证失败，请重新登录<br> |
| 400 | PAYMENT_METHOD_UNSUPPORTED | zh : 不支持的收付款类型<br> |
| 401 | PAYMENT_METHOD_CHANGE_STATUS_FAILED | zh : 修改收付款方式状态失败<br> |
| 402 | PAYMENT_METHOD_EDIT_FAILED | zh : 编辑收付款方式失败<br> |
| 403 | PAYMENT_METHOD_EDIT_NOTHING | zh : 收付款方式属性无修改<br> |
| 404 | PAYMENT_METHOD_OWNER_ERROR | zh : 非该收付款方式拥有者<br> |
| 600 | ACCOUNT_NO_FOUND | zh : usdt账户不存在<br> |
| 601 | PRI_KEY_NO_FOUND | zh : usdt账户对应的密钥不存在<br> |
| 602 | ADDRESS_UNAVAILABLE | zh : usdt地址不可用<br> |
| 603 | TRANSFER_FAILED | zh : usdt转账失败<br> |
| 604 | NO_ENOUGH | zh : usdt余额不足<br> |
| 605 | MORTGAGE_FAILED | zh : usdt抵押失败<br> |
| 606 | BALANCE_INVALID | zh : usdt资产数据不可用<br> |
| 607 | CURRENCY_PARAM_ERROR | zh : usdt金额参数错误<br> |
| 608 | RELEASE_FAILED | zh : usdt赎回失败<br> |
| 609 | CHAIN_BALANCE_ERROR | zh : usdt链上账户数据错误<br> |
| 610 | CHAIN_TRANSACTION_ERROR | zh : usdt链上交易数据错误<br> |
| 611 | CHAIN_SYNC_TOO_FREQUENTLY | zh : usdt同步链上交易数据过于频繁<br> |
| 612 | CALC_BALANCE_FAILED | zh : usdt演算账户金额失败<br> |
| 613 | GET_SIGNED_TX_FAILED | zh : usdt获取离线签名交易数据失败<br> |
| 800 | QUERY_AGENT_FAILED | zh : 查询用户代理信息失败<br> |
| 801 | QUERY_AGENT_INVITE_CODE_FAILED | zh : 查询用户邀请码信息失败<br> |
| 802 | AGENT_DECREASE_COMMISSION_FAILED | zh : 扣除用户佣金失败<br> |
| 803 | AGENT_WITHDRAW_ADD_RECORD_FAILED | zh : 增加佣金提现记录失败<br> |
| 804 | AGENT_WITHDRAW_UPDATE_RECORD_STATUS_FAILED | zh : 更新佣金提现记录状态失败<br> |
| 805 | AGENT_WITHDRAW_QUERY_RECORD_FAILED | zh : 查询佣金提现记录失败<br> |
| 1001 | USER_REGISTERED | zh : 用户已经注册过<br> |
| 1002 | REGISTER_ERR | zh : 注册失败<br> |
| 1500 | OTC_APPLY_EXCHANGER_PENDING | zh : 你的申请正在处理中<br> |
| 1501 | OTC_NOT_FOUND_EXCHANGER | zh : 没有找到承兑商<br> |
| 1502 | OTC_TRADE_TOO_SMALL | zh : 设置的交易金额太小<br> |
| 1503 | OTC_LACK_AVAILABLE_TO_SELL | zh : 可以出售的EUSD太少了<br> |
| 1504 | OTC_DAY_LIMIT_SELL | zh : 达到今日出售限额<br> |
| 1505 | OTC_ORDER_NOT_FOUND | zh : 没有找到订单<br> |
| 1506 | OTC_ORDER_CANNOT_CANCEL | zh : 订单不能取消<br> |
| 1507 | OTC_ORDER_STATUS_ERR | zh : 订单状态异常<br> |
| 1508 | OTC_BUY_LOWER_LIMIT | zh : 购买达到限额<br> |
| 1509 | OTC_SETTING_ERR | zh : 设置失败<br> |
| 1510 | OTC_PAY_TYPE_EMPTY | zh : 支付方式为空<br> |
| 1511 | OTC_PAY_TYPE_ERR | zh : 支付方式错误<br> |
| 1512 | OTC_NOT_MATCH_EXCHANGER | zh : 没有找到合适的承兑商<br> |
| 1513 | OTC_TRADE_TOO_BIG | zh : 交易金额超过限额<br> |
| 1514 | OTC_PAYMENT_NOT_FOUND | zh : 未找到收付款方式<br> |
| 1515 | OTC_LACK_PAYMENT | zh : 缺少支付方式或者支付方式都已经达到限额了<br> |
| 1516 | OTC_ACCOUNT_LOCK | zh : 账号被锁定<br> |
| 1517 | OTC_NOT_A_EXCHANGER | zh : 你不是一个承兑商<br> |
| 1518 | OTC_TRANSFER_AVAILABLE_LACK | zh : 余额不足<br> |
| 2001 | SIGN_TRANSACTION_FAIL | zh : 交易签名失败<br> |
| 2002 | GET_BLOCK_INFO_ERROR | zh : 获取区块信息失败<br> |
| 2003 | PUSH_TRANSACTION_ERROR | zh : 推送交易失败<br> |
| 2004 | ACTION_TO_ABI_ERROR | zh : 转换ABI失败<br> |
| 2005 | BUY_RAM_TO_ABI_ERROR | zh : 购买RAM转换ABI失败<br> |
| 2006 | DELEGATE_TO_ABI_ERROR | zh : 抵押转换ABI失败<br> |
| 2007 | NEW_ACCOUNT_TO_ABI_ERROR | zh : 创建账号转换ABI失败<br> |
| 2008 | UNDELEGATE_TO_ABI_ERROR | zh : 赎回转换ABI失败<br> |
| 2009 | BIND_WALLET_ERROR | zh : 绑定钱包失败<br> |
| 2010 | CREATE_ACCOUNT_ERR | zh : 生成新钱包账号失败<br> |
| 2011 | UID_PARAMS_ERROR | zh : UID 参数错误<br> |
| 2012 | TRANSFER_LACK_AVAILABLE | zh : 可用TOKEN不足<br> |
| 2013 | TRANSFER_FAIL_LOCK | zh : 转账锁定失败，请重试<br> |
| 2014 | CONFIG_LACK | zh : 配置信息缺失<br> |
| 2015 | TRANSFER_DB_OUT | zh : 出账失败（DB）<br> |
| 2016 | TRANSFER_DB_INTO | zh : 入账失败（DB）<br> |
| 2017 | USER_OTC_ABLE | zh : 用户成为承兑商错误<br> |
| 2018 | WEALTH_LOCK | zh : 账户被冻结<br> |
| 2019 | QUANTITY_ERR | zh : 数量不正确<br> |
| 2020 | EUSD_LACK | zh : 币数量不足<br> |
| 2021 | WEALTH_NOT_FOUND | zh : 未找到账号信息<br> |
| 2022 | WEALTH_OTC_TRANSFER | zh : 划转失败<br> |
| 2023 | OTC_TRANSFER_LOCK | zh : OTC冻结资金失败<br> |
| 2024 | OTC_TRANSFER_UNLOCK | zh : OTC解冻资金失败<br> |
| 2025 | OTC_TRANSFER_OUT | zh : OTC转账失败<br> |
| 2026 | OTC_SET_SELL | zh : 设置出售失败，请重试<br> |
| 2027 | OTC_SET_BUY | zh : 设置买入失败，请重试<br> |
| 2028 | OTC_NOT_EXCHANGER | zh : 用户不是承兑商<br> |
| 2500 | GAME_LOGIN_FAILED | zh : 游戏登录失败<br> |
| 2501 | GAME_ADD_USER_FAILED | zh : 增加游戏账户失败<br> |
| 2502 | GAME_USER_NO_EXIST | zh : 游戏账户不存在<br> |
| 2503 | GAME_ADD_REDEEM_LOG_FAILED | zh : 增加游戏转账记录失败<br> |
| 2504 | GAME_REDEEM_IN_FAILED | zh : 游戏账户存款失败<br> |
| 2505 | GAME_REDEEM_OUT_FAILED | zh : 游戏账户提款失败<br> |
| 2506 | GAME_ONLINE_PLAYERS_FAILED | zh : 查询游戏在线玩家失败<br> |
| 2507 | GAME_PLAYER_NOT_OFFLINE | zh : 游戏玩家当前在线<br> |
| 2508 | GAME_BALANCE_FALIED | zh : 获取游戏玩家余额信息失败<br> |