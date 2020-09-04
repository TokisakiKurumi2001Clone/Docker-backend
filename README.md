# Docker-backend
A docker repo for building some necessities for backend

# How to use
## Build Docker image
```
docker build -t <name_tag> .
```
This will take very long on installing torch.

## Execute
```
docker run -d -p 8080:80 <name_tag>
```
Go to `localhost:8080/` to see result.

## Extract latitude, longitude
Navigate to `localhost:8080/predict/pic_1.jpg?crs=9210` for example.
All images are saved in root for the mean time.
Also available at `https://obscure-retreat-69161.herokuapp.com` but there is a problem with memory quota.

## Return invaluable information to front-end
Front-end to create a get request to backend and expect to get the json format of latitude and longitude:

https://apple-slice-2001.herokuapp.com/predict/pic_5.jpg?crs=9210

{"latitude":10.95082750045397,"longitude":106.58720175464157}
