FROM jenkins/jenkins:lts-centos
USER jenkins
ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"
ENV JENKINS_USER admin
ENV JENKINS_PASS admin
COPY ./credentials.xml /var/jenkins_home
COPY ./plugins.txt /usr/share/jenkins/ref/
COPY ./default-user.groovy /usr/share/jenkins/ref/init.groovy.d/
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt