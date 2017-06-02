---

copyright:
  years: 2015, 2017
lastupdated: "2017-03-23"

---

{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Neueste Aktualisierungen für das Liberty-Buildpack
{: #latest_updates}

## Eine Liste mit den neuesten Aktualisierungen im Liberty-Buildpack.

### 14. März 2017: Liberty-Buildpack v3.8-20170308-1507 aktualisiert

* Die Standardversion der Liberty-Laufzeit wurde auf Release 17.0.0.1 aktualisiert.
* Die Standardversion der Liberty-Laufzeit umfasst auch das PI75512 WebSockets iFix.
* Die monatliche Liberty-Laufzeitversion wurde auf das Release [2017.2.0.0](https://developer.ibm.com/wasdev/blog/2017/02/17/beta-websphere-liberty-tools-february-2017/) aktualisiert.
* Die IBM JRE-Versionen 8 und 7.1 wurden auf SR4 FP1 aktualisiert.
* Die Unterstützung für die automatische Konfiguration wurde auf [ibm-websphere-extreme-scale IBM Container](https://console.ng.bluemix.net/docs/images/docker_image_extreme_scale/ibm-websphere-extreme-scale_starter.html) erweitert.
* Die Unterstützung für die automatische Konfiguration für [Cloudant NoSQL Database](https://console.ng.bluemix.net/docs/services/Cloudant/index.html) wurde aktualisiert, um die Option zur Verwendung von Cloudant Java Library anstelle von org.ektorp zur Verfügung zu stellen. Um die Verwendung von Cloudant Java Library zu aktivieren, müssen Sie die folgende Umgebungsvariable festlegen:    
```
cf set-env <appName> LBP_SERVICE_CONFIG_CLOUDANTNOSQLDB 'type : cloudant'
```
* Das Buildpack bietet ferner eine aktualisierte Version des Agenten für den [Service 'Auto-Scaling'](/docs/services/Auto-Scaling/index.html) und eine Reihe von Anwendungsmanagementerweiterungen.
* Dieses Buildpack ändert außerdem die Funktionsweise der automatischen Konfiguration für den [Service 'Monitoring and Analytics'](/docs/services/monana/index.html). Anwendungen mit dem kostenfreien Plan verfügen bei Ihren Anwendungen nicht mehr über die Protokollfunktion; die durch logmet ersetzt wurde.  


### 23. Januar 2017: Liberty-Buildpack v3.7-20170118-2046 aktualisiert
* Die monatliche Liberty-Laufzeit wurde auf das Release [2017.1.0.0](https://developer.ibm.com/wasdev/blog/2017/01/20/beta-websphere-liberty-tools-january-2017/) aktualisiert.
* Die IBM JRE-Version 8 wurde auf die Version SR3 FP22 aktualisiert. 
* Die Unterstützung für die [automatische Konfiguration](autoConfig.html) wurde auch auf den [Service 'Compose for MongoDB'](https://console.ng.bluemix.net/docs/services/ComposeForMongoDB/index.html) erweitert. (Aktuell nur über die monatliche Liberty-Laufzeit verfügbar.)

### 13. Dezember 2016: Liberty-Buildpack v3.6-20161209-1351 aktualisiert
* Die Standardversion der Liberty-Laufzeit wurde auf Release [16.0.0.4](http://www-01.ibm.com/support/docview.wss?uid=swg27009661) aktualisiert. 
* Die IBM JRE-Version 8 wurde auf die Version SR3 FP21 aktualisiert. 
* Die Unterstützung für die [automatische Konfiguration](autoConfig.html) wurde auch auf den [Service 'Compose for PostgreSQL'](https://console.ng.bluemix.net/docs/services/ComposeForPostgreSQL/index.html) erweitert.
* Das Buildpack stellt auch eine aktualisierte Version des Agenten für den [Service 'Auto-Scaling'](/docs/services/Auto-Scaling/index.html) bereit.
* Das Buildpack wurde für die Unterstützung von Umgebungsvariablen als Teil der Includepositionen (include locations) in den Dateien `server.xml`-Dateien aktualisiert.

### 29. November 2016: Liberty-Buildpack v3.5-20161114-1152 aktualisiert
* Die Standardversion der Liberty-Laufzeit `16.0.0.3` wurde aktualisiert, um den iFix [PI62375](https://www-01.ibm.com/support/docview.wss?uid=swg24042712) einzuschließen und die Komfortfuntion `microProfile-1.0` zur Verfügung zu stellen.
* Die monatliche Liberty-Laufzeitversion wurde auf das Release `2016.11.0.0` aktualisiert.
* Das Buildpack enthält ferner aktualisierte IBM JREs: Version 8 SR3 FP20 und Version 7.1 SR3 FP60.
* Der DB2 JDBC-Treiber wurde auf Version `4.21.29` aktualisiert.
* Die Integration des Service 'Monitoring and Analytics' wurde verändert, um die Funktion mit [Diego ![Symbol 'Externer Link'](../../icons/launch-glyph.svg "Symbol 'Externer Link'")](https://docs.cloudfoundry.org/concepts/diego/diego-architecture.html) zu ermöglichen.
* Die Serviceintegrationen von [Dynatrace](dynatrace.html) wurden aktualisiert, um eine bessere Funktion mit den Serviceangeboten von Dynatrace zu ermöglichen.
* Die Unterstützung für die [automatische Konfiguration](autoConfig.html) für die PostgreSQL- und MySQL-Servicetypen wurde verbessert, damit die Bereitstellung eines Serververzeichnisses oder eines paketierten Servers besser zu funktioniert.
* Die Node.js-Laufzeit, die von den [App-Management-Dienstprogrammen 'devconsole' und 'shell'](/docs/manageapps/app_mng.html#app_management) verwendet wird, wurde auf die neueste Version `0.12.17` aktualisiert.
* [Sicherheitsfixes](http://www.ibm.com/support/docview.wss?uid=swg21994945) für die Liberty-Laufzeit sind eingeschlossen. 

### 1. November 2016: Liberty-Buildpack v3.4.1-20161030-2241 aktualisiert
* Das Buildpack enthält eine Programmkorrektur für ein Problem beim Starten bestimmter Anwendungstypen. Insbesondere Anwendungen, die als Serververzeichnis oder paketierter Server mit Anwendungsdateien im Verzeichnis `dropins` bereitgestellt wurden. 

### 21. Oktober 2016: Liberty-Buildpack v3.4-20161018-2004 aktualisiert
* Die Standardversion der Liberty-Laufzeit `16.0.0.3` wurde aktualisiert, um die iFixes [PI68805](http://www-01.ibm.com/support/docview.wss?uid=swg1PI68805) und [PI69141](http://www-01.ibm.com/support/docview.wss?uid=swg1PI69141) einzuschließen. 
* Die monatliche Liberty-Laufzeitversion wurde auf das Release [2016.9.0.1](https://developer.ibm.com/wasdev/blog/2016/09/23/beta-websphere-liberty-and-tools-october-2016/) aktualisiert. 
* Das Buildpack enthält ferner eine aktualisiere Version der IBM JRE 8.0: SR3 FP12.
* Die IBM JRE 8.0 und 7.1 sind nun so konfiguriert, dass sie [alle TLS-Protokolle aktivieren, wenn `SSLContext.getContext("TLS")` aufgerufen wird](https://www.ibm.com/support/knowledgecenter/SSYKE2_8.0.0/com.ibm.java.security.component.80.doc/security-component/jsse2Docs/matchsslcontext_tls.html), um das Verhalten der JRE von Oracle abzugleichen. IBM JRE 7.1 wird ferner konfiguriert, um [alle TLS-Protokolle zu aktivieren, wenn `SSLContext.getDefault()` aufgerufen wird](https://www.ibm.com/support/knowledgecenter/SSYKE2_7.1.0/com.ibm.java.security.component.71.doc/security-component/jsse2Docs/overrideSSLprotocol.html), um das Verhalten der JRE 8.0 von IBM abzugleichen. 
* Das Buildpack stellt einen aktualisierten Datenkollektor für den [Service 'Monitoring and Analytics'](/docs/services/monana/index.html#monana_oview) bereit.
* Das Buildpack wurde zurückgeändert, um den aktuellsten 1.5.x [MariaDB Connector/J JDBC-Treiber ![Symbol 'Externer Link'](../../icons/launch-glyph.svg "Symbol 'Externer Link'")](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/) herunterzuladen, wenn die [automatische Konfiguration für Services vom Typ MySQL](autoConfig.html) ausgeführt wird.
* Das Buildpack führt die Unterstützung für die Verhaltensanpassung des automatischen Konfigurationsservice über die Umgebungsvariable `LBP_SERVICE_CONFIG_<serviceType>` ein. Diese kann zum Beispiel verwendet werden, um die Position oder Version eines JDBC-Treibers für das Herunterladen für den MySQL-Service zu ändern. Weitere Informationen finden Sie in der Dokumentation zu den [Services, die die automatische Konfiguration unterstützen](autoConfig.html). 
* Das Buildpack enthält ferner eine Reihe von Verbesserung für [Diego ![Symbol 'Externer Link'](../../icons/launch-glyph.svg "Symbol 'Externer Link'")](https://docs.cloudfoundry.org/concepts/diego/diego-architecture.html), die mit der Statusprüfung der Anwendung und der Funktion [App-Management](/docs/manageapps/app_mng.html) zusammenhängen.

### 16. September 2016: Liberty-Buildpack v3.3-20160912-1729 aktualisiert
* Die Standardversion der Liberty-Laufzeit wurde auf Release [16.0.0.3](http://www-01.ibm.com/support/docview.wss?uid=swg27009661) aktualisiert. Die monatliche Liberty-Laufzeit wurde auf das Release [2016.9.0.0](https://developer.ibm.com/wasdev/blog/2016/08/26/beta-websphere-liberty-and-tools-september-2016/) aktualisiert. Mit diesen Aktualisierungen stehen die Liberty-Features `cloudant-1.0` und `passwordUtilities-1.0`, die zuvor als Features der Betaversion verfügbar waren, nun als für die Produktion einsatzbereite Features zur Verfügung.
* [Sicherheitsfixes](http://www-01.ibm.com/support/docview.wss?uid=swg21990527) für die Liberty-Laufzeit sind eingeschlossen. 
* Das Buildpack enthält ferner eine aktualisierte Version der IBM JRE 8.0: SR3 FP11.
* Das Buildpack wurde so angepasst, dass es den aktuellsten 1.4.x [MariaDB Connector/J JDBC-Treiber ![Symbol 'Externer Link'](../../icons/launch-glyph.svg "Symbol 'Externer Link'")](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/) herunterlädt, wenn aufgrund eines Problems mit dem aktuellen 1.5.x-Treiber eine [automatische Konfiguration für Services vom Typ MySQL](autoConfig.html) ausgeführt wird.

### 26. August 2016: Liberty-Buildpack v3.2-20160822-2200 aktualisiert
* Das Buildpack enthält aktualisierte Versionen von IBM JRE: 8 SR3 FP10 und 7.1 SR3 FP50.
* Die monatliche Liberty-Laufzeitversion wurde auf das Release [2016.8.0.0](https://developer.ibm.com/wasdev/blog/2016/07/28/beta-websphere-liberty-and-tools-august-2016/) aktualisiert.
* Das Service-Plug-in, das [Unterstützung für die automatische Konfiguration](autoConfig.html) für den Service [SQL Database](/docs/services/SQLDB/index.html#SQLDB) bereitstellt, wurde aktualisiert, damit die vertrauenswürdigen Zertifikate der JVM immer verwendet werden, wenn eine Verbindung zum Service über TLS hergestellt wird.

### 22. Juli 2016: Liberty-Buildpack v3.1-20160717-2254 aktualisiert
* Die Funktion [App-Management](/docs/manageapps/app_mng.html) wurde aktualisiert und unterstützt jetzt die eingebundene Authentifizierung. Die Node.js-Laufzeit, die von den Dienstprogrammen `devconsole` und `shell` verwendet wird, wurde auf die neueste Version `0.12.15` aktualisiert.
* Das Buildpack fügt Unterstützung für den Anwendungsüberwachungsagenten [Dynatrace Ruxit ![Symbol 'Externer Link'](../../icons/launch-glyph.svg "Symbol 'Externer Link'")](http://www.dynatrace.com/en/ruxit/) hinzu.
* Das Buildpack stellt einen aktualisierten Datenkollektor für den [Service 'Monitoring and Analytics'](/docs/services/monana/index.html#monana_oview) bereit.
* Das Buildpack stellt auch eine aktualisierte Version des Agenten für den [Service 'Auto-Scaling'](/docs/services/Auto-Scaling/index.html) bereit.
* Die monatliche Liberty-Laufzeitversion wurde auf das Release [2016.7.0.0](https://developer.ibm.com/wasdev/blog/2016/06/30/beta-websphere-liberty-and-tools-july-2016/) aktualisiert.

### 17. Juni 2016: Liberty-Buildpack v3.0-20160608-1450 aktualisiert
* Das Buildpack enthält jetzt zwei Versionen von WebSphere Liberty, das neueste stabile Release und das neueste monatliche Release. Konkret handelt es sich um das stabile Release [16.0.0.2](http://www-01.ibm.com/support/docview.wss?uid=swg21984970) und das monatliche Release [2016.6.0.0](https://developer.ibm.com/wasdev/blog/2016/06/03/beta-websphere-liberty-and-tools-june-2016/). Standardmäßig wird das stabile Release verwendet. Weitere Details finden Sie in [Liberty-Versionen](buildpackDefaults.html#liberty_versions).
* Das Buildpack enthält Sicherheitskorrekturen für die [Sicherheitslücke in Apache Standard Taglibs](http://www-01.ibm.com/support/docview.wss?uid=swg21985531).

### 25. Mai 2016: Liberty-Buildpack v2.9-20160519-1249 aktualisiert
* Das Buildpack enthält eine aktualisierte Version von WebSphere Liberty, die auf der [Betaversion vom Mai](https://developer.ibm.com/wasdev/blog/2016/05/06/beta-websphere-liberty-and-tools-may-2016/) basiert. Mit der aktualisierten Version von Liberty werden die Beta-Features *bluemixLogCollector-1.1* und *logstashCollector-1.1* in Bluemix verfügbar gemacht.

### 5. Mai 2016: Liberty-Buildpack v2.8-20160430-1011 aktualisiert
* Das Buildpack enthält eine aktualisierte Version von WebSphere Liberty, die auf der [Betaversion vom April](https://developer.ibm.com/wasdev/blog/2016/04/08/beta-websphere-liberty-and-tools-april-2016/) basiert. Mit der aktualisierten Version von Liberty werden das GA-Feature *logstashCollector-1.0* und das Beta-Feature *logmetCollector-1.0* in Bluemix verfügbar gemacht.
* Das Buildpack enthält auch aktualisierte Versionen von IBM JRE: 8 SR3 und 7.1 SR3 FP40.
* Das Buildpack fügt Anfangsunterstützung für den Anwendungsüberwachungsagenten [AppDynamics ![Symbol 'Externer Link'](../../icons/launch-glyph.svg "Symbol 'Externer Link'")](https://www.appdynamics.com/) hinzu.
* Die [Dynatrace](dynatrace.html)-Unterstützung wurde verbessert, um die Installation des Agenten zu vereinfachen.
* Das Buildpack stellt einen aktualisierten Datenkollektor für den [Service 'Monitoring and Analytics'](/docs/services/monana/index.html#monana_oview) bereit. Er enthält einen Fix für ein Problem beim Erfassen der maximalen Heapspeicherdaten.
* Die von den [App-Management-Dienstprogrammen 'devconsole' und 'shell'](/docs/manageapps/app_mng.html#app_management) verwendete Node.js-Laufzeit wurde auf die neueste Version 0.12.13 aktualisiert.

### 25. März 2016: Liberty-Buildpack v2.7-20160321-1358 aktualisiert
* Das Buildpack enthält eine aktualisierte Version von WebSphere Liberty, die auf der [Betaversion vom März](https://developer.ibm.com/wasdev/blog/2016/03/18/new-websphere-liberty-features-march-2016/) basiert. Mit der aktualisierten Version von Liberty wird das Beta-Feature 'cloudant-1.0' in Bluemix verfügbar gemacht.
* Das Buildpack enthält auch aktualisierte Versionen von IBM JRE: 8 SR2 FP12 und 7.1 SR3 FP32.
* Das Buildpack stellt eine aktualisierte Version des Agenten für den [Service 'Auto-Scaling'](/docs/services/Auto-Scaling/index.html) bereit.
* Das Buildpack enthält nun einen neuen Datenkollektor für den [Service 'Monitoring and Analytics'](/docs/services/monana/index.html#monana_oview). Der neue Kollektor ermöglicht die Konfiguration von Schwellenwerten für die Überwachung und enthält eine Anzahl Fehlerkorrekturen.
* Das Buildpack stellt die aktualisierte Version 4.19.49 des DB2® JDBC-Treibers bereit.
* Die von den [Dienstprogrammen 'devconsole' und 'shell'](/docs/manageapps/app_mng.html#app_management) verwendete Node.js-Laufzeit wurde auf die neueste Version 0.12.12 aktualisiert.

### 7. März 2016: Liberty-Buildpack v2.6-20160225-1649 aktualisiert
* Das Buildpack fügt Unterstützung für die Dynatrace-Anwendungsüberwachung bereit. Details finden Sie in [Dynatrace verwenden](dynatrace.html).
* Das Buildpack fügt Unterstützung für [DynamicPULSE](www.fujitsu.com/jp/group/fsweb/products/dynamic-pulse/) hinzu.

### 10. Februar 2016: Liberty-Buildpack v2.5-20160209-1336 aktualisiert
* Das Buildpack enthält eine aktualisierte Version von WebSphere Liberty, die auf der [Betaversion vom Februar](https://developer.ibm.com/wasdev/blog/2016/02/12/beta-websphere-liberty-and-tools-february/) basiert. Mit der aktualisierten Version des Liberty-Profils wird das Beta-GA-Feature 'apiDiscovery-1.0' in Bluemix verfügbar gemacht.

### 4. Februar 2016: Liberty-Buildpack v2.4-20160127-1437 aktualisiert
* Das Buildpack enthält eine aktualisierte Version von WebSphere Liberty, die auf der Betaversion vom Januar basiert. Mit dieser Aktualisierung ist das Liberty-Feature 'scim-1.0', das bisher als Beta-Feature verfügbar war, nun als einsatzbereites Feature verfügbar. Mit der aktualisierten Version von Liberty wird auch das Beta-Feature 'passwordUtilities-1.0' in Bluemix verfügbar.
* Das Buildpack enthält auch die aktualisierten JRE-Versionen IBM JRE 7.1 SF3 FP20 und IBM JRE 8 SR2 FP10.
* Das Buildpack wurde aktualisiert, um die aktuellste Version 1.x des [MariaDB Connector/J JDBC-Treibers ![Symbol 'Externer Link'](../../icons/launch-glyph.svg "Symbol 'Externer Link'")](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/) herunterzuladen, wenn die [automatische Konfiguration für Services vom Typ MySQL](autoConfig.html) ausgeführt wird.

### 16. Dezember 2015: Liberty-Buildpack v2.3-20151208-1311 aktualisiert
* Das Buildpack enthält eine aktualisierte Version des Liberty-Profils, die auf der [Betaversion vom Dezember](https://developer.ibm.com/wasdev/blog/2015/11/20/beta-was-liberty-beta-with-tools-december-2015/) basiert. Mit der aktualisierten Version des Liberty-Profils werden die GA-Features 'spnego-1.0' und 'wsSecuritySaml-1.1' und das Beta-Feature 'scim-1.0' in Bluemix verfügbar gemacht.
* Das Buildpack enthält auch die aktualisierte IBM JRE Version 8 SR2.
* Das Buildpack wurde auch aktualisiert, um den aktuellsten [9.4.x PostgreSQL JDBC-Treiber ![Symbol 'Externer Link'](../../icons/launch-glyph.svg "Symbol 'Externer Link'")](https://jdbc.postgresql.org/) und Version des 1.2.x [MariaDB Connector/J JDBC-Treibers ![Symbol 'Externer Link'](../../icons/launch-glyph.svg "Symbol 'Externer Link'")](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/) herunterzuladen, wenn die [automatische Konfiguration](autoConfig.html) für Services vom Typ PostgreSQL oder MySQL ausgeführt wird.

### 23. November 2015: Liberty-Buildpack v2.2-20151119-1720 aktualisiert
* Das Buildpack enthält eine aktualisierte Version der Liberty-Profil-Laufzeit und von WebSphere eXtreme Scale Client mit Sicherheitskorrekturen für die [Apache Commons Collection-Sicherheitslücke](http://www-01.ibm.com/support/docview.wss?uid=swg21971426).
* Das Buildpack enthält ferner eine aktualisierte Version des [Java MongoDB-Treibers ![Symbol 'Externer Link'](../../icons/launch-glyph.svg "Symbol 'Externer Link'")](https://docs.mongodb.org/ecosystem/drivers/java/), Version 2.13.3. Der neue Treiber ist mit MongoDB Version 2.4, 2.6 und 3.0 kompatibel.
* Das Buildpack stellt auch eine aktualisierte Version des Datenkollektors für den [Service 'Monitoring and Analytics'](/docs/services/monana/index.html) bereit. Der aktualisierte Datenkollektor verfügt über verbesserte Funktionen für das Methodentracing.

### 16. Oktober 2015: Liberty-Buildpack v2.1-20151006-0912 aktualisiert
* Das Buildpack enthält eine aktualisierte Version des Liberty-Profils, die auf der [Betaversion vom Oktober](https://developer.ibm.com/wasdev/blog/2015/09/25/beta-was-liberty-beta-with-tools-october-2015/) basiert. Mit dieser Aktualisierung sind die Liberty-Features 'bells-1.0', 'rtcomm-1.0', 'rtcommGateway-1.0', 'samlWeb-2.0', 'sipServlet-1.1', die bisher als Beta-Features verfügbar waren, als einsatzbereite Features verfügbar.
* Das Buildpack enthält auch die aktualisierte JRE-Version IBM JRE 8 SR1 FP11.
* Mit dem Buildpack werden auch eine Reihe von Leistungsverbesserungen und Optimierungen bereitgestellt:
  * Die Funktion für das implizite Bean-Archiv-Scannen in [CDI 1.2](optionsForPushing.html) ist standardmäßig inaktiviert, wenn WAR- oder EAR-Dateien bereitgestellt werden.
  * Zum Reduzieren der Dropletgröße ist für die [App-Management-Dienstprogramme](/docs/manageapps/app_mng.html) 'devconsole' und 'shell' kein Neustart erforderlich, sondern eine Operation zum erneuten Staging.
  * Der Cache von IBM JRE für gemeinsam genutzte Klassen ist inaktiviert, da er in der Bluemix-Umgebung nicht wiederverwendet wurde.

### 18. September 2015: Liberty-Buildpack v2.0-20150914-1535 aktualisiert
* Das Buildpack umfasst zwei bedeutende Änderungen:
  * Mit der Standardkonfiguration für WAR- und EAR-Dateien werden statt den Java EE 6 Web Profile-Features nun die Java EE 7 Web Profile-Features aktiviert.
  * Die Java-Standardversion ist nun Version 8 statt Version 7.
* Weitere Informationen zu diesen Änderungen und dazu, wie sie sich auf Ihre Anwendung auswirken können, finden Sie im Blogbeitrag [Upcoming Liberty for Java buildpack changes](https://developer.ibm.com/bluemix/2015/09/08/upcoming-liberty-for-java-buildpack-changes/).
* Mit dem Buildpack wird außerdem die Konfigurationsoption 'app_state' zum Inaktivieren des Features 'appstate' über die Umgebungsvariable JBP_CONFIG_LIBERTY eingeführt. Das Feature 'appstate' wird mit dem Cloud Foundry-Statusprüfungsprozess integriert, um sicherzustellen, dass die Liberty-Anwendung vollständig initialisiert wird, bevor die Anwendung HTTP-Anforderungen empfangen kann. Zum Inaktivieren des Features 'appstate' können Sie die Umgebungsvariable JBP_CONFIG_LIBERTY auf 'app_state: false' festlegen.

### 4. September 2015: Liberty-Buildpack v1.22-20150824-1104 aktualisiert
* Das Buildpack unterstützt die [Umgebungsvariablen HTTP_PROXY und HTTPS_PROXY](environmentVariables.html). Bei entsprechender Festlegung verwendet das Buildpack den von diesen Umgebungsvariablen angegebenen Proxy-Server, wenn verschiedene Buildpack-Komponenten heruntergeladen werden.

### 19. August 2015: Liberty-Buildpack v1.21-20150811-1342 aktualisiert
* Das Buildpack enthält eine aktualisierte Version des Liberty-Profils, die auf der [Betaversion vom August](https://developer.ibm.com/wasdev/blog/2015/07/30/beta-was-liberty-beta-with-tools-august-2015/) basiert. Mit der aktualisierten Version des Liberty-Profils werden die folgenden neuen [Beta-Features](usingBetaFeatures.html) in Bluemix verfügbar gemacht: 'bells-1.0', 'rtcommGateway-1.0', 'samlWebSso-2.0'.

### 31. Juli 2015: Liberty-Buildpack v1.20.1-20150729-1255 aktualisiert
* Das Buildpack enthält aktualisierte Versionen der folgenden IBM JREs: 7.1 SR1 FP10 und 8 SR1 FP10.
Die aktualisierten JREs enthalten die [neuesten Sicherheitskorrekturen](http://www-01.ibm.com/support/docview.wss?uid=swg21964161) sowie weitere Verbesserungen.
* Das Service-Plug-in, mit dem [Unterstützung für die automatische Konfiguration](autoConfig.html) für den Service [Cloudant NoSQL Database](/docs/services/Cloudant/index.html#Cloudant) bereitgestellt wird, um sicherzustellen, dass die Verbindungen zum Service über einen sicheren Kanal hergestellt werden.

### 21. Juli 2015: Liberty-Buildpack v1.20-20150713-1450 aktualisiert
* Das Buildpack enthält eine aktualisierte Version des Liberty-Profils, die auf dem [Release 8.5.5.6](https://developer.ibm.com/wasdev/blog/2015/06/25/java-ee-7-has-landed-in-was-liberty/) basiert. Mit diesem Release sind alle Java EE 7 Liberty-Features, die bisher als Beta-Features verfügbar waren, als einsatzfähige Features verfügbar. Aufgrund von Portbeschränkungen und anderen Beschränkungen in Bluemix werden manche Features wie beispielsweise ferne EJBs nicht vollständig auf der Plattform unterstützt.
* Das Buildpack erkennt Anwendungen, die in [distZip-style ![Symbol 'Externer Link'](../../icons/launch-glyph.svg "Symbol 'Externer Link'")](https://docs.gradle.org/current/userguide/application_plugin.html) gepackt sind und führt diese aus.
* Das Buildpack enthält einen aktualisierten Datenkollektor für den [Service 'Monitoring and Analytics'](/docs/services/monana/index.html) und für WebSphere eXtreme Scale Client. Diese Komponenten unterstützen die neue Version der Liberty-Laufzeit.

### 30. Juni 2015: Liberty-Buildpack v1.19.1-20150622-1509 aktualisiert
* Diese Version des Buildpacks enthält eine aktualisierte IBM JRE mit einer Sicherheitskorrektur für die [LogJam-Sicherheitslücke](http://www-01.ibm.com/support/docview.wss?uid=swg21961390).
* Der [New Relic](newRelic.html)-Agent wurde auf Version 3.17 aktualisiert. Mit der neuen Version wird eine verbesserte Integration mit der Liberty-Profil-Laufzeit bereitgestellt.

### 14. Juni 2015: Liberty-Buildpack v1.19-20150608-1717 aktualisiert
* Das Buildpack enthält eine Reihe von Verbesserungen für die Anwendungsverwaltung, darunter die Unterstützung für die Entwicklungskonsole und den webbasierten Shellzugriff. Details finden Sie in der [Dokumentation zum App-Management](/docs/manageapps/app_mng.html).
* Außerdem enthält es einen Fix für das Problem, dass das Liberty-Feature für den Service [Monitoring and Analytics](/docs/services/monana/index.html) nicht gefunden werden kann.

### 27. Mai 2015: Liberty-Buildpack v1.18-20150519-1642 aktualisiert
* Das Buildpack enthält eine aktualisierte Version des Liberty-Profils, die auf der [Betaversion vom Mai](https://developer.ibm.com/wasdev/blog/2015/05/08/beta-liberty-and-tools-may-2015/) basiert.

### 5. Mai 2015: Liberty-Buildpack v1.17-20150501-1729 aktualisiert
* Das Buildpack enthält eine aktualisierte Version des Liberty-Profils, die auf der [Betaversion vom April](https://developer.ibm.com/wasdev/blog/2015/04/10/announcing-liberty-beta-with-tools-aprilmay-2015/) basiert. Mit dieser Aktualisierung sind die Liberty-Features 'jsp-2.3', 'el-3.0' und 'jdbc-4.1', die bisher als Beta-Features verfügbar waren, als einsatzbereite Features verfügbar. Des Weiteren sind zusätzliche Java EE 7-Features wie 'jsf-2.2', 'javaMail-1.5', 'webProfile-7.0' und 'javaee-7.0' nun als [Beta-Features](usingBetaFeatures.html) verfügbar.
* Das Buildpack stellt auch einen Erstsupport für Java 8 bereit. IBM JRE 7.1 bleibt die Standard-JRE, aber IBM JRE 8 kann durch Festlegen der Umgebungsvariablen JBP_CONFIG_IBMJDK für Anwendungen aktiviert werden. Das Konfigurieren einer Version von OpenJDK wird ebenfalls unterstützt. Alle Informationen finden Sie unter [JRE anpassen](customizingJRE.html).
* Mit dem Buildpack wird die neue Umgebungsvariable JBP_CONFIG_LIBERTY bereitgestellt. Mit dieser kann das Standardset der Liberty-Features überschrieben werden, die für eine Anwendung aktiviert sind, wenn eine WAR- oder EAR-Datei bereitgestellt wird. Weitere Informationen finden Sie unter [Eigenständige Anwendungen](optionsForPushing.html#stand_alone_apps).
* Das Service-Plug-in für den Service [Monitoring and Analytics](/docs/services/monana/index.html) wurde aktualisiert, um die Größe der für den Service generierten Protokolle zu reduzieren.
* Mit dieser Version des Buildpacks wurde geändert, wie die Anwendungsdateien im Droplet angelegt werden. Durch die Änderung in der Dateistruktur wird die Komplexität beim Verwalten symbolischer Links verringert. Auf die Anwendungen soll diese Änderung jedoch keine Auswirkungen haben.

### 15. April 2015: Liberty-Buildpack v1.16-20150407-1737 aktualisiert
* Diese Version des Buildpacks enthält eine aktualisierte IBM JRE 7.1-2.11 mit einer [Sicherheitskorrektur für die Bar Mitzvah-Sicherheitslücke](http://www-01.ibm.com/support/docview.wss?uid=swg21882777).
* Wenn eigenständige WAR-Dateien bereitgestellt werden, verwendet das Buildpack nun, sofern bereitgestellt, das Kontextstammelement, das in der eingebetteten Datei **ibm-web-ext.xml** als Kontextstammelement der Anwendung angegeben ist. Durch diese Änderung werden Anwendungen, die bisher unter dem Stammkontext bereitgestellt wurden, möglicherweise entsprechend den Einstellungen in der Datei **ibm-web-ext.xml** unter einem anderen Kontext bereitgestellt.

### 3. April 2015: Liberty-Buildpack v1.15-20150402-1422 aktualisiert
* Das Buildpack enthält eine aktualisierte Version des Liberty-Profils, die auf der [Betaversion vom März](https://developer.ibm.com/wasdev/blog/2015/03/13/announcing-liberty-beta-tools-march-2015/) basiert. Mit der aktualisierten Version des Liberty-Profils wird das Beta-Feature 'jsf-2.2' in Bluemix verfügbar gemacht.
* Das Buildpack enthält auch eine aktualisierte Version des Datenkollektors für den Service [Monitoring and Analytics](/docs/services/monana/index.html).

### 20. März 2015: Liberty-Buildpack v1.14-20150319-1159 aktualisiert
* Diese Version des Buildpacks enthält eine aktualisierte IBM JRE 7.1.2.11 mit einer Sicherheitskorrektur für die [FREAK-Sicherheitslücke](http://www-01.ibm.com/support/docview.wss?uid=swg21699864).
* Der Service [SQL Database](services/SQLDB/index.html#SQLDB) bietet kostenpflichtige Pläne, mit denen eine Option für das Herstellen einer Verbindung zum Datenbankserver über das SSL-Protokoll bereitgestellt wird. Der Support für die automatische Konfiguration des Buildpacks für den Service SQL Database wurde aktualisiert und die Laufzeit ist nun so konfiguriert, dass über SSL eine Verbindung zur Datenbank hergestellt werden kann, wenn die SSL-Verbindungsinformationen verfügbar sind.
* Das Buildpack wurde aktualisiert und meldet nun einen Fehler, wenn eine eigenständige WAR- oder EAR-Datei bereitgestellt wird, die im Stammverzeichnis des Anwendungsarchivs die Konfigurationsdatei **server.xml ** enthält.
* Das Buildpack enthält eine Korrektur für das Plug-in für den Service für die automatische Konfiguration von MongoDB, mit dem in bestimmten Fällen eine ungültige Konfiguration in der Datei **server.xml** generiert wurde.

### 10. Februar 2015: Liberty-Buildpack v1.13-20150209-1122 aktualisiert
* Das Buildpack enthält Sicherheitskorrekturen für die [Sicherheitslücken in Apache HttpComponents und im Java-Überschreibungs-Feature](https://www-304.ibm.com/connections/blogs/PSIRT/entry/ibm_security_bulletin_multiple_vulnerabilities_fixed_in_liberty_for_java_for_ibm_bluemix_cve_2012_6153_cve_2014_3577_cve_2015_0178?lang=en_us).
* Das Buildpack enthält eine aktualisierte Version des Liberty-Profils, die auf der [Betaversion vom Februar](https://developer.ibm.com/wasdev/blog/2015/02/13/announcing-liberty-beta-tools-february-2015/) basiert. Mit der aktualisierten Version des Liberty-Profils wird eine aktualisierte Version des GA-Features 'websocket-1.1' von WebSocket bereitgestellt. Mit ihr werden auch die folgenden Java EE 7-Beta-Features in Bluemix verfügbar gemacht:
  * cdi-1.2, el-3.0, jsp-2.3,  jca-1.7, jacc-1.5 und jaspic-1.1
* Das Buildpack bietet die Integration des [JRebel-Tools von ZeroTrunaround ![Symbol 'Externer Link'](../../icons/launch-glyph.svg "Symbol 'Externer Link'")](http://zeroturnaround.com/software/jrebel/). Durch die Integration wird es einfacher, JRebel mit Bluemix-Anwendungen zu verwenden und sofortige Anwendungsaktualisierungen durchzuführen, ohne die Anwendung erneut bereitstellen oder ein erneutes Staging durchführen zu müssen. Es werden nur eigenständige Webanwendungen unterstützt.

### 6. Februar 2015: Liberty-Buildpack v1.12-20150130-1016 aktualisiert
* Das Buildpack enthält eine aktualisierte Version des Liberty-Profils, die auf der [Betaversion vom Januar](https://developer.ibm.com/wasdev/blog/2015/01/16/announcing-liberty-beta-tools-january-2015/) basiert.
* Das Buildpack enthält eine reduzierte Version des Datenkollektors für den [Service 'Monitoring and Analytics'](/docs/services/monana/index.html#gettingstartedtemplate).

### 23. Januar 2015: Liberty-Buildpack v1.11-20150119-1511 aktualisiert
* Das Buildpack enthält die aktualisierte IBM JRE Version 7.1 SR2 FP1.
* Es enthält auch die aktualisierte Version von WebSphere eXterme Scale Client (Version 8.6.0.6) und einen aktualisierten Agenten für den Service für das Auto-Scaling.
* Die Unterstützung für den Service [New Relic](newRelic.html) wurde erweitert, sodass nun auch benutzerdefinierte Services unterstützt werden.
* Das Buildpack wurde verbessert, sodass nun Berichte zu detaillierten Versionen des Liberty-Profils und der IBM JRE erstellt werden.

### 19. Dezember 2014: Liberty-Buildpack v1.10-20141218-0103 aktualisiert
* Das Buildpack stellt einen Entwicklungsmodus für Anwendungen bereit. Der Entwicklungsmodus ist ein spezieller Modus, der es Entwicklern ermöglicht, zahlreiche Aktivitäten für eine Anwendungsinstanz auszuführen, die zuvor nicht möglich waren. Dank dieses Features kann diese Version von IBM Eclipse Tools for Bluemix nun das ferne Debugging mit inkrementellen Dateiaktualisierungen für Liberty-Anwendungen unterstützen, die in Bluemix ausgeführt werden. Dies macht es für Entwickler, die Eclipse verwenden, leichter, eine Anwendung in der Cloud zu debuggen und sofort an dieser Anwendung Änderungen vorzunehmen.
* Das Buildpack enthält außerdem eine aktualisierte Version des Liberty-Profils, die auf der [Betaversion vom Dezember](https://developer.ibm.com/wasdev/blog/2014/12/10/announcing-liberty-beta-december/) basiert.
* Darüber hinaus sind die folgenden vier Liberty-Features, die zuvor in einer Betaversion verfügbar waren, nun als produktionsreife Features verfügbar:
  * concurrent-1.0
  * jsonp-1.0
  * servlet-3.1
  * websocket-1.0.
* Das Buildpack ermöglicht die Integration mit dem New Relic-Service. Sobald eine Anwendung an den New Relic-Service gebunden ist, lädt das Buildpack automatisch die Laufzeitkomponente mit dem New Relic-Agenten herunter und konfiguriert sie.
* Für das Buildpack gelten die folgenden bekannten Einschränkungen:
  * Im Entwicklungsmodus kann kein SessionCache-Service gebunden werden.
  * Im Entwicklungsmodus kann kein Threadspeicherauszug erstellt werden.
  * Bei Verwendung des Features 'servlet-3.1' oder 'websocket-v1.0' kann der Service 'Monitoring & Analytics' nicht gebunden werden.

### 5. Dezember 2014: Liberty-Buildpack v1.9-20141202-0947 aktualisiert
* Das Buildpack bietet erweiterte Unterstützung für JVM-Optionen. Die JVM-Optionen können nun über eine Neustartoperation angewendet werden. Ein erneutes Staging der Anwendung ist nicht erforderlich. Außerdem wurden die JVM-Standardoptionen für die schnelle Fehlerdiagnose optimiert und mit einer allgemeinen Position vorkonfiguriert, die das Auffinden der generierten Speicherauszüge vereinfacht. Weitere Details finden Sie im [Artikel 'Custom Configuration of Java JVM for the Liberty Runtime'](https://developer.ibm.com/bluemix/2014/12/12/custom-configurations-java-jvm-liberty-runtime/).
* Das Buildpack enthält die aktualisierte Version 4.17.29 des DB2-JDBC-Treibers.
* Außerdem enthält es einen Fix für das Problem, das die Erfassung der Informationen zur Belegung des Liberty-Thread-Pools für den Service 'Monitoring & Analytics' verhinderte.

### 21. November 2014: Liberty-Buildpack v1.8-20141118-1610 aktualisiert
* Das Buildpack enthält die aktualisierte IBM JRE Version 7.1 SR2, die einen Fix für die [POODLE-Sicherheitslücke](http://www-01.ibm.com/support/docview.wss?uid=swg21687173) bereitstellt.
* Es enthält außerdem eine aktualisierte Version des Liberty-Profils, die auf der [Betaversion vom November](https://developer.ibm.com/wasdev/blog/2014/11/07/announcing-liberty-profile-beta-november/) basiert.

### 30. Oktober 2014: Liberty-Buildpack v1.7-20141020-1759 aktualisiert
* Das Buildpack enthält die aktualisierte IBM JRE Version 7.1 SR1 FP3.
* Außerdem enthält es einen Fix für ein Problem, das die Implementierung von Anwendungen mit Serverkonfigurationen verhinderte, die Unicode-Zeichen enthalten.

### 23. Oktober 2014: Liberty-Buildpack v1.6-20141013-1628 aktualisiert
* Das Buildpack enthält nun einen neuen Datenkollektor für den Service [Monitoring and Analytics](/docs/services/monana/index.html). Der neue Datenkollektor erfasst tief greifende Diagnoseinformationen und ermöglicht den Benutzern des Service-Diagnoseplans das Diagnostizieren von Anwendungsproblemen bis in die einzelnen Codezeilen.
* Das Buildpack enthält aktualisierte Versionen der Managementagenten und der Agenten für automatische Skalierung, die Fehlerkorrekturen und kleine Verbesserungen einschließen. Es enthält ferner eine aktualisierte Version des [Liberty-Profils](https://developer.ibm.com/wasdev/) und der [Java MongoDB-Treiber ![Symbol 'Externer Link'](../../icons/launch-glyph.svg "Symbol 'Externer Link'")](https://docs.mongodb.org/ecosystem/drivers/java/), Version 2.12.3.
* Im Feature 'cloudAutowiring' wurde ein Fehler behoben, der bei einigen Anwendungen zu Ressourceninjektionsfehlern geführt hat.

### 3. Oktober 2014: Liberty-Buildpack v1.5-20140923-1143 aktualisiert
* In diesem aktualisierten Buildpack können Anwendung nun auf die Liberty-Beta-Features zugreifen, einschließlich WebSocket 1.0, Servlet 3.1 und JAX-RS 2.0. Weitere Informationen finden Sie in [Beta-Features verwenden](usingBetaFeatures.html).

### 30. September 2014: Liberty-Buildpack v1.4-20140908-1803 aktualisiert
* Das Buildpack bietet nun Unterstützung für ElephantSQL- und ClearDB MySQL Database-Services anderer Anbieter. Die automatische Konfiguration wird auch für experimentelle postgresql- und mysql-Services unterstützt. Mit nun insgesamt 13 Services sorgt die Unterstützung für automatische Konfiguration im Liberty-Buildpack für eine schnellere und einfachere Verarbeitung von Bluemix-Services in Liberty-Anwendungen.
* Während des Stagings von Anwendungen zeigt das Buildpack verbesserte Protokollnachrichten zur automatischen Konfiguration und zu weiteren Aktionen an.
* Das Buildpack enthält eine aktualisierte Version des Liberty-Profils mit Fixes und Verbesserungen.
* Ferner enthält es eine aktualisierte Version von IBM JRE Version 7.1, die Leistungsverbesserungen aufweist. Auf der Seite [Neuerungen](http://www-01.ibm.com/support/knowledgecenter/SSYKE2_7.0.0/com.ibm.java.lnx.71.doc/diag/preface/changes_71/changes.html) finden Sie eine detaillierte Auflistung der Änderungen.

### 28. August 2014: Liberty-Buildpack v1.3-20140818-1538 aktualisiert
* Das Buildpack enthält eine aktualisierte Version des [Liberty-Profils](https://developer.ibm.com/wasdev/) mit den neuesten Korrekturen und Verbesserungen.
* In dieser Version des Buildpacks wurde die Unterstützung für die Umgebungsvariable JAVA_OPTS bezüglich der Übergabe zusätzlicher JVM-Optionen an die Anwendungslaufzeit korrigiert.
* Ferner wurde ein Problem behoben, das die Implementierung von eigenständigen Spring-basierten JAR-Anwendungen verhindert hat.
* Es ist nun möglich, IBM JVM-Snap-Traces über die Bluemix-Benutzerschnittstelle zu generieren und herunterzuladen. Weitere Informationen zu Snap-Traces und anderen von der JVM generierten Diagnoseinformationen finden Sie im [Abschnitt 'Fehlerbehebung'](http://www-01.ibm.com/support/knowledgecenter/SSYKE2_7.0.0/com.ibm.java.lnx.70.doc/troubleshooting.html) in der IBM JVM-Dokumentation.

### 29. Juli 2014: Liberty-Buildpack v1.1-20140725-1341 aktualisiert
* Die neue Version der Bluemix Edition von Liberty ist da!
  * In dieser Liberty-Version werden Fixes sowie neue Features bereitgestellt, die Ihnen eine effizientere Verarbeitung von Bluemix-Services ermöglichen.
  * Mit dem neuen Feature 'CouchDB' kann der Cloudant®-Service nun eine automatische Konfiguration der Liberty-Anwendung vornehmen, sodass Ihnen nun ein Connectorobjekt zur Verfügung steht. Das Parsing durch VCAP_SERVICES und die Angabe der Ektorp-Client-JAR-Dateien ist nicht mehr erforderlich.
* Die neue Version von IBM SDK for Java ist da!
  * Wenn Sie nun eine weitere Push-Operation für Ihre Anwendungen durchführen, wird IBM SDK for Java Version 7.1-1.0 verwendet. Dies führt zu einer deutlichen Leistungsverbesserung. Der Durchsatz Ihrer Anwendung wird sich erhöhen und die Speicherbelegung wird reduziert. Weitere Informationen zu IBM Java SDK finden Sie [hier](http://www-01.ibm.com/support/docview.wss?uid=swg21671466).

# Zugehörige Links
{: #rellinks notoc}
## Allgemein
{: #general notoc}
  * [Liberty-Laufzeit](index.html)
  * [Übersicht über das Liberty-Profil](http://www-01.ibm.com/support/knowledgecenter/SSAW57_8.5.5/com.ibm.websphere.wlp.nd.doc/ae/cwlp_about.html)
