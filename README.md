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

# 4 Get-ChildItem<br>

# 5. Build image<br>
docker build -t my-first-app .<br>

# 6. Run container<br>
docker run -d -p 8888:80 --name first-container my-first-app <br>

# 7. Access in browser: http://localhost:8888 <br>
