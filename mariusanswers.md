## Chapter 1

### What is a distributed system? (p.2):

Network that consists of autonomous computers connected through a communication network.

### **What are the two characteristics of a distributed system? (p.2):**

Transparency (looks like a single simple application to the end user) and scalability.

### **What four important goals should be met to make building a distributed system worth the effort? (p.7):**

Resource sharing: Sharing resources like IoT devices or things like applications, API's or databases.

Opennes: Can easily interract with other systems and can be extended or modified as needed.

Scalability: Can scale up, down and sideways. Can scale without increasing complexity.

Fault tolerance: Is fault tolerant, meaning it can handle network partitions.

### **What types of distribution transparency is there? (p.8):**

Location transperency, fault transperency, replication transperency, scale transparency

### **What is middleware in the context of distributed systems?:**

Software layer or set of services that sits at between the hardware and application, acts as a bridge that helps different components communicate with eachother.

### **What is an open distributed system and what can be done to achieve openness?:**

Designed to be open, flexible and interopable.

### **What is scalability with regards to distributed systems and how can distributed systems be scaled?:**

Ability to handle increase in users and load. Therefore also how easy it's for a distributed system to add new servers to the system. Distributed systems can be scaled by either scaling up(upgrading the servers) or adding more servers.

### **What are some pitfalls when designing distributed systems?:**

Consistency and data integrity, concurrency and race conditions, fault tolerance, complexity, data partitioning.

### **What are some types of distributed systems?:**

Client-server system, peer-to-peer system, clusted systems, CDN's, distributed databases, blockchain

### **What is high performance distributed computing?:**

Low latency, high throughput, scalability, efficient resource utilization

### **What are distributed information systems?:**

Think distributed databases, information is distributed over several nodes.

### **What is a pervasive system?:**

A pervasive system is a system that is integrated with some IoT device. he goal of pervasive computing is to create a computing environment that is unobtrusive, intuitive, and capable of providing intelligent and
context-aware support for users.

### **Why is it sometimes hard to hide the occurence of and recovery from a failure in a distributed system?:**

CAP theorem, if we have a partition we can either have availability or consistency, not both.

## Chapter 2:

### **What is an architectural style and how is it formulated?:**

An architectural style describes how the distributed system is built up in terms of how parts communicate and operate (client-server, peer-to-peer)

### **What are the three traditional layer views?:**

OSI, TCP/IP, Internet protocol suite.

### **What are an wrapper or adapter w.r.t. middleware? And how can these be organized?:**

Wrapper/adapter helps 2 other non-compatible processes communicate with eachother by adapting their communication means for it the be understandable. We have wrappers and adapters but we also have brokers where brokers do all the communication leading to a drastic decrease in the amount of wrappers needed.

### **What are an interceptor?  Fig 2.14.:**

Middleware that interrupts and changes the information flow upon a certain happening.

### **Describe an centralized system architecture. p.76:**

Centralized describes single point of failure, lets say we have a controller-worker setup with a master node, if that master node goes down, we are fucked.

### **In a client-server architecture, what does it mean that an operation is idempotent?:**

That the result does not change even if the operation was carried out a second, third or 100 time with same data. Determenistic.

### **How can a centralized system architecture be tiered? Give an example for each tier.:**

Presentation tier(UI), Application tier(Data processing), Data tier(database), Infrastructure tier(Hardware)

### **Describe decentralized organisations (p2p systems):**

No single point of failure, peer-to-peer, blockchain systems

### **What is an structured peer-to-peer system?:**

Nodes can be thought of as in a overlay, meaning that there is some organization of ndoes (chord with nodeid)

### **Describe an unstructured p2p system.:**

Nodes are connected but in no meaningful way, communication can be costly as finding the right node can take a long time and use a lot of badnwidth.

### **Describe two ways of searching for specific data in an unstructured p2p system.:**

Broadcasting for the information and random walks. Broadcasting is simply flooding, random walks is selecting a random node to forward communication to.

### **What are policy-based search methods?:**

Policy-based search methods aim to find an optimal or near-optimal policy, which is a strategy or set of actions that maximize the expected outcome or reward over time.

### **What are Hierarchically organized p2p networks? Give an example of such network.:**

Super-nodes which the non-supernodes are connected too, all comms goes through the super nodes if en-route to non-supers.

### **What is an edge-server system?:**

We have some computation happening closer to the data source. Think of Dag and Tore´s fishing case, we have edges where some computation/capturing is happening with IoT devices.

### **chapter2: What is collaborative distributed systems?:**

System where multiple users at multiple different locations can collaberate on projects togheter. Think google docs.

### **Describe NFS (Network File System).:**

A way of letting computer A access the file system of computer B by adding the file path to the ipaddress:port url. Think ssh.

### **What are the 4 main architecture types?:**

Layered architectyre: calls go down and response goes up. Hierachical manner, each layer provides service to layer above.

Client-server: 2 main compoents, clienst and servers.

Component based: Assemblig pre-built, reusable components or modules.

Microservice: Small, independetly deployable services distributed to several places.

### **What are components, connectors and interfaces in system-architecture?:**

Components are the parts that build up the system, client, server, database etc. Connectors: Connect the components together. Interfaces: How to communicate with the components.

### **Describe a layered system architecture.:**

Presentation layer(ui), Application level(where data processing happens), data level(Database and shit), Infrastructure level(hardware level)

### **Describe a object-based system architecture.:**

We have several objects all encapsulating the information and methods. Helpful for giving abstraction in terms of what methods actually do, how objects communicate with eachother.

### **Describe a resource-based architecture.:**

REST, resources are discrite entities or objects.

### **What is the difference between vertical and horizontal distributed achitectures?:**

