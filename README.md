## Docker MongoDB Cluster (Replication Set)
Easily deploy Mongodb cluster on your local environment

## Getting Started
- Nodes:
    - mongodb1 [master]
    - mongodb2 [rs secondary]
    - mongodb3 [rs secondary]
- Run Mongodb cluster contianers
```shell
$ docker compose up -d
```
- Execute to mongo shell on master node
```shell
$ docker exec -it mongodb1 mongosh
```
- Setup replications
```shell
rs.initiate()
rs.add("mongodb2:27017")
rs.add("mongodb3:27017")

```

## Port Configuration
- nodes:
    - mongodb1: 27027
    - mongodb2: 27078
    - mongodb3: 27079