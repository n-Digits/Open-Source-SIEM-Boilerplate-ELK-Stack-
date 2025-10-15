FROM docker.elastic.co/logstash/logstash:8.15.0

# Remove x-pack content (optional, not required but keeps it lean)
RUN rm -rf /usr/share/logstash/x-pack

COPY logstash.conf /usr/share/logstash/pipeline/logstash.conf
COPY config/logstash.yml /usr/share/logstash/config/logstash.yml

EXPOSE 5044 5000 9600
