FROM rabbitmq:3.8.0

WORKDIR / 

RUN rabbitmq-plugins enable rabbitmq_management && apt-get update && apt-get install -y curl

COPY rabbitmq.config /etc/rabbitmq/
COPY definitions.json /etc/rabbitmq/

EXPOSE 15672
EXPOSE 5672


CMD ["rabbitmq-server"]