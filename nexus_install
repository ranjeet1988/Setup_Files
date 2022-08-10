apt update

apt install openjdk-8-jdk

useradd -M -d /opt/nexus -s /bin/bash -r nexus

echo "nexus   ALL=(ALL)       NOPASSWD: ALL" > /etc/sudoers.d/nexus

wget https://sonatype-download.global.ssl.fastly.net/repository/downloads-prod-group/3/nexus-3.29.2-02-unix.tar.gz

mkdir /opt/nexus

tar xzf nexus-3.29.2-02-unix.tar.gz -C /opt/nexus --strip-components=1

11  ls /opt/nexus/

chown -R nexus: /opt/nexus

vi /opt/nexus/bin/nexus.rc
 run_as_user="nexus"
 
vi /opt/nexus/bin/nexus.vmoptions
 change ../sonatype-work to ./sonatype-work

sudo -u nexus /opt/nexus/bin/nexus start


cat /opt/nexus/sonatype-work/nexus3/admin.password
