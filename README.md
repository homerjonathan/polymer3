# Polymer 3 development environment ready to use
This image should work for there architectures:
-amd64, arm32v6, arm32v7, arm64v8, i386, ppc64le, s390x

Docker image files in [DockerHub](https://hub.docker.com/r/elswork/polymer3/)

Images for arm32v7 and amd64 are available, you can build your own with the following command:

```sh
$ docker build -t elswork/polymer3:latest .
```

You may open the application directory:

```sh
$ cd app
```

Then you can execute some yan commands (init, install, add, ...)

```sh
$ docker run -it -v $(pwd):/root/app elswork/polymer3 yarn init
$ docker run -it -v $(pwd):/root/app elswork/polymer3 yarn install
```

Now you are ready to serve, test, build, ...

```sh
$ docker run -d -p 8081:8081 --name poly3test -v $(pwd):/root/app elswork/polymer3 polymer serve --port 8081 -H 0.0.0.0 --npm
```