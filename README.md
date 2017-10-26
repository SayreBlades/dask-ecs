# Dask ECS

This is an opinionated template for spinning up a dask cluster based on docker.


## Install

Simply navigate to your aws console and import the dask-ecs.yaml file.  In the web portal you can configure to your liking.


## Example Docker Scheduler

https://hub.docker.com/r/sayreblades/dask/


## Example Docker Worker

https://hub.docker.com/r/sayreblades/dask/


## Example client

```
import dask
import distributed


client = distributed.Client(address="[YourDaskServer:Port]")
b = dask.bag.from_sequence([1, 2, 3, 4, 5, 6])
c = b.map(lambda o: o*2)
f = client.compute(c)
f.result()
```

## Logs

Creates logs in cloud watch.  The log group name will be the name you gave the cloud formation stack.

To view logs use the cloudwatch web interface or awslogs: https://github.com/jorgebastida/awslogs

```
awslogs get [log group name] -w
```

## Similar Projects

- https://hub.docker.com/r/magsol/distributed-dask/

- https://github.com/ogrisel/docker-distributed
