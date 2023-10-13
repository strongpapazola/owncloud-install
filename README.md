# Cara Install Owncloud
<pre>
apt update && apt install docker.io -y
VERSION=$(curl --silent https://api.github.com/repos/docker/compose/releases/latest | grep -Po '"tag_name": "\K.*\d')
DESTINATION=/usr/bin/docker-compose
curl -L https://github.com/docker/compose/releases/download/${VERSION}/docker-compose-$(uname -s)-$(uname -m) -o $DESTINATION
chmod 755 $DESTINATION
mkdir bintang
cd bintang/
nano .env
nano docker-compose.yml
docker-compose up -d
docker ps
</pre>
