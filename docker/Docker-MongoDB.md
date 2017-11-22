# MongoDB Docker
v3.4

```bash
# run
docker run --name mongo34 -p 27017:27017 -d mongo:3.4
# connect
docker exec -it mongo34 mongo admin
# create user
db.createUser({ user: 'shawnyan', pwd: 'password', roles: [ { role: "userAdminAnyDatabase", db: "admin" } ] });
```

## Reference

- [docker-mongo](https://github.com/docker-library/mongo)
- [dockerhub/mongo](https://hub.docker.com/_/mongo/)