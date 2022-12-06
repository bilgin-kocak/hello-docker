## Docker HelloWorld Example

Build a docker image with tag

```
docker build -t hello-docker .
```

List the docker images in your pc.

```
docker image ls
```

Run the image with tag name

```
docker run hello-docker
```

You can push this docker to dockerhub

Then you can pull on any pc with docker. You can run the code in **any pc**.

https://labs.play-with-docker.com/

## Another Example

Pull ubuntu image from docker hub.

```
docker pull ubuntu
docker run ubuntu
```

Below command show the docker processes

```
docker ps
docker ps -a
```

Run the docker image in interactive mod. You can see the docker console here.

```
docker run -it ubuntu
```