Scaling up vs scaling out. Scaling up (upgrading hardware on a single node) vs scaling out, having more servers to handle the load instead of a more powerful server.

### **Describe a pub-sub architecture.:**

Servers can subscribe to topics/types and get the updates/data pushed to them when new is posted (if subscribe), very nice as we don't need to poll over and over, but get instant updates, disadvantage is that we have to keep state so that we know where to publish the new information, this requires some fault tolerance and consistency.

### **What is a three-tiered client-server architecture?:**

Presentation(client tier), application(middle tier), data tier(server tier or storage tier)

### **Not every node in a p2p network should become super-peer. What are reasonable requirements that a super-peer should meet?:**

Reliability (high uptime, robustness), Network bandwidth and speed, processing power, stable network address, storage capacity, reliable connectivity, secure, scalability.

### **What is coordination in a distributed system?:**

Coordination in a distributed system is how to make sure that operations and data follow certain rules and guidelines to uphold data and operation consistency.

### **Explain temporal and referential coupling.:**

Temporal coupling: Timing is essential for functionallity, modules must be invoked in a specific order to avoid errors or produce incorrect results. Referential coupling: Refers to how a certain module depends on the data structures and data elements defined in another module.

### **What are the four key characters in RESTful architectures:**

Statelessness, client-server architecture, uniform interface, resource based

### Many people like RESTful approaches because the interface to a service is so simple. What is the catch about it?:

Limited expressivness, overuse of GET, versioning challenges, complex queries, lack of standardization, under- or Over-normalization, security considerations, performance and scalability.

### Can you give an example of a traditional three-layered architectural view?:

Presentation layer, application/processing layer, data/database layer.

## Chapter 3

### What is virtualization?:

Creates illusion of having something we don't, can create VM's which gives illusion of having a whole computer with said operating system, instead we have a computer with other OS running the virtual OS as a program. Virtual processor to create threads.

### Explain software Process, Thread and Processor.:

Process = instance of a program, thread = executor of said instance of program, smallest instance of execution within a process, processor = hardware responsible for running processes.

### Explain context switching (w.rt Processor and Thread).:

Context switching includes saving state of process we are switching from and loading state of other process to run that. Remember OS, context switching gives illusion of parallel programs, but each program is given a super tiny slot of computing. Threads can run processes but can also be run in the same process sharing memory.

### How can a server be constructed?:

Define server purpose and requirments, select hardware, data backup and recovery, scalability planning.

### Give tree different levels of virtualization.:

hardware virtualization, virtual memory, virtual processor etc. Operating system-level virtualization, gives a virtual instance of a OS. Application-level virtualization, containers, lets applications run in isolated env, minimizing conflicts.

### Describe process, native and hosted virtual machines (monitor).:

Process virtualization is a lightweight form of virtualization, allows software to run isolated, be portable and compatible. Native virtual machines, Type 1 hypervisors, run directly on the physical hardware without need for a host operating system. Hosted virtual machines, run on top of a host operating system, provide virtualization layer between the guest virtual machines and the host OS.

### What are privileged and nonpriviliged instrctions. Name the two special instructions.:

Priviliged instructions, refer to instrucitons you can only run if you have higher privilige on the OS (ring 0), elevated access rights. Non-priviliged instructions = user mode instructions, instructions that can be executed in a lower privilige mode. SYSCALL, request services from the OS = I/O, process managment and memory allocation. HLT (halt): instructs the processor to enter a low-power state or halt its execution until an external interrupt even occurs.

### "For any conventional computer, a vmm may be constructd if the set of sensitive instr. for that computer is a subset of the set of privileged instr.". What is the problem with this and what are some solution?:

Oversimplifies the challenges involved. Incomplete definition of sensitivity: doesn't provide a clear definition of what constitues "sensitive instructions". Complex privilige levels: Real-world processors often have multiple privilige lelves or protection rings (ring 0, ring 1, ring 2, and ring 3 on x86), the set of priviliged instructions can vary based on the specific privilige level. Instruction interaction: Virtualization introduces challenges related to instruciton interaction and control. Some instructions may behave differently when executed by a guest virtual machine (VM) compared to when executed nativly on the host.

SOLUTIONS:

Define sensitivty clearly: essential to provide a precise definition of what constitues sensitive instructions in the context of virtualization. Manage privilage levels: Virtualization solutions must manage privilege levels effectivly. Instruction handling: VMM often includes instruction interception and emulation mechanisms. When sensitive instruction, VM intercepts it and emulates its behaviour and enforces security and isolation.

### Distinguish application-level and middleware-level solutions. See figure 3.10 p.124:

Application-level is tightly integrated into a specific application. Designed to address particular requirments or functionalities of that application. These solutions are primarily focused on meeting the specific needs of the application or application domain. Can be finely tuned to meet. the precise needs of the application. Middleware-level solutions on the other hand are independent of specific applications, designed to be reusable common functionallity that can be used by multiple applications.

### Discuss benefits and disadvantages with a thin clients architecture for a distributed system:

Advantages: Centralized managment, software updates, security patches and application changes can be applied centrally on the server or in the cloud. Cost efficient, lower hardware costs, reduced maintenence cost. Security, reduced attack surface, centralized security protocols. Scalability and flexability, device agnostic (can tolerate both new and old, high-end and low-end hardware). Disadvantages: Network dependency, thin clients rely heavily on network connectivity slow or unreliable networks can lead to poor user exp, latency. Limited offline access. Server and infrastructure costs. Limited processing power.

### Reasons to migrate code?:

Performance, privacy/safety, flexibility. A server might be overloaded we can transfer to another server with more availible resources, can also migrate code to get processing closer to data (map-reduce), Privacy/safety, something might be compromised or we might need to segregate data to keep some user information isolated from other.

