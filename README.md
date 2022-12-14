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

## Docker Commands

Delete dangling images

```
docker image prune
```

Show images

```
docker images
```

In dockerfile, you should write stable instruction on the top and changing instruction on the bottom.

CMD, RUN, ENTRYPOINT has shell and execute forms

- CMD npm start // run in new shell
- CMD ["npm", "start"]

Running container with given name in detach mode

```
docker run -d --name blue-sky image-name
```

View logs

```
docker logs -h
docker logs container-id
```

Publishing ports

```
docker run -d -p 80:3000 --name name image-name
```

Execute a command in running docker

```
docker exec container-name ls
docker exec -it container-name sh
```

Stop and start running container

```
docker stop container-name
docker start container-name // docker run start a new container
```

Create persistent volume on container

```
docker volume create volume-name
docker run -d -p 4000:3000 -v volume-name:/app/data image-name
```

Copy file from docker to host or vice versa

```
docker cp container-id:/app/log.txt .
docker cp secret.txt container-id:/app/
```

Sharing source code with docker for development

```
docker run -d -p 4000:3000 -v $(pwd):/app image-name
```
