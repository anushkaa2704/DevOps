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



<hr>
<h3>To Create Docker Image of any application.(powershell)</h3>
mkdir docker-lab<br>
cd docker-lab<br>
echo '<h3>My First Docker App! Success! ✅</h3>' > index.html<br>
@'<br>
FROM nginx:alpine<br>
COPY index.html /usr/share/nginx/html/index.html<br>
'@ | Out-File -FilePath Dockerfile -Encoding utf8<br>

Get-ChildItem<br>

docker build -t my-first-app .<br>
docker run -d -p 8888:80 --name first-container my-first-app <br>

Access in browser: http://localhost:8888 <br>



<h3>push & pull</h3>
docker pull nginx:latest<br>
docker images (ngnix should be visible)<br>
docker tag nginx anushkaa2704/new-nginx<br>
docker images (new-ngnix should be visible)<br>
docker push anushkaa2704/new-nginx<br>




<h4>Pull OS Images</h4>
docker pull ubuntu:20.04<br>
docker pull alpine:latest<br>
<h4> Create Containers </h4>
docker run -it --name ubuntu-os ubuntu:20.04 /bin/bash<br>
docker run -it --name alpine-os alpine:latest /bin/sh<br>
<h4>run</h4>
docker run -it --name ubuntu-container ubuntu:20.04 /bin/bash<br>
docker run -it --name alpine-container alpine:latest /bin/sh<br>