### Explain Push (code shipping) and Pull (code fetching) protocols in weak mobility:

Push protocols are used when there is need for a real-time and near real-time updates. Messaging apps that push new messages to a users device as they arrive, or stock trading apps that push price updates. Server initiated, immediate updates, always connected. Pull protocol: Mobile devices that actively. requests updates, code changes or data from the server or remote source at intervals or when neeeded. Client initiated, on-demand or scheduled, intermittent connectivity. Does not require constant connectivity and therefore more resource friendly, more managle to scale as no state needed, can just pull. Challenges, when to pull? User initieted updates?

### What are the disadvantages and advantages of stateful servers?:

Advantage can use push based protocols for near real-time updates, saving resources and bandwidth. Disadvantage: need to have state that is replicated and consistent if we experience a server failure we don't want all connected clients to miss out on their updates.

### Is it possible to interrupt a server once it has accepted (or is in the process of accepting) a service request?:

Hard to do in stateless, statefule like FTP or SSH easier to do. Also depends on the server design.

### Does connection-oriented communication fit into a stateless design?:

Two distinct approaches in networking and communication. Not inherently compatible but they can be used together. In general they are conceptually opposite. Load balancers often use stateless algos to distribute requests to backend servers.

### Having the first tier, in a three-tiered architecture handle all communication from/to the cluster may lead to a bottleneck. What could be a solution to this?:

Bottleneck in client, can implement load balancers, caching and async comms, use microservices, CDNS, horizontal scaling.

### Migration in heterogeneous systems can cause problems such as the target machine may not be suitable to execute the migrated code. And the definition of process/thread/processor context is highly dependent on local hardware, operating system, and runtime system. There's only one solution to this, what is it? (slides):

Virtualization is the solution as it addresses the compatibility and portability issues when migrating code between heterogeneous systems. Isolation of env, abstraction of hardware, compatibility layers, snapshot and migration.

### X Window System designates a user's terminal as a hosting server, while the application is referred to as the client. Does this make sense? (past exam question):

In X the server (the users computer) is responsible for managing the display, input devices and graphical resources. The client (graphical application) sends requests to the server to draw windows, display graphics and handle user input. This role reversal is somewhat counterintuitive compared to the client-server model commonly used in network communication where server typically provides services to multiple clients. Network transparency: Applications can run on remote servers and display their graphical output on a local machine and vice versa.

### The X protocol suffers from scalability problems. How can these problems be tackled?:

Network improvments, faster network connections, such as high-speed broadband or low-latency networks, can help mitigate some x11 scalability issues by reducing the impact of network latency and bandwidth limitations. Local execution with remote display: may be more efficient to execute resource-intensive applications locally on the client and display them remotly using the x11 or other protocols. Tunneling and compression: SSH tunneling can be used to encrypt and compress x11 traffic, reducing the bandwidth usage and enchaing security over the network.

## **Chapter 4:**

### What are the layers of the OSI-stack and what are the drawbacks of the OSI-model?:

Application layer, network layer, link layer, physical layer, transport layer. Complexity, can be overly complex for practical implementation. Lack of real-world mapping, limited adoption, widely thaught, but TCP/IP reigns supreme.

### What is the middleware layer?:

Reigns between hardware and application layer, enables comms, integration and coordination between distributed components.

### What types of communication do we have?:

Synchronus, Async, request-response, publish subscribe, message-oriented comms, RPC and socket-based, share memory comm, middleware based, p2p, API's.

### What is an RPC?:

Remote Procedure call, abstracts away complexity of api's and treats API calls as a local call (sending method and arguments)

### What are the basic steps of an RPC operation?:

Create a client stub of the operation, send client stub down to client OS, OS sends the stub to server, server unpacks stub and does the procedure, pack the response in a server stub, send server stub response back to client, client unpacks.

### What must be done to pass parameters in a RPC call and why must it be done?:

Parameter serialization, marshalling and demarshalling,  parameter passing order and type matching, parameter validation, error handling, data integrety and security.

### What is an asynchronous RPC and when is it useful?:

When there is now dependency of a response, we can issue the call and move further. Non-blocking operations, parallelism and concurrency, latency hiding.

### What is multicast RPC?:

RPC that is sent to multiple recipients at once, results are typically returned asyncally. Client request: A client sends a single RPC request to a multicast group or channel, specifying the remote procedure to be executed and providing any necessary parameters. Multicast distribution: The RPC request is multicast to mutliple recipients, which can be servers or service instances that have registed to receive request on the multicast groupp all recipients receive the same request simultaneously.

### How does message-oriented communication differ from RPCs?:

Message-oriented communication is typically async and does therefore not block and wait for response. Messages can be sent in a one-way fashion. Messages are typicall structured data units that can carry various types of information including data, commands, events or notifications. Message formats are flexible (JSON, XML, protocol buffers). Can support various comm patterns (publish-sub, point-to-point, request-reply). Supports decoupling, loose coupling between components. Senders and receivers of messages are typically unaware of each other and they communicate through an intermediary message broker or message que. This gives great flexibility and scalability/load balancing.

RPC is typically synchronous in nature. Client inits a PC, waits for response and may block until it receives reply. RPC are centered around invoking functions or methods of remote services or servers. Calls remote function/method as if it was locally placed. Follows request-response pattern, client sends request with parameters and the server processes the request and sends a response back to the client. Stronger coupling, the client needs to know the interface and method signatures of the remote procedures it is invoking.

### What is transient asynchronous communication?:

Transient communication typically refers to comms and interactions in a distributed system that are temporary or short-lived. Often exchange of data, messages or signals between components or nodes for a specific purpose and duration. Async comms = non-blocking, non-waiting. Therefore a host-lived or temporary interactions that are not dependent on immediate or synchronous responses.

