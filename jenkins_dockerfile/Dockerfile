# Author Patrick Steger

# Use Jenkins Alpine because its smaller
FROM jenkins:alpine

# Disable Setup Wizard
ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"

# Create Admin User (disabled because Security is disabled)
# COPY security.groovy /usr/share/jenkins/ref/init.groovy.d/security.groovy

# Copy Plugin List and Install Plugins from List
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt

# Copy config (mainly to disable Jenkins Security)
COPY config.xml /usr/share/jenkins/ref/config.xml.override
COPY config.xml /var/jenkins_home/config.xml
