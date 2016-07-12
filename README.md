# Shopping cart App
-------------------

- Shopping cart
- Catalogue
- Search
- Checkout
- Administration

To run the application:
-------------------	
From the command line with Maven installed:

	$ cd shopizer
	$ mvn clean install
	


copy sm-shop/target/sm-shop.war to tomcat or any other application server deployment dir

Increase heap space to 1024 m or at least 512 m

### Heap space configuration in Tomcat:


If you are using Tomcat, edit catalina.bat for windows users or catalina.sh for linux / Mac users

	in Windows
	set JAVA_OPTS="-Xms1024m -Xmx1024m -XX:MaxPermSize=256m" 
	
	in Linux / Mac
	export JAVA_OPTS="-Xms1024m -Xmx1024m -XX:MaxPermSize=256m" 


### Access the application:


Access the deployed web application at: http://localhost:8080/sm-shop/shop

Acces the admin section at: http://localhost:8080/sm-shop/admin

#####username : admin
#####password : password

The instructions above will let you run the application with default settings and configurations.
Please read the instructions on how to connect to MySQL, configure an email server and configure other subsystems

# Eclipse Setup

Version 2.0.1 is different from previous versions as it uses maven modules instead of having to take care of building each of the modules.

This section explains how to install and configure Eclipse IDE to run the Shopizer web application. Make sure you meet **[Software requirements][setup]**

- Download “*Eclipse IDE for Java EE Developers*” (We have tested the installation with Eclipse Juno and Luna distributions so far) <br/><br/>
Configure Eclipse IDE to run with Apache Maven ** Some distributions might already have the appropriate Maven plug-in installed**<br/><br/>
- Download and install Maven plug-in
- Choose Help > Eclipse Marketplace…
- Search “Maven” in “Find” box.
- Find “Maven Integration for Eclipse WTP”.
<br/>
<br/>
You should increase Eclipse memory if your ntention is to build the project and run it from inside Eclipse
<br/>
<br/>
- Open eclipse.ini
- Edit the memory settings in order to support 1024m [-Xms512m -Xmx1024m]
<br/>
<br/>


Import shopizer project as a maven module project

For this, from eclipse Import – Maven – Existing maven project

Select shopizer and click OK

```xml

Build the project

Right-click shopizer > Run As > Maven clean
Right-click shopizer > Run As > Maven generate-sources
Right-click shopizer > Run As > Maven install

```


