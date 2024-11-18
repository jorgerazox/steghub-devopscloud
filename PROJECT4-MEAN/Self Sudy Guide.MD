# **The OSI Model**

The **Open Systems Interconnection (OSI) model** is a conceptual framework that standardizes the functions of a communication system into seven distinct layers. It was developed by the International Organization for Standardization (ISO) to ensure interoperability among diverse communication systems.

### **The Seven Layers of the OSI Model**

1.  **Physical Layer (Layer 1)**
    -   **Purpose:** Handles the transmission of raw binary data (0s and 1s) over physical media.
    -   **Responsibilities:**
        -   Electrical and physical specifications 
        -   Data encoding and signaling.
        -   Synchronization of bits.
    -   **Examples:** Ethernet cables, fiber optics, network interface cards (NICs).

----------

2.  **Data Link Layer (Layer 2)**
    -   **Purpose:** Ensures reliable data transfer across the physical link by detecting and correcting errors.
    -   **Responsibilities:**
        -   Frame creation, error detection, and correction.
        -   Media Access Control (MAC) and Logical Link Control (LLC).
    -   **Examples:** MAC addresses, Ethernet (802.3), Wi-Fi (802.11).

----------

3.  **Network Layer (Layer 3)**
    -   **Purpose:** Manages data routing, addressing, and packet forwarding across multiple networks.
    -   **Responsibilities:**
        -   Logical addressing 
        -   Path determination and routing.
        -   Fragmentation and reassembly of data packets.
    -   **Examples:** IP (IPv4, IPv6), routers.

----------

4.  **Transport Layer (Layer 4)**
    -   **Purpose:** Ensures complete and reliable data transfer between systems.
    -   **Responsibilities:**
        -   Segmentation and reassembly of data.
        -   Flow control and error control.
        -   Multiplexing/demultiplexing of data streams.
    -   **Examples:** TCP, UDP.

----------

5.  **Session Layer (Layer 5)**
    -   **Purpose:** Manages sessions or connections between applications.
    -   **Responsibilities:**
        -   Establishing, maintaining, and terminating communication sessions.
        -   Synchronization and checkpointing of data streams.
    -   **Examples:** NetBIOS, RPC (Remote Procedure Call).

----------

6.  **Presentation Layer (Layer 6)**
    -   **Purpose:** Translates data between the application layer and the network, ensuring proper formatting and encryption.
    -   **Responsibilities:**
        -   Data formatting and syntax translation.
        -   Encryption and decryption.
        -   Data compression.
    -   **Examples:** SSL/TLS, JPEG, ASCII, MPEG.

----------

7.  **Application Layer (Layer 7)**
    -   **Purpose:** Provides network services directly to end-users or applications.
    -   **Responsibilities:**
        -   User interface and interaction.
        -   Application-specific services like email, file transfer, and web browsing.
    -   **Examples:** HTTP, FTP, SMTP, DNS.

Additional reference:

[# What is the OSI Model?](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)

------
# **Load Balancing and Routing Techniques**

**Load balancing** is a technique to distribute incoming network traffic across multiple servers to ensure no single server becomes overwhelmed. It enhances application availability, reliability, and performance.

Load balancing ensures that application resources are used efficiently by distributing traffic to multiple servers, balancing the load, and preventing any one server from becoming a bottleneck.


### **Types of Load Balancing**

1.  **Hardware Load Balancers**: physical devices designed for load balancing.

2.  **Software Load Balancers**:  applications that perform load balancing. Example:  NGINX.
 
3.  **Cloud-Based Load Balancers**: load balancing services provided by cloud platforms. Example: AWS Elastic Load Balancer (ELB)

### **Techniques of Load Balancing**

1.  **Server-Side Load Balancing** : the load balancer resides between clients and servers and distributes traffic among backend servers.

2. **Client-Side Load Balancing**: the client is responsible for determining which server to send requests to, often using libraries or SDKs.


### **Load Balancing Algorithms**

**Static Algorithms**: decisions are made based on predefined criteria, regardless of server load.

 - **Round Robin:** Traffic is distributed sequentially to each server.
 - **Weighted Round Robin:** Assigns weights to servers; higher-weighted servers receive more traffic.
 -  **Least Connection:** Routes traffic to the server with the fewest active connections.
  - **IP Hash:** Determines the server based on a hash of the client's IP address.

    
**Dynamic Algorithms**: decisions are made in real-time based on server load or health.
-  **Least Response Time:** Routes to the server with the shortest response time.
- **Resource-Based:** Considers server CPU, memory, or bandwidth usage before routing traffic.
----------

### **Routing Techniques in Load Balancing**

#### **Layer 4 Load Balancing (Transport Layer)**
-   Routes traffic based on IP address and port without inspecting packet content. **Example:** TCP/UDP-based traffic distribution.

#### **Layer 7 Load Balancing (Application Layer)**

-   Routes traffic based on request content, such as URL, HTTP headers, or cookies. **Example:** HTTPS load balancing for specific subdomains.

----------

### **Advanced Load Balancing Techniques**
**Global Server Load Balancing (GSLB):**
- Distributes traffic across multiple geographically distributed data centers.

**Sticky Sessions (Session Persistence):**
- Ensures that requests from a particular client are routed to the same server through cookies or IP hashing.

**Health Checks:**
-   Regularly monitors the health of servers to ensure traffic is only routed to healthy nodes. Types: TCP ping, HTTP/HTTPS status codes.
 
 **Failover:**
 - Automatically redirects traffic to a backup server if a primary server fails.

**DNS Load Balancing:**
- Uses DNS to distribute traffic by resolving a domain name to different IP addresses.