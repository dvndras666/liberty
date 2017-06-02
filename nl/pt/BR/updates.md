---

copyright:
  years: 2015, 2017
lastupdated: "2017-03-23"

---

{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Atualizações mais recentes para o buildpack do Liberty
{: #latest_updates}

## Uma lista das atualizações mais recentes no buildpack do Liberty.

### 14 de março de 2017: atualizado o buildpack do Liberty v3.8-20170308-1507

* A versão de runtime padrão do Liberty foi atualizada para a liberação 17.0.0.1.
* O tempo de execução padrão do Liberty também inclui o iFix WebSockets PI75512.
* A versão de runtime mensal do Liberty foi atualizada para a liberação [2017.2.0.0](https://developer.ibm.com/wasdev/blog/2017/02/17/beta-websphere-liberty-tools-february-2017/).
* O IBM JRE versões 8 e 7.1 foi atualizado para SR4 FP1.
* O suporte de configuração automática também foi estendido para funcionar com [ibm-websphere-extreme-scale IBM Container](https://console.ng.bluemix.net/docs/images/docker_image_extreme_scale/ibm-websphere-extreme-scale_starter.html).
* O suporte de configuração automática para o [Cloudant NoSQL Database](https://console.ng.bluemix.net/docs/services/Cloudant/index.html) foi atualizado para fornecer a opção de usar a Biblioteca Java Cloudant em vez de org.ektorp. Para ativar o uso da Biblioteca Java Cloudant, deve-se configurar a variável de ambiente a seguir:    
```
cf set-env <appName> LBP_SERVICE_CONFIG_CLOUDANTNOSQLDB 'type : cloudant'
```
* O buildpack também fornece uma versão atualizada do agente para o [serviço Auto-Scaling](/docs/services/Auto-Scaling/index.html) e vários aprimoramentos de gerenciamento de aplicativo.
* Esse buildpack também muda o modo de funcionamento da configuração automática do [serviço Monitoring and Analytics](/docs/services/monana/index.html). Os aplicativos que usam o plano Gratuito não terão mais a capacidade de log incluída em seus aplicativos; ele está sendo substituído por logmet.  


### 23 de janeiro de 2017: atualizado o buildpack do Liberty v3.7-20170118-2046
* A versão de runtime mensal do Liberty foi atualizada para a liberação [2017.1.0.0](https://developer.ibm.com/wasdev/blog/2017/01/20/beta-websphere-liberty-tools-january-2017/).
* O IBM JRE versão 8 foi atualizado para a versão SR3 FP22.
* O suporte de [configuração automática](autoConfig.html) também foi estendido para funcionar com o [serviço Compose for MongoDB](https://console.ng.bluemix.net/docs/services/ComposeForMongoDB/index.html) (Atualmente disponível somente com o tempo de execução mensal do Liberty).

### 13 de dezembro de 2016: atualizado o buildpack do Liberty v3.6-20161209-1351
* A versão de runtime padrão do Liberty foi atualizada para a liberação [16.0.0.4](http://www-01.ibm.com/support/docview.wss?uid=swg27009661).
* O IBM JRE versão 8 foi atualizado para a versão SR3 FP21.
* O suporte de [configuração automática](autoConfig.html) também foi estendido para funcionar com o [serviço Compose for PostgreSQL](https://console.ng.bluemix.net/docs/services/ComposeForPostgreSQL/index.html).
* O buildpack também fornece uma versão atualizada do agente para o [Serviço de ajuste automático de escala](/docs/services/Auto-Scaling/index.html).
* O buildpack foi atualizado para suportar variáveis de ambiente como parte dos locais de inclusão nos arquivos `server.xml`.

### 29 de novembro de 2016: atualizado o buildpack do Liberty v3.5-20161114-1152
* A versão de runtime padrão do Liberty `16.0.0.3` foi atualizada para incluir o iFix [PI62375](https://www-01.ibm.com/support/docview.wss?uid=swg24042712) e para fornecer o recurso de conveniência `microProfile-1.0`.
* A versão de runtime mensal do Liberty foi atualizada para a liberação `2016.11.0.0`.
* O buildpack também contém os IBM JREs atualizados: versão 8 SR3 FP20 e versão 7.1 SR3 FP60.
* O driver JDBC DB2 foi atualizado para a versão `4.21.29`.
* A integração de serviço Monitoring and Analytics foi corrigida para funcionar com o [Diego ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://docs.cloudfoundry.org/concepts/diego/diego-architecture.html).
* As integrações de serviço [Dynatrace](dynatrace.html) foram atualizadas para funcionar melhor com as ofertas de serviços Dynatrace.
* O suporte de [configuração automática](autoConfig.html) para os tipos de serviços PostgreSQL e MySQL foi melhorado para funcionar melhor ao implementar um diretório do servidor ou um servidor em pacote.
* O tempo de execução Node.js que é usado pelos [utilitários devconsole e shell do App Management](/docs/manageapps/app_mng.html#app_management) foi atualizado para a versão mais recente `0.12.17`.
* [Correções de segurança](http://www.ibm.com/support/docview.wss?uid=swg21994945) para o tempo de execução do Liberty são incluídas.

### 1º de novembro de 2016: atualizado o buildpack do Liberty v3.4.1-20161030-2241
* O buildpack contém uma correção para um problema iniciando em determinados tipos de aplicativos. Especificamente, os aplicativos implementados como um diretório do servidor ou um servidor empacotado com os arquivos de aplicativos no diretório `dropins`.

### 21 de outubro de 2016: atualizado o buildpack do Liberty v3.4-20161018-2004
* A versão de runtime padrão do Liberty `16.0.0.3` foi atualizada para incluir os iFixes [PI68805](http://www-01.ibm.com/support/docview.wss?uid=swg1PI68805) e [PI69141](http://www-01.ibm.com/support/docview.wss?uid=swg1PI69141).
* A versão de runtime mensal do Liberty foi atualizada para a liberação [2016.9.0.1](https://developer.ibm.com/wasdev/blog/2016/09/23/beta-websphere-liberty-and-tools-october-2016/).
* O buildpack também contém uma versão atualizada do IBM JRE 8.0: SR3 FP12.
* O IBM JRE 8.0 e 7.1 agora são configurados para ativar [todos os protocolos TLS quando `SSLContext.getContext ("TLS")` é chamado](https://www.ibm.com/support/knowledgecenter/SSYKE2_8.0.0/com.ibm.java.security.component.80.doc/security-component/jsse2Docs/matchsslcontext_tls.html) para corresponder ao comportamento do JRE do Oracle. O IBM JRE 7.1 também é configurado para ativar [ todos os protocolos TLS quando `SSLContext.getDefault()` é chamado](https://www.ibm.com/support/knowledgecenter/SSYKE2_7.1.0/com.ibm.java.security.component.71.doc/security-component/jsse2Docs/overrideSSLprotocol.html) para corresponder ao comportamento do JRE 8.0 da IBM.
* O buildpack fornece um coletor de dados atualizado para o [serviço de Monitoramento e Analítica](/docs/services/monana/index.html#monana_oview).
* O buildpack foi mudado de volta para fazer download do [driver JDBC MariaDB Connector/J ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/) 1.5.x ao executar a [configuração automática para o tipo de serviços MySQL](autoConfig.html).
* O buildpack apresenta o suporte para customizar o comportamento de configuração automática de serviço por meio da variável de ambiente `LBP_SERVICE_CONFIG_<>serviceType`. Por exemplo, ele pode ser usado para mudar o local ou a versão de um driver JDBC para download do serviço MySQL. Consulte a documentação de [serviços que suportam configuração automática](autoConfig.html) para obter mais informações.
* O buildpack também contém várias melhorias do [Diego ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://docs.cloudfoundry.org/concepts/diego/diego-architecture.html) relacionadas à verificação de funcionamento do aplicativo e à funcionalidade do [App Management](/docs/manageapps/app_mng.html).

### 16 de setembro de 2016: atualizado o buildpack do Liberty v3.3-20160912-1729
* A versão de runtime padrão do Liberty foi atualizada para a liberação [16.0.0.3](http://www-01.ibm.com/support/docview.wss?uid=swg27009661). A versão de runtime mensal do Liberty foi atualizada para a liberação [2016.9.0.0](https://developer.ibm.com/wasdev/blog/2016/08/26/beta-websphere-liberty-and-tools-september-2016/). Com essas atualizações, os recursos `cloudant-1.0` e `passwordUtilities-1.0` do Liberty, anteriormente disponíveis como recursos beta, agora estão disponíveis como recursos prontos para produção.
* [Correções de segurança](http://www-01.ibm.com/support/docview.wss?uid=swg21990527) para o tempo de execução do Liberty são incluídas.
* O buildpack também contém uma versão atualizada do IBM JRE 8.0: SR3 FP11.
* O buildpack foi ajustado para fazer download do [driver JDBC MariaDB Connector/J ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/) 1.4.x mais recente ao executar a [configuração automática para o tipo de serviços MySQL](autoConfig.html) em razão de um problema com o driver 1.5.x mais recente.

### 26 de agosto de 2016: atualizado o buildpack do Liberty v3.2-20160822-2200
* O buildpack contém versões atualizadas do IBM JRE: 8 SR3 FP10 e 7.1 SR3 FP50.
* A versão de runtime mensal do Liberty foi atualizada para a liberação [2016.8.0.0](https://developer.ibm.com/wasdev/blog/2016/07/28/beta-websphere-liberty-and-tools-august-2016/).
* O plug-in de serviço que fornece [suporte de configuração automática](autoConfig.html) para o serviço [SQL Database](/docs/services/SQLDB/index.html#SQLDB) foi atualizado para usar sempre os certificados confiáveis da JVM ao conectar-se ao serviço sobre TLS.

### 22 de julho de 2016: atualizado o buildpack do Liberty v3.1-20160717-2254
* A funcionalidade [App Management](/docs/manageapps/app_mng.html) foi atualizada para suportar autenticação federada. Além disso, o tempo de execução do Node.js que é usado pelos utilitários `devconsole` e `shell` foi atualizado para a versão mais recente `0.12.15`.
* O buildpack inclui suporte para o agente de monitoramento de aplicativo [Dynatrace Ruxit ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://www.dynatrace.com/en/ruxit/).
* O buildpack fornece um coletor de dados atualizado para o [serviço de Monitoramento e Analítica](/docs/services/monana/index.html#monana_oview).
* O buildpack também fornece uma versão atualizada do agente para o [Serviço de ajuste automático de escala](/docs/services/Auto-Scaling/index.html).
* A versão de runtime do Liberty mensal foi atualizada para a liberação [2016.7.0.0](https://developer.ibm.com/wasdev/blog/2016/06/30/beta-websphere-liberty-and-tools-july-2016/).

### 17 de junho de 2016: atualizado o buildpack do Liberty v3.0-20160608-1450
* O buildpack agora contém duas versões do WebSphere Liberty, a liberação estável mais recente e a mensal mais recente. Especificamente, ele fornece a liberação estável [16.0.0.2](http://www-01.ibm.com/support/docview.wss?uid=swg21984970) e a liberação mensal [2016.6.0.0](https://developer.ibm.com/wasdev/blog/2016/06/03/beta-websphere-liberty-and-tools-june-2016/). A liberação estável será usada por padrão. Consulte [versões do Liberty](buildpackDefaults.html#liberty_versions) para obter detalhes adicionais.
* O buildpack contém também correções de segurança para as [vulnerabilidades de Taglibs do Apache Standard](http://www-01.ibm.com/support/docview.wss?uid=swg21985531).

### 25 de maio de 2016: atualizado o buildpack do Liberty v2.9-20160519-1249
* O buildpack contém uma versão atualizada do WebSphere Liberty com base na [beta de maio](https://developer.ibm.com/wasdev/blog/2016/05/06/beta-websphere-liberty-and-tools-may-2016/). A versão atualizada do Liberty torna os recursos beta *bluemixLogCollector-1.1* e *logstashCollector-1.1* disponíveis no Bluemix.

### 5 de maio de 2016: atualizado o buildpack do Liberty v2.8-20160430-1011
* O buildpack contém uma versão atualizada do WebSphere Liberty com base na [beta de abril](https://developer.ibm.com/wasdev/blog/2016/04/08/beta-websphere-liberty-and-tools-april-2016/). A versão atualizada do Liberty disponibiliza no Bluemix os recursos beta *logstashCollector-1.0* GA e *logmetCollector-1.0*.
* O buildpack contém também versões atualizadas do IBM JRE: 8 SR3 e 7.1 SR3 FP40.
* O buildpack inclui suporte inicial para o agente de monitoramento de aplicativo [AppDynamics ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://www.appdynamics.com/).
* O suporte do [Dynatrace](dynatrace.html) foi melhorado para simplificar a instalação do agente.
* O buildpack fornece um coletor de dados atualizado para o [serviço de Monitoramento e Analítica](/docs/services/monana/index.html#monana_oview). Ele contém uma correção para um problema com a coleta dos dados de heap máximo.
* O tempo de execução Node.js que é usado pelos [utilitários de gerenciamento de app devconsole e shell](/docs/manageapps/app_mng.html#app_management) foi atualizado para a versão mais recente 0.12.13.

### 25 de março de 2016: Atualizado o buildpack do Liberty v2.7-20160321-1358
* O buildpack contém uma versão atualizada do WebSphere Liberty com base no [beta de março](https://developer.ibm.com/wasdev/blog/2016/03/18/new-websphere-liberty-features-march-2016/). A versão atualizada do Liberty disponibiliza o recurso beta cloudant-1.0 no Bluemix.
* O buildpack também contém versões atualizadas do IBM JRE: 8 SR2 FP12 e 7.1 SR3 FP32.
* O buildpack fornece uma versão atualizada do agente para o [serviço de ajuste automático de escala](/docs/services/Auto-Scaling/index.html).
* O buildpack agora vem com um novo coletor de dados para o [serviço Monitoring and Analytics](/docs/services/monana/index.html#monana_oview). O novo coletor permite a configuração de limites de monitoramento e contém uma série de correções de bug.
* O buildpack fornece um driver JDBC atualizado do DB2® versão 4.19.49.
* O tempo de execução do Node.js que é usado pelos [utilitários devconsole e shell do App Management](/docs/manageapps/app_mng.html#app_management) foi atualizado para a versão mais recente 0.12.12.

### 7 de março de 2016: Atualizado o buildpack do Liberty v2.6-20160225-1649
* O buildpack inclui suporte para o monitoramento de aplicativos Dynatrace. Veja [Usando o Dynatrace](dynatrace.html) para obter detalhes.
* O buildpack inclui suporte para o [DynamicPULSE](www.fujitsu.com/jp/group/fsweb/products/dynamic-pulse/).

### 10 de fevereiro de 2016: Atualizado o buildpack do Liberty v2.5-20160209-1336
* O buildpack contém uma versão atualizada do WebSphere Liberty com base no [beta de fevereiro](https://developer.ibm.com/wasdev/blog/2016/02/12/beta-websphere-liberty-and-tools-february/). A versão atualizada do perfil Liberty disponibiliza o recurso apiDiscovery-1.0 GA no Bluemix.

### 4 de fevereiro de 2016: Atualizado o buildpack do Liberty v2.4-20160127-1437
* O buildpack contém uma versão atualizada do WebSphere Liberty com base no beta de janeiro. Com essa atualização, o recurso do Liberty scim-1.0, disponível anteriormente como um recurso beta, está agora disponível como um recurso pronto para produção. A versão atualizada do Liberty também disponibiliza o recurso beta passwordUtilities-1.0 no Bluemix.
* O buildpack também contém um IBM JRE 7.1 SF3 FP20 e um IBM JRE 8 SR2 FP10 atualizados.
* O buildpack foi atualizado para fazer download do [driver JDBC MariaDB Connector/J ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/) 1.x mais recente ao executar a [configuração automática para o tipo de serviços MySQL](autoConfig.html).

### 16 de dezembro de 2015: Atualizado o buildpack do Liberty v2.3-20151208-1311
* O buildpack contém uma versão atualizada do perfil Liberty com base no [beta de dezembro](https://developer.ibm.com/wasdev/blog/2015/11/20/beta-was-liberty-beta-with-tools-december-2015/). A versão atualizada do perfil Liberty disponibiliza os recursos spnego-1.0 e wsSecuritySaml-1.1 GA e o recurso beta scim-1.0 no Bluemix.
* O buildpack também contém um IBM JRE 8 SR2 atualizado.
* O buildpack também foi atualizado para fazer download do [driver JDBC 9.4.x PostgreSQL ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://jdbc.postgresql.org/) mais recente e do [driver JDBC MariaDB Connector/J ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/) 1.2.x ao executar a [configuração automática](autoConfig.html) para o tipo de serviços PostgreSQL ou MySQL.

### 23 de novembro de 2015: Atualizado o buildpack do Liberty v2.2-20151119-1720
* O buildpack contém uma versão atualizada do tempo de execução do perfil Liberty e do WebSphere eXtreme Scale Client com correções de segurança para a [Vulnerabilidade do Apache Commons Collection](http://www-01.ibm.com/support/docview.wss?uid=swg21971426).
* O buildpack também contém uma versão atualizada do [Java MongoDB Driver ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://docs.mongodb.org/ecosystem/drivers/java/), v2.13.3. O novo driver é compatível com MongoDB versão 2.4, 2.6 e 3.0.
* O buildpack também fornece uma versão atualizada do coletor de dados para o [serviço Monitoring and Analytics](/docs/services/monana/index.html). O coletor de dados atualizado melhorou as capacidades de rastreio do método.

### 16 de outubro de 2015: Atualizado o buildpack Liberty v2.1-20151006-0912
* O buildpack contém uma versão atualizada do perfil Liberty com base no [Beta de outubro](https://developer.ibm.com/wasdev/blog/2015/09/25/beta-was-liberty-beta-with-tools-october-2015/). Com essa atualização, os recursos do Liberty bells-1.0, rtcomm-1.0, rtcommGateway-1.0, samlWeb-2.0, sipServlet-1.1, disponíveis anteriormente como recursos beta, agora estão disponíveis como recursos prontos para produção.
* O buildpack também contém um IBM JRE 8 SR1 FP11 atualizado.
* O buildpack também fornece um número de otimizações e melhorias de desempenho:
  * O recurso de varredura de bean archive implícito [CDI 1.2](optionsForPushing.html) é desativado por padrão ao implementar os arquivos WAR ou EAR.
  * Para reduzir o tamanho do droplet, os [Utilitários do App Management](/docs/manageapps/app_mng.html) devconsole e shell requerem uma operação de remontagem em vez de uma reinicialização.
  * O cache de classe compartilhada do IBM JRE foi desativado porque não estava sendo reutilizado no ambiente do Bluemix.

### 18 de setembro de 2015: Atualizado o buildpack Liberty v2.0-20150914-1535
* O buildpack apresenta duas mudanças principais:
  * A configuração padrão para arquivos WAR e EAR ativa os recursos do Java EE 7 Web Profile em vez dos recursos Java EE 6 Web Profile.
  * A versão Java padrão é a versão 8 em vez da versão 7.
* Consulte a postagem do blog [Próximas mudanças do buildpack do Liberty for Java](https://developer.ibm.com/bluemix/2015/09/08/upcoming-liberty-for-java-buildpack-changes/) para obter detalhes sobre essas mudanças e como podem afetar seu aplicativo.
* O buildpack também apresenta a opção de configuração app_state para desativar o recurso appstate por meio da variável de ambiente JBP_CONFIG_LIBERTY. O recurso appstate é integrado ao processo de verificação de funcionamento do Cloud Foundry para assegurar que o aplicativo Liberty seja totalmente inicializado antes que o aplicativo possa receber as solicitações de HTTP. Para desativar o recurso appstate, é possível configurar a variável de ambiente JBP_CONFIG_LIBERTY como “app_state: false”.

### 4 de setembro de 2015: Atualizado o buildpack Liberty v1.22-20150824-1104
* O buildpack suporta as [Variáveis de ambiente HTTP_PROXY e HTTPS_PROXY](environmentVariables.html). Se configurado, o buildpack usa o servidor proxy especificado por essas variáveis de ambiente quando fizer download de vários componentes de buildpack.

### 19 de agosto de 2015: Atualizado o buildpack Liberty v1.21-20150811-1342
* O buildpack contém uma versão atualizada do perfil Liberty baseado no [beta de agosto](https://developer.ibm.com/wasdev/blog/2015/07/30/beta-was-liberty-beta-with-tools-august-2015/). A versão atualizada do perfil Liberty disponibiliza os novos [recursos beta](usingBetaFeatures.html) a seguir no Bluemix: bells-1.0, rtcommGateway-1.0, samlWebSso-2.0.

### 31 de julho de 2015: Atualizado buildpack Liberty v1.20.1-20150729-1255
* O buildpack contém versões atualizadas de IBM JREs: 7.1 SR1 FP10 e 8 SR1 FP10.
Os JREs atualizados contêm as [mais recentes correções de segurança](http://www-01.ibm.com/support/docview.wss?uid=swg21964161) e outras melhorias.
* O plug-in de serviço que fornece [suporte de configuração automática](autoConfig.html) para o serviço [Cloudant NoSQL Database](/docs/services/Cloudant/index.html#Cloudant) foi atualizado para assegurar que as conexões com o serviço sejam estabelecidas por meio de um canal seguro.

### 21 de julho de 2015: Buildpack do Liberty v1.20-20150713-1450 atualizado
* O buildpack contém uma versão atualizada do perfil Liberty na [liberação 8.5.5.6](https://developer.ibm.com/wasdev/blog/2015/06/25/java-ee-7-has-landed-in-was-liberty/). Com essa liberação, todos os recursos Java EE 7 Liberty disponíveis anteriormente como recursos beta, agora estão disponíveis como recursos prontos para produção. Devido a restrições de porta e outras restrições no Bluemix, alguns recursos como, por exemplo, EJBs remotos não são totalmente suportados na plataforma.
* O buildpack reconhece e executa aplicativos empacotados no [distZip-style ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://docs.gradle.org/current/userguide/application_plugin.html).
* O buildpack contém um coletor de dados atualizado para o [Monitoring and Analytics Service](/docs/services/monana/index.html) e o Cliente WebSphere eXtreme Scale que suportam o nova versão de tempo de execução do Liberty.

### 30 de junho de 2015: Buildpack do Liberty v1.19.1-20150622-1509 atualizado
* Essa versão do buildpack contém um IBM JRE atualizado com uma correção de segurança para a [Vulnerabilidade LogJam](http://www-01.ibm.com/support/docview.wss?uid=swg21961390).
* O agente [New Relic](newRelic.html) foi atualizado para a versão 3.17. A nova versão fornece integração aprimorada com o tempo de execução do perfil Liberty.

### 14 de junho de 2015: Buildpack do Liberty v1.19-20150608-1717 atualizado
* O buildpack contém inúmeros aprimoramentos de gerenciamento de aplicativo que incluem suporte para o console de desenvolvimento e acesso de shell baseado na web. Consulte a [documentação do App Management](/docs/manageapps/app_mng.html) para obter detalhes.
* O buildpack também contém uma correção para um problema em que o recurso Liberty para o [Monitoring and Analytics Service](/docs/services/monana/index.html) não pôde ser localizado.

### 27 de maio de 2015: Buildpack do Liberty v1.18-20150519-1642 atualizado
* O buildpack contém uma versão atualizada do perfil Liberty com base no [beta de maio](https://developer.ibm.com/wasdev/blog/2015/05/08/beta-liberty-and-tools-may-2015/).

### 5 de maio de 2015: Buildpack do Liberty v1.17-20150501-1729 atualizado
* O buildpack contém uma versão atualizada do perfil Liberty com base no [beta de abril](https://developer.ibm.com/wasdev/blog/2015/04/10/announcing-liberty-beta-with-tools-aprilmay-2015/). Com essa atualização, os recursos do Liberty jsp-2.3, el-3.0 e jdbc-4.1, anteriormente disponíveis como recursos beta, agora estão disponíveis como recursos prontos para produção. Além disso, recursos adicionais do Java EE 7, como jsf-2.2, javaMail-1.5, webProfile-7.0 e javaee-7.0, agora estão disponíveis como [recursos beta](usingBetaFeatures.html).
* O buildpack também fornece suporte inicial para Java 8. O IBM JRE 7.1 permanece o JRE padrão, mas o IBM JRE 8 pode ser ativado para um aplicativo configurando a variável de ambiente JBP_CONFIG_IBMJDK. A configuração da versão do OpenJDK também é suportada. Consulte [Customizando o JRE](customizingJRE.html) para obter todos os detalhes.
* O buildpack fornece uma nova variável de ambiente JBP_CONFIG_LIBERTY que pode ser usada para substituir a configuração padrão dos recursos Liberty ativados para um aplicativo quando implementa um arquivo WAR ou EAR. Consulte [Aplicativos independentes](optionsForPushing.html#stand_alone_apps) para obter mais informações.
* O plug-in de serviço para o [Monitoring and Analytics Service](/docs/services/monana/index.html) foi atualizado para reduzir o tamanho de logs que são gerados para o serviço.
* Com essa versão do buildpack, foi mudada a maneira como os arquivos de aplicativo são colocados no droplet. A mudança na estrutura do arquivo eliminou a complexidade relacionada à manutenção dos links simbólicos e não deve ter impacto nos aplicativos.

### 15 de abril de 2015: Buildpack do Liberty v1.16-20150407-1737 atualizado
* Essa versão do buildpack contém um IBM JRE 7.1-2.11 atualizado com uma [correção de segurança para a vulnerabilidade Bar Mitzvah](http://www-01.ibm.com/support/docview.wss?uid=swg21882777).
* Quando os arquivos WAR independentes são implementados, se fornecidos, o buildpack agora usa a raiz de contexto especificada no arquivo **ibm-web-ext.xml** integrado como a raiz de contexto do aplicativo. Com essa mudança, os aplicativos que foram implementados anteriormente sob o contexto-raiz podem ser implementados sob um contexto diferente com base nas configurações no arquivo **ibm-web-ext.xml**.

### 3 de abril de 2015: Buildpack do Liberty v1.15-20150402-1422 atualizado
* O buildpack contém uma versão atualizada do perfil Liberty com base no [beta de março](https://developer.ibm.com/wasdev/blog/2015/03/13/announcing-liberty-beta-tools-march-2015/). A versão atualizada dos perfis Liberty torna o recurso beta jsf-2.2 disponível no Bluemix.
* O buildpack também contém uma versão atualizada do coletor de dados para o [Monitoring and Analytics Service](/docs/services/monana/index.html).

### 20 de março de 2015: Buildpack do Liberty v1.14-20150319-1159 atualizado
* Essa versão do buildpack contém um IBM JRE 7.1.2.11 atualizado com uma correção de segurança para a [vulnerabilidade FREAK](http://www-01.ibm.com/support/docview.wss?uid=swg21699864).
* O serviço [ Banco de dados SQL](services/SQLDB/index.html#SQLDB) oferece planos pagos que fornecem uma opção para conectar-se ao servidor de banco de dados através do protocolo SSL. O suporte de configuração automática do buildpack para o serviço de banco de dados SQL foi atualizado para configurar o tempo de execução e conectar-se ao banco de dados através do SSL, caso as informações de conexão SSL estejam disponíveis.
* O buildpack foi atualizado para relatar um erro, quando for implementado um arquivo WAR ou EAR independente que contém um arquivo de configuração **server.xml ** na raiz do archive do aplicativo.
* O buildpack contém uma correção para o plug-in de serviço de configuração automática do MongoDB que em certos casos gerou uma configuração **server.xml** inválida.

### 10 de fevereiro de 2015: Buildpack do Liberty v1.13-20150209-1122 atualizado
* O buildpack contém correções de segurança para as [vulnerabilidades do Apache HttpComponents e do recurso de sobreposição Java](https://www-304.ibm.com/connections/blogs/PSIRT/entry/ibm_security_bulletin_multiple_vulnerabilities_fixed_in_liberty_for_java_for_ibm_bluemix_cve_2012_6153_cve_2014_3577_cve_2015_0178?lang=en_us).
* O buildpack contém uma versão atualizada do perfil Liberty com base no [beta de fevereiro](https://developer.ibm.com/wasdev/blog/2015/02/13/announcing-liberty-beta-tools-february-2015/). A versão atualizada do perfil Liberty fornece uma versão atualizada do recurso WebSocket GA websocket-1.1. Ela também disponibiliza os recursos beta do Java EE 7 a seguir no Bluemix:
  * cdi-1.2, el-3.0, jsp-2.3,  jca-1.7, jacc-1.5 e jaspic-1.1
* O buildpack fornece integração com a [ferramenta JRebel do ZeroTrunaround ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://zeroturnaround.com/software/jrebel/). A integração facilita usar o JRebel com aplicativos Bluemix e executar atualizações instantâneas do aplicativo sem reimplementar ou remontar o aplicativo. Somente os aplicativos da web independentes são suportados.

### 6 de fevereiro de 2015: Buildpack do Liberty v1.12-20150130-1016 atualizado
* O buildpack contém uma versão atualizada do perfil Liberty com base no [beta de janeiro](https://developer.ibm.com/wasdev/blog/2015/01/16/announcing-liberty-beta-tools-january-2015/).
* O buildpack contém uma versão aparada do coletor de dados para o [serviço Monitoring and Analytics](/docs/services/monana/index.html#gettingstartedtemplate).

### 23 de janeiro de 2015: Buildpack do Liberty v1.11-20150119-1511 atualizado
* O buildpack contém um IBM JRE versão 7.1 SR2 FP1 atualizado.
* Ele também contém um WebSphere eXterme Scale Client versão 8.6.0.6 atualizado e um agente atualizado para o serviço de ajuste automático de escala.
* O suporte ao serviço [New Relic](newRelic.html) foi aprimorado para suportar serviços definidos pelo usuário.
* O buildpack foi melhorado para relatar versões detalhadas do perfil Liberty e do IBM JRE.

### 19 de dezembro de 2014: buildpack do Liberty atualizado v1.10-20141218-0103
* O buildpack fornece um modo de desenvolvimento para aplicativos. O modo de desenvolvimento é um modo especial que permite aos desenvolvedores conduzir várias atividades de uma instância de aplicativo que não eram possíveis antes. Usando esse recurso, essa versão do IBM Eclipse Tools for Bluemix agora pode suportar a depuração remota com atualizações de arquivos incrementais com relação a um aplicativo Liberty em execução no Bluemix. Isso torna-o conveniente para um desenvolvedor que use o Eclipse para depurar um aplicativo na nuvem e aplicar mudanças nesse aplicativo instantaneamente.
* O buildpack contém também uma versão atualizada do perfil do Liberty com base no [Beta de dezembro](https://developer.ibm.com/wasdev/blog/2014/12/10/announcing-liberty-beta-december/).
* Além disso, os quatro recursos do Liberty a seguir que estavam disponíveis anteriormente como recursos beta, agora estão prontos para produção:
  * concurrent-1.0
  * jsonp-1.0
  * servlet-3.1
  * websocket-1.0.
* O buildpack fornece integração com o serviço New Relic. Uma vez que um aplicativo está ligado ao serviço New Relic, o buildpack faz downloads e configura automaticamente o tempo de execução com o agente do New Relic.
* O buildpack tem as limitações conhecidas a seguir:
  * Quando estiver no modo de desenvolvimento, um serviço SessionCache não pode ser ligado.
  * Quando estiver no modo de desenvolvimento, um dump de encadeamento não pode ser criado.
  * Ao usar o recurso do servlet-3.1 ou websocket-v1.0, o serviço Monitoring & Analytics não poderá ser ligado.

### 5 de dezembro de 2014: buildpack do Liberty atualizado v1.9-20141202-0947
* O buildpack fornece um suporte à opção JVM aprimorada. As opções de JVM agora podem ser aplicadas com uma operação de reinicialização. Não é necessário migrar novamente o aplicativo. Além disso, as opções JVM padrão são otimizadas para falha rápida e pré-configurada com um local comum que facilita a localização dos dumps gerados. Mais detalhes são fornecidos no [artigo Configuração customizada de JVM Java pra o tempo de execução do Liberty](https://developer.ibm.com/bluemix/2014/12/12/custom-configurations-java-jvm-liberty-runtime/).
* O buildpack contém um driver JDBC atualizado do DB2 versão 4.17.29.
* Ele contém também uma correção para um problema que impediu a coleta das informações de uso do conjunto de encadeamento do Liberty para o serviço Monitoring & Analytics.

### 21 de novembro de 2014: buildpack do Liberty atualizado v1.8-20141118-1610
* O buildpack contém um IBM JRE versão 7.1 SR2 atualizado que fornece uma correção para a [vulnerabilidade POODLE](http://www-01.ibm.com/support/docview.wss?uid=swg21687173).
* Ele contém também uma versão atualizada do perfil do Liberty com base no [beta de novembro](https://developer.ibm.com/wasdev/blog/2014/11/07/announcing-liberty-profile-beta-november/).

### 30 de outubro de 2014: buildpack do Liberty atualizado v1.7-20141020-1759
* O buildpack contém um IBM JRE atualizado versão 7.1 SR1 FP3.
* Ele fornece também uma correção de um problema que impediu a implementação de aplicativos com a configuração do servidor que continha caracteres Unicode.

### 23 de outubro de 2014: Buildpack do Liberty atualizado v1.6-20141013-1628
* Agora, o buildpack vem com um novo coletor de dados para o [Monitoring and Analytics](/docs/services/monana/index.html). O novo coletor de dados coleta informações mais abrangentes de diagnóstico, permitindo que os usuários do plano de Diagnósticos do serviço diagnostiquem problemas com seus aplicativos, indo diretamente para a linha específica do código.
* O buildpack contém versões atualizadas dos agentes de gerenciamento e de ajuste automático de escala, que incluem correções de bugs e outras melhorias. Ele também inclui uma versão atualizada do [perfil Liberty](https://developer.ibm.com/wasdev/) e do [Java MongoDB Driver![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://docs.mongodb.org/ecosystem/drivers/java/), v2.12.3.
* No recurso cloudAutowiring, um erro que causava erros de injeção de recurso em alguns aplicativos foi corrigido.

### 3 de outubro de 2014: Buildpack do Liberty atualizado v1.5-20140923-1143
* Com o buildpack atualizado, agora, os aplicativos podem usar os recursos beta do Liberty, incluindo o WebSocket 1.0, o Servlet 3.1 ou o JAX-RS 2.0. Para obter mais informações, veja [Usando os recursos beta](usingBetaFeatures.html).

### 30 de setembro de 2014: Buildpack do Liberty atualizado v1.4-20140908-1803
* Agora o buildpack fornece suporte aos serviços de banco de dados de terceiros, ElephantSQL e ClearDB MySQL. O suporte de configuração automática também trabalha com os serviços experimentais do posgresql e do mysql. Com o novo total de 13 serviços, o suporte de configuração automática no buildpack do Liberty faz com que o consumo de serviços do Bluemix seja mais rápido e fácil nos aplicativos Liberty.
* Durante a preparação do aplicativo, o buildpack exibe mensagens de log melhoradas sobre a configuração automática e outras ações que ele toma.
* O buildpack contém uma versão atualizada do perfil do Liberty com as correções e melhorias.
* Também contém uma versão atualizada do IBM JRE versão 7.1, que tem melhorias de desempenho. Consulte a página [O que há de novo](http://www-01.ibm.com/support/knowledgecenter/SSYKE2_7.0.0/com.ibm.java.lnx.71.doc/diag/preface/changes_71/changes.html) para obter um conjunto detalhado das mudanças.

### 28 de agosto de 2014: Buildpack do Liberty atualizado v1.3-20140818-1538
* O buildpack contém uma versão atualizada do [perfil Liberty](https://developer.ibm.com/wasdev/) com as correções e melhorias mais recentes.
* Esta versão do buildpack corrige o suporte para a variável de ambiente JAVA_OPTS passando opções JVM adicionais para o tempo de execução de aplicativo.
* Ela também corrige um problema que impedia a implementação de aplicativos Jar independentes baseados em Spring.
* Agora é possível gerar e fazer o download de traços snap do IBM JVM usando a IU do Bluemix. Veja o [tópico Resolução de problemas](http://www-01.ibm.com/support/knowledgecenter/SSYKE2_7.0.0/com.ibm.java.lnx.70.doc/troubleshooting.html) na documentação do IBM JVM para aprender mais sobre os traços snap ou outras informações de diagnóstico geradas pela JVM.

### 29 de julho de 2014: Buildpack do Liberty atualizado v1.1-20140725-1341
* A nova versão do Bluemix Edition do Liberty está aqui!
  * Com essa versão do Liberty, existem correções além dos novos recursos que permitem consumir os serviços Bluemix de forma mais efetiva!
  * Com o novo recurso CouchDB disponível, o serviço Cloudant® agora pode configurá-lo automaticamente para que um objeto do conector fique disponível com facilidade! Não é mais necessário analisar através do VCAP_SERVICES e fornecer os jars de cliente ektorp.
* A nova versão do IBM SDK for Java está aqui!
  * Quando seus aplicativos forem enviados por push novamente, eles usarão o IBM SDK for Java Versão 7.1-1.0. Isso é fornecido com um upgrade de desempenho substancial. Seu aplicativo mostra melhor rendimento e uso de memória reduzido. Saiba mais sobre o IBM Java SDK [aqui](http://www-01.ibm.com/support/docview.wss?uid=swg21671466).

# rellinks
{: #rellinks notoc}
## geral
{: #general notoc}
  * [Tempo de execução do Liberty](index.html)
  * [Visão geral do perfil Liberty](http://www-01.ibm.com/support/knowledgecenter/SSAW57_8.5.5/com.ibm.websphere.wlp.nd.doc/ae/cwlp_about.html)
