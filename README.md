# Blynk Server Docker Image

[![](https://images.microbadger.com/badges/image/mpherg/blynk-server.svg)](http://microbadger.com/images/mpherg/blynk-server
"Get your own image badge on microbadger.com") [![](https://images.microbadger.com/badges/version/mpherg/blynk-server.svg)](http://microbadger.com/images/mpherg/blynk-server
"Get your own version badge on microbadger.com")

Runs your own [Blynk Server](https://github.com/blynkkk/blynk-server) in a Docker container instead of relying on Blynk's public server.

[Blynk](http://www.blynk.cc) is the "first drag-n-drop IoT app builder for Arduino, Raspberry Pi, ESP8266, SparkFun boards, and others." Super fun.

## How To Use It


To persist data, create volumes and run a container:

```sh
docker run -d --restart unless-stopped --name blynk-server -v blynk-data:/data -v blynk-config:/config -v blynk-data-backup:/data/backup -p 8440:8440 -p 8080:8080 -p 9443:9443 mzabolotnov/blynk-server
```

Or you can use a data volume in another container (check out different data volume techniques [here](https://docs.docker.com/engine/tutorials/dockervolumes/)).
