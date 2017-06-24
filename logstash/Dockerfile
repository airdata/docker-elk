# https://github.com/elastic/logstash-docker
FROM docker.elastic.co/logstash/logstash:5.4.2
ADD patterns /etc/logstash/patterns
ADD regex /etc/logstash/regex
COPY ./logstash-forwarder.crt /etc/logstash/logstash-forwarder.crt
COPY ./logstash-forwarder.key /etc/logstash/logstash-forwarder.key
RUN logstash-plugin install logstash-filter-multiline
# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json
