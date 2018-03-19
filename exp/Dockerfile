From jenkins
workdir /app 
#ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"
#install nodejs npm 
User root 
Run mkdir -p /var/lib/apt/lists/partial
RUN curl -sL https://deb.nodesource.com/setup_6.x | bash -
Run apt-get -y install nodejs 
#volume 
Volume /var/jenkins_home
#download plugins 
#Copy plugins.txt /usr/share/jenkins/ref/plugins.txt 
User root
Run  /usr/local/bin/install-plugins.sh < /usr/share/jenkins/plugins.txt
#Run ["apt-get", "update"]
#Run ["apt-get", "install", "-y", "vim"]
User jenkins
# port 
Expose 8080
Expose 50000
#CMD []

