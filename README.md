# docker-hello-world-with-proxy

## Getting Started

In your terminal, or in the server on docker is running,

```console
# Clone this project
$ git clone https://github.com/totto357/docker-hello-world-with-proxy.git
$ cd docker-hello-world-with-proxy

# If you did **NOT** create a `common_link` network
$ docker network create --driver bridge common_link

# Launch a proxy server (`hello-world-proxy` container),
$ cd proxy
$ docker-compose -d up

# Launch a web server (`hello-world-web` container),
$ cd ../web
$ docker-compose -d up

# Make sure hellowold is displayed
$ curl http://localhost/hello
<xmp>
Hello World


                                       ##         .
                                 ## ## ##        ==
                              ## ## ## ## ##    ===
                           /""""""""""""""""\___/ ===
                      ~~~ {~~ ~~~~ ~~~ ~~~~ ~~ ~ /  ===- ~~~
                           \______ o          _,/
                            \      \       _,'
                             `'--.._\..--''
</xmp>
```

If docker is started up on external server, as follows in your local terminal
```console
$ curl http://{SERVER_IP}/hello
```

