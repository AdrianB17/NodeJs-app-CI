# Configurations & Tools

# ---------Installing Jenkins---------
<p align="left">sudo wget https://updates.jenkins.io/download/war/2.387.3/jenkins.war</p>
<p align="left">sudo apt update -y</p>
<p align="left">sudo apt install openjdk-11-jre -y</p>
<p align="left">java -jar jenkins.war  --httpPort=8082</p>

# ---------Installing Docker---------
<p align="left">sudo apt-get update</p>
<p align="left">sudo apt-get install ca-certificates curl gnupg</p>
<p align="left">sudo install -m 0755 -d /etc/apt/keyrings</p>
<p align="left">curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg</p>
<p align="left">sudo chmod a+r /etc/apt/keyrings/docker.gpg</p>
<p align="left">echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
</p>
<p align="left">sudo apt-get update</p>
<p align="left">sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin</p>
<p align="left">sudo apt install docker-compose</p>
<p align="left">service docker restart</p>
<p align="left">sudo usermod -aG docker $USER</p>
<p align="left">newgrp docker</p>
<p align="left">sudo chmod 666 /var/run/docker.sock</p>
<p align="left">sudo systemctl restart docker</p>

# ---------Installing SonarQube---------
<p align="left">docker run -d --name sonar -p 9000:9000 sonarqube:lts-community</p>

<p align="left"></p>
<p align="left"></p>
<p align="left"></p>
<p align="left"></p>
<p align="left"></p>
<p align="left"></p>
<p align="left"></p>
