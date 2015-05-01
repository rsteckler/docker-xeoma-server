Run Xeoma with Docker
================

### Purpose
Xeoma (Security Monitoring Software) in a Docker

### EULA
Make sure you read this - http://felenasoft.com/xeoma/en/eula/ as you are effectively agreeing to it by running this docker.

### Getting the Docker
From Docker Index
```
docker pull jedimonkey/xeoma
```

Build yourself
```
git clone https://github.com/jedimonkey/xeoma-docker.git
docker build --rm -t jedimonkey/xeoma xeoma-docker
```

### Running
To run the container, fire up docker like so:

```
$ sudo docker run -d --name="xeoma" --restart="always" --net=host -p 8090:8090 jedimonkey/xeoma
```

### Notes
Due to how many security cameras work, this needs to be on the host network stack.  This probably can be changed to not be so insecure, but I haven't done it yet.

