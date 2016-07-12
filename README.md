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