### Briefly describe message-oriented persistent communication through message-oriented middle-ware.:

Async comms, abstarcts complexities of low-level messaging and provides a set of services and protocols for sending, receiving and managing messages. Loose coupling between components and enables components to continue their work independetly. Persistent, messages sent through MOM are often designed to be stored persistently until theey are succsessfully deliverd and acked. Guarateed delivery, ensures that messages are succsessfully delivered.

### Why was the Advanced Message Queuing protocol created?:

Heterogeneous enviroments: different applications, platforms and programming languages need to communicate seemlessly. Diverse messaging needs: Messaging requirments can vary from point-to-point, publish-subscribe and request-response. Reliability and scalability: Reliably delivered and infrastructure that can scale to handle growing workloads.

## **Chapter 5:**

### What is naming used for in distributed systems?:

Access points of entities, names -> addresses -> access points.

### What is an access point?:

Where to reach an entity, how to contact (phone number or home address for a human)

### What does it mean when a name is location independent?:

Name is not dependent of location of entity, does not include information about location (phone number for humans not home address)

### Which properties does an identifier have?:

An identifier refers to at most 1 entity, an entity is refered to by at most 1 identifier, an identifier always refers to the same entity.

### How can flat names be resolved?:

Broadcasting, forwarding pointers, home-based approach, DHT

### Explain DNS, how does this system lookup?:

Domain name system, works recursivly www.facebook.com, starts with .com, looks for facebok under that domain. Utilizes domain hierachy, DNS records, local cache and DNS resolver.

### Describe distributed hash table (Chord 😍😝).:

Nodes are given a node id, with nodes having a previous and succsessor + finger table. Based on keysize/chordsize a node will have keysize amount of entries in the finger table pointing to nodes with id >= ft entry index (own id + 2^i) where i is index and 0'indexed, these FT entries are tuple, node id + ipaddress:port.

### What is a hierarchical location scheme? Describe an approach to it.:

File system for example, breaks down larger space into smaller nested components, each of which can be identified within the context of its parent component.

### What are name spaces?:

namespace is a container or context that holds a collection of names for items, objects or entities to prevent naming conflicts and provide organization and scope within a system or application. Name isolation, scoping, organization, modularity, name clarity, avoiding confusion.

### How can name spaces be distributed?:

Hierarchical naming, namespaces, contextual naming, distributed naming services, namespace resolution, flat naming with unique prefixes, hashing and semantic naming.

### What are the principles of name resolution (recursive and iterative).:

Recursive resolution: Client-server interaction, in recursive resolution the DNS resolver (client) sends a query to a DNS recursive resolver or a DNS server that supports recursive resolution, typically provided by the client's internet service provider(ISP). The recursive resolver takes on the responsibility of resolving the entire query on behalf of the client, it does not return an incomplete or partial answer to the client. Caching intermediate results. Complete response, it sends a complete response to the client, providing the requested IP address.

Iterative name resolution: Client-server interaction, in iterative resolution the DNS resolver(client) sends a query to a DNS server, which can be any DNS server, including a caching server or an authoritative server. Partial response, the DNS server that receives the query sends a partial response if the query is not resolved completely. Client responsibility, the client is responsible for making iterative queries to the DNS servers specified in the referals.

### What are Hilbert space-filling curves?

Based on properties and values of these properties the Hilbert space-filling curves are mapped (think snake on nokia) in 2D space which again maps to address.

### What is a pure name?:

Typically refers to a unique identifier or lable used to identify a network resource, object or entity without revealing any information about the location, physical properties or attributes of that resource. Location transparency, decoupling, global uniqueness, abstraction, resolution.

### What is broadcasting?:

Think flooding, sending same request to all possible or wanting clients/servers. single source -> multiple recipients.

### What is the Address resolution protocol (ARP)?:

ARP is the address rosolution protocol used for finding a specific computer in a network of machines, done by broadcasting to all computers asking if they are the machine we are looking for before forwarding specific request there.

### What is meant by forwarding pointers?:

Points to where we should go next to find a entity, Lets say A is first store in layer 2, but then more matchin entries are added to layer 2, we move A to layer 3 and add a forwarding pointer in layer 2 telling it that A is now in layer 3.

### What are home-based approaches and when are they used?:

Home based approaches refer to having a home "central" which a machine is usually connected to. To find the machine simply ask the "home" address, but if the machine is on the move, the home central is updated on the new location of the machine and therefore can refer anyone searching for it to go there. Think sleepover as a kid, someone looking for you they go to your home, your mom tells them you are at Kristoffers place, they now know where to find you. Mobile devices, network mobility, resource load balancing, virtualization

### How can network proximity be exploited to get rid of problems like erratic message transfers?:

Local communication, geographic data replication, proximity-aware routing, traffic engineering, peer selection.

### What is hierarchal location services (HLS)?:

Refers to a method of organizing and managing location-related information in a hierarchical or structured manner in distributed systems, particularly in the context of geographic or spatial information. Some key aspects include: Hierachal structure, location resolution, spatial indexing, scalability, location-based queries, navigation and routing, geographic information systems, location based services.

### How is lookup and insertion done in a HSL tree?:

To perform a lookup in HSL, start at the higher level of the hierarchy such as country or region, then drill down the hierachy select more specific regions, areas/ cities, neighborhoos, streets etc. The user can then continue to narrow down the search until result is found.

To insert the system must first determine the appropriate level of granularity at which to store the data. System inserts into the corresponding node or leaf of hierarchy.

### How is scalability in an HLS and what can be done to scale such a system?:

