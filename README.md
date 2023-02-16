# Introduction

This is a clone of the [Original Repository](https://github.com/raeperd/realworld-springboot-java/). Once it is used in a book for teaching and training purpose, it is important to have a stable version such that people can use according to book examples.

Thanks for [RealWorld Project | Realworld.io](https://github.com/gothinkster/realworld)

# Getting started

## Before you start

Please, if necessary, you may adjust server configurations located `application.properties`.

Default condifuration will start the server (backend) at `http://localhost:3000/api`.

This consigiration is defined by two properties inside `application.properties`:

- `server.port=3000`
- `server.servlet.context-path=/api`

Additionaly, once the client may be running on a different port, in the `application.properties` file there is also a configuration to enable CORS from a specific machine. In our case, the default configuration assumes client will connect to the server from `http://127.0.0.1:3001`

- `security.allowedOrigins=http://127.0.0.1:3001`

Also, if you change any configuration above, you also need to adjuts the file `doc/run-api-test.sh`.

In this file, there is the definition of a variable indicating the API URL. Please, change it according to your new configuration. Its default value is:

```shell
APIURL=${APIURL:-http://localhost:3000/api}
```

## Build from scratch

``` shell
 $ ./gradlew build
```
 
## How to test 

After run application, you can try one of followings

### using shell script

``` shell
$ ./doc/run-api-tests.sh
```

# Contact

Case you hava any problem, we may contact us via pull request in this project.

# License
[MIT License](./LICENSE)
