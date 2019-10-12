# Go + Gin Conduit API Server

This codebase was created to demonstrate a fully fledged fullstack application built with **Golang/Gin** including CRUD operations, authentication, routing, pagination, and more.

# How it works

```
.
├── gorm.db             //created in the initial run
├── main.go             //entrypoint for the server
├── common
│   ├── utils.go        //small tools function
│   └── database.go     //DB connect manager
└── users
    ├── models.go       //data models definition & DB operation
    ├── serializers.go  //response computing & format
    ├── routers.go      //business logic & router binding
    ├── middlewares.go  //put the before & after logic of handle request
    └── validators.go   //form/json checker
```

# Getting started

## Install the Golang version 1.12

https://golang.org/doc/install

## Start

```
➜  go run .
```

## Test

```
➜  go test -v ./... -cover
```

## Build

```
➜  go build -i -o ./bin/server
➜  chmod +x ./bin/server
➜  ./bin/server
```

If you are on Windows, add `.exe` to the `server` executable name

```
➜  go build -i -o ./bin/server.exe
➜  ./bin/server.exe
```

## Todo

- More elegance config
- Test coverage (common & users 100%, article 0%)
- ProtoBuf support
- Code structure optimize (I think some place can use interface)
- Continuous integration (done)
