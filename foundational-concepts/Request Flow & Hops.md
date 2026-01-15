# Request Flow & Hops

In the context of **foundational concepts** for backend engineering, understanding the **request flow and hops** is presented as the starting point for gaining a "big picture" view of how systems communicate. Rather than focusing on specific languages or frameworks, which can create "blind spots," this approach focuses on the underlying systems that allow a client to communicate with a server.

### **Request Flow and Network Hops**
The sources describe the request flow as a high-level journey that begins at the client side and moves through various infrastructure layers:

*   **The Origin:** A request is initiated from a **browser**.
*   **The Hops:** As the request travels over the internet, it passes through different **"hops,"** which include **network firewalls** and other routing mechanisms.
*   **The Destination:** The request is eventually **routed to a backend server**, which may be located in a remote environment, such as an **AWS server**.
*   **The Response:** Once the server processes the request, it sends a **response** back through the network to the client, completing the communication cycle.

### **Request Flow within the Foundational Context**
The concept of request flow is not isolated; it serves as the framework for several other foundational backend principles mentioned in the sources:

*   **HTTP Protocol:** The communication during this flow is established via **HTTP**. This involves understanding raw messages, methods (GET, POST, PUT, DELETE), and the role of various **HTTP headers** (request, representational, general, and security headers).
*   **CORS and Pre-flight Requests:** The flow can vary depending on the nature of the request. For instance, the sources highlight the difference between a **simple request** and a **pre-flight request flow**, which involves an initial check from the browser to the server and back before the actual request is sent.
*   **Serialization and Deserialization:** For data to move through these hops, it must be **serialized** (translated into a format like JSON, XML, or Protobuf) before being sent over the network and **deserialized** back into a native format upon arrival.
*   **Middleware Pipeline:** Once a request reaches the server, it often passes through a **middleware flow**. This is a sequence of functions—such as logging, authentication, and validation—that can **short-circuit** the request or pass control until it reaches the final handler.
*   **Request Context:** Throughout the flow, **metadata** (such as URL headers, request IDs, and user information) is maintained in a **request context**. This provides a temporary, **request-scoped state** that is shared across different layers of the application.

By mastering these foundational concepts of how a request flows through various hops and internal server layers, an engineer can build systems that are **reliable, scalable, fault-tolerant, and maintainable**, regardless of the specific programming language used.
