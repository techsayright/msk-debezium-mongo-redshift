FROM confluentinc/cp-kafka-connect-base

RUN confluent-hub install --no-prompt confluentinc/kafka-connect-aws-redshift:latest\
    && confluent-hub install --no-prompt debezium/debezium-connector-mongodb:latest

ADD connectors /etc/kafka-connect/connectors

WORKDIR /etc/kafka-connect/connectors

CMD ["./register_connectors.sh"]