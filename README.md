# JavaSimpleServer

A simple HTTP server implementation in Java that follows the HTTP/1.1 specification (RFC 7230).

## Description

JavaSimpleServer is a lightweight, educational HTTP server built from scratch in Java. It demonstrates core HTTP protocol concepts including request parsing, response generation, and connection handling.

## Features

- HTTP/1.1 compliant request parsing
- Support for GET and HEAD methods
- Configurable port and webroot
- Multi-threaded connection handling
- JSON-based configuration
- Comprehensive HTTP status code handling
- Logging with SLF4J and Logback

## Requirements

- Java 7 or higher
- Maven 3.x

## Building

To build the project, run:

```bash
mvn clean compile
```

To build and run tests:

```bash
mvn clean test
```

To create a JAR file:

```bash
mvn clean package
```

## Running

1. Configure the server by editing `src/main/resources/http.json`:
   ```json
   {
     "port": 8080,
     "webroot": "/tmp"
   }
   ```

2. Run the server:
   ```bash
   mvn exec:java -Dexec.mainClass="com.github.mpanczak.httpserver.HttpServer"
   ```

   Or if you have a JAR file:
   ```bash
   java -cp target/SimpleServer-1.0-SNAPSHOT.jar com.github.mpanczak.httpserver.HttpServer
   ```

3. The server will start and listen on the configured port (default: 8080).

## Configuration

The server configuration is stored in `src/main/resources/http.json`:

- `port`: The port number the server will listen on (default: 8080)
- `webroot`: The root directory for serving files (default: /tmp)

## HTTP Specification

This implementation follows the HTTP/1.1 specification as defined in [RFC 7230](https://datatracker.ietf.org/doc/html/rfc7230).

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.
