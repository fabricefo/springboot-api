# Run MongoDB

docker pull mongo:latest
docker run -d --name=mongodb \
        -e MONGODB_INITDB_ROOT_USERNAME=admin \
        -e MONGODB_INITDB_ROOT_PASSWORD=password \
        -p 27017:27017 mongo:latest
docker exec -it mongodb bas

> mongosh
> db.createUser({user: "springuser", pwd: "springpwd", roles: ["readWriteAnyDatabase"]})

Create database "demo"
(The simpliest way is to add VScode extension to manage MongoDB)

# Run app

Clone the repository.

./mvnw clean install
./mvnw spring-boot:run

# Test API

http://localhost:8080/swagger-ui.html



