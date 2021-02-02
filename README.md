# `docker`
A few examples of `docker` and `docker-compose`

## docker `hello world!`

### Build the `hello` docker image
```shell
➜ cd hello
➜ docker build -t hello .
```
### Run the `hello` image as a container
```shell
➜ docker run --rm hello
```

## docker `mongodb-sample-data` image
```shell
➜ cd mongo-sample-data
➜ docker build -t mongo-sample-data .
```

### Run the `mongodb-sample-data` image as a container
```shell
➜ docker run -d               \
  --name my-mdb-db             \
  -v     $PWD/data:/data/db    \
  mongo-sample-data
```

### Run the `mongodb-sample-data` container using `docker-compose`
```shell
➜ docker-compose up -d
```