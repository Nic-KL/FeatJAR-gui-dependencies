# Eclipse GLSP Server Framework

Contains the needed dependencies from [GLSP](https://github.com/eclipse-glsp/glsp) to create server components for [FeatJAr-gui](https://github.com/Nic-KL/FeatJAR-gui-new). 

## Building

Run `./gradlew build` to execute `./mvnw clean verify -Pm2` or execute the wrapper directly. 

### Traditional

The server bundles are built with Java 17 or higher and maven.
Execute `mvn clean verify -Pm2` (for maven) or `mvn clean verify -Pp2` (for p2).

## Structure of this repository

- `org.eclipse.glsp.graph`: EMF-based implementation of graphical model that's used for client-server communication
- `org.eclipse.glsp.layout`: Server-based layout using the [Eclipse Layout Kernel](https://www.eclipse.org/elk/) framework (adapted from [Eclipse Sprotty Server](https://www.github.com/eclipse/sprotty-server))
- `org.eclipse.glsp.server`: Generic base implementation for standalone GLSP servers (based on JSON-RPC)
- `org.eclipse.glsp.server.emf`: Reusable implementations if an [EMF](https://www.eclipse.org/modeling/emf/)-based source model is used
- `org.eclipse.glsp.server.websocket`: Extension of the base server implementation for communication over websockets


