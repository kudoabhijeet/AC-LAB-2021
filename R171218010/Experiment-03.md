# Experiment 3: Docker Networking

## Aim
To understand networking in docker and create a network allowing containers to communicate.

## Steps Performed
 - Create a Network. `docker network create mNetwork`
![1](https://user-images.githubusercontent.com/46739435/107745687-b066f400-6d3a-11eb-9ef7-cb843d12b367.png)

 - Create a container and assign created network to container. `docker run -dit --name=ub1 --net=mNetwork ubuntu`
![3](https://user-images.githubusercontent.com/46739435/107745697-b230b780-6d3a-11eb-9666-cc504fd91b65.png)

 - Use `docker ps` to list running containers.
![4](https://user-images.githubusercontent.com/46739435/107745699-b2c94e00-6d3a-11eb-8e12-8501a04436b5.png)

 - Create another container in same network and verify connectivity using ping command.
    `docker run -d --net=mNetwork alpine ping ub1`
    Docker uses DNS to locate IP address of container, thus making communication work.
![5](https://user-images.githubusercontent.com/46739435/107745702-b361e480-6d3a-11eb-8cd7-d3e3abd56771.png)

- A single container can be attached to multiple network. And we can connect already created container to a network using 
    `docker network connect newNetwork ub2`
![6](https://user-images.githubusercontent.com/46739435/107745704-b3fa7b00-6d3a-11eb-840a-38ffd0309eb8.png)
![7](https://user-images.githubusercontent.com/46739435/107745707-b4931180-6d3a-11eb-9682-aad6221b0e9b.png)
![8](https://user-images.githubusercontent.com/46739435/107745708-b4931180-6d3a-11eb-8f54-cdc42052a8d5.png)

- We can create alias for container which will create a new entry a DNS.
    `docker network connect --alias main newNetwork ub1`
![9](https://user-images.githubusercontent.com/46739435/107745710-b52ba800-6d3a-11eb-86f1-d237b5f888a6.png)

- We can use `docker network ls` to list available networks.
![10](https://user-images.githubusercontent.com/46739435/107745711-b5c43e80-6d3a-11eb-941e-d6afc86604e2.png)

- We can use `docker network inspect mNetwork` to inspect network.
![11](https://user-images.githubusercontent.com/46739435/107745713-b65cd500-6d3a-11eb-8c65-8555d0a3b8df.png)
![12](https://user-images.githubusercontent.com/46739435/107745715-b6f56b80-6d3a-11eb-8347-6683c0af8a8e.png)

- To disconnect a container form network use `docker network disconnect mNetwork ub1`.
![13](https://user-images.githubusercontent.com/46739435/107745718-b78e0200-6d3a-11eb-9624-63edc30d4ce0.png)