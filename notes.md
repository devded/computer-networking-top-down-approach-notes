# Chapter 1: Computer Networks and the Internet

## 1.1 A Nuts-and-Bolts Description (Infrastructure based Internet)

- The Internet connects billions of computing devices worldwide, including traditional computers, smartphones, and various nontraditional devices.
- The term "**hosts**" or "**end systems**" refers to all connected devices. Each End systems are interconnected by a network of communication links and packet switches.
- Packet switches, such as routers and link layer switches, forward packets to their destinations.
- The sequence of links and switches a packet traverses is called a **route** or **path** through the network.
- Packet switched networks are compared to transportation networks, with packets analogous to trucks and communication links to highways and roads.
- End systems access the Internet through various types of **Internet Service Providers (ISPs)**, including residential, corporate, university, WiFi, and cellular data ISPs.
- ISPs connect to content providers, and lower tier ISPs are interconnected through national and international upper tier ISPs.
- Internet protocols, such as TCP and IP, govern data transmission within the Internet, collectively known as TCP/IP.
Internet standards, developed by the ```Internet Engineering Task Force (IETF)``` and documented as requests for comments (**RFCs**), ensure interoperability.
- There are nearly 9000 RFCs defining various Internet protocols, and other bodies specify standards for network components, such as the **IEEE** 802 LAN Standards Committee for Ethernet and WiFi.

## 1.2 A Services Description (Service based Internet)

- The Internet can be viewed as an infrastructure that serves applications.
- Internet applications include various services like messaging, mapping, streaming, social media, etc.
- Internet applications are distributed and run on end systems, not within packet switches.
- To create an Internet application, you need to write programs for end systems.
- End systems use a **socket interface** to instruct the Internet to deliver data to other end systems. It has rules that must be followed.

> A socket interface that specifies how a program running on one end system asks the Internet infrastructure to deliver data to a specific destination program running on another end system.
    
> A protocol defines the format and the order of messages exchanged between two or more communicating entities, as well as the actions taken on the transmission and/or receipt of a message or other event.

## 1.3 The Network Edge

- End systems, which include computers, smartphones, and other devices, are found at the network edge.
- End systems are also known as hosts and run application programs.
- Hosts can be divided into clients (e.g., desktops, laptops, smartphones) and servers (more powerful machines).
- Servers store and distribute content, often in large data centers.
- Large companies like Google have multiple data centers worldwide with millions of servers.

## 1.4 Access Networks

> Access Network — the network that physically connects an end system to the first router (also known as the “edge router”) on a path from the end system to any other distant end system.

### 1.4.1 Home Access: DSL 

- The two most common broadband residential access types are **DSL** and **cable**.
- DSL is often provided by the local telephone company, acting as `both telco and ISP`.
- DSL connections involve DSL modems at homes communicating with a DSLAM at the telco's central office.
- DSL allows data and telephone signals to share the same line using frequency division multiplexing.
- Splitters at the customer's end and DSLAMs at the telco end manage signal separation.
- DSL offers varying transmission rates, both downstream and upstream, with the potential for high speed access.
- DSL access can be asymmetric, with different rates for downstream and upstream.
- Achievable rates may be lower due to distance, line quality, and provider limitations.
- DSL is best suited for short distances from the central office, typically within 5 to 10 miles.

<img src="https://lh3.googleusercontent.com/pw/AIL4fc8Mjg-m_XwafZaE4lRMp6fpu9DwIJgZkiExxghXGh9Qgxsim6HBe-fnkxqSo6HH8bP_kVqIlEti8LEkvk9E0hzqz0Z2aJ_SfQlOVK21jFqxO92JFJ_Iq5vBibrrl7OcXmegiq0N0dLzvQhKRgf0xcSt=w1920-h860-s-no" width="700" height="300">

### 1.4.2 Home Access: Cable 

- Cable Internet uses the existing cable TV infrastructure.
- Fiber optics connect the cable head end to neighborhood junctions, then coaxial cable reaches individual homes.
- Because both fiber and coaxial cable are employed in this system, it is often referred to as hybrid fiber coax (HFC).
- Cable Internet requires cable modems to connect to home PCs via Ethernet.
- The cable modem termination system (CMTS) turns analog signals from cable modems into digital format.
- Cable Internet has downstream and upstream channels; downstream typically has higher transmission rates.
- Cable Internet is a shared broadcast medium, leading to shared bandwidth.
- Simultaneous usage can reduce individual user rates, but Web surfing is less affected.
- The upstream channel is also shared, requiring a multiple access protocol to avoid collisions.

<img src="https://lh3.googleusercontent.com/pw/ADCreHfdQzhpcW3Nqdx6s9Q_Z5hjTLqeWEM9okcmdCuwfbBvUoPaEZ4n9cJw4rR8iMS4wxuMWCzvzSd_4JsilUCHJ906VUKs6ayT5EcW8mkt8PXaPpphzNAfghV24ssJjVHHY3DrBNzuB5XYRlWXl2JznOOK=w1920-h934-s-no" width="700" height="300">

### 1.4.3 Home Access: FTTH 

- Fiber to the home (FTTH) is a technology providing high speed residential broadband access via optical fiber.
- FTTH can offer gigabit per second internet speeds.
- Optical distribution networks for FTTH include direct fiber and shared fibers.
- Shared fiber networks use two architectures: **active optical networks (AON)** and **passive optical networks (PON)**.
- PON is used in Verizon's FiOS service and involves optical **network terminators (ONTs)** connected to a neighborhood splitter.
- The splitter combines multiple homes onto a shared optical fiber, which connects to an **optical line terminator (OLT)** in the central office.
- OLT connects to the internet via a telco router, and users connect their home routers to the ONT for internet access.
- In the PON architecture, all packets sent from OLT to the splitter are replicated at the splitter.


<img src="https://lh3.googleusercontent.com/pw/ADCreHfDt9ikXrQ0-2QZvqlKumBfhaRU9zh5meb36d0NOPJIinODENCl24OWvCxFxU_FUoMLI08IbvQ-Goz8aEDXwKgqzvfaXZiwa5biqMD0mD9Nhf7fprl9Gp3_emoohUaZmqKwOrufobgbJCbGEDJIJprt=w1808-h902-s-no" width="700" height="350">

### 1.4.4 Home Access: 5G Fixed Wireless

- 5G fixed wireless is an emerging technology for high speed residential access.
- It eliminates the need for **costly** and **unreliable cabling** from the telco's central office (CO) to homes.
- Data is sent wirelessly from a provider's base station to a modem in the home using beam forming technology.
- A WiFi wireless router is connected to the modem, similar to cable or DSL modem setups.

### 1.4.5 Enterprise & Home Access: Ethernet, WiFi

- Ethernet is the predominant LAN technology, using twisted pair copper wire with access speeds from 100 Mbps to tens of Gbps.
- Wireless LAN users connect to an access point, which is linked to the enterprise's network (usually via wired Ethernet).
- IEEE 802.11 (WiFi) is widely used for wireless LAN access with shared transmission rates exceeding 100 Mbps.
- Ethernet and WiFi are used not only in enterprise settings but also in home networks.
- Home networks often combine broadband residential access with wireless LAN technologies.

## 1.5 Physical Media

- Network access technologies in the Internet use various physical media, including fiber cable, coaxial cable, copper wire, and radio spectrum.

>  Physical media fall into two categories: guided media and unguided media. With guided media, the waves are guided along a solid medium, such as a fiber optic cable, a twisted pair copper wire, or a coaxial cable. With unguided media, the waves propagate in the atmosphere and in outer space, such as in a wireless LAN or a digital satellite channel.

- Installation labor costs for physical links can be significantly higher than material costs, motivating builders to install multiple types of media to save on future wiring expenses.
- **Twisted pair copper wire** is a common guided transmission medium, widely used in telephone networks and LANs. It consists of two insulated copper wires twisted together to **reduce interference**. Data rates for LANs range from 10 Mbps to 10 Gbps.
- Twisted pair technology, like category 6a cable, can achieve data rates of 10 Gbps for short distances, making it a dominant solution for high speed LAN networking.
- **Coaxial cable** consists of `two concentric copper conductors` and is commonly used in cable television systems. Coupled with cable modems, it provides high speed Internet access at rates of hundreds of Mbps.
- Coaxial cable can serve as a guided shared medium, allowing multiple end systems to connect directly to the cable and receive signals sent by other end systems.

> In cable television and cable Internet access, the transmitter shifts the digital signal to a specific frequency band, and the resulting analog signal is sent from the transmitter to one or more receivers.

- **Optical fibers** conduct light pulses as bits and offer high data rates, low attenuation, and resistance to interference.
- Fiber optics are ideal for long distance transmission but costly for short haul applications.

- **Terrsetial Radio channels** are wireless and versatile, influenced by propagation environment and distance.
- Three categories of terrestrial radio channels: `short range,` `local area`, and `wide area`.
- Radio channel characteristics include `path loss`, `shadow fading`, `multipath fading`, and `interference`.

- **Satellite communication** involves `geostationary` and `low earth orbiting (LEO)` satellites.
- Geostationary satellites stay fixed above one spot on Earth but introduce signal propagation delay.
- LEO satellites are closer to Earth, move in orbits, and may require multiple satellites for continuous coverage.
- Satellite links offer high speeds and serve areas without DSL or cable based Internet access.

## 1.6 Packet Switching (Store and forward Transmission)

- Most packet switches use **store and forward** transmission.
- Packet switch must receive the entire packet before transmission.

> Because the router employs store and forwarding, at this instant of time, the router cannot transmit the bits it has received; instead it must first buffer (i.e., “store”) the packet’s bits. Only after the router has received all of the packet’s bits can it begin to transmit (i.e., “forward”) the packet onto the outbound link

- `Delay = 2L/R` for a simple source destination network.
- General delay formula for N links each of rate R: `d = N * (L/R)`.

- **Queuing Delays and Packet Loss:** Packet switches have output buffers (output queues).
- Queuing delays occur when the link is busy.
- Packet loss can happen when the buffer is full due to congestion.

> If, during a short interval of time, the arrival rate of packets to the router (when converted to bits per second) exceeds 15 Mbps, congestion will occur at the router as packets queue in the link’s output buffer before being transmitted onto the link.

<img src="https://lh3.googleusercontent.com/pw/ADCreHfX55Xjkoab8kOtoXWB6Pz5F-CWrWrw5L4EFCw6OkzWdqMTgG54E0ZuEkveIh6dnKOvYNbfjwErwsKZvKgvWt-PqDh9Baiy-U_naufuJ4_MSsowqxExy_HUJVPfTrVjW2q_9N7vcgW3QgqDMD4RF2zK=w1806-h1130-s-no" width="700" height="400">

- **Forwarding Tables and Routing Protocols:** Routers use forwarding tables to determine outbound links.
- IP addresses are used for destination routing.
- Routers consult forwarding tables based on destination addresses.
- Internet uses routing protocols to configure forwarding tables automatically.

## 1.7 Circuit Switching

> In circuit switched networks, the resources needed along a path (buffers, link transmission rate) to provide for communication between the end systems are reserved for the duration of the communication session between the end systems.

- Circuit switched networks reserve resources (buffers, link transmission rate) for the entire communication session, while packet switched networks use resources on demand and may involve queuing.
- Traditional telephone networks are examples of circuit switched networks, where circuits are established and transmission rate is reserved for the entire connection.
- **Multiplexing in circuit switched networks** can use `frequency division multiplexing (FDM)` or `time division multiplexing (TDM)`.

<img src="https://lh3.googleusercontent.com/pw/ADCreHcnymJYAUF4Fn1TBsyIZwgZJ6JIBFewHZxR1y6w26eel_YuQjD32j5gqkJZ-NqMjqr32WXra6HCaP_Z9-HXc6oKcrzDifgPrrmuGzS7ec1I4rjT_R5SEviCfBTv0nLAHwlFcVUsi1hTgfto2b6-cU4q=w1482-h1088-s-no" width="600" height="400">

>  FDM, the frequency domain is segmented into four bands, each of bandwidth 4 kHz. For TDM, the time domain is segmented into frames, with four time slots in each frame.

- Packet switching is seen as more efficient because it doesn't reserve resources during idle periods, while circuit switching does.
- Packet switching allows better sharing of transmission capacity and is simpler and more cost effective than circuit switching.
- Packet switching allocates link use on demand, while circuit switching pre allocates link use regardless of demand.

## 1.8 Networks of Networks

- **Network Structures:** Various network structures are discussed, including global transit ISPs, regional ISPs, and tier 1 ISPs.
- **Peering:** ISPs can peer, enabling direct traffic exchange without payment. Tier 1 ISPs also peer.
- **IXPs:** Internet Exchange Points facilitate ISPs' direct connections, enhancing efficiency.
- **Content Provider Networks:** Large providers like Google create their networks for control and cost reduction.

<img src="https://lh3.googleusercontent.com/pw/ADCreHfe3VrXVOkt6FxFDHy4qRsByO6EugEHMcLkEvVuXtz2Bz3iZW28h32W2rJs7faFriHzgxJIfbOPV2Gd5L1_0e9PqKnc_pCtjmqNN0OxeH15auTYBd17kowR13spgnTFSgBjINghCV3Ew7gDsBC8lIh5=w1920-h926-s-no" width="600" height="300">

## 1.9 Delay, Loss, Throughput

<img src="https://lh3.googleusercontent.com/pw/ADCreHfL-nbDiTeiYVwKehMcZPCWS4vbdLyINcp3vKml8sDHzFSTYe1VwuexfmBm7WMuOcHHtZM3jBvRVSjVQPA5Nf3_UIDoQ0kpJrBEbwNwm-aBnnEFXz7mxgiKweHMy39iecCa53_7H2PxFA-5-pKN45Dq=w1920-h812-s-no" width="700" height="300">

- **Types of Delays:** Several types of delays affect packets during their journey, including nodal processing delay, queuing delay, transmission delay, and propagation delay.
- **Processing Delay:** Part of the processing delay includes examining the packet's header and checking for bit level errors. High speed routers have processing delays typically in microseconds.
- **Queuing Delay:** Queuing delay occurs as packets wait in a queue before being transmitted onto the link. It depends on the number of packets ahead in the queue and can range from microseconds to milliseconds.
- **Transmission Delay:** It is the time required to push all of a packet's bits into the link, determined by the packet's length and the transmission rate of the link. It is typically in microseconds to milliseconds.
- **Propagation Delay:** It is the time for a bit to propagate from one router to the next, dependent on the distance between routers and the propagation speed of the link. It can be in milliseconds for wide area networks.
- **Comparing Transmission and Propagation Delay:** Transmission delay is about pushing out the packet, while propagation delay is about bit propagation. They can be thought of as the time it takes for a caravan of cars to travel between tollbooths on a highway.
- **Traffic Intensity:** The traffic intensity (La/R) plays a vital role in estimating queuing delay. If it exceeds 1, queuing delay can approach infinity. It varies based on the rate of packet arrivals and the transmission rate.

