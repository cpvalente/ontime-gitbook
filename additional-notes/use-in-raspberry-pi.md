---
description: Use a docker image to run Ontime in a Raspberry Pi
---

# Use in Raspberry Pi

From version 1.10.0, Ontime is available as a docker image, targeting Arm v6 and v7 devices. Meant explicitly for Raspberry Pis.

This method leverages a lightweight image that runs Ontime server in a headless raspberry Pi without UI. All UIs and views are still available through the local network.

To get started using Ontime in a Raspberry Pi.

* [ ] Install Docker on your Raspberry Pi. You can do this by running the following command in the terminal. Alternatively please refer to Docker or Raspberry Pi guides
* [ ] Once Docker is installed, pull the `getontime/ontime` image from dockerhub with the command

```bash
docker pull getontime/ontime
```

* [ ] You can now start the image by using the provided docker compose file

```bash
docker-compose up -d
```

Ontime is now running in the Pi and accessible through the local network on port 4001

Documentation for the docker process can be [found with the image in Dockerhub](https://hub.docker.com/r/getontime/ontime)
