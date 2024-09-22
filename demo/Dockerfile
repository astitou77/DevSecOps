# Use the official Jenkins image as the base
FROM docker.io/jenkins/jenkins:lts

# Switch to root user to install Maven
USER root

# Install Maven
RUN apt-get update && \
    apt-get install -y maven && \
    apt-get clean

# Switch back to the Jenkins user
USER jenkins

