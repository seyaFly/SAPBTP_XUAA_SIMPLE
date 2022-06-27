### 目录
- [目录](#目录)
  - [摘要](#摘要)
  - [部署](#部署)
  - [参考](#参考)

#### 摘要
该demo的主要目标是建立两个应用程序， approuter 和 productlist ， 用户通过访问approouter 来实现对productlist applicaiton 进行安全认证。认证方式采用oauth + SAP IDP , 用户可通过登录SAPBTP的用户方式来登录并访问productlist applciation

#### 部署

部署采用cloud foundry命令行来实现, 开发人员进入到product-list文件夹，并使用以下命令行部署

```
cf api <api endpoint>
cf login
cf create-service xsuaa application xsuaa-service-tutorial -c security/xs-security.json  //创建xuaa servervice
cf push

```

#### 参考

* [SAP Authorization and Trust Management 服务 教程](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/902ae800c1d04c7388e407b7815e5cc8.html)
* [cp-cf-security-xsuaa](https://developers.sap.com/tutorials/cp-cf-security-xsuaa-create.html)
* [sap xuaa pilot app](https://github.com/SAP-samples/teched2019-cloud-cf-product-list/tree/sap-tutorial-xsuaa)