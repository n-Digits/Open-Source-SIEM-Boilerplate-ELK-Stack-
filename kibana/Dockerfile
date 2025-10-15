FROM docker.elastic.co/kibana/kibana:8.15.0

# Disable security for dev use
ENV ELASTICSEARCH_HOSTS=http://elasticsearch:9200
ENV SERVER_HOST=0.0.0.0
ENV XPACK_SECURITY_ENABLED=false

EXPOSE 5601
