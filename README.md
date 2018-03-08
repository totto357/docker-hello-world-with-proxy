# docker-hello-world-with-proxy

## Getting Started

Clone this project,

```
git clone https://github.com/totto357/docker-hello-world-with-proxy.git
cd docker-hello-world-with-proxy
```

If you do **NOT** created `common_link` networks,

```
docker network create --driver bridge common_link
```

Launch `hello-world-proxy` container,

``` 
cd proxy
docker-compose -d up
```

Launch `hello-world-web` container,

``` 
cd ../web
docker-compose -d up
```
