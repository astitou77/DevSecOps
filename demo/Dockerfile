# Use the official Jenkins image as the base
FROM docker.io/jenkins/jenkins:lts

# Switch to root user to install Maven
USER root

# Install Maven & Curl & cleanup
RUN apt-get update && \
    apt-get install -y maven && \
    apt-get clean && \
    apt-get install -y curl && \
    rm -rf /var/lib/apt/lists/*

# Install JFrog CLI
RUN curl -fL https://getcli.jfrog.io | sh && \
    mv jfrog /usr/local/bin/ && \
    chmod +x /usr/local/bin/jfrog

# Switch back to the Jenkins user
USER jenkins

