From jenkins/jenkins:latest 
workdir /app 
#install nodejs npm 
User root 
Run mkdir -p /var/lib/apt/lists/partial
RUN curl -sL https://deb.nodesource.com/setup_6.x | bash -
Run apt-get -y install nodejs 
#download plugins 
Copy plugins.txt /usr/share/jenkins/plugins.txt
Run  /usr/local/bin/install-plugins.sh < /usr/share/jenkins/plugins.txt
#Run /usr/local/bin/install-plugins.sh build-timeout
#port 
Expose 8080
Expose 50000
#CMD []

