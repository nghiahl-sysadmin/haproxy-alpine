# How to use this image
- Since no two users of HAProxy are likely to configure it exactly alike, this image does not come with any default configuration.
- Please refer to https://docs.haproxy.org/ documentation on the subject of configuring HAProxy for your needs.
- Docker repository https://hub.docker.com/r/nghiahl/haproxy
## Create a ```Dockerfile```
```
FROM nghiahl/haproxy:alpine-v2.8.5
COPY path/to/haproxy.cfg /etc/haproxy/haproxy.cfg
```
## Build the container
```
$ docker build -t local/haproxy:alpine-v2.8.5 .
```
## Run the container
```
$ docker run -d --name haproxy local/haproxy:alpine-v2.8.5
```
