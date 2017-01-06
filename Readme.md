# Minio Docker Container for ARM
This Dockerfile installs Minio on your ARM-Plarform (e.g. Raspberry Pi)

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

# Links
GitHub Repository - https://github.com/pixelchrome/minio-arm
Docker Hub Repository - https://hub.docker.com/r/pixelchrome/minio-arm
