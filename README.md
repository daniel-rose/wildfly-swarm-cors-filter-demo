# wildfly-swarm-cors-filter-demo

A WildFly Swarm CORS Filter Demo

## Usage

###  Run the app

``` sh
./mvnw clean package
java -jar target/wildfly-swarm-cors-filter-demo-swarm.jar 
```

### Access API

``` sh
curl localhost:8080 -v
```

You can see the response headers for CORS.

``` sh
< Access-Control-Allow-Origin: *
< Access-Control-Allow-Headers: Origin, X-Requested-With, Content-Type, Accept
< Access-Control-Allow-Methods: GET, POST, PUT, DELETE, OPTIONS
< Access-Control-Max-Age: -1
```

### Run the app with prod profile

``` sh
java -jar target/wildfly-swarm-cors-filter-demo-swarm.jar -Sprod
```

``` sh
curl localhost:8080 -v
```

The `Access-Control-Max-Age` header values changed.

``` sh
< Access-Control-Max-Age: 86400
```