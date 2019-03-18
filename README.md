# 目录
> * [介绍](#chapter-1)
> * [整体架构](#chapter-2)
> * [各子系统介绍](#chapter-3)
> * [应用开发步骤](#chapter-4)

# 1. <a id="chapter-1"></a>介绍
WeBASE（WeBank Blockchain Application Software Extension） 是在区块链应用和底层之间搭建的一套通用组件，可以屏蔽区块链底层的复杂度，降低开发者的门槛，大幅提高区块链应用的开发效率。包含了节点前置、节点管理、上链代理和Web管理平台等子系统。开发者搭建完底层节点后，部署WeBASE，可大幅提升应用层的开发效率。

# 2. <a id="chapter-2"></a>整体架构

![[架构图]](./architecture.png)

# 3. <a id="chapter-3"></a>各子系统介绍
**1 webase-front (节点前置)**
集成web3jsdk；以HTTP接口的形式，和节点进行交互，如获取节点快高，部署合约，发送交易等；内置内存数据库，采集节点健康度数据；内置web控制台，实现节点的可视化操作；上报节点数据到指定服务。

**2 webase-transcation(交易上链代理)**
接收交易请求，缓存,异步上链。

**3 webase-node-mgr(节点管理)**
管理各个节点的状态；接收节点上报的数据，并存储；对区块链的数据进行统计、分析；交易审计；处理前端页面所有；web请求；私钥管理；管理区块链上所有的合约；

**4 webase-web(区块链管理平台)**
数据概览，可以查看机构、节点、合约、区块和交易详情；
节点管理：查看区块链上所有节点的状态；
合约管理：编辑、编译、部署、调试、测试合约；
私钥管理：管理各用户的公私钥；
系统监控：错误日志查看、各节点的监控数据查看；
交易审计：异常交易事后审计；

# 4. <a id="chapter-4"></a>应用开发步骤
1 部署WeBASE。

2 登录WeBASE管理平台，开发智能合约，编译、部署、测试合约。

3 配置私钥。

4 根据协议规范，组装HTTP包，发送交易。