WebServiceFrameWork
WebServiceFrameWork is used to free the team member from writing the code of servlet for every request.This framework only works on server which are based on j2EE specifications.
Instructions for using the framework:
1.	Download tmService.jar add it in lib folder of your webApplication.
2.	Download any latest version of gson and put it in your webapplication lib folder
3.	After adding jar file to your lib folder you need to add following xml part to your web.xml
<servlet>
<servlet-name>TMServiceLoader</servlet-name>
<servlet-class>com.thinking.machines.servlets.TMServiceLoader</servlet-class>
<load-on-startup>0</load-on-startup>
</servlet>
<servlet>
<servlet-name>TMService</servlet-name>
<servlet-class>com.thinking.machines.TMService</servlet-class>
</servlet>
<servlet-mapping>
<servlet-name>TMService</servlet-name>
<url-pattern>/service/*</url-pattern>
</servlet-mapping>
To Compile The framework :
     For Windows:
Javac  -classpath path_to_your_webserver_base_folder/webapps/name_of_unzipped_folder/WEB_INF/classes; path_to_your_webserver_base_folder/webapps/name_of_unzipped_folder/WEB_INF/lib/*;. Your_file_name.java
     For Linux:
Javac  -classpath path_to_your_webserver_base_folder/webapps/name_of_unzipped_folder/WEB_INF/classes: path_to_your_webserver_base_folder/webapps/name_of_unzipped_folder/WEB_INF/lib/*:. Your_file_name.java
To Test Your Service:
You need to write following URL in your browser(chrome,firefox)
http://server_ip(for local computer you need to write localhost):serverPort(By default 8080)/webapp_name/service/path_on_class/path_on_method
Some Rules You Need To Follow For Dealing With This Framework :
1.	For sending any data from client to server you always need to use json.
2.	Do Not make any changes to following folder:
WEB_INF/classes/com/thinking/machines/servlets,
WEB-INF/classes/com/thinking/machines/annotations,
WEB-INF/classes/com/thinking/machines/interfaces.
  