Data partitioning, divide the geographic area covered by the HLS into manageable partitions or regions. Assign each partition to a dedicated server or node responsible for managing location data (geographic sharding). Load balancing, implement load balancing mechanisms to distribute the user requests evenly across HLS servers or nodes. Caching, data replication. Horizontal scaling, database optimization. Async processing, content delivery, monitoring and analytics, global distribution, content delivery and distribution algos, scalability testing.

### What is structured naming?:

Refers to structuring and organizing naming data, resources or entities into a systematic and hierarchical manner using predefined structure or format. This is done to make it easier to categorize, locate and manage information, especially in large and complex systems. Meaningful names, hierichal structure, consistency, ease of navigation, data organization, resource managment, compatibility.

### How do you resolve a name in a given name space?:

Parsing and splitting, context and namespace identification, local lookup, caching and optimization, recursive or iterative resolution.

### What is a closure mechanism?:

Where to start in when resolving a name space and when to stop.

### What is name linking and what forms of linking are there?:

Hard links and soft links (remember OS), soft links are pointers, hard links are copies.

### What is mounting?:

Process of integrating a file system or storage device into the existing directory of an operating system. When you mount a file system or device it becomes accessible to the system and can be access through a specific directoy (mount point)

### How can a distributed name-space be implemented?:

Hierarchical structure, namespace resolution, distributed directory services, replication and redundancy, scalability, security and access control, namespace federation, consistency and concurrency control.

### What are the two methods of resolving a name and how are they done?:

Recursive and iterative :), explained over.

### What are some scalability issues in distributed name-spacing and what can be done to counter it?:

Namespace partitioning, load balancing, caching, replication all problems. Caching at various levels, replicate namespace data across multiple servers for fault tolerance and improved performance. Load balancing, evenly distribute requests among the namespace servers.

### What is attribute-based naming?:

Query for attribute values.

### How can attribute-naming systems (directory services) be implemented?:

Group addresses based on attribute values

### What is LDAP?:

Lightweight directory access protocol, accessing and managing directoy information over a network, typically in a hieracrhical and organized fashion. LDAP is a lightweight client-server protocol that allows clients to interact with directory services, such as directory servers, to perform operations like querying, searching, adding, modifying, and deleting directory entries.

### What is a distributed in dex?:

directory exchange typically referrs to a system or infrastructure designed to exchange or share directory information across distributed or networked environments. This dir information may include data related to users, resources, services, devices and other objects within a organization.

## Chapter 6:

### In time synchronization, what are the differences between "The Berkeley Algorithm" and "The Time Network Protocol"?:

Berkely: centralized calculates clock skew and fixes time, looking question beneath, NTP: distributed, nodes sync with each other.

#### How can clocks be synchronized over a wireless network?:

Using a time server that first pings for response to calculate network latency, it can then the adjusted time to all parties to be synced and have them receive the actual time to sync.

### How can tokens be used to elect super-peers in peer-to-peer networks?:

Bully algo, token is node id or something.

### What is the main principle behind logical clocks (eg. Lamport Clocks)?:

Happens before relationships, I.E A -> B, and B -> C, then A -> C since A was before B and B was before C.

### Describe a decentralized system for mutual exclusion.:

Ring based approach, nodes structured in a ring, can send the mutex token round and round, nodes that want to do work, have to wait for the token to come around, if a node does nto need the token simply pass forward.

### How does a computer keep track of time?:

Real time clock (RTC), hardware component in the motherboard. quartz crystal oscillator to generate a stable and accurate time reference. When system boots, RTC inits the time based on the information stored in its memory.

### What is clock skew?:

Refers to discrepency or offset in the time readings of two separate clocks, often expressed as a time difference.

### What is UTC?:

Coordinated universal time. The primary standard time used worldwide for regulating and syncing time accross different regions and time zones.

### What is the goal of clock synchronization and what types of synchronization do we have?:

To achive coordination and consistency having synced clocks is super useful. WE have time transfer sync, transferring current time from a source (time server) to nodes in a distributed system. Event ordering sync (Lamport logical clocks). Vector clocks. Time sync for real-time systems.

### What is clock drift?:

over time internal clocks of computers or devices can drift away from correct time due to variations in the clock oscillators frequency. This gradual drift can lead to increasing clock skew.

### How can the network time protocol (NTP) be used to adjust time between two machines?:

NTP is designed to ensure that computer clocks remain accurate and synced, even when connected to a distributed network with varying network latencies. NTP server provides accurate time information, while the clients sync their clocks with the server.

### How can the Berkeley algorithm be used to keep track of time without UTC?:

Round trip calculation, time adjustment, estimation of server time.

### What is the reference broadcast system (RBS)?:

Aims to provide highly accurate and reliable time sync for distributed systems, particularly in scenarios where traditional methods may not be feasible or suitable. Broadcast based sync. One-way time transfer principle.

### What is a happened-before relationship?:

Describes sequence of events in systems, if A sends message to B, then A sending must have happend before B can receive.

### What is a logical clock?:

Lamport logical clocks C(A) < C(B) or vector clocks

#### Where should the logical clocks be implemented?:

Software or application layer of a distributed system. These clocks are not physical devices or components of the operating system or hardware, instead they are abstract mechanisms used for tracking and ordering events within a distributed system. Abstract event ordering, independence of hardware and OS, application specific context, flexibility, event recording.

### How can Lamport’s logical clocks be used for mutual exclusion?:

Event ordering, meaning that when request for lock is sent, the node with lowest "time" is given the lock. If all process continiously communicate they will always update their clocks to adjust for drift/skew and will therefore be relativly synced.

### What is a vector clock?:

A clock where all nodes in to keep track of are given a dimensional index, this index is increment every time a node receives or sends. 3 nodes (0,0,0) all of them, process 1 sends to process B, process B receives (1, 0, 0), since it receives we increment to (1,1,0), it then sends back to A which then has (2,2,0), A sends to C, which receives and increments to (3,2,1). The sum of all vectors tell the "time".

