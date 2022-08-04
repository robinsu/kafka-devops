FROM confluentinc/cp-kafka-connect:7.0.1

RUN confluent-hub install --no-prompt confluentinc/kafka-connect-jdbc:latest

ENV CONNECT_PLUGIN_PATH="/usr/share/java,/usr/share/confluent-hub-components"

ARG JDBC_JAR_LOCATION="/usr/share/confluent-hub-components/confluentinc-kafka-connect-jdbc/lib"

ARG MYSQL_CONNECTOR_VERSION="8.0.26"
RUN curl -k -SL "https://repo1.maven.org/maven2/mysql/mysql-connector-java/${MYSQL_CONNECTOR_VERSION}/mysql-connector-java-${MYSQL_CONNECTOR_VERSION}.jar" \
    -o "${JDBC_JAR_LOCATION}/mysql-connector-java-${MYSQL_CONNECTOR_VERSION}.jar"

