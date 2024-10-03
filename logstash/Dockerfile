## Dockerfile
# Use the official Logstash image as the base
FROM docker.elastic.co/logstash/logstash:7.2.0

# Set environment variable for Java options
ENV LS_JAVA_OPTS="-Xms512m -Xmx512m"

# Copy the JDBC driver into the correct directory
COPY mssql-jdbc-8.4.1.jre8.jar /usr/share/logstash/logstash-core/lib/jars/

# Specify the default command to run Logstash
CMD ["-f", "/usr/share/logstash/pipeline/logstash.conf"]