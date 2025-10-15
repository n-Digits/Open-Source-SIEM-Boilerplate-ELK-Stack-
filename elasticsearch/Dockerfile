FROM docker.elastic.co/elasticsearch/elasticsearch:8.15.0

# Elasticsearch runs as open-source; no need to disable built-in x-pack manually
# Just ensure security and SSL are off for simplicity (dev mode)
ENV xpack.security.enabled=false
ENV discovery.type=single-node

EXPOSE 9200

