# Set the base image using a variable with a default value
ARG STACK_VERSION=8.1.2  # Default to version 8.1.2, change as necessary
FROM docker.elastic.co/logstash/logstash:${STACK_VERSION}

# Install necessary dependencies
USER root
RUN apt-get update && apt-get install -y shared-mime-info

# Switch back to the logstash user
USER logstash

# Install the Google Cloud Storage plugin
RUN logstash-plugin install logstash-input-google_cloud_storage
