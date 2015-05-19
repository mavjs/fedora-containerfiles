Fedora based Application Dockerfiles
====================================
Install [Docker](https://www.docker.io/).

```sudo yum install docker-io```

```sudo docker pull mavjs/chrome``` or any other app

For GUI apps, run as below to get display and sound working:

```
    sudo docker run -it \
    --net host \
    --cpuset-cups 1 \
    --memory 512mb \
    -v /tmp/.X11-unix:/tmp/.X11-unix \
    -e DISPLAY=unix$DISPLAY \
    -v /dev/snd:/dev/snd --privileged \
    -v /dev/shm:/dev/shm \
    -v /etc/machine-id:/etc/machine-id \
    -v /var/lib/dbus:/var/lib/dbus \
    -v /run/user/`id -u`/pulse/native:/run/user/`id -u`/pulse/native \
    -v ~/.pulse:/home/$dockerUsername/.pulse \
    --name chrome \
    mavjs/chrome
```
*You may want to delete the image after using*

```
    sudo docker rm chrome
```

**PROFIT!!**
