iDempiere Atlantic Theme
========

iDempiere theme based on ZK atlantic theme 

How to install:

1. Download theme fragment from [releases](https://github.com/anozimada/idempiere-atlantic-theme/releases)
2. Install the fragment jar [using Apache Felix Web Console](http://wiki.idempiere.org/en/Developing_Plug-Ins_-_Get_your_Plug-In_running#Apache_Felix_Web_Console)
3. Login to iDempiere System and open System Configurator:
  * Set **ZK_THEME_USE_FONT_ICON_FOR_IMAGE** value from **N** to **Y**
  * Set **ZK_THEME** value from **default** to **atlantic**
4. Edit **idempiere-server.sh** and add **-Dorg.zkoss.zk.config.path=/WEB-INF/zk-atlantic.xml** to **VMOPTS** so it will looks similar to following
```
VMOPTS="-Dorg.osgi.framework.bootdelegation=sun.security.ssl,org.w3c.dom.events
-Dosgi.compatibility.bootdelegation=true
-Djetty.home=$BASE/jettyhome
-Djetty.base=$BASE/jettyhome
-Djetty.etc.config.urls=etc/jetty.xml,etc/jetty-deployer.xml,etc/jetty-ssl.xml,etc/jetty-ssl-context.xml,etc/jetty-http.xml,etc/jetty-alpn.xml,etc/jetty-http2.xml,etc/jetty-https.xml
-Dosgi.console=localhost:12612
-Dmail.mime.encodefilename=true
-Dmail.mime.decodefilename=true
-Dmail.mime.encodeparameters=true
-Dmail.mime.decodeparameters=true
-Dorg.zkoss.zk.config.path=/WEB-INF/zk-atlantic.xml"
```
