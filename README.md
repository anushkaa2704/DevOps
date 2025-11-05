Docker:<br>
cd desktop <br>
mkdir DockerFiles<br>
cd DockerFiles<br>
echo. > Dockerfile<br>
echo FROM ubuntu > Dockerfile <br>
echo RUN apt-get update >> Dockerfile <br>
echo CMD ["echo", "Container created successfully..."] >> Dockerfile <br>
type Dockerfile <br>
docker build -t a26 . <br>
docker images <br>
docker run img_id <br>
