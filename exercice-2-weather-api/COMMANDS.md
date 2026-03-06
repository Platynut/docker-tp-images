docker build -t platynut/weather-api:1.0.0 .

docker run -d -p 3000:3000 --name weather platynut/weather-api:1.0.0

docker push platynut/weather-api:1.0.0

docker tag platynut/weather-api:1.0.0 platynut/weather-api:latest

docker push platynut/weather-api:latest