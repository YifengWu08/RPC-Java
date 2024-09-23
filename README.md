# RPC-Java

## Startup Process

1. Install and start Zookeeper

2. Run TestServer in the Server package, then run TestClient in the Client package.



# RPC Introduction

### Theory

1. RPC (Remote Procedure Call Protocol) is a protocol for remote procedure calls.
2. RPC is a protocol that allows services to request functionality from programs on remote computers over a network without needing to understand the underlying network technology.
3. The main purpose of RPC is to make method calls between different services as simple as local calls.




### Common RPC Application

Application-level service frameworks: ：Dubbo/Dubbox、Google gRPC、Spring Boot/Spring Cloud。
Remote communication protocols：RMI、Socket、SOAP(HTTP XML)、REST(HTTP JSON)。
Communication Frameworks：MINA & Netty



### Why RPC?

1. Service-Oriented Architecture: For microservices and cross-platform service remote calls.
2. Distributed System Architecture: Distributed services call each other across machines remotely.
3. Service Reusability: Develop a common service that can be remotely called by multiple services.
4. Interaction Between Systems: For example, if you have two servers, A and B, and an application a on server A needs to call a method provided by application b on server B, but the two applications do not share the same memory space and cannot call directly. In this case, RPC facilitates remote method invocation and data transmission over the network.

#### Use Cases

1. Large websites: Involving multiple subsystems with many services and interfaces.
2. Service discovery mechanisms: Technologies like Nacos or Dubbo typically have a registry, and when there are multiple instances of a service, the caller is unaware of which instance it is interacting with.
3. Security: Resources are not exposed.
4. Service governance: Useful for microservice architecture and distributed architecture.



# Functionalities

**Version 1**

- Implement basic RPC calls
- Dynamic proxy on the client side
- Define standardized request and response formats
- Introduce Netty framework for data transmission
- Custom message format
- Introduce Zookeeper as the service registry



**Version 2**

- Custom Netty encoders, decoders, and serializers
- Build local service cache on the client side
- Implement dynamic updates to the local cache

  


**Version 3**

- Implement client-side load balancing
- Implement client-side fault tolerance: retry on failure
- Service whitelisting




**part4**

- Implement service rate limiting and graceful degradation
- Implement circuit breaker


  

