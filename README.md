# Fuse 7 - Karaf, Camel and ActiveMQ QuickStart

Quick example using Fuse7 anbd Karaf for amq6 connectivity goodness.

```text
[user@localhost assembly]$ ./bin/karaf 
Unable to register security provider: java.lang.ClassNotFoundException: org.bouncycastle.jce.provider.BouncyCastleProvider
        __ __                  ____      
       / //_/____ __________ _/ __/      
      / ,<  / __ `/ ___/ __ `/ /_        
     / /| |/ /_/ / /  / /_/ / __/        
    /_/ |_|\__,_/_/   \__,_/_/         

  Apache Karaf (4.2.0.fuse-720061-redhat-00001)

Hit '<tab>' for a list of available commands
and '[cmd] --help' for help on a specific command.
Hit '<ctrl-d>' or type 'system:shutdown' or 'logout' to shutdown Karaf.


karaf@root()> bundle:list
START LEVEL 100 , List Threshold: 50
 ID │ State  │ Lvl │ Version                         │ Name
────┼────────┼─────┼─────────────────────────────────┼────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
121 │ Active │  50 │ 2.21.0.fuse-720050-redhat-00001 │ camel-blueprint
122 │ Active │  50 │ 2.21.0.fuse-720050-redhat-00001 │ camel-core
123 │ Active │  50 │ 2.21.0.fuse-720050-redhat-00001 │ camel-jms
124 │ Active │  60 │ 3.0.11.fuse-720027-redhat-00001 │ Fabric8 :: Karaf :: Core
125 │ Active │  65 │ 3.0.11.fuse-720027-redhat-00001 │ Fabric8 :: Karaf :: Blueprint
126 │ Active │  65 │ 3.0.11.fuse-720027-redhat-00001 │ Fabric8 :: Karaf :: Checks
127 │ Active │  80 │ 1.0.0.SNAPSHOT                  │ Fabric8 :: Quickstarts :: Karaf 2 :: Camel and ActiveMQ
karaf@root()> osgi:headers 127

Fabric8 :: Quickstarts :: Karaf 2 :: Camel and ActiveMQ (127)
-------------------------------------------------------------
Bnd-LastModified = 1551686180979
Build-Jdk = 1.8.0_201
Built-By = user
Created-By = Apache Maven Bundle Plugin
Manifest-Version = 1.0
Tool = Bnd-1.50.0

Bundle-Description = Karaf 2 example running a Camel route connecting to ActiveMQ
Bundle-ManifestVersion = 2
Bundle-Name = Fabric8 :: Quickstarts :: Karaf 2 :: Camel and ActiveMQ
Bundle-SymbolicName = com.nullendpoint.fuse7-karaf-amq6-example
Bundle-Version = 1.0.0.SNAPSHOT

Export-Package = 
	com.nullendpoint;uses:="org.apache.camel,org.apache.camel.spi";version=1.0.0.SNAPSHOT
Import-Package = 
	org.apache.activemq.camel.component,
	org.apache.camel;version="[2.21,3)",
	org.apache.camel.spi;version="[2.21,3)",
	org.osgi.service.blueprint;version="[1.0.0,2.0.0)"


``` 