### How can causally ordered multicasting be done?:

Casually ordered mutlicasting is done to ensure that all recipients receive the messages in a way that ensures that events that casually depend on each other are delivered in the correct order. To achive casual ordering, typically use lamport timestamps or vector clocks to timestamp events or messages. When message is sent, attach lamport or vector timestamp. Receivers compare the timestamp with their own (local timestamp or vector clock), if the timestamp is greater or concurrent with respect to recipient's timestamp that means the message represents a casually dependent event. If the received message is casually dependent (its timestamp indicates it's a valid event) the process delivers the message to its local application or takes appropriate action. if not casully dependent, buffer the message until the missing casual events arrive.

### What is mutual exclusion in a distributed system?:

Think locks, we give exclusive acess to a resource or operation to a given node in the system, meaning all other nodes can not acess that data or operation before they have the mutex lock.

### What are two basic mutual exclusion techniques in distributed systems?:

Centralized and decentralized (token based vs centralized)

### How can permission-based schemes be implemented?:

User auth, user role and managment, resource identification, permission definitions, ACL's

### What is Ricart’s and Agrawala’s distributed algorithm for mutual exclusion?:

Each process has unique process identifier(pid), processes are aware of the total number of processes in the system, reliable comms exists between processes. Request que, timestamps, states.

All processes start in the released state, requesting access to critical section, when a process wants to access the critical section, it transitions to the "wanted" state. Broadcasts a request message to all other processes with its lamport timestamp. Upon receiving a request message from another process a process compares the timestamp of the received request with its own timestamp. If the receiving process is not interested in accessing the critical section, it sends ACK back. if the recever is also interested, but has lower timestamp (priority) it sends ack to sender and enters waiting que. When a process exits critical section it broadcasts to all other processes indicating that it has left. When a waiting process receives an ACK it checks if it has ACK from ALL other processes, and if it does it can enter the critical region.

#### How can a decentralized mutual exclusion algorithm be implemented?:

Ring, sending the mutex token around.

### What isan election algorithm and what assumptions need to be made in an election algorithm?:

Election algo is used to elect leader(duh), assumptions that can be made are

### How does the bully algorithm work?:

All nodes have a ID, if new election happens a node sends election with its id to all other nodes, if they have higher id they respond and say "i take it from here", if a node does not get a response it has bullied all other nodes and is elected leader.

### How can election be done on a ring structure?:

Start the process of sending election process round in the ring structure, all alive nodes add their id to the forwarded list, if id is already in the list, then we are done forwarding and can exit. The remaining list when around selects the node with highest (or lowest) Id and sets that to leader. Then forwards that list to all nodes around the ring to let them know who the leader is and make them aware of all alive nodes in the ring.

### What is the goal of election in wireless environments and how can election be done in such environments?:

The goal of an election is to elect a leader that can take elevated responsibility (coordinator, load balancer, fault tolerance).

### What are locations system?:

LBS are technologies and services that determine and utilize the geographical or physical location of a device, object or user within a defined area. These systems rely on various technologies and methods to identify and track locations accurately. Location systems have a wide range of applications in industries such as telecom, navigation, transport, healthcare, logistics and more.

### How can position be calculated?:

3 points and can triangulate using radius math between the 3 positions.

### How can Global positioning system (GPS) be used to find the position of a node?:

Trilateration.

### When cannot GPS be used to find a position and what alternatives do we have?:

Indoor env, urban canyons, underwater, deep inside buildings or tunnels

### How is positioning done in a centralized system?:

Central server or authority, device registration, signal messurments, triangulation and trilateration.

### How can positioning be done in a decentralized system?:

Peer-to-peer comms, signal exchange, collaberative sensing, trilateration, reference nodes.

### What is event matching?:

The main goal of event matching is to detect meaningful events, anomalies, or incidents by combining and correlating information from diverse sources. Event sources, event types. Techniques: pattern recognition, rule based matching, machine learning.

### How can event matching be done in a centralized manner?:

Peer-to-peer collaberation, distributed event processing, event propagation, peer discovery

### How can brokers route notifications to the appropriate set of subscribers?:

Topic based matching, message queues, filtering and rounting, content based matching, mutlicast and broadcast.

### What is gossip-based coordination?:

Gossiping happening/events to known nodes to coordinate what is happening around the system.

### What is aggregation?:

Concept of combining or summarizing multiple individual elements or data points into a single entity or result.

### What is a peer-sampling service (PSS)?:

A pss continously maintains a dynamic sample of network nodes allowing for adaptation to changes in the network, such as node arrivals, departures or failures. Random selection of nodes, small sample size, local interaction, failure detection, scalability, decentralization.

## Chapter 7:

### What are the reasons for replication in distributed systems?:

Performance, consistency, fault tolerance.

### What is a consistency unit and what is it used for?:

Can be a single file or a directory of files, in a distributed db can be a single table or database shard or specific partition of data. In distributed cache can be a cache entry or a group of related cache entries. (unit to keep consistent)

### What is the connection between sequential consistency and logical clocks?:

The connection between sequential consistency and logical clocks lies in their shared goal of establishing a meaningful event order in a distributed system. Logical clocks establish a partial order of events in a distributed system, while sequential consistency enforeces a global total order of memory operations that respects this partial order.

### Describe the underlying principle of causal consistency.:

Preserve the causality or cause-and-effect relationship between events. If event A preceds event B (B is dependent on the outcome of A), then the system ensures that event A is observed by all processes before event B.

### What are the differences between "Monotonic read/write" consistency and "Read your writes" consistency?:

