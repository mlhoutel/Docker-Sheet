# DOCKER SHEET
## Docker Setup
[Docker Hub](https://hub.docker.com/)

[Docker Website](https://www.docker.com//)



## Connect to the VM
```
user: docker
pwd: tcuser
```

Get the VM ip with 
```
ifconfig eth1
```

Set the azert keyboard
```
su docker
tce-load -wi kmaps
sudo loadkmap < /usr/share/kmap/azerty/fr-latin9.kmap
```

### Use Putty
```
Session\Window\Selection\Action = Compromise
paste : ctrl + shift + V
```
### Use SSH
```
ssh docker@192.168.99.103
```
## Tutorial
```
install nginx server: docker run -d -p 8080:80 nginx
open webpage: http://192.168.99.103:8080/
```

### Get container id
in Linux: 
```
sudo docker ps -aqf "name=containername"
```
in Windows: 
```
docker ps -aqf "name=containername"
```

### Operational bash cmd: 
```
docker exec -ti 2769d51daeb2 bash
```

### Edit nginx webpage:
```
cd /usr/share/nginx/html
```

Get Nano:
```
apt-get update
apt-get install apt-file
apt-file update
apt-get install nano
```

# Helps
Stop container: 
```
docker stop 2769d51daeb2 
```
Remove docker: 
```
docker rm 2769d51daeb2 
```
Pull container: 
```
docker pull hello-world
```
List of running container : 
```
docker ps
```
List of containers images : 
```
docker images -a
```
Clean and remove all container : 
```
docker system prune
```
