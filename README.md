# Spark 2 docker images

Yet another spark 2 docker images

## Instructions

Build:

```
docker-compose build
```

Run:

```
docker-compose up -d
```

Scale slaves:
```
docker-compose scale slave=2
```

Run interactive spark-shell:
```
docker run --rm -it --link spark2docker_master_1:master spark2docker_master /usr/local/spark/bin/spark-shell --master spark://master:7077
```
