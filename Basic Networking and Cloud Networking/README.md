# Basic Networking and Cloud Networking


### What is Networking?

A computer network is a set of computers sharing resources located on or provided by network nodes. The computers use common communication protocols over digital interconnections to communicate with each other.

### What is MAC Address?

A media access control address is a unique identifier assigned to a network interface controller for use as a network address in communications within a network segment. This use is common in most IEEE 802 networking technologies, including Ethernet, Wi-Fi, and Bluetooth.

### What is NIC Card?

A network interface controller is a computer hardware component that connects a computer to a computer network. Early network interface controllers were commonly implemented on expansion cards that plugged into a computer bus.

### What is IP Address?

An IP address, or Internet Protocol address, is **a series of numbers that identifies any device on a network**. Computers use IP addresses to communicate with each other both over the internet as well as on other networks.

### What is subnetting and subnet ?

To subnet a network is to create logical divisions of the network. Subnetting, therefore, involves dividing the network into smaller portions called subnets. Subnetting applies to IP addresses because this is done by borrowing bits from the host portion of the IP address. In a sense, the IP address then has three components - the network part, the subnet part and, finally, the host part.

### **What is a network switch** ?

A network switch is a device that operates at the Data Link layer of the OSI model (Layer 2). It takes in packets being sent by devices that are connected to its physical ports and sends them out again, but only through the ports that lead to the devices the packets are intended to reach.

### ****How does a network switch work?****

Once a device is connected to a switch, the switch identifies its media access control (MAC) address, a code that’s baked into the device’s network-interface card (NIC). The NIC attaches to the Ethernet cable that attaches to the switch.

The switch uses the MAC address to identify which attached device is sending outgoing packets, and where to deliver incoming packets.

When one device sends a data packet to another device, the packet enters the switch and the switch reads the header to determine what to do with it. The switch matches the destination address or addresses and sends the packet out through the appropriate ports that lead to the destination devices.

