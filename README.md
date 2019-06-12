Setup MongoDB with docker compose 
# Build: docker-compose build 
# Run docker-compose up -d 
# Logs docker-compose logs -f 
Create use, role 
use db
db.createUser({
    user: "badges-dev",
    pwd: "badges-dev",
    roles: [ { role: "readWrite", db: "db" } ],
    mechanisms: [ "SCRAM-SHA-1"]
})



