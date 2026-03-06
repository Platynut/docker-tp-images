docker build -t platynut/stats-api:1.0.0 .

docker run -d -p 4000:4000 --name stats platynut/stats-api:1.0.0

docker build -t platynut/stats-api:2.0.0 .

docker images

docker tag platynut/stats-api:2.0.0 platynut/stats-api:latest

docker push -a platynut/stats-api