![switching.jpg](https://github.com/HasanTareq73/GCP-Study-Guide/blob/e1236eadd657fc4227ff9273a79ac89542672f68/image/switching.jpg)

### What is Routing?

Routing is the process of selecting a path for traffic in a network or between or across multiple networks. Broadly, routing is performed in many types of networks, including circuit-switched networks, such as the public switched telephone network, and computer networks, such as the Internet.

Type of Routing:

1.  Static Routing
2.  Dynamic Routing

Dynamic Routing are also 2 types;

1.  Internal Routing (Example: RIP, EIGRP, OSPF, iBGP, ISIS)
2.  External Routing (Example: eBGP)

![routing-diagram.svg](https://github.com/HasanTareq73/GCP-Study-Guide/blob/e1236eadd657fc4227ff9273a79ac89542672f68/image/routing-diagram.svg)

### OSI Model:

The OSI Model is a logical and conceptual model that defines network communication used by systems open to interconnection and communication with other systems. The Open System Interconnection (OSI Model) also defines a logical network and effectively describes computer packet transfer by using various layers of protocols.

### **7 Layers of the OSI Model**

OSI model is a layered server architecture system in which each layer is defined according to a specific function to perform. All these seven layers work collaboratively to transmit the data from one layer to another.

-   **The Upper Layers**: It deals with application issues and mostly implemented only in software. The highest is closest to the end system user. In this layer, communication from one end-user to another begins by using the interaction between the application layer. It will process all the way to end-user.
-   **The Lower Layers**: These layers handle activities related to data transport. The physical layer and datalink layers also implemented in software and hardware.

Upper and Lower layers further divide network architecture into seven different layers as below

-   Application (Layer-7)
-   Presentation (Layer-6)
-   Session (Layer-5)
-   Transport (Layer-4)
-   Network (Layer-3)
-   Data-link (Layer-2)
-   Physical layers (Layer-1)

![092119_0729_LayersofOSI1.webp](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6f4ae7c9-162e-4109-aee7-5af7143b014a/092119_0729_LayersofOSI1.webp)

![OSI-Layer-Please-Do-Not-Tell-Secret-Passwords-Anytime-blackMORE-Ops-1 (1).png](https://github.com/HasanTareq73/GCP-Study-Guide/blob/e1236eadd657fc4227ff9273a79ac89542672f68/image/OSI-Layer-Please-Do-Not-Tell-Secret-Passwords-Anytime-blackMORE-Ops-1%20(1).png)

### What is Socket and Socket binding?

A socket is an endpoint that enables communication between two processes. This communication is irrespective of where the processes are running. **Furthermore, we highlight that sockets in the context of TCP/IP-based networks are called a Network Socket or Internet Socket. In this case, a socket executes between transport and application layers of the TCP/IP stack.**

There are three main types of sockets:

-   **Datagram: a socket that creates the interprocess communication with User Datagram Protocol (UDP).** In this way, datagram sockets enable simple IP communication without establishing any connection between processes.
-   **Stream: sockets that enable the communication between processes with Transmission Control Protocol (TCP).** Thus, stream sockets require the execution of a three-way handshake to connect processes and provide communication with particular message delivering guarantees.
-   **Raw: sockets that read network traffic from a network interface regardless of the transmission layer protocol.** A typical use of raw sockets is on the development of packet sniffers.

A socket is created but does not have any address assigned. **So, the bind operation is responsible for establishing specific addresses to sockets.**

### **What is DNS?**

The Domain Name System (DNS) is the phonebook of the Internet. Humans access information online through [domain names](https://www.cloudflare.com/learning/dns/glossary/what-is-a-domain-name/), like [nytimes.com](http://nytimes.com) or [espn.com](http://espn.com). Web browsers interact through [Internet Protocol (IP)](https://www.cloudflare.com/learning/network-layer/internet-protocol/) addresses. DNS translates domain names to [IP addresses](https://www.cloudflare.com/learning/dns/glossary/what-is-my-ip-address/) so browsers can load Internet resources.

### ****How does DNS work?****

The process of DNS resolution involves converting a hostname (such as [www.example.com](http://www.example.com)) into a computer-friendly IP address (such as 192.168.1.1). An IP address is given to each device on the Internet, and that address is necessary to find the appropriate Internet device - like a street address is used to find a particular home. When a user wants to load a webpage, a translation must occur between what a user types into their web browser ([example.com](http://example.com)) and the machine-friendly address necessary to locate the [example.com](http://example.com) webpage.

### ****What are the steps in a DNS lookup?****

For most situations, DNS is concerned with a domain name being translated into the appropriate IP address. To learn how this process works, it helps to follow the path of a DNS lookup as it travels from a web browser, through the DNS lookup process, and back again. Let's take a look at the steps.

****The 8 steps in a DNS lookup:****

1.  A user types ‘[example.com](http://example.com)’ into a web browser and the query travels into the Internet and is received by a DNS recursive resolver.
2.  The resolver then queries a DNS root nameserver (.).
3.  The root server then responds to the resolver with the address of a Top Level Domain (TLD) DNS server (such as .com or .net), which stores the information for its domains. When searching for [example.com](http://example.com), our request is pointed toward the .com TLD.
4.  The resolver then makes a request to the .com TLD.
5.  The TLD server then responds with the IP address of the domain’s nameserver, [example.com](http://example.com).
6.  Lastly, the recursive resolver sends a query to the domain’s nameserver.
7.  The IP address for [example.com](http://example.com) is then returned to the resolver from the nameserver.
8.  The DNS resolver then responds to the web browser with the IP address of the domain requested initially.

Once the 8 steps of the DNS lookup have returned the IP address for [example.com](http://example.com), the browser is able to make the request for the web page:

1.  The browser makes a [HTTP](https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/) request to the IP address.
2.  The server at that IP returns the webpage to be rendered in the browser (step 10).

![dns-lookup-diagram.webp](https://github.com/HasanTareq73/GCP-Study-Guide/blob/e1236eadd657fc4227ff9273a79ac89542672f68/image/dns-lookup-diagram.webp)

### **What is a DNS query?**

A DNS query (also known as a DNS request) is a demand for information sent from a user's computer (DNS client) to a DNS server. In most cases a DNS request is sent, to ask for the IP address associated with a domain name. An attempt to reach a domain, is actually a DNS client querying the DNS servers to get the IP address, related to that domain.

## **Types of queries**

In general, there are two ways of resolving a host or a domain name to an IP address, using the domain name system – a **Recursive** query and a **non-Recursive** query.

1.  The **Recursive** query is, when a DNS client directly gets the IP address of a domain, by asking the name server system to perform the complete translation.
2.  The **non-Recursive** query is, when a DNS client contacts the name servers, one by one, until it finds the server, containing the needed information.

## **How do they work?**

The process behind **Recursive** queries, can be explained by the following example:

1.  A user opens up his favorite browser and enters [https://www.somedomain.com](https://www.somedomain.com) in the address bar. His computer does not know the IP address for [www.somedomain.com](http://www.somedomain.com), so it sends a request to the user’s DNS resolver.
2.  The resolver does not know the IP address for [www.somedomain.com](http://www.somedomain.com), so it will query one of the root DNS servers.
3.  The root servers know the locations of all the TLDs, such as .com, they do not know the IP of [www.somedomain.com](http://www.somedomain.com), so they return the location of the .com servers.
4.  Once the query reaches the .com TLD servers, it will find the Authoritative DNS server of [www.somedomain.com](http://www.somedomain.com) and will reply to the resolver with that server.
5.  The resolver will send a query to the Authoritative DNS server of the domain and will resolve it.
6.  The Authoritative DNS server of the domain will check within its database and will find an entry for [www.somedomain.com](http://www.somedomain.com), which has an IP address.
7.  Finally the resolver will know the IP address for [www.somedomain.com](http://www.somedomain.com) and will send the result to the user's computer.

The process behind **non-Recursive** queries, follows the same procedure, but the DNS client (the machine from which the user tries to resolve the domain) will have to find the authoritative DNS server for the domain, by itself.

### ****Egress and Ingress flow****

Egress in the world of networking implies traffic that exits an entity or a network boundary, while Ingress is traffic that enters the boundary of a network.

if we try to told simply, When we want to browse a website like Google or Facebook that means our request goes to the google server from our computer that’s Egress traffic or outbound traffic . when we try to download some document from google or Facebook and download is running that means traffic (download file) is coming in our computer that’s Ingress traffic or incoming traffic .

![ingress-egress-1-1024x465.png](https://github.com/HasanTareq73/GCP-Study-Guide/blob/e1236eadd657fc4227ff9273a79ac89542672f68/image/ingress-egress-1-1024x465.png)

### What is Container?

**Containers are lightweight packages of your application code together with dependencies such as specific versions of programming language runtimes and libraries required to run your software services.**

### ****Containers vs. VMs****

You might already be familiar with VMs: a guest operating system such as Linux or Windows runs on top of a host operating system with access to the underlying hardware. Containers are often compared to virtual machines (VMs). Like virtual machines, containers allow you to package your application together with libraries and other dependencies, providing isolated environments for running your software services.

-   Containers are much more lightweight than VMs
-   Containers virtualize at the OS level while VMs virtualize at the hardware level
-   Containers share the OS kernel and use a fraction of the memory VMs require

### What is Docker ?

Docker is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers. The service has both free and premium tiers. The software that hosts the containers is called Docker Engine.

### ### What is Network Namespace?

Linux network namespaces are a Linux kernel feature allowing us to isolate network environments through virtualization. For example, using network namespaces, you can create separate network interfaces and routing tables that are isolated from the rest of the system and operate independently.

### **Create Your Namespaces**

Let’s create two network namespaces:

```bash
sudo ip netns add ns1

sudo ip netns add ns2

```

Once they are added we can view them with `ip netns list`.

now have a very simple container that can’t do much at the moment. To get more functionality we can connect the namespaces using a `veth` device.

### Create a Bridge

A Bridge is a **Layer 2 Switch** which defines a network and can hold multipule namespaces within this network using **veth** (virtual ethernet) cable. For example we are going to define 10.0.0.0/24 network to this bridge. Let's create a bridge first.

```bash
sudo ip link add vBridge type bridge

```

Now verify the bridge is created or not:

```bash
sudo ip link

```

As you can see the br0 bridge interface has been created but it's **DOWN**. Now turn it **UP** and assin an **IP address** to vBridge.

```bash
sudo ip link set vBridge up
sudo ip addr add 10.0.0.1/16 dev vBridge

```

### **Create a Virtual Ethernet Cable for Each Namespace**

A veth device is a virtual ethernet device that you can think of as a real ethernet cable connecting two other devices. Virtual ethernet devices act as tunnels between network namespaces. They create a bridge to a physical network device in another namespace.

In our example, we are creating two veth pairs. The ns1 namespace will connect to the veth-ns1 end of the cable, and the other cable end should attach to a bridge that will create the network for our namespaces. We create the same cable and connect it to the bridge on the ns2 side

To create both veth pairs, use the command:

```bash
sudo ip link add veth-ns1 type veth peer name bridge-ns1-veth

sudo ip link add veth-ns2 type veth peer name bridge-ns2-veth

```

Now when you look at the devices you will see your veth pairs on the host network.

```bash
ip link list

```

Now that we have a veth pair in the host namespace, let’s move the ns1 and ns2 sides of the cables out into the ns1 and ns2 namespaces.

```bash
sudo ip link set veth-ns1 netns ns1

sudo ip link set veth-ns2 netns ns2

```

Now if you check `ip link`, you will see the bridge-ns1-veth and bridge-ns2-veth is **missing**, because it **belongs** to **ns1 and ns2** now.

After that, Connect the other side of the cable **veth-ns1 and veth-ns2** into the **vBridge**
