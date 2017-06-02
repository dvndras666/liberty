---

copyright:
  years: 2015, 2017
lastupdated: "2017-03-23"

---

{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Liberty buildpack 的最新更新
{: #latest_updates}

## Liberty buildpack 中最新更新的列表。

### 2017 年 3 月 14 日：更新了 Liberty buildpack V3.8-20170308-1507

* 缺省 Liberty 运行时版本已更新为 17.0.0.1 发行版。
* 缺省 Liberty 运行时还包含 PI75512 WebSockets iFix。
* 每月 Liberty 运行时版本已更新为 [2017.2.0.0](https://developer.ibm.com/wasdev/blog/2017/02/17/beta-websphere-liberty-tools-february-2017/) 发行版。
* IBM JRE V8 和 V7.1 已更新为 SR4 FP1。
* 此外，自动配置支持还扩展为可用于 [ibm-websphere-extreme-scale IBM Container](https://console.ng.bluemix.net/docs/images/docker_image_extreme_scale/ibm-websphere-extreme-scale_starter.html)。
* [Cloudant NoSQL Database](https://console.ng.bluemix.net/docs/services/Cloudant/index.html) 的自动配置支持已更新为提供使用 Cloudant Java 库来代替 org.ektorp 的选项。要启用 Cloudant Java 库，必须设置以下环境变量：    
```
cf set-env <appName> LBP_SERVICE_CONFIG_CLOUDANTNOSQLDB 'type : cloudant'
```
* 该 buildpack 还提供了用于 [Auto-Scaling 服务](/docs/services/Auto-Scaling/index.html)的更新版本的代理程序以及若干应用程序管理增强功能。
* 该 buildpack 还更改了 [Monitoring and Analytics 服务](/docs/services/monana/index.html)的自动配置工作方式。使用免费套餐的应用程序不再向其应用程序添加日志功能；此功能将替换为 logmet。  


### 2017 年 1 月 23 日：更新了 Liberty buildpack V3.7-20170118-2046
* 每月 Liberty 运行时版本已更新为 [2017.1.0.0](https://developer.ibm.com/wasdev/blog/2017/01/20/beta-websphere-liberty-tools-january-2017/) 发行版。
* IBM JRE V8 已更新为 SR3 FP22 版本。
* 此外，[自动配置](autoConfig.html)支持还扩展为可用于 [Compose for MongoDB 服务](https://console.ng.bluemix.net/docs/services/ComposeForMongoDB/index.html)（目前仅每月 Liberty 运行时中可用）。

### 2016 年 12 月 13 日：更新了 Liberty buildpack V3.6-20161209-1351
* 缺省 Liberty 运行时版本已更新为 [16.0.0.4](http://www-01.ibm.com/support/docview.wss?uid=swg27009661) 发行版。
* IBM JRE V8 已更新为 SR3 FP21 版本。
* 此外，[自动配置](autoConfig.html)支持还扩展为可用于 [Compose for PostgreSQL 服务](https://console.ng.bluemix.net/docs/services/ComposeForPostgreSQL/index.html)。
* 该 buildpack 还提供了用于 [Auto-Scaling 服务](/docs/services/Auto-Scaling/index.html)的更新版本的代理程序。
* 该 buildpack 已更新为支持环境变量作为 `server.xml` 文件中 include location 的一部分。

### 2016 年 11 月 29 日：更新了 Liberty buildpack V3.5-20161114-1152
* 缺省 Liberty 运行时版本 `16.0.0.3` 已更新为包含 [PI62375](https://www-01.ibm.com/support/docview.wss?uid=swg24042712) iFix 并提供 `microProfile-1.0` 方便功能。
* 每月 Liberty 运行时版本已更新为 `2016.11.0.0` 发行版。
* 该 buildpack 还包含更新的 IBM JRE：V8 SR3 FP20 和 V7.1 SR3 FP60。
* DB2 JDBC 驱动程序已更新为 `4.21.29` 版本。
* Monitoring and Analytics 服务集成已修订，可与 [Diego ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://docs.cloudfoundry.org/concepts/diego/diego-architecture.html) 一起使用。
* [Dynatrace](dynatrace.html) 服务集成已更新，可更好地与 Dynatrace 服务产品一起使用。
* 对 PostgreSQL 和 MySQL 类型服务的[自动配置](autoConfig.html)支持已改进，在部署服务器目录或打包服务器时更好用。
* [devconsole 和 shell 应用程序管理实用程序](/docs/manageapps/app_mng.html#app_management)使用的 Node.js 运行时已更新为最新的 `0.12.17` 版本。
* 同时包括 Liberty 运行时的[安全修订](http://www.ibm.com/support/docview.wss?uid=swg21994945)。

### 2016 年 11 月 1 日：更新了 Liberty buildpack V3.4.1-20161030-2241
* 该 buildpack 包含启动特定类型应用程序时所发生问题的修订。具体来说，是使用 `dropins` 目录中的应用程序文件，将应用程序部署为服务器目录或打包服务器。

### 2016 年 10 月 21 日：更新了 Liberty buildpack V3.4-20161018-2004
* 已更新缺省 Liberty 运行时版本 `16.0.0.3`，以包括 [PI68805](http://www-01.ibm.com/support/docview.wss?uid=swg1PI68805) 和 [PI69141](http://www-01.ibm.com/support/docview.wss?uid=swg1PI69141) iFix。
* 每月 Liberty 运行时版本已更新为 [2016.9.0.1](https://developer.ibm.com/wasdev/blog/2016/09/23/beta-websphere-liberty-and-tools-october-2016/) 发行版。
* 该 buildpack 中还包含更新版本的 IBM JRE 8.0：SR3 FP12。
* 现在已配置 IBM JRE 8.0 和 7.1，以[在调用 `SSLContext.getContext("TLS")` 时启用所有 TLS 协议](https://www.ibm.com/support/knowledgecenter/SSYKE2_8.0.0/com.ibm.java.security.component.80.doc/security-component/jsse2Docs/matchsslcontext_tls.html)，以匹配 Oracle 的 JRE 行为。同时也配置了 IBM JRE 7.1，以[在调用 `SSLContext.getDefault()` 时启用所有 TLS 协议](https://www.ibm.com/support/knowledgecenter/SSYKE2_7.1.0/com.ibm.java.security.component.71.doc/security-component/jsse2Docs/overrideSSLprotocol.html)，以匹配 IBM 的 JRE 8.0 行为。
* 该 buildpack 提供了用于 [Monitoring and Analytics 服务](/docs/services/monana/index.html#monana_oview)的更新版本的数据收集器。
* 该 buildpack 已更改回在执行 [MySQL 服务类型的自动配置](autoConfig.html)时，下载最新的 1.5.x [MariaDB Connector/J JDBC 驱动程序 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/)。
* 该 buildpack 通过 `LBP_SERVICE_CONFIG_<serviceType>` 环境变量引入了定制服务自动配置行为的支持。例如，它可用于更改 JDBC 驱动程序的位置或版本，以针对 MySQL 服务进行下载。有关更多信息，请参阅[支持自动配置的服务](autoConfig.html)文档。
* 该 buildpack 还包含与应用程序运行状况检查和[应用程序管理](/docs/manageapps/app_mng.html)功能相关的若干 [Diego ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://docs.cloudfoundry.org/concepts/diego/diego-architecture.html) 改进。

### 2016 年 9 月 16 日：更新了 Liberty buildpack V3.3-20160912-1729
* 缺省 Liberty 运行时版本已更新为 [16.0.0.3](http://www-01.ibm.com/support/docview.wss?uid=swg27009661) 发行版。每月 Liberty 运行时版本已更新为 [2016.9.0.0](https://developer.ibm.com/wasdev/blog/2016/08/26/beta-websphere-liberty-and-tools-september-2016/) 发行版。通过这些更新，先前作为 Beta 功能提供的 `cloudant-1.0` 和 `passwordUtilities-1.0` Liberty 功能现在都作为可用于生产的功能提供。
* 同时包括 Liberty 运行时的[安全修订](http://www-01.ibm.com/support/docview.wss?uid=swg21990527)。
* 该 buildpack 中还包含更新版本的 IBM JRE 8.0：SR3 FP11。
* 该 buildpack 已调整为在执行 [MySQL 服务类型的自动配置](autoConfig.html)时，下载最新的 1.4.x [MariaDB Connector/J JDBC 驱动程序 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/)，因为使用最新的 1.5.x 驱动程序会发生问题。

### 2016 年 8 月 26 日：更新了 Liberty buildpack V3.2-20160822-2200
* 该 buildpack 包含更新版本的 IBM JRE：8 SR3 FP10 和 7.1 SR3 FP50。
* 每月 Liberty 运行时版本已更新为 [2016.8.0.0](https://developer.ibm.com/wasdev/blog/2016/07/28/beta-websphere-liberty-and-tools-august-2016/) 发行版。
* 更新了用于为 [SQL 数据库](/docs/services/SQLDB/index.html#SQLDB)服务提供[自动配置支持](autoConfig.html)的服务插件，以在通过 TLS 连接到该服务时，始终使用 JVM 的可信证书。

### 2016 年 7 月 22 日：更新了 Liberty buildpack V3.1-20160717-2254
* [应用程序管理](/docs/manageapps/app_mng.html)功能已更新为支持联合认证。此外，`devconsole` 和 `shell` 实用程序使用的 Node.js 运行时已更新到最新的 `0.12.15` 版本。
* 该 buildpack 添加了对 [Dynatrace Ruxit ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://www.dynatrace.com/en/ruxit/) 应用程序监视代理程序的支持。
* 该 buildpack 提供了用于 [Monitoring and Analytics 服务](/docs/services/monana/index.html#monana_oview)的更新版本的数据收集器。
* 该 buildpack 还提供了用于 [Auto-Scaling 服务](/docs/services/Auto-Scaling/index.html)的更新版本的代理程序。
* 每月 Liberty 运行时版本已更新为 [2016.7.0.0](https://developer.ibm.com/wasdev/blog/2016/06/30/beta-websphere-liberty-and-tools-july-2016/) 发行版。

### 2016 年 6 月 17 日：更新了 Liberty buildpack V3.0-20160608-1450
* 该 buildpack 现在包含 WebSphere Liberty 的两个版本，即最新的稳定发行版和最新的每月发行版。具体而言，其提供的是 [16.0.0.2](http://www-01.ibm.com/support/docview.wss?uid=swg21984970) 稳定发行版和 [2016.6.0.0](https://developer.ibm.com/wasdev/blog/2016/06/03/beta-websphere-liberty-and-tools-june-2016/) 每月发行版。缺省情况下，将使用稳定发行版。请参阅 [Liberty 版本](buildpackDefaults.html#liberty_versions)，以获取其他详细信息。
* 该 buildpack 还包含针对 [Apache Standard Taglibs 漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg21985531)的安全修订。

### 2016 年 5 月 25 日：更新了 Liberty buildpack V2.9-20160519-1249
* 该 buildpack 包含更新版本的 WebSphere Liberty（基于[五月 Beta](https://developer.ibm.com/wasdev/blog/2016/05/06/beta-websphere-liberty-and-tools-may-2016/)）。更新版本的 Liberty 使 *bluemixLogCollector-1.1* 和 *logstashCollector-1.1* Beta 功能在 Bluemix 中可用。

### 2016 年 5 月 5 日：更新了 Liberty buildpack V2.8-20160430-1011
* 该 buildpack 包含更新版本的 WebSphere Liberty（基于[四月 Beta](https://developer.ibm.com/wasdev/blog/2016/04/08/beta-websphere-liberty-and-tools-april-2016/)）。更新版本的 Liberty 使 *logstashCollector-1.0* GA 功能和 *logmetCollector-1.0* Beta 功能在 Bluemix 中可用。
* 该 buildpack 还包含更新版本的 IBM JRE：8 SR3 和 7.1 SR3 FP40。
* 该 buildpack 添加了对 [AppDynamics ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.appdynamics.com/) 应用程序监视代理程序的初始支持。
* 改进了 [Dynatrace](dynatrace.html) 支持，以简化代理程序的安装。
* 该 buildpack 提供了用于 [Monitoring and Analytics 服务](/docs/services/monana/index.html#monana_oview)的更新版本的数据收集器。其中包含对收集最大堆数据时所出现问题的修订。
* [devconsole 和 shell 应用程序管理实用程序](/docs/manageapps/app_mng.html#app_management)使用的 Node.js 运行时已更新到最新的 0.12.13 版本。

### 2016 年 3 月 25 日：更新了 Liberty buildpack V2.7-20160321-1358
* 该 buildpack 包含更新版本的 WebSphere Liberty（基于[三月 Beta](https://developer.ibm.com/wasdev/blog/2016/03/18/new-websphere-liberty-features-march-2016/)）。更新版本的 Liberty 使 cloudant-1.0 Beta 功能在 Bluemix 中可用。
* 该 buildpack 还包含更新版本的 IBM JRE：8 SR2 FP12 和 7.1 SR3 FP32。
* 该 buildpack 提供了用于 [Auto-Scaling 服务](/docs/services/Auto-Scaling/index.html)的更新版本的代理程序。
* 该 buildpack 现在随附用于 [Monitoring and Analytics 服务](/docs/services/monana/index.html#monana_oview)的新数据收集器。新收集器支持配置监视阈值，并包含大量错误修订。
* 该 buildpack 提供了更新的 DB2® JDBC V4.19.49 驱动程序。
* [devconsole 和 shell 应用程序管理实用程序](/docs/manageapps/app_mng.html#app_management)使用的 Node.js 运行时已更新到最新的 0.12.12 版本。

### 2016 年 3 月 7 日：更新了 Liberty buildpack V2.6-20160225-1649
* 该 buildpack 添加了对 Dynatrace 应用程序监视的支持。请参阅[使用 Dynatrace](dynatrace.html)，以获取详细信息。
* 该 buildpack 添加了对 [DynamicPULSE](www.fujitsu.com/jp/group/fsweb/products/dynamic-pulse/) 的支持。

### 2016 年 2 月 10 日：更新了 Liberty buildpack V2.5-20160209-1336
* 该 buildpack 包含更新版本的 WebSphere Liberty（基于[二月 Beta](https://developer.ibm.com/wasdev/blog/2016/02/12/beta-websphere-liberty-and-tools-february/)）。更新版本的 Liberty 概要文件使 apiDiscovery-1.0 GA 功能在 Bluemix 中可用。

### 2016 年 2 月 4 日：更新了 Liberty buildpack V2.4-20160127-1437
* 该 buildpack 包含更新版本的 WebSphere Liberty （基于一月 Beta）。通过此更新，先前作为 Beta 功能提供的 scim-1.0 Liberty 功能现在作为可用于生产的功能提供。更新版本的 Liberty 还使 passwordUtilities-1.0 Beta 功能在 Bluemix 中可用。
* 该 buildpack 还包含更新的 IBM JRE 7.1 SF3 FP20 和 IBM JRE 8 SR2 FP10。
* 该 buildpack 已更新为在执行 [MySQL 服务类型的自动配置](autoConfig.html)时，下载最新的 1.x [MariaDB Connector/J JDBC 驱动程序 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/)。

### 2015 年 12 月 16 日：更新了 Liberty buildpack V2.3-20151208-1311
* 该 buildpack 包含更新版本的 Liberty 概要文件（基于[十二月 Beta](https://developer.ibm.com/wasdev/blog/2015/11/20/beta-was-liberty-beta-with-tools-december-2015/)）。更新版本的 Liberty 概要文件使 spnego-1.0 和 wsSecuritySaml-1.1 GA 功能以及 scim-1.0 Beta 功能在 Bluemix 中可用。
* 该 buildpack 还包含更新的 IBM JRE 8 SR2。
* 该 buildpack 已更新为在执行 PostgreSQL 或 MySQL 类型服务的[自动配置](autoConfig.html)时，下载最新的 [9.4.x PostgreSQL JDBC 驱动程序 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://jdbc.postgresql.org/) 和 1.2.x [MariaDB Connector/J JDBC 驱动程序 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/)。

### 2015 年 11 月 23 日：更新了 Liberty buildpack V2.2-20151119-1720
* 该 buildpack 包含更新版本的 Liberty 概要文件运行时和 WebSphere eXtreme Scale Client，带有针对 [Apache Commons Collection 漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg21971426)的安全修订。
* 该 buildpack 还包含更新版本的 [Java MongoDB Driver ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://docs.mongodb.org/ecosystem/drivers/java/) V2.13.3。新的驱动程序与 MongoDB V2.4、2.6 和 3.0 兼容。
* 该 buildpack 还提供了用于 [Monitoring and Analytics 服务](/docs/services/monana/index.html)的更新版本的数据收集器。更新的数据收集器改进了方法跟踪功能。

### 2015 年 10 月 16 日：更新了 Liberty buildpack V2.1-20151006-0912
* 该 buildpack 包含更新版本的 Liberty 概要文件（基于[十月 Beta](https://developer.ibm.com/wasdev/blog/2015/09/25/beta-was-liberty-beta-with-tools-october-2015/)）。通过此更新，先前作为 Beta 功能提供的 bells-1.0、rtcomm-1.0、rtcommGateway-1.0、samlWeb-2.0 和 sipServlet-1.1 Liberty 功能现在都作为可用于生产的功能提供。
* 该 buildpack 还包含更新的 IBM JRE 8 SR1 FP11。
* 该 buildpack 还提供许多性能改进和优化：
  * 缺省情况下，部署 WAR 或 EAR 文件时，会禁用 [CDI 1.2](optionsForPushing.html) 隐式 Bean 归档扫描功能。
  * 要降低 Droplet 的大小，[应用程序管理](/docs/manageapps/app_mng.html)实用程序 devconsole 和 shell 需要执行重新编译打包操作而不是重新启动操作。
  * 因为 Bluemix 环境中未复用 IBM JRE 的共享类高速缓存，因此已将其禁用。

### 2015 年 9 月 18 日：更新了 Liberty buildpack V2.0-20150914-1535
* 该 buildpack 引入两个主要更改：
  * WAR 和 EAR 文件的缺省配置启用 Java EE 7 Web 概要文件功能，而不启用 Java EE 6 Web 概要文件功能。
  * 缺省 Java 版本是 V8，而不是 V7。
* 请参阅即将发布的 [Liberty for Java buildpack 更改](https://developer.ibm.com/bluemix/2015/09/08/upcoming-liberty-for-java-buildpack-changes/)博客帖子，以获取有关这些更改及其可能对应用程序产生哪些影响的详细信息。
* 该 buildpack 还引入了 app_state 配置选项，可通过 JBP_CONFIG_LIBERTY 环境变量禁用 appstate 功能。appstate 功能与 Cloud Foundry 运行状况检查进程集成在一起，可确保 Liberty 应用程序经过完全初始化后，才能接收 HTTP 请求。要禁用 appstate 功能，可以将 JBP_CONFIG_LIBERTY 环境变量设置为“app_state: false”。

### 2015 年 9 月 4 日：更新了 Liberty buildpack V1.22-20150824-1104
* 该 buildpack 支持 [HTTP_PROXY 和 HTTPS_PROXY 环境变量](environmentVariables.html)。如果设置，那么该 buildpack 在下载各种 buildpack 组件时，将使用这两个环境变量指定的代理服务器。

### 2015 年 8 月 19 日：更新了 Liberty buildpack V1.21-20150811-1342
* 该 buildpack 包含更新版本的 Liberty 概要文件（基于[八月 Beta](https://developer.ibm.com/wasdev/blog/2015/07/30/beta-was-liberty-beta-with-tools-august-2015/)）。更新版本的 Liberty 概要文件使以下新 [Beta 功能](usingBetaFeatures.html)在 Bluemix 中可用：bells-1.0、rtcommGateway-1.0 和 samlWebSso-2.0。

### 2015 年 7 月 31 日：更新了 Liberty buildpack V1.20.1-20150729-1255
* 该 buildpack 包含更新版本的 IBM JRE：7.1 SR1 FP10 和 8 SR1 FP10。
更新的 JRE 包含[最新的安全修订](http://www-01.ibm.com/support/docview.wss?uid=swg21964161)和其他改进。
* 更新了用于为 [Cloudant NoSQL Database](/docs/services/Cloudant/index.html#Cloudant) 服务提供[自动配置支持](autoConfig.html)的服务插件，以确保通过安全通道建立与该服务的连接。

### 2015 年 7 月 21 日：更新了 Liberty buildpack V1.20-20150713-1450
* 该 buildpack 包含更新版本的 Liberty 概要文件（基于 [8.5.5.6 发行版](https://developer.ibm.com/wasdev/blog/2015/06/25/java-ee-7-has-landed-in-was-liberty/)）。通过此发行版，先前作为 Beta 功能提供的所有 Java EE 7 Liberty 功能现在都作为可用于生产环境的功能提供。由于 Bluemix 中的端口和其他限制，某些功能（例如，远程 EJB）在该平台中未得到完全支持。
* 该 buildpack 识别并运行以 [distZip 样式 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://docs.gradle.org/current/userguide/application_plugin.html) 打包的应用程序。
* 该 buildpack 包含更新的数据收集器，用于支持新 Liberty 运行时版本的 [Monitoring and Analytics 服务](/docs/services/monana/index.html)和 WebSphere eXtreme Scale Client。

### 2015 年 6 月 30 日：更新了 Liberty buildpack V1.19.1-20150622-1509
* 此版本的 buildpack 包含更新的 IBM JRE，其中包含针对 [LogJam 漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg21961390)的安全修订。
* [New Relic](newRelic.html) 代理程序已更新为 V3.17。新版本改进了与 Liberty 概要文件运行时的集成。

### 2015 年 6 月 14 日：更新了 Liberty buildpack V1.19-20150608-1717
* 该 buildpack 包含多个应用程序管理增强功能，其中包括对开发控制台和基于 Web 的 shell 访问的支持。请参阅[应用程序管理文档](/docs/manageapps/app_mng.html)以获取详细信息。
* 该 buildpack 还包含一个修订，该修订解决了找不到用于 [Monitoring and Analytics 服务](/docs/services/monana/index.html)的 Liberty 功能的问题。

### 2015 年 5 月 27 日：更新了 Liberty buildpack V1.18-20150519-1642
* 该 buildpack 包含更新版本的 Liberty 概要文件（基于[五月 Beta](https://developer.ibm.com/wasdev/blog/2015/05/08/beta-liberty-and-tools-may-2015/)）。

### 2015 年 5 月 5 日：更新了 Liberty buildpack V1.17-20150501-1729
* 该 buildpack 包含更新版本的 Liberty 概要文件（基于[四月 Beta](https://developer.ibm.com/wasdev/blog/2015/04/10/announcing-liberty-beta-with-tools-aprilmay-2015/)）。通过此更新，先前作为 Beta 功能提供的 jsp-2.3、el-3.0 和 jdbc-4.1 Liberty 功能现在都作为可用于生产的功能提供。此外，其他 Java EE 7 功能（例如，jsf-2.2、javaMail-1.5、webProfile-7.0 和 javaee-7.0）现在都作为 [Beta 功能](usingBetaFeatures.html)提供。
* 该 buildpack 还提供了对 Java 8 的初始支持。IBM JRE 7.1 仍是缺省 JRE，但通过设置 JBP_CONFIG_IBMJDK 环境变量，可以对应用程序启用 IBM JRE 8。此外，还支持配置 OpenJDK 版本。请参阅[定制 JRE](customizingJRE.html) 以获取所有详细信息。
* 该 buildpack 提供了新的 JBP_CONFIG_LIBERTY 环境变量，可用于覆盖在部署 WAR 或 EAR 文件时为应用程序启用的缺省 Liberty 功能集。请参阅[独立应用程序](optionsForPushing.html#stand_alone_apps)以获取更多信息。
* [Monitoring and Analytics 服务](/docs/services/monana/index.html)的服务插件已更新，从而减小为该服务生成的日志大小。
* 通过此版本的 buildpack，更改了应用程序文件在 Droplet 中的布局方式。文件结构的更改使维护符号链接变得简单，并且对应用程序应该没有任何影响。

### 2015 年 4 月 15 日：更新了 Liberty buildpack V1.16-20150407-1737
* 此版本的 buildpack 包含更新的 IBM JRE 7.1-2.11，以及[针对 Bar Mitzvah 漏洞的安全修订](http://www-01.ibm.com/support/docview.wss?uid=swg21882777)。
* 部署独立 WAR 文件（如果提供）时，现在该 buildpack 会使用在内嵌 **ibm-web-ext.xml** 文件中指定的上下文根作为应用程序的上下文根。借助此更改，先前部署在根上下文下的应用程序可根据 **ibm-web-ext.xml** 文件中的设置部署到其他上下文下。

### 2015 年 4 月 3 日：更新了 Liberty buildpack V1.15-20150402-1422
* 该 buildpack 包含更新版本的 Liberty 概要文件（基于[三月 Beta](https://developer.ibm.com/wasdev/blog/2015/03/13/announcing-liberty-beta-tools-march-2015/)）。更新版本的 Liberty 概要文件使 jsf-2.2 Beta 功能在 Bluemix 中可用。
* 该 buildpack 还包含用于 [Monitoring and Analytics 服务](/docs/services/monana/index.html)的更新版本的数据收集器。

### 2015 年 3 月 20 日：更新了 Liberty buildpack V1.14-20150319-1159
* 此版本的 buildpack 包含更新的 IBM JRE 7.1.2.11，其中有针对 [FREAK 漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg21699864)的安全修订。
* [SQL Database](services/SQLDB/index.html#SQLDB) 服务提供了付费计划，可选择通过 SSL 协议与数据库服务器连接。该 buildpack 对 SQL Database 服务的自动配置支持已更新，可将运行时配置为在 SSL 连接信息可用时通过 SSL 与数据库连接。
* 该 buildpack 已更新，可报告部署独立 WAR 或 EAR 文件（该文件在应用程序归档根目录中包含 **server.xml** 配置文件）时发生的错误。
* 该 buildpack 包含用于 MongoDB 的自动配置服务插件的修订，之前在某些情况下，该插件会生成无效的 **server.xml** 配置。

### 2015 年 2 月 10 日：更新了 Liberty buildpack V1.13-20150209-1122
* 该 buildpack 包含针对 [Apache HttpComponents 和 Java 覆盖功能漏洞](https://www-304.ibm.com/connections/blogs/PSIRT/entry/ibm_security_bulletin_multiple_vulnerabilities_fixed_in_liberty_for_java_for_ibm_bluemix_cve_2012_6153_cve_2014_3577_cve_2015_0178?lang=en_us)的安全修订。
* 该 buildpack 包含更新版本的 Liberty 概要文件（基于[二月 Beta](https://developer.ibm.com/wasdev/blog/2015/02/13/announcing-liberty-beta-tools-february-2015/)）。更新版本的 Liberty 概要文件提供了更新版本的 WebSocket GA 功能 websocket-1.1。它还使以下 Java EE 7 Beta 功能在 Bluemix 中可用：
  * cdi-1.2、el-3.0、jsp-2.3、jca-1.7、jacc-1.5 和 jaspic-1.1
* 该 buildpack 提供了与 [ZeroTrunaround 的 JRebel 工具 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://zeroturnaround.com/software/jrebel/) 的集成。通过该集成，能轻松将 JRebel 与 Bluemix 应用程序一起使用，并执行即时应用程序更新，而无需对应用程序进行重新部署或重新编译打包。仅支持独立 Web 应用程序。

### 2015 年 2 月 6 日：更新了 Liberty buildpack V1.12-20150130-1016
* 该 buildpack 包含更新版本的 Liberty 概要文件（基于[一月 Beta](https://developer.ibm.com/wasdev/blog/2015/01/16/announcing-liberty-beta-tools-january-2015/)）。
* 该 buildpack 包含用于 [Monitoring and Analytics 服务](/docs/services/monana/index.html#gettingstartedtemplate)的修剪版本的数据收集器。

### 2015 年 1 月 23 日：更新了 Liberty buildpack V1.11-20150119-1511
* 该 buildpack 包含更新的 IBM JRE V7.1 SR2 FP1。
* 它还包含更新的 WebSphere eXterme Scale Client V8.6.0.6 和用于 Auto-Scaling 服务的已更新代理程序。
* 增强了 [New Relic](newRelic.html) 服务支持的功能，现在可支持用户定义的服务。
* 该 buildpack 已改进，可报告 Liberty 概要文件和 IBM JRE 的详细版本。

### 2014 年 12 月 19 日：更新了 Liberty buildpack V1.10-20141218-0103
* 该 buildpack 为应用程序提供了开发方式。开发方式是一种特殊方式，允许开发者对应用程序实例执行许多以前无法执行的活动。利用此功能，此版本的 IBM Eclipse Tools for Bluemix 现在可以支持通过增量文件更新对 Bluemix 中运行的 Liberty 应用程序进行远程调试。这样，开发者就可以方便地使用 Eclipse 在云中对应用程序进行调试，并立即将更改应用于该应用程序。
* 该 buildpack 还包含更新版本的 Liberty 概要文件（基于[十二月 Beta](https://developer.ibm.com/wasdev/blog/2014/12/10/announcing-liberty-beta-december/)）。
* 此外，先前作为 Beta 功能提供的以下四个 Liberty 功能现在可用于生产环境：
  * concurrent-1.0
  * jsonp-1.0
  * servlet-3.1
  * websocket-1.0
* 该 buildpack 提供了与 New Relic 服务的集成。将应用程序绑定到 New Relic 服务后，该 buildpack 将使用 New Relic 代理程序自动下载并配置运行时。
* 该 buildpack 具有以下已知限制：
  * 使用开发方式时，无法绑定 SessionCache 服务。
  * 使用开发方式时，无法创建线程转储。
  * 使用 servlet-3.1 或 websocket-v1.0 功能时，找不到 Monitoring & Analytics 服务。

### 2014 年 12 月 5 日：更新了 Liberty buildpack V1.9-20141202-0947
* 该 buildpack 提供了增强的 JVM 选项支持。现在，可以通过重新启动操作来应用 JVM 选项。不需要重新编译打包应用程序。此外，还对缺省 JVM 选项进行了优化，以便实现快速故障恢复，还为它们预配置了一个通用位置，方便查找所生成的转储。有关更多详细信息，请参阅 [Custom Configuration of Java JVM for the Liberty Runtime 一文](https://developer.ibm.com/bluemix/2014/12/12/custom-configurations-java-jvm-liberty-runtime/)。
* 该 buildpack 包含更新的 DB2 JDBC 驱动程序 V4.17.29。
* 还包含一个修订，其解决了阻止为 Monitoring & Analytics 服务收集 Liberty 线程池使用情况信息的问题。

### 2014 年 11 月 21 日：更新了 Liberty buildpack V1.8-20141118-1610
* 该 buildpack 包含更新的 IBM JRE V7.1 SR2，其中提供对 [POODLE 漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg21687173)的修订。
* 还包含更新版本的 Liberty 概要文件（基于[十一月 Beta](https://developer.ibm.com/wasdev/blog/2014/11/07/announcing-liberty-profile-beta-november/)）。

### 2014 年 10 月 30 日：更新了 Liberty buildpack V1.7-20141020-1759
* 该 buildpack 包含更新的 IBM JRE V7.1 SR1 FP3。
* 还提供一个修订，其解决了阻止使用包含 Unicode 字符的服务器配置部署应用程序的问题。

### 2014 年 10 月 23 日：更新了 Liberty buildpack V1.6-20141013-1628
* 该 buildpack 现在随附用于 [Monitoring and Analytics](/docs/services/monana/index.html) 的新数据收集器。这个新的数据收集器会收集具体到特定代码行的诊断信息，这些信息可帮助该服务诊断计划的用户诊断其应用程序的问题。
* 该 buildpack 包含管理和自动调节代理程序的更新版本（包括错误修订和少量改进）。它还包括更新版本的 [Liberty 概要文件](https://developer.ibm.com/wasdev/)和 [Java MongoDB Driver ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://docs.mongodb.org/ecosystem/drivers/java/) V2.12.3。
* 在 cloudAutowiring 功能中，导致某些应用程序中资源注入错误的错误已修订。

### 2014 年 10 月 3 日：更新了 Liberty buildpack V1.5-20140923-1143
* 具有更新的 buildpack 后，应用程序现在可以使用 Liberty Beta 功能，包括 WebSocket 1.0、Servlet 3.1 或 JAX-RS 2.0。有关更多信息，请参阅[使用 Beta 功能](usingBetaFeatures.html)。

### 2014 年 9 月 30 日：更新了 Liberty buildpack V1.4-20140908-1803
* 该 buildpack 现在提供对 ElephantSQL 和 ClearDB MySQL Database 第三方服务的支持。自动配置支持也可用于 posgresql 和 mysql 试验性服务。新服务共计 13 个，通过这些新服务，Liberty buildpack 中的自动配置支持使在 Liberty 应用程序中使用 Bluemix 服务变得速度更快，操作更简单。
* 在应用程序编译打包期间，buildpack 会显示有关自动配置和其采取的其他操作的已改进日志消息。
* 该 buildpack 包含 Liberty 概要文件的更新版本，其中带有修订和改进。
* 它还包含具有性能改进的 IBM JRE V7.1 的更新版本。请参阅[新增内容](http://www-01.ibm.com/support/knowledgecenter/SSYKE2_7.0.0/com.ibm.java.lnx.71.doc/diag/preface/changes_71/changes.html)页面，以获取详细的更改集。

### 2014 年 8 月 28 日：更新了 Liberty buildpack V1.3-20140818-1538
* 该 buildpack 包含更新版本的 [Liberty 概要文件](https://developer.ibm.com/wasdev/)，其中包含最新修订和改进。
* 此版本的 buildpack 修订支持用于将其他 JVM 选项传递到应用程序运行时的 JAVA_OPTS 环境变量。
* 它还解决了阻止部署基于 Spring 的独立 Jar 应用程序的问题。
* 现在，可以使用 Bluemix UI 来生成并下载 IBM JVM 快照跟踪。请参阅 IBM JVM 文档中的[故障诊断](http://www-01.ibm.com/support/knowledgecenter/SSYKE2_7.0.0/com.ibm.java.lnx.70.doc/troubleshooting.html)主题，以了解有关 JVM 生成的快照跟踪或其他诊断信息的更多信息。

### 2014 年 7 月 29 日：更新了 Liberty buildpack V1.1-20140725-1341
* 这是 Liberty 的 Bluemix Edition 的新版本！
  * 此版本的 Liberty 不仅有新功能，还有多个修订，可支持您更有效地使用 Bluemix 服务！
  * 由于提供了新的 CouchDB 功能，因此 Cloudant® 服务现在可以自动对其进行配置，使连接器对象方便可用！无需再通过 VCAP_SERVICES 进行解析并提供 ektorp 客户机 jar。
* 这是 IBM SDK for Java 的新版本！
  * 重新推送应用程序时，应用程序将使用 IBM SDK for Java V7.1-1.0。此版本已进行显著的性能升级。应用程序的吞吐量更大，而内存使用量更少。请参阅[此处](http://www-01.ibm.com/support/docview.wss?uid=swg21671466)，以获取有关 IBM Java SDK 的更多信息。

# 相关链接
{: #rellinks notoc}
## 常规
{: #general notoc}
  * [Liberty 运行时](index.html)
  * [Liberty 概要文件概述](http://www-01.ibm.com/support/knowledgecenter/SSAW57_8.5.5/com.ibm.websphere.wlp.nd.doc/ae/cwlp_about.html)
