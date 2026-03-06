docker build -t hello-flask:1.0.0 .

docker run -d -p 5000:5000 --name mon-flask hello-flask:1.0.0

docker tag hello-flask:1.0.0 hello-flask:latest
docker images