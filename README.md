# Configurations & Tools

# ---------Installing Jenkins---------
<p align="left">sudo apt update -y</p>
<p align="left">curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null</p>
<p align="left">echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null</p>
<p align="left">sudo apt-get update -y</p>
<p align="left">sudo apt-get install jenkins -y</p>
<p align="left">sudo systemctl enable jenkins</p>
<p align="left">sudo systemctl start jenkins</p>
<p align="left">sudo systemctl status jenkins</p>


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

# ---------Installing Trivy---------
<p align="left">sudo apt-get install wget apt-transport-https gnupg lsb-release</p>
<p align="left">wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | gpg --dearmor | sudo tee /usr/share/keyrings/trivy.gpg > /dev/null
</p>
<p align="left">echo "deb [signed-by=/usr/share/keyrings/trivy.gpg] https://aquasecurity.github.io/trivy-repo/deb $(lsb_release -sc) main" | sudo tee -a /etc/apt/sources.list.d/trivy.list</p>
<p align="left">sudo apt-get update</p>
<p align="left">sudo apt-get install trivy</p>
<p align="left"></p>
<p align="left"></p>
