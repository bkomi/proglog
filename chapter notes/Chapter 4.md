# Serve Requests with gRPC


2 common problems before gRPC:
- compatibility bet client and server - API versioning
- performance
  - db and business logic optimizations
  - marshal/unmarshal cost

gRPC - open-source, high performing RPC framework

Goals When Building a Service
- Simplicity 
  - gRPC is mid-to-high level compared to express (low level)
  - offers features like bidirectional streaming
  - Rails is high level since it abstracts everything
- Maintainability
  - API versioning
  - protobouf's field versioning
- Security
  - SSL/TLS
- Ease of use
  - Type checking of requests, responses, models, serialization
- Performance
  - fast serialization
  - long-lasting connection over HTTP/2
- Scalability
  - load balancing types - client-side, proxy, look-aside, service mesh
  - Scaling people due to langauge agnosticism



- Error handling for gRPC using status
- golang Context - A Context carries deadlines, cancellation signals, and other request-scoped values across API boundaries and goroutines.