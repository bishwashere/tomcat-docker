# Install Tomcat & openjdk 8 (has java and javac)
FROM tomcat:jdk8-openjdk

# Copy source files to tomcat folder structure
COPY . /usr/local/tomcat/webapps/

# -cp, Adding compile time classpath as Tomcat's /lib/servlet-api.jar file.
# - d, destination output location.
RUN ["javac", "-cp", ".:/usr/local/tomcat/lib/servlet-api.jar", "-d", "/usr/local/tomcat/webapps/myApp/WEB-INF/classes/", "/usr/local/tomcat/webapps/myApp/src/TestingServlet.java"]

# Serve Tomcat
EXPOSE 8080
CMD ["catalina.sh", "run"]
