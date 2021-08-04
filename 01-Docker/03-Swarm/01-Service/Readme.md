  ```
  32  docker node ls
   33  docker service ls
   34  docker service create --replicas 1 --name hello-swarm nginx
   35  docker service create --replicas 1 --name hello-swarm nginx -o yaml
   36  docker service create --replicas 1 --name hello-swarm nginx --help
   37  docker service ls
   38  docker service ls -o wide
   39  docker service ls --help
   40  docker service list
   41  docker service ls
   42  docker service inspect hello-swarm
   43  docker service --help
   44  docker service ps hello-swarm
   45  docker ps
   46  docker service ps hello-swarm
   47  docker service ls
   48  docker service scale hello-swarm=5
   49  docker service ls
   50  docker service ps
   51  docker service ps hello-swarm

# Scale In 
   59  docker service ls
   60  docker service scale hello-swarm=2
   61  docker service ls
   62  docker service ps hello-swarm

```
