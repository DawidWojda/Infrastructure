FROM jenkins/ssh-agent:4.2.1-jdk11

RUN apt update && \
    apt install -y curl python3-pip unzip ansible git

RUN curl -fsSL https://get.docker.com/ | sh

RUN usermod -aG docker jenkins

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && unzip awscliv2.zip && ./aws/install

RUN curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose && chmod +x /usr/local/bin/docker-compose

RUN newgrp docker