<img src="https://lh3.googleusercontent.com/pw/ADCreHd2b-31EKHc-W0Ah_HtMogmvFSs7LCK5p-2s6gK7o4h2dv7yao9fDUTvge6xrDnoPiVzIlly5XMmSi-l-sLOQST4M6NFGPxk7GSChBXEqVrqqEJD_ZESJ2vL-SSSzsXRw8dMtxXjAUJUIHuei8cA2j7=w1092-h888-s-no" width="600" height="400">

> **Trace Route**: measure end to end delay in a computer network by tracing the route taken by packets and measuring round-trip delays to routers.

> If the source receives fewer than three messages from any given router (due to packet loss in the network), Traceroute places an asterisk just after the router number and reports fewer than three round trip times for that router.

## 1.10 Throughput

> If the file consists of F bits and the transfer takes T seconds for Host B to receive all F bits, then the average throughput of the file transfer is F/T bits/sec.

- **Instantaneous vs. Average Throughput**: It explains the difference between instantaneous throughput (bits/sec at a given moment) and average throughput (bits/sec over the entire transfer).
- **Two Link Network**: In a simple network with two links, the throughput is determined by the slower link, which acts as the **bottleneck**. `min{Rc, Rs}`
- **Multiple Links**: In a network with multiple links between source and destination, the throughput is limited by the slowest link along the path.
- **Access Network**: In today's Internet, the access network is often the bottleneck for throughput due to over provisioned core network links.
- **Intervening Traffic**: Throughput can be affected by other data flows sharing the same link, even if the link has a high transmission rate.
- **General Dependence**: Throughput depends not only on link transmission rates but also on intervening traffic, making it a more complex concept.

## 1.11 Protocol Layers

- **Protocol Layering**: Network protocols are organized into layers, with each layer providing specific services and using services from the layer below. This structure helps in the design and modularity of network protocols.
- **Implementation of Layers**: Protocols can be implemented in software, hardware, or a combination of both. Application and transport layer protocols are typically implemented in software, while physical and data link layers are often implemented in hardware.
- **Advantages of Layering**: Protocol layering offers modularity, making it easier to update components. It provides a structured way to discuss system components.
- **Drawbacks of Layering**: Some argue against layering due to potential duplication of functionality and information dependencies between layers.
- **Protocol Stack**: The protocols of different layers collectively form the protocol stack. The Internet protocol stack consists of five layers: physical, link, network, transport, and application layers.
- **Encapsulation**: Data is encapsulated as it moves down the protocol stack. Each layer adds its header information to the data received from the layer above, creating a packet with header fields and a payload field.

## 1.12 Networks Under Attack

- **Malware Consequences:** Malware can have severe consequences, including file deletion, data theft (e.g., passwords and personal information), and turning compromised hosts into part of botnets used for malicious purposes.
- **Self Replicating Malware:** Many malware types are self replicating, meaning they can infect one host and then spread to other hosts over the Internet, leading to exponential growth in infections.
- **Types of DoS Attacks:** DoS attacks can be categorized into three types: `vulnerability attacks`, `bandwidth flooding`, and `connection flooding`. These attacks disrupt services or crash hosts.
- **Distributed DoS (DDoS) Attacks**: In a DDoS attack, attackers control multiple sources to launch attacks, making them harder to detect and defend against.
- **Cryptography Defense**: Cryptography is one of the defenses against packet sniffing. It can help secure communication channels and protect against eavesdropping.
- **IP Spoofing**: Attackers can forge source addresses on packets, allowing them to masquerade as someone else. This is known as IP spoofing and presents a security challenge.
- **End Point Authentication**: To address IP spoofing and ensure message authenticity, end point authentication mechanisms are needed. These mechanisms verify the source of messages.

# Chapter 2: Application Layer

## 2.1 Principle of Network Applications

- **Client-Server Architecture**: In a client server architecture, there is a dedicated server that services requests from multiple client hosts. Clients do not directly communicate with each other but interact with the server. The server has a fixed, well-known IP address. Examples include the Web, FTP, Telnet, and email.
- **Peer-to-Peer (P2P) Architecture**: In a P2P architecture, there is minimal reliance on dedicated servers in data centers. Peers, which are intermittently connected hosts, communicate directly with each other without a dedicated server intermediary.
- **P2P Scalability**: P2P architectures offer self scalability, with peers contributing service capacity by distributing files to other peers. They are cost effective and do not require significant server infrastructure.
- **Challenges of P2P Architectures**: P2P applications face challenges related to security, performance, and reliability due to their highly decentralized structure.
- **Communication Between Processes**: Processes running on different end systems communicate with each other by exchanging messages across the computer network.
- **Socket**: Messages sent between processes must pass through the network using a software interface called a `socket`. A socket is analogous to a door through which a process sends and receives messages.
- **Socket Communication**: Sockets serve as the interface between the application layer and the transport layer within a host. They are the `Application Programming Interface (API)` for building network applications.

<img src="https://lh3.googleusercontent.com/pw/ADCreHfjdzN47NUqgVF6Leej5qKJLDdzI8ZtOIy4Gbq0EoANrQ8oLeWTBbPJ8_oCehHJG19bSWgldXa86Lw0hEMNjGrGleqJBJijilrs61lEfjnfH26Fy_3VD2Qe_voulh7kOk_Q0Fk0nfvo490o_3tOK-zZ=w1920-h940-s-no" width="680" height="350">

- **Addressing Processes**: To send messages between processes, the receiving process's address needs to be specified. This includes the host's IP address and a destination port number. The IP address identifies the host, while the port number identifies the specific receiving process.
- **Port Numbers**: Popular applications are assigned specific port numbers (e.g., Web server on port 80, mail server on port 25)

## 2.2 Transport Services (TCP & UDP)

- **Choosing a Transport Layer Protocol**: When developing an application, you must choose a transport layer protocol that suits your application's needs. The choice is typically based on services such as reliable data transfer, throughput, timing, and security.
- **Reliable Data Transfer**: Reliable data transfer ensures that data sent by one end is delivered correctly and completely to the other end. Some applications require this service to prevent data loss, while others like multimedia apps can tolerate some loss.
- **Throughput**: Throughput is the rate at which bits are delivered from the sender to the receiver in a communication session. Bandwidth sensitive applications need guaranteed throughput.
- **Timing**: Timing guarantees are essential for real time applications like Internet telephony, teleconferencing, and multiplayer games. Low delay is crucial for their effectiveness.
- **Security**: Transport protocols can provide security services like encryption for confidentiality, data integrity, and end-point authentication.
- **UDP and TCP**: The Internet offers two transport layer protocols: UDP and TCP. UDP is lightweight and provides unreliable data transfer, while TCP offers reliable data transfer and connection oriented services.
- **Services Not Provided**: Neither UDP nor TCP provide throughput or timing guarantees, which means the Internet cannot guarantee specific timing or throughput for time sensitive applications.

> the Internet community has developed an enhancement for TCP, called Transport Layer Security (TLS) [RFC 5246]. TCP enhanced with TLS not only does everything that traditional TCP does but also provides critical process to process security services, including encryption, data integrity, and end point authentication.

> In particular, if an application wants to use the services of TLS, it needs to include TLS code (existing, highly optimized libraries and classes) in both the client and server sides of the application. TLS has its own socket API that is similar to the traditional TCP socket API. 

## 2.3 Application Layer Protocol: Web and HTTP

- **HTTP**: `HTTP (HyperText Transfer Protocol)` is the primary application layer protocol of the World Wide Web. It relies on client and server programs that communicate by exchanging HTTP messages. Web pages are composed of objects, which are individual files with unique URLs.
- **Web Page Structure**: A web page typically includes a base HTML file and referenced objects like images, stylesheets, and videos. Objects are identified by URLs, which consist of a `hostname` and a `path name`.
- **HTTP and TCP**: HTTP uses TCP (Transmission Control Protocol) as its underlying transport protocol. Clients initiate TCP connections with servers to exchange HTTP messages.

> The HTTP client first initiates a TCP connection with the server. Once the connection is established, the browser and the server processes access TCP through their socket interfaces. 

> HTTP need not worry about lost data or the details of how TCP recovers from loss or reordering of data within the network. 

- **Stateless Protocol**: HTTP is a stateless protocol, meaning servers `don't store client specific information.` If a client requests the same object multiple times, the server doesn't remember previous requests.
- **HTTP Versions**: `HTTP/1.0` and `HTTP/1.1` are common versions, with HTTP/1.1 supporting persistent connections. Newer versions like HTTP/2 are also emerging.
### 2.3.1 Non Persistent and Persistent Connections 
- Non persistent connections create a new connection for each requested object. Persistent connections allow multiple objects to be sent over the same connection, improving efficiency.

> Although HTTP uses persistent connections in its default mode, HTTP clients and servers can be configured to use non persistent connections instead.

> round trip time (RTT), which is the time it takes for a small packet to travel from client to server and then back to the client. The RTT includes packet propagation delays, packet queuing delays in intermediate routers and switches, and packet processing delays.

<img src="https://lh3.googleusercontent.com/pw/ADCreHcP6O3E33NG7QnDmzX1ZUYsYN4WdmaGZSwLxO79aCwgpc2VRQI5lV8oSDjGyga6BN6nbLTnXzZnfZe49s3o9JvbZT35Z1vqiUG1c97LMJbYwZwMhTgBitpNwl5znilEEFnGID7QpG4z98mGuwdk6xPg=w1456-h1130-s-no" width="520" height="520">

- The three way handshake involves the client and server exchanging messages, taking one round trip time (RTT) for this process.
- After completing the handshake, the client sends an HTTP request message along with an acknowledgment into the TCP connection.
- The server responds by sending the HTML file over the established connection.
- The total response time is approximately two RTTs plus the transmission time for the HTML file.

### 2.3.2 HTTP Message Format: 

