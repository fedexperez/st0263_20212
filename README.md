## Instalar docker en linux-ami2

    sudo amazon-linux-extras install docker -y
    sudo yum install git -y

    sudo systemctl enable docker
    sudo systemctl start docker
    sudo usermod -a -G docker ec2-user

## instalar docker-compose: https://docs.docker.com/compose/install/

    sudo curl -L https://github.com/docker/compose/releases/download/1.29.2/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
 
    sudo chmod +x /usr/local/bin/docker-compose

    exit

## Instalar docker en Ubuntu:

    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu$(lsb_release -cs) stable"
    sudo apt-get update
    sudo apt-get install docker-ce

## Instalar docker en Centos 7

    source: https://docs.docker.com/install/linux/docker-ce/centos/

    sudo yum install -y epel-release yum-utils vim
    sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
    sudo yum install docker-ce -y
    sudo systemctl start docker
    sudo systemctl enable docker
    sudo usermod -aG docker userdca



