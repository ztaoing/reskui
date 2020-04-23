# 架构
    用户接口层（apis）：用户接口层用来存储协议， 网络交互适配层相关的代码
* -web：存放web接口
  1. account.go
  2. envelopo.go
  
* -thrift

    
-------

    应用层（services）：封装了所有的业务逻辑
* 结构
  1. accounts.go
  2. envelopes.go

-------
    核心领域层（core）：存放业务逻辑的代码，是业务系统的核心。包含一个或多个核心业务领域
* 用于业务领域 users
* 红包业务领域 envelopes
  1. po_goods.go 商品订单
  2. po_item.go 商品详情
  3. dao_goods.go 商品数据库
  4. dao_item.go 商品详情
  5. domain_goods.go
  6. domain_item.go
  7. domains.go
  
  
* 账户业务领域 accounts
  1. po_account.go 持久结构体文件
  2. po_account_log.go 账户流水
  1. dao_account.go
  2. dao_account_log.go
  1. domain_account.go
  2. domain_account_log.go
  3. domains.go
  1. service.go

-------
    基础设施层（infra）：存放数据库、缓存、消息队列、算法、工具函数等，和业务无关的基础代码
    
-------
    doc：存储项目文档
    
-------
    brun:存储项目的main函数和其他相关工具以及相关文件的内容，编译之后的二进制代码都在这里运行
1. main.go
-------
    public：存放css、js、图片、html模板、静态文件
    
------- 
1. core 核心应用层、领域、持久层
2. apis :用户接口层
3. brun :应用程序
4. doc :文档
5. infra :基础设施
6. services :应用层接口：应用服务# reskui
