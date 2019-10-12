docker build -t drone-nolimit:latest .
docker run -d --rm --name drone-nolimit -p 1000:80 -p 1443:443 -e DRONE_GITEA_SERVER=http://gitea.192.168.1.158.xip.io -e DRONE_SERVER_HOST=drone.192.168.1.158.xip.io drone-nolimit:latest
