FROM pegasystems/pega-ready
EXPOSE 8080
COPY --chown=pegauser:root  /prweb ${CATALINA_HOME}/webapps/prweb
RUN chmod -R g+rw   ${CATALINA_HOME}/webapps/prweb
COPY --chown=pegauser:root postgresql-42.3.6.jar ${CATALINA_HOME}/lib/
ENV JDBC_URL jdbc:postgresql://172.17.0.2:5432/postgres
ENV JDBC_CLASS org.postgresql.Driver
ENV DB_USERNAME postgres
ENV DB_PASSWORD postgres
