# Clean Up



## Clean Up

Completing this lab results in a bunch of running containers on your host. Let's clean these up.

1. First get a list of the containers running using `docker container ls`. 

```bash
$ docker container ls
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                     NAMES
d6777df89fea        nginx               "nginx -g 'daemon ..."   3 minutes ago       Up 3 minutes        0.0.0.0:8080->80/tcp      nginx
ead80a0db505        mongo               "docker-entrypoint..."   3 minutes ago       Up 3 minutes        0.0.0.0:8081->27017/tcp   mongo
af549dccd5cf        ubuntu              "top"                    8 minutes ago       Up 8 minutes                                  priceless_kepler
```

1. Next,  run `docker container stop [container id]` for each container in the list. You can also use the names of the containers that you specified before.

   ```bash
   $ docker container stop d67 ead af5
   d67
   ead
   af5
   ```

**Note**: You only have to reference enough digits of the ID to be unique. Three digits is almost always enough.

1. Remove the stopped containers

`docker system prune` is a really handy command to clean up your system. It will remove any stopped containers, unused volumes and networks, and dangling images.

```bash
$ docker system prune
WARNING! This will remove:
        - all stopped containers
        - all volumes not used by at least one container
        - all networks not used by at least one container
        - all dangling images
Are you sure you want to continue? [y/N] y
Deleted Containers:
7872fd96ea4695795c41150a06067d605f69702dbcb9ce49492c9029f0e1b44b
60abd5ee65b1e2732ddc02b971a86e22de1c1c446dab165462a08b037ef7835c
31617fdd8e5f584c51ce182757e24a1c9620257027665c20be75aa3ab6591740

Total reclaimed space: 12B
```

## Summary

In this lab, you created your first Ubuntu, Nginx and MongoDB containers.

Key Takeaways

* Containers are composed of linux namespaces and control groups that provide isolation from other containers and the host.
* Because of the isolation properties of containers, you can schedule many containers on a single host without worrying about conflicting dependencies. This makes it easier to run multiple containers on a single host: fully utilizing resources allocated to that host, and ultimately saving some money on server costs.
* Avoid using unverified content from the Docker Store when developing your own images because these images may contain security vulnerabilities or possibly even malicious software.
* Containers include everything they need to run the processes within them, so there is no need to install additional dependencies directly on your host.