- HTTP messages have two types: `request messages` and `response messages`. Request messages include a method (e.g., GET), URL, and HTTP version, followed by header lines. Response messages include a `protocol version`, `status code` (e.g., 200 OK), and `header lines`, followed by the `entity body`. [Click here for more info](https://github.com/VasanthVanan/web-application-hackers-handbook-notes/blob/main/Chapters/Chapter-3%20Web%20Application%20Technologies.md#311-http-requests)

```http
GET /somedir/page.html HTTP/1.1 \r\n
Host: www.someschool.edu \r\n
Connection: close \r\n
User-agent: Mozilla/5.0 Accept-language: fr \r\n
```

```http
HTTP/1.1 200 OK \r\n
Connection: close \r\n
Date: Tue, 18 Aug 2015 15:44:04 GMT \r\n
Server: Apache/2.2.3 (CentOS) \r\n
Last-Modified: Tue, 18 Aug 2015 15:11:03 GMT \r\n
Content-Length: 6821 \r\n
Content-Type: text/html \r\n
\r\n

(data data data data data ...)
```

- **Header Lines**: Header lines provide additional information in HTTP messages. Examples of request headers include `Host`, `Connection`, `User-agent`, and `Accept-language`. Examples of response headers include `Connection`, `Date`, `Server`, `Last-Modified`, `Content-Length`, and `Content-Type`.
- **Status Codes**: Status codes (e.g., 404 Not Found) indicate the result of an HTTP request. [Click here for more info](https://github.com/VasanthVanan/web-application-hackers-handbook-notes/blob/main/Chapters/Chapter-3%20Web%20Application%20Technologies.md#318-status-codes)
- **HTTP Methods**: HTTP includes methods like GET, POST, PUT, and DELETE for different types of requests and actions.
- **Entity Body**: The entity body in HTTP messages contains data related to the request method.

### 2.3.3 Cookies

- There are situations where web sites need to identify users, for security or personalization purposes. HTTP uses cookies to achieve user identification and tracking.
- Cookies have four components: a `cookie header` in HTTP `response` and `request` messages, a `cookie file` on the user's end system, and a `back end database` on the web site.

<img src="https://lh3.googleusercontent.com/pw/ADCreHfFwZxxD_q6lNIW4MotRBCCUUmdnTTAst3aa9ByyF1GoQxQGr9oMpd-3hudmL_VvIqWZhb9sF4Dsw3YYeV3N38qe-HBB9afByGpuvPj1gSfGeATqwiuckHdhRVluCOM_E_NXmqLYBN82wpku2x_BUd1=w1326-h1130-s-no" width="620" height="630">

- Cookies work by sending a unique identification number in a `Set-cookie` header from the server to the user's browser.
- The browser stores the identification number and sends it back to the server in a Cookie header with subsequent requests.
- Cookies are used to track user activity and offer personalized services, like shopping carts or recommendations.
- Users can be identified over multiple sessions by maintaining the same identification number in cookies.
- Cookies are controversial due to potential privacy concerns, as websites can gather and potentially sell user information.

### 2.3.4 Web Caching

- Web caches, or proxy servers, handle HTTP requests on behalf of origin servers.
- Caches store copies of requested objects, reducing the need to fetch them from the origin server.
- Users can configure browsers to direct requests through caches for faster responses.
- Caches serve as both servers (to clients) and clients (to servers) in the caching process.
- Installed by ISPs and institutions, caches enhance performance and lower bandwidth costs.
- Benefits include faster responses, reduced bandwidth upgrades, and decreased overall Internet traffic.
- Content Distribution Networks (CDNs) use distributed caching to localize content delivery.

> An HTTP request message is a so called conditional GET message if (1) the request message uses the GET method and (2) the request message includes an If-Modified-Since: header line.

- `Conditional GET` checks for freshness by comparing the `If-Modified-Since` header with object modification date.
- If an object hasn't changed, a `304 Not Modified response` allows the cache to serve the locally cached object.

> value of the If-modified-since: header line is exactly equal to the value of the Last-Modified: header line that was sent by the server initially.

### 2.3.5 HTTP/2

> The primary goals for HTTP/2 are to reduce perceived latency by enabling request and response multiplexing over a single TCP connection, provide request prioritization and server push, and provide efficient compression of HTTP header fields.

- **HTTP/2 Motivation:** HTTP/1.1's persistent TCP connections caused HOL blocking. Browsers used multiple parallel TCP connections to work around this issue.

> Head of Line (HOL) blocking: occurs when a web page has a large video clip and numerous small objects. With a slow bottleneck link, the video clip causes delays for small objects queued behind it. 

- **HTTP/2 Solution (Framing):** Reduces the need for parallel TCP connections by breaking messages into frames and interleaving them, significantly reducing user perceived delay. Includes binary frame encoding for efficiency.

> The ability to break down an HTTP message into independent frames, inter leave them, and then reassemble them on the other end is the single most important enhancement of HTTP/2.

- **Message Prioritization:** Developers assign weights (1-256) to messages, and the server prioritizes higher weight responses. Clients can specify message dependencies.
- **Server Push:** Enables sending additional objects to the client without explicit requests, reducing latency.
- **HTTP/3 and QUIC:** QUIC, a new transport protocol over UDP and supports features like message multiplexing, is used for HTTP/3. This streamlined design incorporates HTTP/2 features and leverages QUIC's advantages.

## 2.4 Application Layer Protocol: SMTP

> A typical message starts its journey in the sender’s user agent, then travels to the sender’s mail server, and then travels to the recipient’s mail server, where it is deposited in the recipient’s mailbox. Reattempts are often done every 30 minutes

### 2.4.1 Email Components

- **User Agents:** Tools like Microsoft Outlook, Apple Mail, and Gmail, allowing users to manage emails.
- **Mail Servers:** The central infrastructure, hosting mailboxes for recipients like Bob.
- **SMTP (Simple Mail Transfer Protocol):** The principal protocol to send emails between servers.

### 2.4.2 SMTP Basics

- SMTP transfers messages between sender and recipient mail servers at `Port 25`.
- The client (sender's server) initiates a connection to the recipient's server via TCP.

```http
S: 220 hamburger.edu 
C: HELO crepes.fr
S: 250 Hello crepes.fr, pleased to meet you 
C: MAIL FROM: <alice@crepes.fr>
S: 250 alice@crepes.fr ... Sender ok
C: RCPT TO: <bob@hamburger.edu>
S: 250 bob@hamburger.edu ... Recipient ok
C: DATA
S: 354 Enter mail, end with ”.” on a line by itself 
C: Do you like ketchup?
C: How about pickles?
C: .
S: 250 Message accepted for delivery
C: QUIT
S: 221 hamburger.edu closing connection
```

- It introduces the sender and recipient, transmits the message, and uses a persistent connection for multiple messages.

### 2.4.3 Mail Message Structure

- Email messages consist of a `header` and a `body`.
- The header includes sender and recipient information, such as `"From," "To," and "Subject."`. The header lines and the body of the message are separated by a blank line (that is, by CRLF).
- These headers are distinct from SMTP commands used for server handshake communication.

```http
From: alice@crepes.fr
To: bob@hamburger.edu
Subject: Searching for the meaning of life.
```

### 2.4.4 Mail Access Protocols

<img src="https://lh3.googleusercontent.com/pw/ADCreHe0fyv4ULp_uamEsceCVVhVIa89gH-EYeg8F5QQ9MJOB6_HPfvS8QpwFXnBbpd_o5WBJf3SYSGt_KwkgMRBQ0BUtFHZP6lTTLAvPlWIfoypiutfj2fm5ZktaSNOuMKNcfdEXXH7OafVuFbqC-vIcfa4=w1876-h442-s-no" width="680" height="220">

> Bob’s user agent can’t use SMTP to obtain the messages because obtaining the messages is a pull operation, whereas SMTP is a push protocol.

- Users retrieve their email messages from a shared mail server using either HTTP or IMAP.
- HTTP is often used for web based email clients like Gmail, while IMAP is common with clients like Microsoft Outlook.
- Both the HTTP & IMAP approaches allow to manage folders, move messages to folders, delete messages, mark messages as important, and so on.

## 2.5 Application Layer Protocol: DNS

- DNS is an essential service that translates human friendly hostnames into IP addresses.
- It's a distributed database and an application layer protocol, implemented with `DNS servers`, often running `BIND` software and runs over UDP and uses port 53.

> People prefer the more mnemonic hostname identifier, while routers prefer fixed length, hierarchically structured IP addresses.

- DNS services include:
    - **hostname aliasing**: host with a complicated canonical hostname can have one or more alias names.
        ```http
        relay1.west-coast.enterprise.com (canonical/official website name)
        enterprise.com (alias name)
        ```
    - **Mail Server Aliasing**: DNS resolves alias hostnames to canonical forms for mail servers and retrieves corresponding IP addresses.
        ```http
        bob@yahoo.com --> bob@relay1.west-coast.yahoo.com
        ```
    - **Load Distribution**: DNS balances traffic among replicated servers by rotating IP addresses within replies, ensuring even distribution. This technique is also applied to email servers with shared alias names.

### 2.5.1 How DNS Works: High Level Overview

> gethostbyname() is the function call that an application calls in order to perform the translation.

- DNS operates through query and reply messages using UDP datagrams on port 53.
- DNS queries involve multiple servers globally distributed.
- A simple centralized design for DNS is not feasible due to scalability issues.
- Issues with centralized design: `single point of failure,` `high traffic volume`, `distant database`, and `maintenance`.
- DNS uses a hierarchical structure and a distributed database., to handle the vast number of hosts on the Internet.

### 2.5.2 Distributed, Hierarchical Database


<img src="https://lh3.googleusercontent.com/pw/ADCreHfjtoFE2ozufMyfFi_xvvvjhwhvWHxaFcgn2jVCEG50nQsaQlTqhQQovC1HaJrlB0h8La--jGtCdoz8c6RxZVLsou9ISfsTEy7uaS-fjCMZNBiZtfTPnFpbVbYUDbQ49wyFPKQJJNUc-_7h4wmYm2IX=w1920-h710-s-no" width="580" height="220">

- DNS uses three classes of servers: `Root` DNS servers, `top level domain (TLD)` DNS servers, and `authoritative` DNS servers.
- Root DNS servers provide IP addresses for TLD servers. TLD servers provide IP addresses for authoritative DNS servers Authoritative DNS servers store DNS records for specific organizations.
- A `local DNS server`, specific to an ISP, also plays a crucial role in DNS queries. It cache DNS information to reduce query traffic and improve performance.

> When a host makes a DNS query, the query is sent to the local DNS server, which acts a proxy, forwarding the query into the DNS server hierarchy.

- DNS extensively utilizes caching to enhance performance. These are stored temporarily and it allows DNS servers to quickly respond to subsequent queries for the same hostname.

### 2.5.3 Recursive vs Iterative DNS Queries

<img src="https://lh3.googleusercontent.com/pw/ADCreHcDzbK4FY8RExEyQO82XsXu_OFQXOqMXfJx6q8TO_Tx4wYRJt9WaiktQr-4bF482giEXJmGfkLMszdS7Ufn_sjYphuuVOdpKVn7RI6laoHLFKiPUtFpU_kOUnZ_UJN7NjeJdt5Bp65KPlNKkiEpFrIF=w1708-h1044-s-no" width="780" height="520">

### 2.5.4 DNS Records & Messages

- DNS servers store resource records (RRs) in the distributed database.
- A resource record (RR) is a four tuple: `(Name, Value, Type, TTL)`.
- **TTL** (Time to Live) determines when a resource should be removed from a cache.
- Types of resource records:
    - `Type=A`: Maps hostname to IP address.
    - `Type=NS`: Maps a domain to the hostname of an authoritative DNS server.
    - `Type=CNAME`: Provides the canonical name for an alias hostname.
    - `Type=MX`: Maps to the canonical name of a mail server with an alias hostname.

> To obtain the canonical name for the mail server, a DNS client would query for an MX record; to obtain the canonical name for the other server, the DNS client would query for the CNAME record.

- DNS messages have a header section with several fields, including `query/reply` flags, `recursion` flags, and more.
- DNS messages consist of a question section, answer section (resource records), authority section, and additional section.

> A 1 bit query/reply flag indicates whether the message is a query (0) or a reply (1). A 1 bit authoritative flag is set in a reply message when a DNS server is an authoritative server for a queried name. 

> A 1 bit recursion desired flag is set when a client (host or DNS server) desires that the DNS server perform recursion when it doesn’t have the record. 

> A 1 bit recursion available field is set in a reply if the DNS server supports recursion. 

### 2.5.5 Inserting Records to DNS Database

> A registrar is a commercial entity that verifies the uniqueness of the domain name, enters the domain name into the DNS database (as discussed below), and collects a small fee from you for its services.

- To register a domain name, you need to provide registrar with DNS server names and IP addresses. Registrar enters `Type NS` and `Type A` resource records for `authoritative` DNS servers into `TLD` servers.
- Additional resource records, like Type A and Type MX, must be added for Web and mail servers.

# Chapter 3: Transport Layer


> transport layer -- extending the network layer’s delivery service between two end systems to a delivery service between two application layer processes running on the end systems.


## 3.1 Transport-Layer Services

- The transport layer resides between the application and network layers, providing communication services to application processes on different hosts.
- Transport layer protocols enable `logical communication` between application processes on different hosts, abstracting the physical infrastructure.
- It converts application messages into transport layer `segments`, encapsulated within network layer packets (datagrams) for transmission.
- Transport protocols work only within end systems and are not involved in routing or network core activities.
- These protocol provides communication between application **processes**, while network layer protocol provides communication between **hosts**.

-  IP makes its “best effort” to deliver segments between communicating hosts, but it makes no guarantees. (IP is said to be an unreliable service)

> The most fundamental responsibility of UDP and TCP is to extend IP’s delivery service between two end systems to a delivery service between two processes running on the end systems. Extending host-to-host delivery to process-to-process delivery is called transport layer multiplexing and demultiplexing.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### Best way to remember TCP vs UDP
- Imagine two cars, each with a bouncing ball inside, driving down a slope. These cars handle the bouncing ball differently in two scenarios:
#### Scenario 1: Car A – Cautious Approach
- Car A is equipped with a protective shield to prevent the ball from bouncing out. The driver is extremely cautious and stops the car every time the ball moves to ensure it remains in the correct spot.
> **Result**: Car A successfully reaches the bottom of the slope with the ball intact. However, the journey is slower because of frequent stops to check on the ball.

#### Scenario 2: Car B – Reckless Approach
- Car B lacks a protective shield and drives down the same slope at high speed. The driver is reckless and doesn’t stop to check on the ball’s position, allowing it to bounce freely and even risk flying out of the car.
> **Result**: Car B reaches the bottom of the slope faster than Car A. Unfortunately, the ball gets lost along the way.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

- Key Differences in UDP vs TCP Protocols:

| Aspect                      | UDP (User Datagram Protocol)        | TCP (Transmission Control Protocol)      |
|-----------------------------|----------------------------------|-----------------------------------------|
| Service Model               | Unreliable and connectionless    | Reliable and connection-oriented         |
| Application Selection       | Chosen by the application developer | Chosen by the application developer    |
| Terminology                | Uses "datagram" for segments     | Uses "segment" for segments             |
| Network Layer Protocol     | Operates on top of IP (Internet Protocol) | Operates on top of IP (Internet Protocol) |
| Services Provided          | Process to process data delivery and error checking | Reliable data transfer, flow control, sequence numbers, acknowledgments, timers, and congestion control |
| Reliability                 | Unreliable - Does not guarantee data integrity or delivery | Reliable - Ensures data delivery, integrity, and order |
| Congestion Control         | Unregulated - No congestion control | Regulated - Prevents excessive traffic and aims for fair sharing of network resources |
| Complexity                  | Simpler and less complex         | Complex due to additional services and mechanisms |

## 3.2 Multiplexing and Demultiplexing

- **Objective**: Extend host-to-host delivery to process-to-process delivery for applications.

### Demultiplexing

- Transport layer delivers data to an intermediary socket, not directly to a process.
- Each socket has a unique identifier. Fields in a transport layer segment are used to identify these receiving socket.
- Demultiplexing directs the segment to the corresponding socket, ensuring data is delivered to the correct process.
- In the household analogy, this is similar to handing out mail to the right person based on the address.

### Multiplexing

- Multiplexing involves gathering data from different sockets, encapsulating it with header information to create segments, and passing the segments to the network layer.
- The transport layer in intermediate hosts performs both demultiplexing and multiplexing.
- Sockets have unique identifiers. Special fields in segments identify the socket for delivery.
- These fields include `source port number` and `destination port number`.
- Port numbers are 16 bit numbers, ranging from 0 to 65535. The well known port numbers (0 to 1023) are reserved for established application protocols.


## 3.3 Connectionless Multiplexing and Demultiplexing

- UDP sockets are automatically assigned port numbers in the range 1024 to 65535.
- Servers typically assign specific port numbers, while clients often let the transport layer assign them.
- Alternatively, a specific port number can be associated with a UDP socket using the `bind()` method.

```python
clientSocket = socket(AF_INET, SOCK_DGRAM)
clientSocket.bind((’’, 19157))
```

- UDP segments have source and destination port numbers for identification.
- A socket is fully identified by a `destination IP address` and a `destination port number`.
- Segments are directed to the corresponding socket based on the destination port number.
- If different segments have the same destination IP and destination port numbers, they go to the same destination process.
- The source port number in a UDP segment serves as part of the **"return address"**. It allows the recipient to send a response back to the sender.


> A-to-B segment the source port number serves as part of a “return address”—when B wants to send a segment back to A, the destination port in the B-to-A segment will take its value from the source port value of the A-to-B segment. 


## 3.4 Connection Oriented Multiplexing and Demultiplexing

- TCP sockets are identified by a four tuple: (source IP address, source port number, destination IP address, destination port number).
- A connection establishment request includes destination and source port numbers.
- Host operating systems use these values to locate the server process waiting for connections.
- Server and client sockets are established and identified with four tuple values.
- All subsequent segments are demultiplexed based on these four values to the correct socket.

<img src="https://lh3.googleusercontent.com/pw/ADCreHcmMPDSQ4fOctkpXLDYANE30KxCaIIeiv4cNkwy7qP5yrIkfrHwx0vMaMeRo7aSooqns-GiXxoULVwt7bLenIiyAi49A2ZMf4zAg82q2jzIWVFuD6Sx19TF--PFa21b_2xfQVsyIR7oNZDQWG4Vv5S_=w1920-h1060-s-no" width="580" height="350">

- Web servers may have multiple processes or threads to handle connections.
- Each process or thread has its connection socket for receiving HTTP requests and sending responses.
- High performing servers typically use one process and multiple threads or lightweight subprocesses.
- One process can have many connection sockets, each with different identifiers.

### Persistent vs. Non Persistent HTTP

- Persistent HTTP exchanges messages over the same server socket during a connection.
- Non persistent HTTP creates and closes a new TCP connection and socket for every request/response.
- Frequent socket creation and closure can impact the performance of busy Web servers.

## 3.5 UDP (User Datagram Protocol)

- UDP is a minimalistic transport protocol. It provides `multiplexing`/`demultiplexing` and minimal `error checking`. Unlike TCP, it adds very little to IP.

> If the application developer chooses UDP instead of TCP, then the application is almost directly talking with IP layer. UDP takes messages from the application process, attaches source and destination port number fields for the multiplexing/demultiplexing service, adds two other small fields, and passes the resulting segment to the network layer. 

- `Connectionless`: No handshaking between sender and receiver. Often used for `real time`, `low delay`, and `low overhead` applications.
- Some applications are better suited for UDP
  - Allows `finer control over data sent and timing`.
  - `No connection establishment`, minimizing delays.
  - `No connection state,` supporting more active clients.
  - `Small packet header` overhead (UDP's 8 bytes vs. TCP's 20 bytes).  
- Reliability can be added to applications using UDP like QUIC protocol, but it's nontrivial. It can be built directly into the application.
- Allows reliable communication without TCP's congestion control limitations.
- Key fields in the UDP header:
  - `Port numbers`: For demultiplexing.
  - `Length`: Specifies the segment length (header + data).
  - `Checksum`: Used for error detection.
- Checks for alterations during data transmission.

    <img src="https://lh3.googleusercontent.com/pw/ADCreHccqsKMoJTpHKrpeBpWY5ePn7ro94y-9gTfw5NPXZ4IInxs2ZdGrHqi441xgHndC9vwiDPl3x3As6aVZTs6GQWNAMmBZTMwvHlIoT1R3MRvymYK7XqkB1O-OEWd8JhmP4Cm_f_nrzKGJwPARpdRqcQ=w1316-h1088-s-no" width="450" height="350">

> UDP at the sender side performs the 1s complement of the sum of all the 16 bit words in the segment, with any overflow encountered during the sum being wrapped around.

<img src="https://lh3.googleusercontent.com/pw/ADCreHd6aGmd6Jk9aEfaOuteJHdj1V8Tl3M-w_eAdWjDwwqOUuDR8hobSh1fjb2PyblDTqlzm8bLz72502F7YGVJF2x5nirudlaEPwHHrIdqbkWzDpvPUb6K3jccQN5bxYKKsbptwUDTjAnvI0uhICFYGpRv=w1286-h1130-s-no" width="550" height="500">

- Thus, the 1s complement of the sum `0100101011000010` is `1011010100111101`,

> At Receiver, all the four 16 bits (3 + checksum) are added, If no errors are introduced into the packet, then clearly the sum at the receiver will be 1111111111111111. If one of the bits is a 0, then we know that errors have been introduced into the packet.

> It is useful for the transport layer to provide error checking as a safety measure. Although UDP provides error checking, it does not do anything to recover from an error. Some implementations of UDP simply discard the damaged segment; others pass the damaged segment to the application with a warning.

## 3.6 Building Reliable Data Transfer Portocol

### 3.6.1 RDT 1.0:
- **Basic Version:** RDT 1.0 is the most basic version of the Reliable Data Transfer protocol.
- **Key Characteristics:**
  - Sender sends data to the receiver.
  - Receiver simply accepts the data without providing feedback. (unidirectional communication)
  - Assumes a perfectly reliable channel where data is never lost or corrupted.
  - No error detection or correction mechanisms in place.

### 3.6.2 RDT 2.0:
- **Enhanced Reliability:** RDT 2.0 is an enhanced version of the RDT 1.0 protocol.
- **Key Characteristics:**
  - Introduces a basic acknowledgment mechanism.
  - Sender sends data and waits for an `acknowledgment` (`ACK` / `NAK`) from the receiver.
  - Receiver sends an ACK to confirm successful data reception.
  - If ACK is not received, sender retransmits the data.
  - Addresses the issue of lost or corrupted data and ensures basic reliability.

  > The message dictation protocol uses both positive acknowledgments (“OK”) and negative acknowledgments (“Please repeat that.”). These control messages allow the receiver to let the sender know what has been received correctly, and what has been received in error and thus requires repeating. It is known as `ARQ (Automatic Repeat reQuest)` protocols.

  > when the sender is in the wait for ACK or NAK state, it cannot get more data from the upper layer; that will happen only after the sender receives an ACK and leaves this state. This is known as `Stop and Wait` protocol.

### 3.6.3 RDT 2.1:
- **Extended Reliability:** RDT 2.1 further improves upon reliability.
- **Key Characteristics:**
  - Adds a `sequence number` to each frame sent by the sender.
  - Receiver identifies duplicate frames and discards them.
  - If the receiver receives a frame with the wrong sequence number, it discards it.
  - This prevents duplicate frames from being delivered and enhances reliability.

### 3.6.4 RDT 3.0:
- **Enhanced Error Handling:** RDT 3.0 focuses on error handling and retransmission.
- **Key Characteristics:**
  - Similar to RDT 2.1, it uses sequence numbers to handle duplicate frames.
  - Introduces a `timeout mechanism`.
  - If the receiver doesn't receive an expected frame within a certain time (timeout), it requests retransmission.
  - Sender retransmits the missing frame.
  - Adds the ability to recover from lost frames more efficiently.
  - RDT 3.0 is a functionally correct protocol but has performance limitations due to its stop and wait behavior.

- **Performance Example:**
  - Consider two hosts on the opposite coasts of the United States with a round trip propagation delay (RTT) of 30 milliseconds.
  - The transmission rate (R) is 1 Gbps, and the packet size (L) is 1,000 bytes.
  - The time needed to transmit a packet into the link is 8 microseconds (dtrans).
  - In a stop and wait scenario, the sender utilizes the channel very inefficiently.
  - Only 0.00027 of the sender's time is spent sending data into the channel, resulting in a low effective throughput, even on a high capacity link.

- **Introducing Pipelining:**
  - The stop and wait protocol's performance is poor due to its sender utilization. It can severely limit the capabilities of high-capacity network links.
  - The sender can improve utilization by transmitting multiple packets before waiting for acknowledgments (`pipelining`).
  - This allows for a more efficient use of the channel and effectively increases sender utilization.
  - Introducing pipelining requires several changes:
    - Expanding the `range of sequence numbers` to account for multiple in transit packets.
    - Both sender and receiver may need to `buffer multiple packets`.
  - Two basic approaches for pipelined error recovery are `Go Back N` and `selective repeat`.

### 3.6.5 Go-Back-N (GBN)

Animation: [Go-Back-N ARQ](https://www2.tkn.tu-berlin.de/teaching/rn/animations/gbn_sr/)

> In a Go-Back-N (GBN) protocol, the sender is allowed to transmit multiple packets (when available) without waiting for an acknowledgment, but is constrained to have no more than some maximum allowable number, N, of unacknowledged packets in the pipeline. 


- **Sender Behavior in GBN:**
  - The window slides forward over the sequence number space, making N the window size.
  - N is referred to as the window size, and GBN is considered a sliding-window protocol.
  - `Flow control` and `congestion control` are some of the reasons for limiting the number of unacknowledged packets to N.

<img src="https://lh3.googleusercontent.com/pw/ADCreHf6riQ0xiX1Y8x0IaZhnnaUd6EYEaffccwXfQry67IIKawSascIKFG6Md8mSFxQh_g33BxvYHcKuYAEE2U9AlpXm-r64b5UlepEhonQYufEGA4w63KF1rhgAlaSNo4jzfsUfamxAi-tT4kk0VtgR3Cj=w1920-h440-s-no" width="750" height="200">

- **Sliding Window Behaviour**
  - Sequence numbers between `0` and `'base-1'` are for sent and acknowledged packets.
  - `'base'` to `'nextseqnum-1'` represents sent but unacknowledged packets.
  - Sequence numbers from `'nextseqnum'` to `'base+N-1'` are available for sending when data arrives.
  - Sequence numbers beyond `'base+N'` can't be used until unacknowledged packets are acknowledged.
  - GBN receiver acknowledges correctly received packets and discards out of order packets.

- **Sender's Actions:**
  - The sender must respond to three types of events: invocation from above, receipt of an ACK, and a timeout event.

  > an acknowledgment for a packet with sequence number N will be taken to be a `cumulative acknowledgment`, indicating that all packets with a sequence number up to and including N have been correctly received at the receiver. 

  - The sender checks if the window is full before sending a packet. If the window is full, data is returned to the upper layer.
  - If there are lost or delayed packets, a timer is used to recover them. The timer for the oldest transmitted but unacknowledged packet is managed.

- **Receiver's Actions:**
  - The receiver handles correctly received and in-order packets by sending an ACK and delivering the data to the upper layer.
  - Out-of-order packets are discarded, as the receiver must deliver data in order.
  - Throwing away out-of-order packets simplifies receiver buffering.

### 3.6.6 Selective Repeat (SR)

Animation: [Selective Repeat ARQ](https://www2.tkn.tu-berlin.de/teaching/rn/animations/gbn_sr/)

- **Performance Issues with GBN:**
  - GBN allows the sender to fill the pipeline with packets but can suffer from performance problems, especially when the window size and bandwidth-delay product are large.
  - A single packet error can trigger unnecessary retransmissions, potentially filling the pipeline with these redundant packets.
  - Selective-repeat protocols aim to avoid unnecessary retransmissions by having the sender retransmit only suspected lost or corrupted packets.
  - In SR, the sender can receive ACKs for some packets in the window, unlike GBN.

- **SR Sender Events and Actions:**
  1. **Data Received:** Send data if it's within the window, otherwise buffer or return it.
  2. **Timeout:** Use individual timers for packet retransmission.
  3. **ACK Received:** Update the window and transmit new in-window packets.

- **SR Receiver Events and Actions:**
  1. **Packet Received:** Send selective ACKs and deliver consecutive in-window packets to the upper layer.
  2. **Special Packet:** Generate ACK for correctly received packets outside the window.
  3. **Other Cases:** Ignore packets not fitting the above scenarios.

- **Synchronization and Implications:**
  - SR protocols lack synchronization between sender and receiver windows.
  - The finite range of sequence numbers can lead to consequences in scenarios involving packet reordering.

### 3.6.7 Improvements in RDT Protocols 

| Mechanism          | Purpose                                            | Comments |
|--------------------|----------------------------------------------------|-----------|
| Checksum           | Detect bit errors in transmitted packets.         | -       |
| Timer              | Timeout for packet retransmission due to lost packets. | Duplicate packets may occur due to premature timeouts or lost ACKs. |
| Sequence number    | Sequential numbering for packet order and lost packet detection. | Gaps indicate lost packets; duplicates detect duplicate packets. |
| Acknowledgment     | Confirms correct receipt of packets.              | Can be individual or cumulative, depending on the protocol. |
| Negative acknowledgment (NAK) | Notifies sender about incorrectly received packets. | Typically carries the sequence number of the problematic packet. |
| Window and Pipelining | Increases sender utilization by allowing multiple unacknowledged packets in the pipeline. | Window size is determined by the receiver's capacity and network congestion. |


## 3.7 TCP (Transmission Control Protocol)

- **Full-Duplex and Point-to-Point:**
  - TCP connections provide a full-duplex service, allowing data to flow in both directions simultaneously.
  - Each TCP connection is between a single sender and a single receiver, and multicasting is not supported.

- **Data Transfer in TCP:**

<img src="https://lh3.googleusercontent.com/pw/ADCreHftJQQO-Aubels0acw3xS3UmGDa2n1Fnh3DkQRsy122XtlIjFenjTHSv7amS_EDWg84DBERoOp7h6XmPOM9vuNdynFKwDSoA-Tv0pS-TnhEmjybGHv3AM-q4Z0H5GYIX47JiNbCeSzjYUORJBXy3sU=w1920-h808-s-no" width="550" height="300">

  - Application-layer data flows from the client process to the server process.
  - Data is passed through the connection's `send buffer` during data transmission.
  - TCP controls when data is sent based on its convenience, and the `Maximum Segment Size (MSS)` limits data size.

    > MSS is the maximum amount of application-layer data in the segment, not the maximum size of the TCP segment including headers.

    > To fit within a single link-layer frame, set the MSS, considering a typical 40-byte TCP/IP header, to 1460 bytes, as Ethernet and PPP have an MTU of 1500 bytes.
  
  - Each data chunk is encapsulated in a TCP header to form TCP segments and further encapsulated in IP datagrams for network transmission.
  - The receiver places the received data into the connection's `receive buffer`, and the application reads the data from there.

- **TCP Segment Structure:**
  - A TCP segment consists of `header` fields and a `data` field.
  - Key fields include `source port` and `destination port`, `checksum`, `sequence number`, `acknowledgment number`, `receive window`, `header length`, and `flags`.
  - An options field can be included for features like maximum segment size (MSS) negotiation and window scaling.
  
  <img src="https://lh3.googleusercontent.com/pw/ADCreHcSNDV-yVd1BdDU6Nj4ezCL_1_VjcuUWaPSqFQBBYShSAwrC9jlbpw_LlvY8oITjDuOttW31BPxO9ayFockAc8Z9RjoVpQB9ai8_Sem2JD7fyJrLw32MmKF15kWA5VdEYtQSpshhgcUYFYip4ICJUY=w1406-h1130-s-no" width="530" height="400">


- **Sequence Numbers and Acknowledgment Numbers:**
  - Sequence numbers are assigned to bytes in the data stream and are included in the segment header.
  - Acknowledgment numbers represent the `next expected byte` in the opposite direction of data flow.
  - TCP uses `cumulative acknowledgments`, acknowledging the last byte received.
  - Handling out-of-order segments is left to TCP implementation and may involve discarding or waiting for missing bytes.


### 3.7.1 Round-Trip Time Estimation and Timeout in TCP

- **Round-Trip Time Estimation:**
  - TCP uses round-trip time (RTT) estimation to determine the time between sending a segment and receiving an acknowledgment.
  - The sample RTT (`SampleRTT`) is measured for a single segment at a time, typically for one of the `unacknowledged segments`.
  - The SampleRTT is computed as the time between sending the segment and receiving an acknowledgment.
  - Multiple SampleRTT values may fluctuate due to network and load variations.
  - TCP calculates an average RTT, `EstimatedRTT` of `SampleRTT`, using an *exponentially weighted moving average (EWMA)* formula:

    ```
    EstimatedRTT = (1 - alpha) * EstimatedRTT + alpha * SampleRTT (alpha = 0.125)
    ```
  - EstimatedRTT gives more weight to recent samples, reflecting current network conditions.

- **RTT Variation Measurement:**
  - TCP also measures RTT variation (`DevRTT`) to estimate how much SampleRTT deviates from EstimatedRTT.
  - DevRTT is calculated as an EWMA of the difference between `SampleRTT` and `EstimatedRTT`.
  
    ```
    DevRTT = (1 – beta) * DevRTT + beta * | SampleRTT – EstimatedRTT |
    ```

- **Setting the Retransmission Timeout Interval:**
  - The retransmission timeout (TimeoutInterval) should be greater than or equal to EstimatedRTT to avoid unnecessary retransmissions.
  - It shouldn't be much larger than EstimatedRTT to avoid delays when retransmitting lost segments.
  - DevRTT plays a role in determining the timeout interval:
    ```
    TimeoutInterval = EstimatedRTT + 4 * DevRTT
    ```
  - An initial TimeoutInterval of 1 second is recommended. After a timeout, the TimeoutInterval is doubled to prevent premature timeouts for subsequent segments, but it's recomputed based on the formula afterward.
  

### 3.7.2 Reliable Data Transfer

- **TCP Timer Management:**
  - An individual timer for each unacknowledged segment is conceptually simple but can have considerable overhead.
  - Recommended TCP timer management uses only a single retransmission timer, even for multiple unacknowledged segments.
  - TCP reliable data transfer is described in two steps: `timeout based recovery` and recovery using `duplicate acknowledgments`.

- **Timeout and Retransmission Handling:**

  1. **Data Received from Application Above:**
      - A TCP segment is created with a sequence number.
      - If the timer is not running, start the timer. The timer is associated with the oldest unacknowledged segment.
      - Pass the segment to IP.
      - Timer expiration interval is `TimeoutInterval`, calculated from `EstimatedRTT` and `DevRTT`.

  2. **Timeout Event:**
      - Retransmit the unacknowledged segment with the smallest sequence number.
      - Restart the timer.

  3. **ACK Received:**
      - On ACK with field value y, compare y with SendBase.
      - Update SendBase if y > SendBase.
      - If any unacknowledged segments remain, start the timer.

    <img src="https://lh3.googleusercontent.com/pw/ADCreHfd0XeL8ZXe8ewMBM-9XEzLjEQHHXXBQSAGJXOiPCYUlRUDfrbo1FCzGP5NLdxRoCmTgjI1auHjGNDFbkm3fxXuNQ7cv7k65Ha4DrT7hCo_r_rpKPo1vxmCad40jF1o7lAbrDf-0DV7-9xmkbekxu8=w1920-h616-s-no?authuser=2" width="740" height="330">

- **Scenarios:**
  - `Duplicate ACKs` can trigger a `fast retransmit` (retransmission before timeout).
  - TCP employs exponential back off for timer intervals.
  - The sender can often detect packet loss before a timeout by observing duplicate ACKs.

  > A duplicate ACK is an ACK that reacknowledges a segment for which the sender has already received an earlier acknowledgment.

  > If the TCP sender receives three duplicate ACKs for the same data, it takes this as an indication that the segment following the segment that has been ACKed three times has been lost. Then, the TCP sender performs a `fast retransmit` retransmitting the missing segment before that segment’s timer expires. 

  - TCP's error recovery mechanism is categorized as a hybrid of `Go-Back-N (GBN)` and `Selective Repeat (SR)` protocols.


### 3.7.3 Flow Control

Animation: [Flow Control](https://www2.tkn.tu-berlin.de/teaching/rn/animations/flow/)

TCP Flow Control ensures that the sender doesn't overwhelm the receiver's buffer. When data arrives at the receiver, it's placed in a receive buffer, which the application reads from. If the application reads slowly, the sender can easily overflow the buffer.

- **Flow Control vs. Congestion Control:**
  - Flow control matches sender rate to receiver reading speed.
  - Congestion control manages sender rate due to network congestion.
  - Although they both throttle the sender, they serve different purposes.

- **TCP Flow Control:**

    <img src="https://lh3.googleusercontent.com/pw/ADCreHdwuKcHW7WDAFNgV855UgY1P66rxQ52f8nFf1Czx7h1J2gZoP60wVYzQRbXRwM6ooQbGPuL0WQxy2XKUZHWMPCoeRNV4p-vCd_dQv9AEn_dxAZ3SxIifgzty24DQQVfFs0ZOvasX8PyUvRoGx3TCfM=w1748-h860-s-no?authuser=2" width="400" height="250">

  - The sender maintains a `receive window variable (rwnd)` to determine available buffer space at the receiver.
  - Full duplex communication means both sender and receiver have `distinct receive windows`.
  - rwnd is `dynamic`, and Host B informs Host A by including rwnd in its segments.
  
  ```
  rwnd = RcvBuffer - [LastByteRcvd - LastByteRead]
  ```

- **Using rwnd for Flow Control:**
  - Host B's rwnd value reflects its available buffer space.
  - Host A ensures LastByteSent - LastByteAcked ≤ rwnd.
  - If rwnd is zero, TCP mandates that Host A sends segments with one data byte to unblock the connection.
  - This ensures Host A is informed when space becomes available in Host B's receive buffer.

### 3.7.4 TCP Connection Management

<img src="https://lh3.googleusercontent.com/pw/ADCreHerZiPLvIkD639YmnLg4pvsWFpC001vHpsgwfcRnyxsT3JyaW9A4xcLw2SoQIAR4qV6y-8JQ4eMA3WRWUse594rU-mnBwuK6xjDGe5kkqb6JVi7vKdf6pkWXMIDKO0Cr6iuuLM0Pak4vNxgMsWs7_M=w1920-h888-s-no?authuser=2" width="950" height="550">


## 3.8 Congestion Control

  - **End to End Congestion Control**

    In an end to end approach to congestion control, the network layer offers no explicit support to the transport layer for congestion control. 

    > TCP segment loss (as indicated by a timeout or the receipt of three duplicate acknowledgments) is taken as an indication of network congestion, and TCP decreases its window size accordingly. Increasing round trip segment delay as an indicator of increased network congestion

  - **Network Assisted Congestion Control**

    In network assisted congestion control, routers provide explicit feedback to the sender and/or receiver regarding the network's congestion state. Feedback may range from a simple bit indicating congestion at a link to more sophisticated feedback, such as informing the sender of the maximum host sending rate a router can support.

    `Direct Feedback:` A network router directly sends feedback to the sender, often in the form of a choke packet indicating congestion.
      
    `Indirect Feedback:` A router marks/updates a field in a packet flowing from sender to receiver to indicate congestion. Upon receiving a marked packet, the receiver notifies the sender of the congestion indication. This method takes a full round trip time.

    <img src="https://lh3.googleusercontent.com/pw/ADCreHdnnrFdP89vVF72PcX0cr3fwCFXpUNq7I1UnVh0Dd60mQLfNAvfLNUNulyNT1f9eoQKGNAUKV0n2d__ihzX_3kBfBIkX7vSg1FA4rlG0qOca-eM8F75lTHPnGqxhEK5aeSXNvEBhXqHZBhNMMfBDtg=w1920-h1038-s-no?authuser=2" width="550" height="300">


### 3.8.1 Classic TCP Congestion Control

TCP adopts an approach where each sender limits the rate of sending traffic into its connection based on perceived network congestion. This raises questions about how the sender limits its rate, how it perceives congestion, and the algorithm used to adjust its rate.

- **Rate Limiting Mechanism**

TCP sender limits the rate using a `congestion window (cwnd)` variable, constraining the amount of unacknowledged data. The constraint is given by:

```
LastByteSent - LastByteAcked <= min (cwnd, rwnd)
```

Assuming a large receive buffer, the constraint solely depends on cwnd, limiting the sender's rate. The sender adjusts cwnd to control its sending rate based on network conditions.

> Thus the sender’s send rate is roughly `cwnd/RTT bytes/sec`. By adjusting the value of cwnd, the sender can therefore adjust the rate at which it sends data into its connection.

- **Perceiving Congestion**

  TCP perceives congestion through loss events, defined as either a timeout or three duplicate ACKs. Excessive congestion causes router buffers to overflow, resulting in dropped datagrams, triggering a loss event at the sender. In a congestion free network, acknowledgments for unacknowledged segments arrive, signaling successful delivery and leading to an increase in cwnd.

- **Determining Sending Rate**

  TCP addresses the challenge of determining the sending rate to avoid network congestion while utilizing available bandwidth. It follows guiding principles:
  - **Loss Event:** A lost segment implies congestion, decreasing the sender's rate.
  - **Acknowledged Segment:** Acknowledgments indicate successful delivery, allowing an increase in the sender's rate.
  - **Bandwidth Probing:** TCP probes for congestion onset by increasing the rate until a loss event occurs, adjusting the transmission rate based on implicit signals.

  > The TCP sender thus increases its transmission rate to probe for the rate that at which congestion onset begins, backs off from that rate, and then to begins probing again to see if the congestion onset rate has changed.

- **TCP Congestion Control Algorithm**

  The TCP congestion control algorithm, standardized in [RFC 5681], consists of three major components:

    1. **Slow Start:** Initially, cwnd is small, and the sending rate doubles each round until a threshold is reached or a loss event occurs. Slow start ends on loss, setting cwnd to 1 MSS, and transitions to congestion avoidance.
      
    2. **Congestion Avoidance:** Linear increase of cwnd by 1 MSS per round, avoiding aggressive growth. Ends on loss, similar to slow start.

    > TCP’s congestion avoidance algorithm behaves the same when a timeout occurs as in the case of slow start: The value of cwnd is set to 1 MSS, and the value of ssthresh is updated to half the value of cwnd when the loss event occurred.

    3. **Fast Recovery:** Recommended but not required. It involves increasing cwnd for duplicate ACKs and transitioning to congestion avoidance on ACK for the missing segment.

    > TCP Tahoe, unconditionally cut its congestion window to 1 MSS and entered the slow start phase after either a timeout indicated or triple duplicate ACK indicated loss event. The newer version of TCP, TCP Reno, incorporated fast recovery.

    <img src="https://lh3.googleusercontent.com/pw/ADCreHfOLql8zoOonXOmIYdDXSO1lR3sBlmC5onGe2wHtLP4czHe02kSgwFNjVnJyYM9wpI3Ycw7WGUuaFGEdXiSnE9EULNAue-yJlaEfMLU8R8EjPf379tcqPvSpv86k-Qu3Xu2CVQdgo94ETgsx9IjNTI=w1768-h1094-s-no?authuser=2" width="600" height="400">

    TCP's congestion control exhibits `saw tooth` behavior, referred to as `additive increase, multiplicative decrease` **(AIMD)**. AIMD aims to simultaneously optimize user and network performance, probing for available bandwidth in an asynchronous manner.


## 3.9 Network Assisted Congestions

### 3.9.1 Explicit Congestion Notification

<img src="https://lh3.googleusercontent.com/pw/ADCreHdgekG0rBZ1X-scpp5eaH2nUlJLL8xjB0dn958V8M8MBapJ46_dUNdkB-nqR__S6m142ELWrX-QJ7ytpicpWKDSYooKp5y3_lqADmCP-wFgjxEfuYuL4K_bLKdYfDtJ-51tZ0k_RNTaf8uO553bckQ=w910-h496-s-no?authuser=2" width="550" height="300">

- ECN is a form of network assisted congestion control in the Internet that involves both TCP and IP.
- Two bits in the IP datagram header's `Type of Service` field are reserved for `ECN`.
- One ECN setting indicates router `congestion`; the other indicates ECN `capability of sender and receiver`.
- Router congestion indication is forwarded to the destination host, informing the sending host.
- TCP sender reacts to ECN congestion indication by halving the congestion window and setting the CWR bit.
- Other transport layer protocols, including DCCP, DCTCP, and DCQCN, also use ECN.
- Increasing deployment of ECN capabilities in popular servers and routers.

### 3.9.2 Delay based Congestion Control

- Proactively detects congestion onset before packet loss.
- TCP Vegas measures RTT for acknowledged packets and adjusts the congestion window based on throughput.
- TCP Vegas operates under the intuition that TCP senders should “Keep the pipe just full, but no fuller”
- BBR congestion control builds on TCP Vegas ideas, competing fairly with non BBR TCP senders.
- Google adopted BBR for all TCP traffic on its private B4 network, replacing CUBIC.


## 3.10 Evolution of Transport Layer Functionality

The design and implementation of transport layer functionality has continued to evolve.

- Various versions of TCP developed, implemented, and deployed, including TCP CUBIC, DCTCP, CTCP, BBR, and more.
- Measurements indicate wider deployment of newer TCP versions on Web servers than classic TCP Reno.
- Many versions of TCP designed for specific conditions, such as wireless links, high bandwidth paths, paths with packet re-ordering, and more.
- Diversity in TCP versions handling priorities, parallel paths, acknowledgment, and session establishment/closure.
- Survey of TCP versions available in [Afanasyev 2010] and [Narayan 2018].

- **QUIC: Quick UDP Internet Connections**

If the transport services needed by an application don’t quite fit either the UDP or TCP service models, application designers can create their own protocol at the application layer. This approach is taken in the QUIC (Quick UDP Internet Connections) protocol

- QUIC is an application layer protocol designed to improve the performance of transport layer services for secure HTTP.
- Widely deployed, still in the process of being standardized as an Internet.
- Google has deployed QUIC on many public facing Web servers, in its mobile video streaming YouTube app, in its Chrome browser, and in Android’s Google Search app.

<img src="https://lh3.googleusercontent.com/pw/ADCreHfVhmjEoNV9ljCuYm4MgS-ltGLRRuIXknk6mQo8MLz90CWgfXkWTPKiBgxMfprg7j18tq_jPgfhBKPiKKAKOgfbJ4bAprTPK2fVTutTBvj3Nz28qHfR89VPEXoJ_DK9dpvmNJ_BWTsrMTp3JC81cvx4=w1920-h750-s-no?authuser=2" width="600" height="300">

 - **Major Features of QUIC:**

    1. **Connection Oriented and Secure:**
        - Similar to TCP, QUIC is a connection oriented protocol between two endpoints.
        - Requires a handshake between endpoints to set up the QUIC connection state.
        - All QUIC packets are encrypted for security.
        - Combines handshakes needed for connection establishment, authentication, and encryption, providing faster establishment compared to TCP.

    2. **Streams:**
        - Allows multiple application level `streams` to be multiplexed through a single QUIC connection.
        - New streams can be quickly added once a QUIC connection is established.
        - A stream is an abstraction for reliable, in order bi directional data delivery between two QUIC endpoints.

    3. **Reliable, TCP friendly Congestion Controlled Data Transfer:**
        - Provides reliable data transfer on a per stream basis.
        - Each stream operates independently, minimizing HOL blocking problems.
        - Congestion control mechanisms similar to TCP’s, based on TCP NewReno.



[Yet To Complete]
- TCP Cubic
- TCP Reno Throughput

# Chapter 4: Network Layer (Data Plane)

## 4.1 Overview

The network layer's primary role is to move packets from a sending host to a receiving host. Two key functions are involved:

- **Forwarding:**

    > Forwarding refers to the router-local action of transferring a packet from an input link interface to the appropriate output link interface.

  - Moves packets from a router's `input link` to the appropriate `output link`.
  - The primary function in the data plane.
  - Implemented in hardware.
  
- **Routing:**
    > Routing refers to the network-wide process that determines the end-to-end paths that packets take from source to destination. 

  - Determines the route or path packets take from sender to receiver.
  - Implemented in the control plane.
  - Routing algorithms calculate these paths.
  - Implemented in software

- A router's forwarding table is crucial for packet forwarding. It indexes header values to determine the outgoing link interface.
- `Software-Defined Networking` (SDN) separates the control plane from the router. A remote controller computes and distributes forwarding tables to routers. SDN allows for open, software-based implementations.

## 4.2 Router Architecture

#### Components of a Generic Router:

1. **Input Ports:**
   - Terminate incoming physical links.
   - Perform link-layer functions for interoperability.
   - Conduct a lookup function to determine the output port using the forwarding table.
   - Forward control packets (e.g., carrying routing protocol information) to the routing processor.
   - The number of ports varies, from a few in enterprise routers to hundreds in ISP edge routers.

2. **Switching Fabric:**
   - Connects input ports to output ports.
   - Completely contained within the router.
   - a network inside of a network router!

3. **Output Ports:**
   - Store and transmit packets received from the switching fabric.
   - Conduct link-layer and physical-layer functions.
   - Paired with input ports for bidirectional links.

4. **Routing Processor:**
   - Performs control-plane functions.
   - In traditional routers, executes routing protocols, maintains routing tables, and computes forwarding tables.
   - In SDN routers, communicates with the remote controller, receives forwarding table entries, and performs network management functions.
   - Operates at millisecond or second timescales.

<img src="https://lh3.googleusercontent.com/pw/ADCreHdojxc4ewnh58kAQUrzO6NtwOoEEm69fVwJ7RpsndlMvEb5BTNSvChBSXYZrCqd5AOJwDCbNe9dMgebE2AoJU6ffdfqM39fTHTNzn10HW8GZiBi9iGEGSwB_oCQDh4WDxQ_f8euMQKXI8LI5WcaNEt-=w1497-h927-s-no?authuser=2" width="900" height="600">

### 4.2.1 Input Port Processing and Destination-Based Forwarding

#### Forwarding Table Management:

- The forwarding table is either computed and updated by the routing processor, employing a routing protocol to interact with other routers.
- Alternatively, the table may be received from a remote SDN controller.
- A shadow copy at each line card allows local forwarding decisions, reducing the need for centralized processing on a per-packet basis.

#### Handling Scale: Prefix Matching Example

- Brute-force implementation with one entry for every possible destination address is impractical due to scale.
- `Prefix matching` is introduced as an efficient alternative.
- For instance, a forwarding table might look like this for a specific case:

  | Prefix                                | Link Interface  |
  |---------------------------------------|-----------------|
  | 11001000 00010111 00010               | 0               |
  | 11001000 00010111 00011000            | 1               |
  | 11001000 00010111 00011               | 2               |
  | Otherwise                             | 3               |

- The router matches a packet's destination address with the prefixes in the table.
- `Longest prefix matching` rule is used when multiple matches occur.

#### Fast Lookup Challenges:

- At Gigabit transmission rates, lookup must be performed in nanoseconds.
- Hardware implementation is essential, and techniques beyond a simple linear search are required.
- Memory access times are critical, leading to designs with embedded on-chip DRAM and faster SRAM.

#### Input Port Processing:

1. **Match:**
   - Packet's output port determined through lookup.
   - Longest prefix matching rule applied.
   
2. **Action:**
   - Packet sent into the switching fabric.
   - Temporary blocking possible if fabric is currently in use by other input ports.
   - Blocked packets queued at the input port and scheduled for later transmission.

3. **Additional Actions:**
   - Physical- and link-layer processing.
   - Checking packet's version number, checksum, and time-to-live field.
   - Updating counters for network management.

### 4.2.2 Switching Fabric in Router Architecture

The switching fabric serves as the core of a router, facilitating the actual switching (or forwarding) of packets from input ports to output ports. Different methods of switching are used, each influencing the overall performance and throughput.

#### 1. Switching via Memory:

  - Early routers, acting as traditional computers, controlled switching via the CPU (routing processor).
  - Input ports signaled the CPU through interrupts.
  - Packets were copied into processor memory, and the CPU handled destination address lookup and forwarding table processing.
  - Limited forwarding throughput due to shared system bus constraints.

#### 2. Switching via a Bus:

  - Input port transfers a packet directly to the output port over a shared bus without routing processor involvement.
  - A switch-internal label indicates the local output port.
  - Limited by bus speed; only one packet can cross the bus at a time.
  - Common in small local area and enterprise networks.

#### 3. Switching via an Interconnection Network:

  - Uses a sophisticated interconnection network, e.g., a crossbar switch.
  - Crossbar switch consists of 2N buses connecting N input ports to N output ports.
  - Crosspoints controlled by a switch fabric controller, enabling `non-blocking` and `parallel forwarding`.


### 4.2.3 Output Port Processing

- Output port processing involves transmitting packets stored in the output port's memory over the output link.
- Tasks include packet selection (scheduling), de-queuing for transmission, and executing link-layer and physical-layer functions.

#### Input Queueing

- Minimal queuing at input ports when the switching fabric (Rswitch) is N times faster than the line speed (Rline).
- If Rswitch is not fast enough, packet queues form at input ports, causing `head-of-the-line (HOL) blocking` and potential packet loss.

#### Output Queueing

- Even with a fast switching fabric, output port queues may form if packets from all N input ports are destined for the same output port.
- Queued packets can overwhelm the output port's memory, leading to potential packet loss.

#### How Much Buffering Is "Enough?"

- Traditional rule: Buffering (B) equals average round-trip time (RTT) times link capacity (C), i.e., 
   ```B = RTT * C```.
- Modern Rule: B = `RTT C (2N)^1/2`
- Optimal buffer size is a nuanced consideration, balancing decreased packet loss with increased queueing delays.
- Active queue management (AQM) algorithms, like `Random Early Detection (RED)`, help manage buffer dynamics.

#### Bufferbloat and Complexities

- `Bufferbloat` refers to persistent buffering, showcasing the complexity of managing queues.
- Interaction among senders at the network edge and queues within the network can be subtle.

### 4.2.4 Packet Scheduling

<img src="https://lh3.googleusercontent.com/pw/ADCreHcFLP8aO7hejw7Bz_Pi6SDL4Mn_JCH-uqICUcpReaA3zqp-zmofVtV7jExfIroysPj2720oVq_PGQbRkTk7Y02KAYeLl4FzrAJEU22PuhYmyQpY0GKGamDgPNIctL-cHeb23Fzgf3f0BFlZ7a3l3MKi=w1920-h386-s-no?authuser=2" width="900" height="200">

#### Comparison Table

| Discipline            | Description                                | Operation                                                     |
|-----------------------|--------------------------------------------|---------------------------------------------------------------|
| **FIFO**               | Queuing in arrival order; packets leave in the same order they arrived. | Selection based on arrival order; removal after transmission |
| **Priority Queuing**  | Classifies packets into priority classes; serves higher-priority packets first. | Highest priority class with nonempty queue served first      |
| **Round Robin**       | Alternates service among classes; each class served in a circular manner. | Round-robin service pattern                                   |
| **Weighted Fair Queuing (WFQ)** | Generalized round robin with differential service based on weights assigned to each class. | Service based on weighted round-robin pattern                |

## 4.3. IP Addressing

### 4.3.1 IPv4

<img src="https://lh3.googleusercontent.com/pw/ADCreHduJMEOpHZpP3FXB5m6nzbxOzzFUvu3eIBqzrcg70qXQVH4SKc-2Qbq4wvAh4pdCtO7VINEji6qQvC4e944DTm_96sKkCR6Q7PAcOYEKjfzdBDW-eOpdQWuM_EO1jmIKQDPMVqeVflTjRWBuH7DN8Gc=w1352-h948-s-no?authuser=2" width="600" height="400">

| Field                   | Description                                                                                                         |
|-------------------------|---------------------------------------------------------------------------------------------------------------------|
| **Version number**      | Specifies the IP protocol version of the datagram (IPv4 or IPv6).                                                      |
| **Header length**       | Determines the start of the payload in the IP datagram; typically 20 bytes for most datagrams.                        |
| **Type of service**     | Bits used to distinguish different types of IP datagrams based on the required level of service.                      |
| **Datagram length**     | Total length of the IP datagram (header plus data) in bytes; maximum theoretical size is 65,535 bytes.                 |
| **Identifier, flags, fragmentation offset** | Fields related to IP fragmentation, where large datagrams are broken into smaller fragments for transmission.        |
| **Time-to-live**        | Ensures datagrams do not circulate indefinitely; decremented by routers, and dropped if it reaches 0.                  |
| **Protocol**            | Indicates the specific transport-layer protocol for the data portion of the IP datagram (e.g., TCP, UDP).             |
| **Header checksum**     | Aids in detecting bit errors in the received IP datagram; computed using 1s complement arithmetic.                    |
| **Source and destination IP addresses** | Source inserts its IP address, and destination's address is determined, usually via DNS lookup.                    |
| **Options**             | Allow IP header extension for rare use cases, but omitted in IPv6 for simplicity.                                      |
| **Data (payload)**      | Contains the transport-layer segment (e.g., TCP or UDP) or other data, such as ICMP messages.                         |

*Note: An IP datagram typically has a 20-byte header (excluding options). If carrying a TCP segment, each datagram includes a total of 40 bytes of header (20 bytes of IP header plus 20 bytes of TCP header) along with the application-layer message.*

### 4.3.2 CIDR (Classless Interdomain Routing)

CIDR is the Internet's address assignment strategy, allowing the division of IP addresses into two parts, a network portion and a device portion. This approach improves address allocation efficiency.

- The network portion is indicated by the x most significant bits of the address (prefix), reducing the size of forwarding tables in routers.
- The remaining 32-x bits distinguish devices within the organization.
- CIDR allows flexible subnetting, avoiding the constraints of classful addressing (class A, B, C networks).


### 4.3.3 Dynamic Host Configuration Protocol (DHCP)

The Internet Corporation for Assigned Names and Numbers (ICANN) manages IP addresses globally. It allocates addresses to regional Internet registries, which further manage addresses within their regions.

After obtaining a block of addresses, an organization assigns individual IP addresses to host and router interfaces. 
Dynamic Host Configuration Protocol (DHCP) is commonly used for automatic host address assignment.

#### DHCP Process:

1. **DHCP Server Discovery:**
   - The host sends a DHCP discover message to find a DHCP server.
   - The message is broadcast to all nodes on the subnet using IP broadcast.
   > creates an IP datagram containing its DHCP discover message along with the broadcast destination IP address of 255.255.255.255 and a “this host” source IP address of 0.0.0.0. 

2. **DHCP Server Offer(s):**
   - DHCP server(s) respond with offer messages.
   - Offers include the proposed IP address, network mask, and lease time.

3. **DHCP Request:**
   - The client chooses an offer and responds with a DHCP request.

4. **DHCP ACK:**
   - The server acknowledges the request with a DHCP ACK message.
   - The client can use the allocated IP address for the lease duration.

DHCP's plug-and-play capability makes it efficient for network administrators, especially in scenarios with frequent host mobility.

> If no server is present on the subnet, a DHCP relay agent (typi- cally a router) that knows the address of a DHCP server for that network is needed.

### 4.3.4 Network Address Translation (NAT)

- Network Address Translation (NAT) provides a simpler approach to address allocation, especially in scenarios like SOHO networks.

- The addressing within the home network remains as a private network with addresses like 10.0.0.0/24, reserved for private realms. NAT hides the details of the home network from the outside world.

- **Private Address Realm:** The home network computers use private addresses (e.g., 10.0.0.0/24), which are meaningful only within the given network.
- **Single IP Address to the World:** The NAT router represents the home network to the external world with a single IP address (e.g., 138.76.29.7).
- **DHCP Usage:** The router often uses DHCP to get its address from the ISP, and it runs a DHCP server for internal network devices.

> NAT routers use a translation table to keep track of internal hosts and their corresponding ports. When a datagram from an internal host is forwarded to the WAN, the NAT router performs address and port translation, updating the source IP address and port.

### 4.3.5 IPv6

<img src="https://lh3.googleusercontent.com/pw/ADCreHfHs4kPC6QGsL7q-0yCrpp5_QZddnjOJtMVac9UDP0gLPW-DFpAMthbUFsFBDydYEPNwrvqZbClMvtNo-zJotLMOuk_cyi5ozrgos5acXsOVtBJGzUF3cMEvpjBJXqn1NYfOvKmjC-ub6uaXf_t0ONs=w1522-h856-s-no?authuser=2" width="600" height="400">

| Field             | Size (bits) | Description                                                                                                              |
|-------------------|-------------|--------------------------------------------------------------------------------------------------------------------------|
| Version           | 4           | Identifies the IP version number. IPv6 carries a value of 6 in this field.                                                |
| Traffic Class     | 8           | Similar to the TOS field in IPv4, it can prioritize datagrams within a flow or from specific applications.               |
| Flow Label        | 20          | Identifies a flow of datagrams, allowing special handling for quality of service or real-time service.                    |
| Payload Length    | 16          | Unsigned integer indicating the number of bytes in the IPv6 datagram following the fixed-length 40-byte header.          |
| Next Header       | 8           | Identifies the protocol to which the datagram's contents will be delivered (e.g., TCP or UDP).                             |
| Hop Limit         | 8           | Decremented by each forwarding router; if it reaches zero, the datagram is discarded.                                    |
| Source Address    | 128         | IPv6 128-bit address format.                                                                                             |
| Destination Address | 128       | IPv6 128-bit address format.                                                                                             |
| Data              | Variable    | Payload portion of the IPv6 datagram, passed on to the protocol specified in the Next Header field.                      |
| Fragmentation/Reassembly | N/A | IPv6 does not allow fragmentation and reassembly at intermediate routers. "Packet Too Big" ICMP error is sent if needed. |
| Header Checksum   | N/A         | Removed in IPv6, as checksumming is performed by transport and link-layer protocols.                                      |
| Options           | Variable    | No longer part of the standard IP header; included as one of the possible next headers, resulting in a fixed-length header.|

#### Transitioning from IPv4 to IPv6

The most widely adopted approach for IPv4-to-IPv6 transition involves **tunneling**. Tunneling is a concept applicable in diverse scenarios, including all-IP cellular networks. In tunneling, if two IPv6 nodes (e.g., B and E) want to communicate but are connected through intervening IPv4 routers, a tunnel is established.


<img src="https://lh3.googleusercontent.com/pw/ADCreHd2h_OChNHQc4WNwCHNijHEFo39w0IatpNIbkEBUimj97YnwrCBPSOhDnyipU0dBtwJ81Kw_nqllRnhZINyMzV0eZ24O1Vd7PJ5FrLdzOpAq0lJJdHL85DDlWIlejWaHrol4lMMiRTlz35FP31xPwx3=w1442-h1094-s-no?authuser=2" width="600" height="400">

- The IPv6 node on the sending side (B) encapsulates the entire IPv6 datagram in the payload of an IPv4 datagram.
- The IPv4 datagram is addressed to the IPv6 node on the receiving side (E) and sent into the tunnel.
- Intervening IPv4 routers route the IPv4 datagram, unaware that it contains a complete IPv6 datagram.
- The receiving IPv6 node extracts the IPv6 datagram and routes it as if received directly.


[Yet To Complete]
- Match-Plus-Action
- Middleboxes

# Chapter 5: Network Layer (Control Plane)

- The Control Plane Network layer is a component in networking that manages the communication and coordination between network devices. It is responsible for handling tasks such as routing, signaling, and configuration. 
- In essence, the control plane determines how data should be forwarded through the network by making decisions based on the network's state and topology.

<img src="https://lh3.googleusercontent.com/pw/ABLVV85gXLe2Oe-ngOZehumdWU7yMgPW3sZDlT7-2vK-Ec_jOTZqntb02OxO4GwOLliURJP5kG9VGDK0RQHj5FLm30CISMkl9HIiPeUaQYRdQO1FIG1bzWcR67s9oBLbZqqeduhFhW5IOzEFF0VGxL736TmP=w1542-h1014-s-no?authuser=3" width="60%" height="auto">

## 5.1 Routing Algorithms

**Distance Vector Algorithm:** Each router maintains a table with distances to destinations, updating based on information exchanged with neighbors (e.g., RIP protocol).

**Link State Algorithm:** Routers share comprehensive information about network link states to build a shortest path based on the complete network topology for efficient path calculations (e.g., OSPF protocol).

| Feature                        | Distance Vector Routing         | Link State Routing             |
|--------------------------------|---------------------------------|--------------------------------|
| Information Exchange           | Exchange routing tables         | Exchange Link State Database   |
| Update Triggers                | Periodic updates or triggered   | Event-driven updates           |
| Hop Count                      | Based on hop count              | Based on shortest path         |
| Path Selection                 | May not always find shortest    | Always finds shortest path     |
| Convergence Time                | Slower convergence              | Faster convergence             |
| Memory Usage                   | Lower memory usage              | Higher memory usage            |
| Bandwidth Usage                | Higher bandwidth usage          | Lower bandwidth usage          |
| Routing Table Size              | Larger routing tables           | Smaller routing tables         |
| Example Protocols               | RIP, EIGRP                      | OSPF, IS-IS                    |
| Loop Prevention                | Split Horizon, Poison Reverse   | SPF Algorithm                  |
| Scalability                    | Limited scalability            | Highly scalable                |
| Fault Tolerance                | Less fault-tolerant             | More fault-tolerant            |
| Example Implementations        | Traditional networks            | Internet scale networks        |

## 5.2 Intra-AS Routing: OSPF

> An autonomous system is identified by its globally unique autonomous system number (ASN). AS numbers, like IP addresses, are assigned by `ICANN` regional registries.

- **Definition:** Routers organized into Autonomous Systems (ASs), each under the same administrative control.
- **AS Identification:** Globally unique Autonomous System Numbers (ASNs) assigned by ICANN.
- **Routing Algorithm:** Intra-Autonomous System Routing Protocol.

### 5.2.1 OSPF (Open Shortest Path First)

> OSPF is a link state protocol that uses flooding of link state information and a Dijkstra’s least cost path algorithm. With OSPF, each router constructs a complete topological map (that is, a graph) of the entire autonomous system. Each router then locally runs Dijkstra’s shortest path algorithm to determine a shortest path tree to all subnets

- **Link State Protocol:**
  - Utilizes flooding of link state information.
  - uses Dijkstra’s least cost path algorithm.
- **Complete Topological Map:**
  - Each router constructs a full topological map of the entire AS.
  - Locally runs Dijkstra’s algorithm to determine shortest path trees.
- **Link Costs:**
  - Configured by the network administrator.
  - Allows flexibility (e.g., minimum hop routing or weights based on link capacity).

### 5.2.2 OSPF Features and Advancements

1. **Security:**
   - Authentication to ensure only trusted routers participate.
   - Supports `simple` and `MD5` authentication, the latter providing higher security.
   - Guards against replay attacks using sequence numbers.

2. **Multiple Same Cost Paths:**
   - OSPF permits the use of multiple paths when several have the same cost.

3. **Integrated Unicast and Multicast Routing:**
   - MOSPF (Multicast OSPF) extends OSPF to support multicast routing.

4. **Hierarchy Support:**
   - OSPF AS can be configured hierarchically into areas.
   - Area Border Routers facilitate routing between areas, with a designated backbone area.

   <img src="https://lh3.googleusercontent.com/pw/ABLVV84X2z2FuF11XHSg5DVPAaJX1KWa8AfEWP3MRClK3DTwVMMU2nJh6UcOXd_1QF5zn3K9jzTG2fDyE3YyfWPedybHOuGE73JZCvCC9X4oFtD8AhVckBFy8KmfXpYJKkGjYPIMWCuZw1yODVzJHKQxgQ7S=w1920-h564-s-no?authuser=3" width="80%" height="auto">


## 5.3 Inter-AS Routing: BGP

BGP (Border Gateway Protocol) is a fundamental inter autonomous system routing protocol in the Internet. It acts as the glue that binds thousands of ISPs together, facilitating communication across multiple ASs.

### 5.3.1 BGP Responsibilities

- **Destination Representation:** Routes packets to `CIDRized prefixes`, each representing a subnet or a collection of subnets.
- **Advertising Reachability Information:** Allows subnets to advertise their existence across ASs.
- **BGP Connections:**
  - Advertising reachability information through BGP messages.
  - External BGP (eBGP) connections: Between gateway routers in different ASs.
  - Internal BGP (iBGP) connections: Within routers of the same AS.

### Determining the Best Routes

> When a router advertises a prefix across a BGP connection, it includes with the prefix several BGP attributes. In BGP jargon, a prefix along with its attributes is called a route. Two of the more important attributes are `AS-PATH` and `NEXT-HOP`. 

> The AS-PATH attribute contains the list of ASs through which the advertisement has passed. To generate the AS-PATH value, when a prefix is passed to an AS, the AS adds its ASN to the existing list in the AS-PATH. The NEXT-HOP is the IP address of the router interface that begins the AS-PATH.

- **BGP Attributes:**
  - `AS-PATH`: List of ASs through which the advertisement has passed.
  - `NEXT-HOP`: IP address of the router interface starting the AS-PATH.
- **Choosing the Best Route:** Routers choose among various paths based on cost and policy.

<img src="https://lh3.googleusercontent.com/pw/ABLVV87jx9vAP4G_DTrfiu8oIOSr29Rxs8KtvpWAMnxMCDuobDG3fmX2zZ_8QAy81L6rTQ22jgmaAXHeoCqnZV6OTatkhVz_C-GcgifrfteMUK6viSvc7b-2zUhbhHrUkwKwXBVfXRNV8gLO1vskH_RpPbCP=w1650-h690-s-no?authuser=3" width="60%" height="auto">

Three components: NEXT-HOP; AS-PATH; destination prefix.

```
3d; AS3; X --> 2a; AS2 AS3; X
```

### 5.3.2 Hot Potato Routing in BGP

Hot Potato Routing is a fundamental algorithm in BGP (Border Gateway Protocol) used for selecting the best route to a destination prefix. This algorithm prioritizes getting packets out of an Autonomous System (AS) quickly with minimal cost.

- `Goal`: Quickly move packets out of the AS with the least possible cost.
- `Analogy`: Similar to passing a burning "hot potato" to another person (AS) as quickly as possible.
- `Selfish Algorithm`: Focuses on reducing costs within its AS, ignoring other end to end costs outside the AS.

#### Algorithm Overview

1. **Learn Routes:**
   - Router 1b learns about two possible BGP routes to prefix x.
   
2. **Cost Calculation:**
   - Utilizes intra AS routing information to find the least cost intra AS path to NEXT-HOP routers (2a and 3d).
   - Defines cost as the number of links traversed.

3. **Route Selection:**
   - Selects the route with the smallest of these least cost paths.
   - Example: Cost to router 2a is 2, cost to router 3d is 3, so router 2a is selected.

4. **Forwarding Table Update:**
   - Consults the forwarding table (configured by intra AS algorithm) to find the interface (I) on the least cost path to router 2a.
   - Adds (x, I) to its forwarding table.

5. **Adding Outside AS Prefix**
    - When adding an outside AS prefix to the forwarding table, both inter AS (BGP) and intra AS (e.g., OSPF) routing protocols are utilized.

### 5.3.3 IP Anycast in BGP

BGP is also utilized for implementing the IP anycast service. `IP anycast` is used in applications like DNS to replicate content across dispersed geographical locations, ensuring users access the nearest server. IP Anycast in BGP facilitates efficient content distribution by leveraging BGP's route selection capabilities.

#### Implementation in CDN (Content Delivery Network)

<img src="https://lh3.googleusercontent.com/pw/ABLVV864FDCHULkGWDYpKV8xXjS0m7oS4lKLhOqi1jNCNc7li0xhyTEgzTOzb-FrM-dMoiFY0ZvFG8tt34J4zKpL3ca4WeItSS7V8YE3KdDGRN5cqzhkZJ5XCX9fLfxcv0coumD5uEBVYEnuYla-zvYuhw5A=w1544-h1094-s-no?authuser=1" width="60%" height="auto">

1. **IP-Anycast Configuration:**
   - CDN assigns the same IP address to all servers.
   - Standard BGP is used to advertise this IP address from each server.

2. **BGP Route Selection Algorithm:**
   - BGP routers treat multiple route advertisements for the same IP address as different paths to the same physical location.
   - Local BGP route selection algorithm is applied to choose the "best" route (e.g., closest in AS hop counts).

3. **Routing Table Configuration:**
   - Each router configures its routing table to route packets to the chosen location based on the BGP route selection.

4. **Content Distribution:**
   - CDN distributes content, and when a client requests the common IP address, routers forward the request to the "closest" server as per BGP route selection.


## 5.4 ICMP (Internet Control Message Protocol)

The Internet Control Message Protocol (ICMP) facilitates communication of network layer information among hosts and routers. Primarily used for error reporting.

- **ICMP Message Structure**
   - ICMP messages consist of a `type` and a `code` field.
   - They contain the header and the initial 8 bytes of the IP datagram causing the ICMP message in error identification.

<img src="https://lh3.googleusercontent.com/pw/ABLVV84DD19PxZRIY_yE1aDBHuosSKOAMH3bB32nPN8m7R1_PdwXWZmaktEQL5lFx3sel3XoChEiWoJfOGOrPUbFotIxdVxQ4hqNTitFkv7h4xSo1mq5Sp3VikWBElhDmfq9qywQ0MbZp_qmHEJAswQ3IgFb=w1474-h1094-s-no?authuser=1" width="60%" height="auto">

- **Ping Program (Echo Request and Echo Reply):**
  - Type 8 (Echo Request) and type 0 (Echo Reply) messages.
  - Ping client sends an Echo Request, and the destination host responds with an Echo Reply.

- **Source Quench Message:**
  - Used for congestion control, but used in practice.
  - Allows a congested router to send a source quench ICMP message to instruct a host to reduce its transmission rate.

- **Traceroute Program:**
  - Implemented using ICMP messages (type 11 code 0).
  - Determines routers between source and destination by sending UDP datagrams with incrementing TTL values.
  - Round trip time, router names, and IP addresses are obtained from ICMP warning messages.

## 5.5 Network Management

> Network management includes the deployment, integration, and coordination of the hardware, software, and human elements to monitor, test, poll, configure, analyze, evaluate, and control the network and element resources to meet the realtime, operational performance, and Quality of Service requirements at a reasonable cost.

### 5.5.1 Network Management Components

#### Managing Server
- centralized network that controls collection, processing, analysis, dispatching of network management information and commands.
- Initiates actions to configure, monitor, and control managed devices.

#### Managed Device
- Network equipment, like hosts, routers, switches, including software residing on a managed network.
- Holds configuration parameters, operational data, and device statistics.

#### Data
- **Configuration data**: Explicitly configured device information by the network manager.
- **Operational data**: Information acquired by the device during operation (e.g., OSPF neighbors).
- **Device statistics**: Status indicators and counts updated during operation.

<img src="https://lh3.googleusercontent.com/pw/ABLVV86mSMgXm0aoXrptE6wP4uRVNPusPVS-X3pOZoKs7WexcNGvUbHKogDhsZ5PbxqxzpGzTLn0nTjO_Wu5iYqbbAiD543bHqZQ5PuolgPBzP_KqWcDvPyCfOMwUoeM52fbz_1aadIWG4FD87KZpKRSCA6z=w1272-h1094-s-no?authuser=1" width="60%" height="auto">

#### Network Management Agent
- Software in the managed device that communicates with the managing server, taking local actions as directed.

#### Network Management Protocol (SNMP)
- Facilitates communication between managing server and managed devices.
- Allows querying device status and taking actions via agents.
- Informs managing server of exceptional events (e.g., component failures).
- MIB objects represent operational state and configuration data of managed devices.

### 5.5.2 SNMPv3 Message Types

| SNMPv3 PDU Type    | Description                                                           | Sender-Receiver            |
|---------------------|-----------------------------------------------------------------------|----------------------------|
| GetRequest          | Get value of one or more MIB object instances                         | Manager-to-Agent           |
| GetNextRequest      | Get value of next MIB object instance in list or table                | Manager-to-Agent           |
| GetBulkRequest      | Get values in a large block of data, e.g., values in a large table    | Manager-to-Agent           |
| InformRequest       | Inform remote managing entity of MIB values remote to its access     | Manager-to-Manager         |
| SetRequest          | Set value of one or more MIB object instances                         | Manager-to-Agent           |
| Response            | Generated in response to GetRequest, GetNextRequest, GetBulkRequest, SetRequest, or InformRequest PDUs | Agent-to-Manager or Manager-to-Manager |
| SNMPv2-Trap         | Inform manager of an exceptional event                                | Agent-to-Manager           |


### 5.5.3 NETCONF/YANG

> NETCONF specifies in a structured XML document, and activates a configuration at the managed device. NETCONF uses a remote procedure call (RPC), where protocol messages are also encoded in XML and exchanged between the managing server and a managed device over a secure, connection oriented session such as the TLS protocol.

> YANG is the data modeling language used to precisely specify the structure, syntax, and semantics of network management data used by NETCONF. All YANG definitions are contained in modules, and an XML document describing a device and its capabilities can be generated from a YANG module.

- A more abstract, network wide approach to network management.
- Emphasizes configuration management and atomic operations over multiple devices.
- YANG (data modeling language) models configuration and operational data.
- NETCONF protocol communicates YANG compatible actions and data.

# Chapter 6: Link Layer and LANs

## 6.1 Link Layer

The Link Layer, part of the OSI model's Layer 2, provides communication between devices in a local network. It includes protocols like Ethernet (IEEE 802.3), Wi-Fi (IEEE 802.11), PPP, HDLC, and ARP, managing tasks like framing, link access(MAC), reliable delivery, and error detection.

- Link layer is implemented on a chip called the network adapter or `network interface controller (NIC)`.
- Integrated into the motherboard chipset or implemented via a dedicated Ethernet chip.
- Implemented in hardware, handling framing, link access, error detection, etc.

## 6.2 Error Detection & Correction Techniques

### 6.2.1 Parity Checks

- `Even Parity:` Ensures that the total number of 1s in a data unit (including the parity bit) is even.
  - If an odd number of bits are in error, the parity check will detect it.
- `Odd Parity:`
  - Requires the total number of 1s to be odd.
- `Forward Error Correction (FEC)` is an error correction technique where extra bits are added to transmitted data, allowing the receiver to correct errors without retransmission.

### 6.2.2 Checksumming Methods

- Checksums involve summing up the values of a set of data units and appending the result to the data being transmitted.
- **Checksum Calculation:**
  - Sender calculates a checksum value based on the data.
  - Sender sends both the data and the checksum.
  - Receiver calculates its checksum on the received data.
  - If the calculated checksum mismatches the received checksum, an error is detected.
- See more on: [Checksums in UDP](https://github.com/VasanthVanan/computer-networking-top-down-approach-notes/blob/main/Chapter%203%3A%20Transport%20Layer.md#35-udp-user-datagram-protocol)

### 6.2.3 Cyclic Redundancy Check (CRC)

- CRC is a more sophisticated error-checking technique.
- **Polynomial Division:**
  - Data is treated as coefficients of a polynomial.
  - Division is performed using a predetermined divisor polynomial.
  - Remainder is appended to the data for transmission.
- **Error Detection:**
  - Receiver performs the same division and checks the remainder.
  - If the remainder is not zero, an error is detected.

## 6.3 Multiple Access Links and Protocols

|                | **Point-to-Point Links** | **Broadcast Links**                            |
|----------------|--------------------------------|------------------------------------------------------|
| **Characteristics** | Connects two devices directly. Dedicated communication link between them. | Single communication channel shared by multiple devices. Data sent by one device is received by all others. |
| **Link Access Control** | Since it's a point-to-point link, there's no contention for the link. No need for a MAC protocol for multiple access. | Requires a MAC protocol to coordinate access among multiple devices. Avoids collisions and ensures fair access. |
| **Efficiency** | Efficient use of bandwidth since only two devices share the link. Full capacity available to each device. | Bandwidth is shared among multiple devices. Efficiency depends on the effectiveness of the MAC protocol. |
| **Examples** | Traditional telephone lines and Point-to-point leased lines. | Ethernet networks (using CSMA/CD or CSMA/CA protocols). Wireless LANs (using protocols like Wi-Fi). |


* Classification of multiple access protocols into three categories: 
  - channel partitioning, 
  - random access, and 
  - taking-turns (controlled access).

### 6.3.1 Channel Partitioning Protocols

#### Time-Division Multiplexing (TDM)

- TDM divides time into time frames and further divides each time frame into N time slots. 
- Each time slot is then assigned to one of the N nodes. TDM allows one node to speak for a fixed period, then another node speaks, and so on. 
- This ensures fairness, but has drawbacks. See Also [Circuit Switching](https://github.com/VasanthVanan/computer-networking-top-down-approach-notes/blob/main/Chapter%201%3A%20Computer%20Networks%20and%20the%20Internet.md#17-circuit-switching).

#### Frequency-Division Multiplexing (FDM)

- FDM divides the R bps channel into different frequencies and assigns each frequency to one of the N nodes, creating N smaller channels of R/N bps. 
- While avoiding collisions, FDM limits a node to a bandwidth of R/N, even when it's the only active node.

#### Code Division Multiple Access (CDMA)

- CDMA assigns a different code to each node. Nodes use their unique codes to encode data bits. 
- CDMA allows simultaneous transmissions with minimal interference. 

### 6.3.2 Random Access Protocols

In a random access protocol, a transmitting node always transmits at the full rate of the channel (R bps). Collisions are handled by retransmitting frames after a random delay.

#### Pure ALOHA

- The first ALOHA protocol was unslotted and fully decentralized. 
- Nodes immediately transmit frames into the channel and waits for acknowledgement. 
- If ACK not received, node waits for random backoff time and re-sends data.
- If a collision occurs, nodes retransmit with a probability. Efficiency is less than slotted ALOHA. 
- If a first bit of a new frame overlaps with the last bit of a nearly finished frame, both frames will be completely destroyed and must be retransmitted later.

  <img src="https://www.myreadingroom.co.in/images/stories/docs/dcn/aloha%20Protocols_Pure%20aloha.JPG" width="60%" height="auto">

#### Slotted ALOHA

- A simple random access protocol where time is divided into time-slots. 
- Nodes are allowed to transmit at slot beginnings. Collisions are detected, and nodes retransmit with a probability. 
- If a station misses out the allowed time, it must wait for the next slot. This reduces the probability of collisions.
- Efficiency is determined by the long-run fraction of successful slots.

  <img src="https://www.myreadingroom.co.in/images/stories/docs/dcn/aloha%20Protocols_Slotted%20aloha.JPG" width="60%" height="auto">


#### Carrier Sense Multiple Access (CSMA)

- CSMA protocols introduce `carrier sensing` to listen before transmitting and `collision detection` to stop transmitting if interference is detected. 
- The possibility of collision still exists because of propagation delay
- Types of CSMA:
  - 1-Persistent CSMA: If station is busy, it will **CONTINUOUSLY** sense the medium and transmit the data again. [Probability=1]
  - Non-persistent CSMA: If station is busy, it will wait for a random time and **RANDOMLY** sense the medium before transmitting again.
  - p-Persistent CSMA: It applies to slotted channels; If station is idle, it it will **CONTINUOUSLY** sense and waits for the slotted time to transmits the data  [Probability=p]

    <img src="https://lh3.googleusercontent.com/pw/ABLVV85KjpQ0qYdwG8uIEdt8Cc9gmX_OuSDW8miulqzMWK6G4hWCye5msmonru0zsxMhdGGPvPA5v2BLjAbqQ8wdiKADibiq3uBky0cCGSA7HyDAtNAiEGnhGPQEKmwed5E1vho35A8BWl89Evxu11cV7nOY=w792-h912-s-no?authuser=1" width="60%" height="auto">

#### CSMA/CD

- CSMA/CD is a variant of CSMA that introduces collision detection.
- **Transmission Period**: The time required for a node to transmit a frame.
- **Idle Period**: The time required for a node to wait before transmitting again.
- **Contention Period**: The time required for a node to sense the medium before transmitting again. 
- **Binary Exponential Backoff**: It uses binary exponential backoff algorithm to handle collisions. 
- Nodes choose a random value from an increasing set for waiting after collisions.
- When a collision is detected, the transmitting nodes immediately stop transmitting and enter a backoff state.


#### CSMA/CA

- Similar to CSMA/CD, CSMA/CA begins with carrier sensing. Nodes listen to the channel to determine if it's busy or idle.
- CSMA/CA introduces virtual carrier sensing to estimate the channel's status. 
- CSMA/CA uses a contention window, which is a range of time during which a node may choose to transmit after sensing the channel is idle.
- The size of the contention window may vary, and it influences the probability of a successful transmission.

### 6.3.3 Taking Turns Protocols (Controlled Access)

#### Reservation

- A station need to make a reservation before sending data.
- In each interval, a reservation frame precedes the data frames sent in that interval.
- If there are N stations in the system, there are exactly N reservation minislots in the reservation frame.
- When a station needs to send a data frame, it makes a reservation in its own minislot.
- The stations that have made reservations can send their data frames after the reservation frame. 

  <img src="https://lh3.googleusercontent.com/pw/ABLVV87UZqcqWAnjvjtJEv4aOyT7zCUGjsXN3IpnbYXROTCMHMKk0MYs_I4YY3UiacY0VLciUZX3UFWBZeQos1iVeAI13UpJi5mpykVtukwb8KrtujF3js3tJY1g-KeteIAkCjYeT6bwj8-N--2Av-TrdgCx=w1920-h422-s-no?authuser=1" width="60%" height="auto">

#### Polling

- The polling protocol requires one of the nodes to be designated as a Master node (Primary station).
- The master node polls each of the nodes in a round-robin fashion.
- The master node can determine when a node has finished sending its frames by observing the lack of a signal on the channel.
- `Functions`: `Poll` (receive) and `Select` (send) functions
- `Drawback`: Polling Delay; If master node fails, channel will be inoperative.

#### Token Passing

- The token passing protocol is similar to polling, but it uses a token to determine when a node has finished sending its frames.
- Decentralised and highly efficient; (No Master Node)
- A small, special-purpose frame known as a token is exchanged among the nodes in some fixed order.
- When a node receives a token, it holds onto the token only if it has some frames to transmit; otherwise, it immediately forwards the token to the next node.
- `Examples`: Physical, Dual, Star, and Bus Ring.

## 6.4 Link Layer Addressing

### 6.4.1 Media Access Control (MAC) Addresses

  - MAC addresses have a flat structure and remain constant for an adapter, analogous to a social security number.
  - Typically 6 bytes (48 bits) long (for most LANs) and expressed in hexadecimal notation.
  - Originally designed to be permanent, but now changeable via software.
  - Managed by IEEE to ensure uniqueness; Companies purchase a chunk of address space (224 addresses) for manufacturing adapters.

### 6.4.2 Address Resolution Protocol (ARP)

  - ARP resolves IP addresses to MAC addresses (between Network and Link-Layer Addresses).
  - Hosts and routers maintain ARP tables mapping IP addresses to MAC addresses.
  - ARP query packet used to obtain MAC address for a given IP address on the same subnet.
  - Plug-and-play; ARP tables get built automatically.
  - ARP table also contains a time-to-live (TTL) value, which indi- cates when each mapping will be deleted from the table. 

    <img src="https://ipcisco.com/wp-content/uploads/2018/10/arp-packet-format-ipcisco.jpg" width="60%" height="auto">

    > A MAC address table, sometimes called a Content Addressable Memory (CAM) table, is used on Ethernet switches to determine where to forward traffic on a LAN.

    | Feature                  | CAM Table                                    | ARP Table                                    |
    |--------------------------|----------------------------------------------|----------------------------------------------|
    | **Purpose**              | Manages MAC (Media Access Control) addresses  | Resolves IP addresses to MAC addresses       |
    | **Function**             | Stores MAC addresses associated with ports   | Stores IP addresses and corresponding MAC addresses |
    | **Scope**                | Limited to the local network or VLAN          | Network-wide, may involve broadcast messages |
    | **Storage Type**          | Typically stored in hardware (CAM)           | Stored in software, often in the OS's ARP cache |
    | **Security Implications** | Vulnerable to MAC address spoofing            | Can be exploited for ARP spoofing attacks    |
    | **Examples**              | Cisco switches, Ethernet switches             | Operating systems (Windows, Linux, etc.)    |



**Sending a Datagram off the Subnet**

  - When a host on a subnet wants to send a datagram to another subnet, ARP is still used.
  - Router interfaces play a crucial role in forwarding the datagram.
  - The destination MAC address is the router interface's MAC address, not the final destination's MAC address.
  - ARP is used to obtain the MAC address of the first-hop router.
  - Router consults a forwarding table to determine the correct interface for forwarding the datagram.
  - ARP is used again to obtain the MAC address of the ultimate destination.

    <img src="https://lh3.googleusercontent.com/pw/ABLVV85ip3uwpFb-_CdsLD7jkOiO3qB8xndr_7sjDFGBl1Bc0LMva75FMgNGtshNuxoLYOVNC1QtRRlhdZS5VMZEwma62vSR_VMyF30dCzCORAaGmYF6Xqzp4pixg7nXi0klaFi1QfMvewAaR9duSc9X1jNU=w1098-h298-s-no?authuser=1" width="60%" height="auto">

### 6.4.3 Ethernet Frame Structure

An Ethernet frame consists of the following components:

1. **Data field (46 to 1,500 bytes):** Carries the IP datagram, with a maximum transmission unit (MTU) of 1,500 bytes.
2. **Destination address (6 bytes):** MAC address of the destination adapter.
3. **Source address (6 bytes):** MAC address of the transmitting adapter.
4. **Type field (2 bytes):** Permits multiplexing of network-layer protocols.
5. **Cyclic redundancy check (CRC) (4 bytes):** Detects bit errors in the frame.
6. **Preamble (8 bytes):** Synchronizes clocks between adapters.


## 6.5 Link Layer Switches

- The primary role of a switch is to receive incoming link-layer frames and forward them to outgoing links. Switches employ buffers in output interfaces to handle potential rate mismatches.
- Switches perform two key functions: `filtering` and `forwarding`. 
- Filtering determines whether a frame should be dropped or forwarded, while forwarding identifies the interfaces to which a frame should be directed. 
- This is achieved through a switch table, containing MAC addresses, associated interfaces, and entry timestamps. Unlike routers, switches forward based on MAC addresses, not IP addresses.

When a frame arrives:
- If no entry exists for the destination address, the switch broadcasts the frame.
- If there's an entry for the destination on the same interface, the frame is discarded.
- If there's an entry for a different interface, the frame is forwarded to that interface.

**Advantages of Switches**
- `Elimination of Collisions`: Switches prevent collisions, maximizing bandwidth.
- `Heterogeneous Links`: Different LAN links can operate at varying speeds and media types.
- `Management`: Switches offer enhanced security and ease of network management.

**Self-Learning Capability**

Switches possess the self-learning property, automatically building and updating their switch tables without manual intervention. The process involves recording MAC addresses, associated interfaces, and timestamps for each incoming frame. Entries are removed after a specified aging time, ensuring the switch table remains accurate.

## 6.6 Virtual Local Area Networks (VLANs)

- Hosts within a VLAN communicate as if connected directly to the switch, creating broadcast domains within each VLAN. 
- VLANs effectively isolate traffic, optimize switch utilization, and simplify user management.

In a port-based VLAN,
- Switch ports are grouped into VLANs by the network manager.
- Each VLAN forms a broadcast domain, isolating broadcast traffic within the VLAN.

**VLAN Switch Configuration**

- The network manager configures port-to-VLAN mappings using switch management software. 
- Switch hardware delivers frames only between ports belonging to the same VLAN. 
- However, this introduces a challenge: How can traffic from one VLAN be sent to another?

**VLAN Trunking**

- To address inter-VLAN communication, VLAN trunking was introduced. A trunk port on each switch, configured to belong to all VLANs, facilitates VLAN interconnection. Trunk links forward frames between switches, ensuring effective communication.

- The IEEE standard 802.1Q defines VLAN trunking. A special Ethernet frame format includes a four-byte VLAN tag in the header, carrying the VLAN identity. The VLAN tag contains a Tag Protocol Identifier (TPID) field, Tag Control Information field with a VLAN identifier, and a priority field.

  <img src="https://lh3.googleusercontent.com/pw/ABLVV86GRpSCpPwDC_6jYwJMrRJN_qv1J9ibbzlXHiLnhqUDrzYnys_mi0UWgCl23AiOvD6pj5uSwmq2vfZCEwBnR6W4jHveYtPYUuApve3oEhqSQwx2EgrTUDipODFighaOcZSCm8vYj43Tc-rwjNgelxXX=w1070-h326-s-no?authuser=1" width="60%" height="auto">

## 6.7 Multiprotocol Label Switching (MPLS)

MPLS enhances IP router's forwarding speed by incorporating a key concept from virtual-circuit networks: `fixed-length labels`. Unlike circuit-switched networks, MPLS is a packet-switched, virtual-circuit network, co-existing with IP infrastructure.

- An MPLS-capable router adds a small MPLS header to a link-layer frame between MPLS-capable devices. This header includes fields like the `label`, `experimental bits`, an S bit indicating the end of a stacked header series, and a `time-to-live` field.
- MPLS-capable routers, known as `label-switched` routers, forward MPLS frames by looking up labels in their forwarding tables, eliminating the need to extract IP addresses for routing decisions.
- MPLS labels and their associations with IP destinations are distributed among MPLS-capable routers. 
- MPLS introduces traffic engineering capabilities, allowing routers to forward packets along paths not determined by standard IP routing protocols. This enables network operators to override normal IP routing for specific traffic management purposes.
- MPLS can be utilized for fast restoration of forwarding paths, implementing virtual private networks (VPNs), and various other purposes.

  <img src="https://lh3.googleusercontent.com/pw/ABLVV85_ezMEMThiI57Cz0Nl6TJ9fqu5Hy_LhUBUIBekDQIscXCMhItu_f5nWHDMaVJbf-jawTk7U1O373NdGqgU4NAKtSjzFaJUXNmikDk12nLxgQlGLXK2n3IPH1zcOhw5aw9MjKkbRu5CfDZmn1Lp_XJe=w908-h558-s-no?authuser=1" width="60%" height="auto">