Monotonic reads = when reading a value x we will never read a older version of x, only the same or newer version. Once a write is observed by a process or node, all subsequent reads from that process or node will reflect that update or a more recent one. In other words, the writes appear to be monotonically increasing in their visibility. No guarantee on other processes. Read your writes is a stronger guarantee that applies to a single client or process. It ensures that once a client performs a write operation(update), all subsequent read operations by that cleint will reflect that write or a more recent one. Key difference is the scope of their guarantees: Monotonic focuses on ensuring that a single process or node observes its own writes before any subsequent reads. It does not make guarantees about the order in which other processes observe operations. Read your writes is stronger guarantee that ensures that a single client always observes its own writes before any subsequent reads.

### What does replica placement involve?:

Placement of replica database/storage. Fault tolerance and high availability, data consistency, latency and read performence.

### What are the three main ways of doing content replication?:

Full replication ( high fault tol, low latency reads) (High storage overhead, increased write complex, limitied scalability), nice for small to moderatly sized datasets where fault tol and low-latency reads are critical, and storage capacity is not a major constraint, partial replication(lower storage overhead, improved scale, easier managment) (reduced fault tol, potentially higher latency reads) larger datasets where a balance between fault tol and storage efficiency and performance is required. Caching(low-latency access, reduced load on the source, dynamic adaptation) (data staleness, limited capacity, cache coordination) low-latency is key, data freshness can be managed effectively. Web cashing or CDNs

### What are the three ways content can be propagated to replica servers?:

Eager replication, copying data to replica as soon as updates or changes occur on the primary server. Propogated to replicates without delay, ensures that all replicas are kept up to date in real-time. Low-latency, immediate fault tolerance. Increased network usage and storage usages, potential consistency issues. Used when fault tol and real-time consistency are ritical.

Lazy replication, also known as deferred or delayed replication, involves delaying the propagation of changes to replica servers. Instead of immediatley cipying updates, changes are collected and batched before being sent to replicas at specific intervals or when a treshold is reached. Reduced network and storage usage, lower update latency on primary. Potentially higher data staleness, longer recovery time. Suitable for scenarios where low network and storage overhead is prioritized over real-time consistency. CDNs and backup systems.

Quarum based replication. Changes propogated when quorum is reached. Provides a blaance between consistency and performance, fault tolerant. Complex, increased latency compared to eager replication. Used when both fault tolerance aond consistency are key.

### What is the difference between a push-based and a pull-based data transfer scheme?:

Push based the server inits the sending, in pull based the client asks for the information. Responsivness: push based more responsive as it pushes out at new change, pull is less frequently updated. Sender has more control when data is pushed to recipients, can decide which recipient can receive the data and when to send it. Push based can be efficient where data needs to be delivered quickly. Needs state(big drawback). Pull based less effective as it has to poll continiously, when to poll? Waste of bandwidth, does not need state tho.

### What is a lease and how can lease expiration time be decided?:

Lease is aggreament to get all updates while lease is valid (duration), can set the exp time of the lease based on the data type, event ocurrence or based on algo.

### When should multicasting and unicasting be used with regards to push and pull protocols?:

Multicasting is more suitable when you want to send data or messages to multiple recipients at the same time and all receivers want the same information. Common when subscribers or participants, is efficient and relevant. Push and multicast, is often used when you have real-time or event-driven data that needs to disseminated to a group of interested recipients. Unicasting: appropriate when you need to send data or messages to specific individual recipients and the content may vary for each recipient. Common when customization or personalization is required. Pull and unicast: pull-based unicast is often used when data is requested by individual recipients on an as-needed basis.

### What is a consistency protocol?:

A protocol to uphold consistency between primary storage and eventual backups. Strict consistency, sequential, casual, eventual, quorum, two-phase commit, paxos and raft.

### How can the three ranges of continuous consistency be implemented?:

Strong consistency: involves using coordination and consensus protocols like raft or paxos. All replicas must ack the updates before they considered and committed. Used when data consistency is crucial and the system can tolerate latency and performance overhead. Bounded staleness: hybrid consistency models that combine elements of strong and eventual consistency. Techniques like quorum-based systems with tunable parameters or vector clocks can be eplyoed to track casual dependencies. Useful when applications require a balance between strong consistency and low-latency access to data, strict consistency is not always needed as seen in CDN's. Eventual consistency: Allows replicas to converge to the same state over time, even in the presence of network partitions and concurrent updates. Well suited for systems where immediate consistency is not a strict requirment, and it is acceptable for data to be temporarily inconsistent across replicas. Like CDN's, collaberative editing apps and social media.

### What are primary based consistency protocols?: 

Primary based server/database which handles all writes and propogates these writes out to backup servers that are closer to clients.

### What kind of primary based consistency protocols do we have?:

Remote-write: send request for write to local server/db, local server/db forwards to primary db, which after doing the write sends ack to local server that operation is done, local server performs same operation and returns. Local-write: find data we want to write to, and move it to local storage and write new value, propogate the change.

### What is replicated-write protocols?:

Write operations can be carried out at several replicas at the same time instead of only one which is the case for primary-based replicas.

### How can client-centric consistency be implemented?:

Session identification, assign unique id to each client session. Session isolation, operations on one client should not interfere with or affect the consistency of other sessions. Session state managment, session guarantees, conflict resolution.

## Chapter 8:

### Being Fault tolerant are related to being a dependable system. What does Dependability mean in this context? Give the four properties of Dependability.:

Availabile, Reliability, safety and maintainability.

### Fail, error and fault is three ways a system can lead to failure. Describe these properties.:

Fault in the system leads generates a error which creates a fail. Bug in code is fault, that generates a error, which gives a fail.

### Which types of failures can a system have?:

Crash failure, omission (send and receive), timing, response (value and state transfer), byzantine.

