## Docker-node-web-server-deploy
Docker-Deploy
Dockerizing a Node.js web app
### Building your image
 ```docker build . -t <your username>/node-web-app> ```
### Your image will now be listed by Docker:

```$ docker images

# Example
REPOSITORY                      TAG        ID              CREATED
node                            16         3b66eb585643    5 days ago
<your username>/node-web-app    latest     d64d3505b0d2    1 minute ago
```
### Run the image

```docker run -p 49160:8080 -d <your username>/node-web-app```

### Print the output of your app:

```# Get container ID
$ docker ps

# Print app output
$ docker logs <container id>

# Example
Running on http://localhost:8080
```

### Test

```$ docker ps

# Example
ID            IMAGE                                COMMAND    ...   PORTS
ecce33b30ebf  <your username>/node-web-app:latest  npm start  ...   49160->8080
```
$ curl -i localhost:49160

```HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: text/html; charset=utf-8
Content-Length: 12
ETag: W/"c-M6tWOb/Y57lesdjQuHeB1P/qTV0"
Date: Mon, 13 Nov 2017 20:53:59 GMT
Connection: keep-alive

Hello world
```
