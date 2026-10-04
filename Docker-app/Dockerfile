FROM tomcat:9-jdk17-temurin

# Remove default apps
RUN rm -rf /usr/local/tomcat/webapps/*

# Copy WAR
COPY target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

# Optional: non-root user (tomcat image already has 'tomcat' user)
RUN mkdir -p /usr/local/tomcat/webapps && chown -R tomcat:tomcat /usr/local/tomcat/webapps

EXPOSE 8080

CMD ["catalina.sh", "run"]