### How can a fault toleraant system hide the occurence of failures from other processes using redundancy?:

Replication, data redundency, communication redundency, software redundency, error detection and correction.

### How can resilience be done using process groups? Describe process groups, and their internal structure.:

Group processes based on definition and common goals, replication, communication, coordination, fault detection and recovery.

### Process resilience  with grouping needs to be managed in some way. Give how the management protocols can be implemented.:

Membership managment, failure detection, leader election, consensus and agreement.

### Process grouping is a part of the solution for building fail-tolerant. How should process in these groups be replicated?:

Active-active replication, state machine replication, N-modular redundancy, passive replication with checkpointing

### What is meant when a system is k-fault tolerant?:

That the system tolerates faults in k-nodes/servers.

### What is meant by reaching consensus in a fail-tolerant system? Describe approaches to reach consensus.:

Consensus is having all nodes in the system/group agree upon 1 and exactly 1 thing despite network partitions. Can use paxos or raft to do this :)

### How can a system detect failures?:

Non consistent answer with other nodes, timing failure, heartbeating, pinging.

### What are the five diferent classes of failures that can occur in rpc systems, and how can these be solved?:

Server not found: raise exception.

Request to server is lost: Timeout, and resend when no-ack

Server crashes after receiving: Atleast-once semantics, keep retrying to send the request until ack is received. Or atmost-once semantics, gives up immediatly and reports failure.

Reply message to client is lost: Resend request if not received in time. Idempotent (atomic).

Client crashes when sending request: Orphan, keep log on harddrive or some crash resilient piece of hardware. Orphan extermination, write records for every rpc to disk (expensive), reincarnation split time into epochs. Try to locate owner, no owner? exterminate.

### What is reliable group communication?:

Reliability, ordered delivery, fault tolerant, atomicity, membership managment, scalability, consensus and coordination.

### What is a distributed commit? Mention the three protocols in distributed commit.:

Distributed commit is a commit that is ensured to have taken place on all relecant replicas. Two-phase, three-phase and paxos commit.

### Explain the protocols, one-phase commit protocol, two-phase commit protocol and three-phase commit protocol.:

1PC, single coordinator responsible for managing transaction. Coordinator sends a commit request to all participants. if all ack commit request, coordinator assumes that teh transaction is succsess and sends a global commit to all cohorts, if any cohorts fail to ack the commit request or if failure the transaction is aborted. 2PC: Prepare phase, commit or abort phase. Send prepare, cohorts reply with yes or no, (they do not commit yet), based on results from prepare phase cooridantor sends global commit to all cohorts to make them commit. If any cohort reply "no" a abort message is broadcasted to all cohorts. 3PC handles error from 2PC where coordinator crashes after prepare phase is done. Prepare, pre-commit, commit or abort. Adds the pre-commit phase where cohorts receive the intent to commit but do not commit yet. If the coordinator receives ack from all on intent message it commits and broadcasts.

### What is forward error recovery?:

Forwarding past the point of failure to a stable state again.

### What is backward error recovery?:

Rollbacking to a previous fail-free state with no issues.

### What is message logging?:

Logging of all messages sent and received (RPC)

### What is a distributed snapshot?:

Captures the entire distributed system at a particular moment, includes states of all processes the contents of communication channels and the states of shared resources. Used for tasks like debugging and monitoring to understand the system behaviour at a specific time.

### What is Independent checkpointing?:

Saving state to crash-tolerant hardware as checkpointing to revert to that point upon failure.

### What is an orphan process?:

A process with no "parent", process A sends request to B, then process A crashes, and eventually recovers, process A is then orphan.

## Chapter 9:

### How can one control access to an object? Describe the general model, as well as some approaches of implementing a reference monitor.:

Subjects, objects, Access control policies, Reference monitor. Mandatory access control, discretionary access control, role based access control, attribute based access control, rule based access control

### What are some approaches to protect against malicious code?:

Firewalls, antivirus, patch managment, user education, access control, sandboxing, file integrity monitoring, network segmentation, regular backups.

### The use of ACL or cryptography is fine when working with communicating parties which has the same rules. How can one protect resources wher communication is not just done in a isolated network?:

Federated identity and auth, multi-tenancy support, OAuth and API security, end-to-end encryption, ACLs with trust levels, zero trust security model.

### What are the three issues we need to worry about when a client retrieves an object based on some name? and how can secure naming be solved?:

Name resolution security, object auth, confidentiality and privacy, access controls, namespace identifiers, audit and monitoring, regular updates and patching, secure naming services.

### Describe the three main focus levels in computer security design.:

CIA: Integrity, availability, confidentiality.

### What is a systems trusted computing base?:

TCB all the set of security functionallity that creates a trusted system.

### Describe how a public-key cryptosystem can be used to ensure confidential group communication.:

Public key - same key for encryption/decryption. Comms are encrypted making for secure/confidential comms.

### Why are session keys used?:

For authentication, performance and security.

### What is Kerberos and how does it work?:

Auth protocol from MIT, prevents eavesdropping and replay attacks while ensuring strong authentication and confidentiality. Kerberos server (KDC-Key distribution center) -> authentication server(AS), initial auth, verifies the identity of users and issues temp auth credentials called Ticket Granting tickets (TGT's). Ticket granting server(TGS), TGS is responsible for granting access to specific services. Receives TGTs from clients and issues Service Tickets that grant access to specific services.

### How do firewalls work and what are the two main "levels" of a firewall?:

Whitelist and blacklist, allow all comms on whitelist deny if not. Blacklist = optimistic, allow all comms that is not on blacklist.

### What is a DDoS attack and how can it be prevented?:

Denial of service attack, overloading the system. Can be prevented by either scaling out elasticly or by ip-banning/timeout after certain amounts of request in a span of time.
