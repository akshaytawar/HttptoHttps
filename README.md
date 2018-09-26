# HttptoHttps
covert http to https in Apache Tomcat

Case 1) :

1) Java provides dummy SSL certificate generation facility.
     Path: jdk/bin/keytool.exe

2) Command to generate dummy SSL certificate 
Command : keytool -genkeypair -alias akshaycert(shortNameForCertificate) -keyalg RSA -ketstore "C://akshay.cert"(the location where certificate should be generated)

3) Add KeystoreFile path and keystorepass to Server.xml File
<Connector port="8443" protocol="org.apache.coyote.http11.Http11Protocol"
               maxThreads="150" SSLEnabled="true" scheme="https" secure="true"
               clientAuth="false" sslProtocol="TLS" 
	       keystoreFile="C:\.......\akshay.cert" keystorePass="pass"/>
                 
  Case 2) :
  
  4) when we type http://www.google.com then it will redirect automatically to https://www.goole.com. To do so we to add security-constratint element to web.xml.
  
	       
	      
	
