![Docker Pulls](https://img.shields.io/docker/pulls/pixelchrome/minio-arm)
![Build Status](https://img.shields.io/docker/cloud/build/pixelchrome/minio-arm)

# Minio Docker Container for ARM
This Dockerfile installs Minio on your ARM-Platform (e.g. Raspberry Pi)

# Minio
Please visit the Minio Website for more details https://minio.io

Minio is an object storage server released under Apache License v2.0. It is compatible with Amazon S3 cloud storage service. It is best suited for storing unstructured data such as photos, videos, log files, backups and container / VM images. Size of an object can range from a few KBs to a maximum of 5TB.

Minio server is light enough to be bundled with the application stack, similar to NodeJS, Redis and MySQL.

# Installation
```
$ sudo docker build -t minio-arm .
```

Or you can pull it from hub.docker.io
```
$ sudo docker pull pixelchrome/minio-arm
```

# Run Minio Standalone on Docker
```
sudo docker run -p 9000:9000 -v /export/minio -v /export/mino-config:/root/.minio minio-arm server /export
```

# Detailed information
A more detailed description can be found here https://docs.minio.io/docs/minio-docker-quickstart-guide

# Not tested
Distributed Minio on Docker has not been tested

# Whats the `Dockerfile.arm32v7` &  `Dockerfile.arm64v8`?

The `Dockerfile.arm32v7` &  `Dockerfile.arm64v8` have been created to use the automated build process on the [Hub](hub.docker.com). Also the scripts in the `hooks` directory.

As DockerHub is not natively building ARM-Images, it is necessary to find a way around that limitation.

Thanks to [trion.de](https://www.trion.de) for their detailed article how to get it running (link below).

# Links
* GitHub Repository - https://github.com/pixelchrome/minio-arm
* Docker Hub Repository - https://hub.docker.com/r/pixelchrome/minio-arm
* Multi-Arch Images als Autobuild - https://www.trion.de/news/2019/10/14/docker-multi-arch-dockerhub.html
* Support automated ARM builds - https://github.com/docker/hub-feedback/issues/1261