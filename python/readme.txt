# create docker image and tag it using -t
docker build -t friendlyhello .

# new docker image should show up in local Docker image registry
docker image ls

# run app in container and map local machine's port 4000 to container's published port 80 using -p
docker run -p 4000:80 friendlyhello

# open http://localhost:4000 in local machine's browser

# quit app with CTRL+C

# explictly stop container (on Windows only)
docker container ls
docker container stop <container_name or container_id>

# run app in background, in detached mode using -d
docker run -d -p 4000:80 friendlyhello