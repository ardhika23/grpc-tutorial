# 📝Tutorial & Exercise📝

**Student Details :**

|  `Attribute`  | `Information`              |
|---------------|----------------------------|
| Name          | Ardhika Satria Narendra    |
| Student ID    | 2206821866                 |
| Class         | Advanced Programming KKI   |

---
<details>
<summary>Module 09: High Level Networking</summary>

## Questions and Answers

### -> Reflection 

#### 1. What are the key differences between unary, server streaming, and bi-directional streaming RPC (Remote Procedure Call) methods, and in what scenarios would each be most suitable?
- Unary: Simple, one-request-one-response interaction. Ideal for discrete operations like fetching a data record or performing a calculation.
- Server Streaming: Server sends multiple responses from one request. Useful for scenarios like delivering real-time updates or streaming large data like logs or file transfers.
- Bi-Directional Streaming: Both client and server can send messages in a continuous stream. Suitable for real-time, interactive applications such as chat applications or live event handling.

#### 2. What are the potential security considerations involved in implementing a gRPC service in Rust, particularly regarding authentication, authorization, and data encryption?
- Authentication: Ensuring that both client and server verify their identities. SSL/TLS can be used for secure communication channels.
- Authorization: Implementing access control measures to ensure clients can only access resources for which they have permissions.
- Data Encryption: Using transport security with SSL/TLS to encrypt data in transit, protecting against interception.

#### 3. What are the potential challenges or issues that may arise when handling bidirectional streaming in Rust gRPC, especially in scenarios like chat applications?
- Handling concurrent messages efficiently without blocking or losing data.
- Managing connection lifecycles and error handling robustly, especially in network-unstable environments.
- Ensuring that the order of messages is preserved and that there are mechanisms to handle or recover from missed or out-of-order messages.

#### 4. What are the advantages and disadvantages of using the tokio_stream::wrappers::ReceiverStream for streaming responses in Rust gRPC services?
- Advantages: Simplifies handling of asynchronous streams in Rust; integrates well with tonic and tokio for efficient non-blocking communication.
- Disadvantages: Might introduce complexity in error handling and back-pressure management; learning curve for proper utilization within asynchronous Rust code.


#### 5. In what ways could the Rust gRPC code be structured to facilitate code reuse and modularity, promoting maintainability and extensibility over time?
- Utilize Rust's module system to encapsulate functionality and reduce coupling.
- Define clear interfaces for services using traits and generics to allow for flexibility and reuse.
- Implement common functionality as middleware or shared libraries (e.g., error handling, logging).

#### 6. In the __MyPaymentService__ implementation, what additional steps might be necessary to handle more complex payment processing logic?
- Implement additional checks for fraud detection and compliance.
- Integrate with external services for tasks like real-time currency conversion or risk assessment.
- Provide mechanisms for transaction rollback or compensation in case of failures.


#### 7. What impact does the adoption of gRPC as a communication protocol have on the overall architecture and design of distributed systems, particularly in terms of interoperability with other technologies and platforms?
- Facilitates building microservices architectures by defining strict contracts and efficient communication.
- Enhances language-agnostic interoperability through protocol buffers.
- Requires careful design to handle complexities of distributed systems, such as latency, partial failures, and serialization overhead.

#### 8. What are the advantages and disadvantages of using HTTP/2, the underlying protocol for gRPC, compared to HTTP/1.1 or HTTP/1.1 with WebSocket for REST APIs?
- Advantages: HTTP/2 supports multiplexing, reducing latency by allowing multiple messages on the same connection. Efficient for gRPC performance.
- Disadvantages: More complex to implement and debug; potential for issues in environments where HTTP/2 is not fully supported.

#### 9. How does the request-response model of REST APIs contrast with the bidirectional streaming capabilities of gRPC in terms of real-time communication and responsiveness?
- REST typically operates over HTTP/1.1 with stateless servers and predictable, resource-oriented URLs, using JSON. Best for web APIs accessible from browsers and for systems that require cacheable responses.
- gRPC offers bidirectional streaming and operates over HTTP/2, making it better suited for real-time and highly interactive applications where performance and efficiency are critical.

#### 10. What are the implications of the schema-based approach of gRPC, using Protocol Buffers, compared to the more flexible, schema-less nature of JSON in REST API payloads?
- gRPC uses Protocol Buffers, which provide a strong type system, compact binary data format, and a strict schema, enhancing performance and robustness.
- JSON used in REST is more flexible and human-readable, easier to use for dynamic or loosely coupled systems but typically less efficient in terms of performance and type-safety.

---

</details>