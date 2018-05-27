用docker maven build
```
docker run -it --rm --name lubanmall -v "$PWD":/usr/src/mymaven -w /usr/src/mymaven maven:3.5.2-jdk-8-alpine mvn clean install
```