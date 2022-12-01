<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Chela+One&family=Finlandica:ital,wght@1,700&display=swap" rel="stylesheet">
<h1 style="font-size:80px;font-family:Finlandica;padding-top:-100px';" align="center">About Systems</h1>
<ul>
<li><a href="#intro" style="text-decoration:none">Introduction</a><br><br></li>
<li><a href="#abstract" style="text-decoration:none">Abstractions</a></li>
<li><a href="#df" style="text-decoration:none">Design Fundamentals</a><br><br></li>
<li><a href="#cliser" style="text-decoration:none">Client-Server Model</a></li>
<li><a href="#netpro" style="text-decoration:none">Network Protocols</a></li>
<li><a href="#storage" style="text-decoration:none">Storage</a></li>
<li><a href="#landt" style="text-decoration:none">Latency And Throughput</a></li>
<li><a href="#avail" style="text-decoration:none">Availability</a></li>
<li><a href="#cache" style="text-decoration:none">Caching</a></li>
<li><a href="#proxy" style="text-decoration:none">Proxies</a></li>
<li><a href="#lb" style="text-decoration:none">Load Balancers</a></li>
<li><a href="#hash" style="text-decoration:none">Hashing</a></li>
<li><a href="#db" style="text-decoration:none">Databases</a></li>
<li><a href="#kvstore" style="text-decoration:none">Key-Value Stores</a></li>
<li><a href="#ssp" style="text-decoration:none">Specialized Storage Paradigms</a></li>
<li><a href="#repshar" style="text-decoration:none">Replication And Sharding</a></li>
<li><a href="#leader" style="text-decoration:none">Leader Election</a></li>
<li><a href="#peerpeer" style="text-decoration:none">Peer-To-Peer Networks</a></li>
<li><a href="#pollstream" style="text-decoration:none">Polling And Streaming</a></li>
<li><a href="#configuration" style="text-decoration:none">Configuration</a></li>
<li><a href="#ratelimit" style="text-decoration:none">Rate Limiting</a></li>
<li><a href="#logmonitor" style="text-decoration:none">Logging And Monitoring</a></li>
<li><a href="#pubsub" style="text-decoration:none">Publish/Subscribe Pattern</a></li>
<li><a href="#cs" style="text-decoration:none">MapReduce</a></li>
<li><a href="#securityhttps" style="text-decoration:none">Security And HTTPS</a></li>
<li><a href="#cs" style="text-decoration:none">API Design</a></li>
</ul>
<br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">0</div>
<h1 id="intro" style="font-size:30px">System Design</h1>
System design is the process of defining components and their integration, APIs, and data models to build large-scale systems that meet a specified set of functional and non-functional requirements.<br><br><br>
System design uses the concepts of computer networking, parallel computing, and <b>distributed systems</b> to craft systems that scale well and are performant. Distributed systems scale well by nature. However, distributed systems are inherently complex. The discipline of system design helps us tame this complexity and get the work done.
<br><br><br><br>
System design aims to build systems that are <b>reliable</b>, <b>effective</b>, and <b>maintainable</b>, among other characteristics.<br>
- Reliable systems handle faults, failures, and errors.<br>
- Effective systems meet all user needs and business requirements.<br>
- Maintainable systems are flexible and easy to scale up or down. The ability to add<br>&nbsp; new features also comes under the umbrella of maintainability.<br>

<br><br>
Real-world system building is an iterative process where we start with a reasonably good design, measure how it performs, and improve the design in the next iteration.
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">1</div>
<p>Where the coding interview serves primarily as an assessment of your problem-solving ability, the systems design interview is a test of your engineering knowledge veiled behind the facade of an open-ended design question.</p> 
<br><br>
If a coding interview problem is given to someone who has no coding background, no computer science background, they would likely be able to tackle the problem at least a little bit. They wouldn't be able to know that they have to use a certain data structure to solve a problem optimally. But they would be able to conceptually tackle the problem.<br><br>
With Systems Design interviews on the other hand, that would not be possible.If someone with no software engineeering background is given a canonical Systems Design interview question like design Youtube, design a website where millions of people can upload video content and billions of people can view that content and comment on it, like it, that person would not be able to answer this question properly. Because Systems Design interviews really do require a lot of knowledge about Systems, about how to build Robust, Functional, and Scalable Systems. <br>
That's where Design Fundamentals come into play.
<br><br>
<div align="center">
<b>Building scalable, production-ready applications is both art and science.</b>
</div>
<br>
Science, in that it requires knowledge of many topics in computer engineering;<br>art, in that it demands an eye for making smart design choices and piecing together the right technologies.
<br><br><br><br><br><br>
<table style="padding-left:110px">
<tr><th>Coding Interviews</th><th>Design Interviews</th></tr>
<tr><td align="center">Data Strucutres</td><td align="center">Design Concepts</td></tr>
<tr><td align="center">problem solving ability</td><td align="center">engineering knowledge</td></tr>
<tr><td align="center">objective correctness</td><td align="center">subjective correctness</td></tr>
</table>
<br><br><br><br><br><br><br><br><br><br>
veiled - covered, hidden<br>
facade - face<br>
canonical - standard, accepted<br>
<div align="center">2</div>
<h1>How Systems Design interviews actually work?</h1>
System Design interview questions are very intentionally vague. Such vagueness mimics the reality of modern day business.<br>
And it's gonna be your job as the interviewee to be able to take a two-word sentence, like design Uber, and turn it into a 45-minute discussion.<br><br><br>
<h2>Best practices</h2>
<ul>
<li>An applicant should ask the right questions to solidify the requirements.</li>
<li>Applicants also need to scope the problem so that they’re able to make a good attempt at solving it within the limited time frame of the interview.</li>
<li>Communication with the interviewer is critical. </li>
</ul><br><br><br>
A proposed solution to a system design interview question may very well not be objectively correct or objectively incorrect unlike with coding interviews.<br><br><br>
<b>Job:-</b> Justify your Solution.<br>
Explain to rationalise why you made certain choices, why you've designed parts of your system in one way instead of another, make your interviewer understand why your proposed solution is reasonable, why it's sound, and why it might be the best one. Or perhaps why it might not be the best one, why it might be one of many potential solutions.
<br><br><br>
<h2>Possible questions</h2>
Design Interviews often include questions related to how a design might evolve over time as some aspect of the system increases by some order of magnitude—for example, the number of users, the number of queries per second, and so on. It’s commonly believed in the systems community that when some aspect of the system increases by a factor of ten or more, the same design might not hold and might require change.<br><br>
Designing and operating a bigger system requires careful thinking because designs often don’t linearly scale with increasing demands on the system.<br><br><br>
Another question might be related to why we don’t design a system that’s already capable of handling more work than necessary or predicted ? The reason is dollar cost.<br><br><br><br><br>
<div align="center">3</div>
<h1 id="df">What are Design Fundamentals ?</h1>
Design Fundamentals are the foundational knowledge that is needed for Systems Design interviews just as Data Structures are the foundational knowledge that is needed for Coding Interviews.<br><br>
<h2>Four categories of Design Fundamentals</h2>
<ul>
    <li>
        <b>Underlying (or) Fundamental Knowledge</b><br>
        Eg:- client-server architecture, network protocols
     </li>
    <li>
        <b>Key characteristics of systems</b><br>
        Things you might want a system to have, often involving trade offs. <br>
        Eg:- Availability, Latency, Throughput, Redundancy, Consistency
     </li>
     <li>
        <b>Actual components of a system</b><br>
        Tangible things that you can either have in a system or implement in a system. <br>
        Key components that are gonna allow your system to have the key characteristics that we just mentioned above. <br>
        Eg:- Load Balancer, Proxy, Cache, Rate Limiting, Leader Election
    </li>
    <li>
        <b>Actual technology</b><br>
        Real existing products or services that you can actually use in a system either as actual components or to achieve some characteristic in a system. <br>
        Eg:- nginx, Redis, Amazon S3, zookeeper, Etcd, Google cloud storage
    </li>
</ul><br><br>
The fourth category of design fundamentals is the one that's often overlooked.
Also, this is very important one that can really round you off and make you shine in a Systems Design interview.<br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br>
tangible - real, physical
<div align="center">2</div>
A client is a thing that talks to servers. A server is a thing that talks to clients. The client—server model is a thing made up of a bunch of clients and servers talking to one another. <br>
And that, kids, is how the Internet works!
<h1 id="cliser" style="font-size:30px">Client-Server Architecture</h1>

- Foundation of the modern internet.
- Foundation of how computers speak to one another

<br>For time being, lets consider some layman terminology. Client is some machine that speaks to the server. Server is another machine that listens to clients and speaks back to those clients. And when we use the word speak here, what we really mean is sending data. Client requests data from server and then the server returns it.<br>
The architecture works on a <b>request-response model</b>.<br><br><br>
<h3>Q) What happens when you open up your browser and type in your URL bar <br>
&nbsp;&nbsp;&nbsp;https://www.youtube.com/ and then press Enter?</h3>
Well, your browser, be it Google Chrome, or Safari, or Firefox, your browser is a client, and YouTube, for the sake of this example, is the server.<br>
Now, truthfully, YouTube is not a server. It has a server, or multiple servers that act on its behalf.<br><br>
Here, the client(browser) doesn't know actually what the server(YouTube) is.
All that it knows, is that it can communicate with it. It can speak to it, it can request stuff from it. But it doesn't actually know what the server represents. After typing the URL,  the browser doesn't even know how to talk with the server(Youtube).<br><br><br>
<h3>1. Who to speak to ? </h3>
Behind the Scenes: our browser makes a <b>DNS query</b> to find out what the IP address of YouTube is, and only then it can really speak to YouTube. A DNS Query is a special request, that goes to a predetermined set of servers, and basically says <br>
<div align="center" style="margin-top:5px; margin-bottom: 5px">
"Hey, what's the IP Address of youtube.com?"</i>
</div><br>
An <b>IP Address</b> is just a unique identifier for a machine. All computers connected to the internet, have ways to find public IP Addresses, or at least, they have ways to discover routes to those addresses. And that means that, they can send data to IP Addresses. They can send packets of information, in the form of bytes, to IP Addresses. You can almost think of an IP Address as a mailbox, that some entity has granted to a machine. <br><br>
<br><br><br><br>
<div align="center">3</div>
We can find ip address of any website using Terminal. Open the terminal, type 
<div align="center"><b>

```dig youtube.com```

</b></div>
This command allows us to do DNS Queries and then displays the answer in the terminal. This command gives the youtube.com's IP Address. And something very similar happens behind the scenes when in your browser, you type in youtube.com<br><br>
Now the browser having the IP address, knows how to communicate directly with the server of YouTube.<br><br><br>
<h3>2. How are we sending ?</h3>
Our browser sends an <b>HTTP request</b> to this IP Address. HTTP is a way to send information, that server can understand. So, when we say that a browser, or a client, sends an HTTP request to the YouTube servers, basically it sends a bunch of bytes, or characters, that are gonna get packed into what we call packets, in some special format, and then sent over to the YouTube servers.<br><br><br>
<h3>3. How are we getting the response ?</h3>
And that request is also gonna contain the IP Address of the browser, or the computer, and that's gonna be called as the source address of the request. And that's gonna be really important because when the server gets that request, it's gonna know what IP Address it should send a response to. So the YouTube server will use that <b>source IP Address</b>, which is contained in the HTTP request.<br><br>
So the server of YouTube now understands that when you go to youtube.com, you are trying to see the HTML of YouTube and it returns in its response to the client.
And the browser receives the response and then renders the HTML on the page.<br><br><br>
<blockquote><b>Every website you browse, is built on the client-server architecture.</b></blockquote>
A very small percent of the business websites and applications use the peer-to-peer architecture, which is different from the client-server. <br><br><br>
<b>Note:- </b> A single machine or piece of software can be both a client and a server at the same time. For instance, a single machine could act as server for end users and as a client for a database.<br><br><br>
<b>Can the server initiate communication in a client server, request-response model ?</b><br>
No, its always the client<br><br><br><br><br><br>
<div align="center">4</div>
<h2>Ports</h2>
Servers are machines that are waiting to receive requests from clients. A server usually listens for requests on specific ports. Any machine that has a distinct IP Address, has 16000 ports that programs on the machine can listen to. <br>
Let's have some anaolgy: <br>
<div align="center"><b>
IP address - apartment<br>
ports - individual flats
</b></div><br>
So as a client, when you are communicating with a server, you actually have to specify the port that you wanna communicate on. <br>
When we're talking about the Client-Server Model here, it turns out that most clients actually know the port that they should use, depending on the protocol that they are trying to speak to the server with.<br><br>
<table style="padding-left:190px">
<tr><th>protocol</th><th>port</th></tr>
<tr><td>HTTP</td><td>80</td></tr>
<tr><td>HTTPS</td><td>443</td></tr>
<tr><td>secure shell</td><td>22</td></tr>
<tr><td>DNS lookup</td><td>53</td></tr>
</table><br><br><br><br>
<h2>Let's Visualize</h2>
You can simulate this client and server communication experience by opening two terminals using nc. <b>Netcat</b> (or nc) is a command-line utility that reads and writes data across network connections, using the TCP or UDP protocols.<br>
a. In one terminal type <code>nc -l 8081</code> (listen on 8081) <br>
b. In the other terminal type <code>nc 127.0.0.1 8081</code>.= Here, 127.0.0.1 is a special ip &nbsp;&nbsp;&nbsp;addresss that always points to your local machine. <br><br>
This simulates a connection between the two terminals. Anything typed in the second terminal will be seen in the first.<br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">5</div>
<h1>Key Terms</h1>
<h2>CLIENT</h2>
A machine or process that requests data or service from a server.
<h2>SERVER</h2>
A machine or process that provides data or service from a client, usually by listening for incoming network calls.
<h2>CLIENT-SERVER MODEL</h2>
The paradigm by which modern systems are designed, which consists of clients requesting data or service from servers and servers providing data or service to clients.
<h2>IP ADDRESS</h2>
An address given to each machine connected to the public internet. IPV4 addresses consists of four numbers separated by dots: <b>a.b.c.d</b> where all four numbers are between 0 and 255. Special values include: <br>
- <b>127.0.0.1</b>: Your own local machine, also referred to as <b>localhost</b>.<br>
- <b>192.168.x.y</b>: Your private network. For instance your machine and all your machines on your private wifi network will usually have the 192.168 prefix.

<h2>DNS</h2>
Short for Domain Name System, it describes the entities and protocols involved in the translation from domain names to IP Addresses. Typically, machines make a DNS query to a well known entity which is responsible for returning the IP address (or multiple ones) of the requested domain name in the response.

<h2>PORT</h2>
In order for multiple programs to listen for new network connections on the same machine without colliding, they pick a port to listen on. A port is an integer between 0 and 65,535 (2<sup>16</sup> ports total). <br>
Typically, ports 0-1023 are reserved for system ports (also called well-known ports) and shouldn't be used by user-level processes. Certain ports have pre-defined uses, and although you usually won't be required to have them memorized, they can sometimes come in handy. Below are some examples: <br>
22: Secure Shell, 53: DNS lookup, 80: HTTP, 443: HTTPS <br>
<h2>HTTP Protocol</h2>
The entire communication happens over the HTTP protocol. It is the protocol for data exchange over the World Wide Web. HTTP protocol is a request-response protocol that defines how information is transmitted across the web. <br>
It’s a stateless protocol, and every process over HTTP is executed independently and has no knowledge of previous processes.<br><br><br><br>
<div align="center">6</div>
As we all know, proper communication is key for thriving relationships!
<h1 id="netpro" style="font-size:30px">Network Protocols</h1>
Set of rules for communication between two machines.<br>
The majority of network protocols are admittedly very low level.<br><br>
<h3>Q) What does a Network Protocol consists of?</h3>
A network protocol consists of the kinds of messages that are gonna be sent and received by machines, by clients and servers. The format of those messages, how they are structured, the order of those messages if they have an order, and whether or not there should be some sort of response to a message and if there should be, what that response should look like, whether or not there should be rules around when messages can be sent, all of that stuff. <br><br>
There are a lot of network protocols out there but very few that are very popular and that are important to know about. We are gonna cover specifically IP, TCP, and HTTP. <br><br><br>
<h1>Internet Protocol (IP)</h1>
<blockquote><b>Modern Internet Effectively runs on IP</b></blockquote>
When a machine(client) tries to interact with other machine(server) and it sends data to that machine. Then that data is sent in the form of <b>IP packets</b>.<br>
Let's talk about IP packets.<br><br>
- Fundamental units of data that is sent from one machine to another.<br>
- Building blocks of communication between machines over the internet.<br><br>

IP Packets are actually made up of bytes. <br>They have 2 main sections: IP Header and the Data.<br><br><br>
<h2>Header</h2>
IP Header is the section of an IP Packet that is gonna be at the beginning of the packet. It contains all the <b>information about the packet</b> and that is stored in bytes. It contains the source IP Address, destination IP Address.<br><br>
If you have a single IP Packet, you know where that IP Packet is coming from and where it is going to. This is how information flows over the network, on the internet. This is how information knows to go from one machine to another. Because all these IP Packets have the source and destination IP Addresses of the machines that they are coming from and going to. <br><br><br>
<div align="center">7</div>
The header also has other information like the total size of the packet, version of the Internet Protocol that this IP Packet is operating by. There are multiple versions of Internet Protocol and today, there are really 2 versions in practice. There's version 4 known as <b>IPV4</b>, this is really what most of the modern day internet uses, and then there's version 6, <b>IPV6</b> which is now being used more and more. Based on the IP version, the packet might look different. It might be structured a little differently, and a machine will know how it should interpret it based on that version.<br><br>
The header is very small, anywhere between 20 and 60 bytes, and then the rest of the IP Packet is the data part of the IP Packet. <br><br><br>
<h2>Data</h2>
In the data portion of the IP Packet, the information that a machine is trying to send to another machine is gonna be stored.<br><br>
Now IP Packets are limited in size. They are only 2<sup>16</sup> bytes(64 KB). That's really nothing. If you are sending information over the network, you could imagine you might be sending an email, or a big file, or an image.
You are gonna be sending way more than 64 KB. <br><br>
If you are sending information over the network <br>
&nbsp;&nbsp;&nbsp;&nbsp; => that information is likely not gonna fit in one IP packet. <br>
&nbsp;&nbsp;&nbsp;&nbsp; => it will fit into <b>multiple IP packets</b><br><br><br>
This is where things get complicated. When you have multiple IP packets that are sent from one machine to another, if all you are using is the Internet Protocol, then <br><br>
1. You don't actually have a way of guaranteeing that these packets are actually gonna be received. It's very possible that some of the packets are gonna get lost, over the network. And if that's the case, you won't have sent all of the data that you were trying to send. <br>
2. You are also not guaranteeing the order in which the packets will be read or interpreted, and that's obviously not great because you want your packets to be ordered correctly such that your original data is sent in the correct order and in the correct structure that it's meant to be sent in. <br><br>

So Internet Protocol alone kind of falls apart here. <br>
&nbsp;And this is where TCP comes into play. <br><br><br><br><br><br><br><br><br>
<div align="center">8</div>
<h1>Transmission Control Protocol (TCP)</h1>
TCP is built on top of the Internet Protocol. <br>
It's really meant to solve the issues that exists in the IP : <br>
<ul>
<li> It's meant to send IP Packets in an <b>ordered way</b>, meaning that you are guaranteeing the order in which the IP Packets will be read by the destination machine.</li>
<li>It's meant to send IP Packets in a <b>reliable way</b> meaning that you are guaranteed to get those packets actually received by the destination machine or at the very least you will know if some packets keep failing from getting received and in an error-free way.</li>
</ul><br>
If some IP Packets get corrupted for whatever reason when they are being sent over the network, you will know and you will be able to resend those packets to make sure that they're received in an uncorrupted way. <br>
This is what TCP aims to solve in a nutshell. <br><br>
An IP Packet has IP Header and the Data. In TCP, as TCP is built on top of IP, the IP Packet's data portion will have TCP Header and it contains the information about the ordering of the packets and some information about the packet.<br><br><br>
<h2>Communication in TCP</h2>
Now, the core idea behind TCP is that when a machine wants to communicate with another machine over TCP, it is first going to create a TCP connection with the destination machine. And the way that's gonna happen is through what's known as a <b>handshake</b>.<br><br>
A Handshake is a special TCP interaction where one computer basically contacts the other by sending a packet or a few packets saying "Hey, I wanna connect with you."
The other computer responds and says, "Okay, we can connect, we can chat." And then the client or the machine that was trying to establish the connection re-responds again and says, "Okay, we're now connected, we've got an open connection." And this is known as a Handshake. <br><br>
And then once the connection is established, both machines can freely send data to one another but there are few things that might be worth knowing.<br>
- if one of the two machines doesn't send data in a given amount of period, the connection can be timed out.<br>
- if one of the machines wants to end the connection for whatever reason, it can do so by sending some sort of special message to let the other one know that "Hey, I'm about to end the connection." and then the TCP connection is done.<br><br>

To summarize, TCP is basically a more powerful, and more functional wrapper around IP. But still what it lacks is a really robust framework that developers, software engineers can use to really define meaningful and easy to use communication channels for clients and servers in the system. Because with TCP, all that you're really sending is arbitrary data that fits into these underlined IP packets.<br>
And this is where HTTP comes into play.<br>
<div align="center">9</div>
<h1>Hypertext Transfer Protocol(HTTP)</h1>
HTTP is built on top of TCP. It introduces a higher level abstraction above TCP and of course IP.
And this abstraction is the <b>request-response paradigm</b>.<br><br>
So the HTTP protocol introduces this idea of having machines communicate with one another following this request-response paradigm where one machine sends request to another machine and that other machine returns a response to the first machine. And this request response paradigm with of course a set of accompanying rules makes it very easy for developers to create robust and easy to maintain systems. And so this is why most modern day systems rely on the HTTP protocol for communication.<br><br>
So with HTTP, we completely forget about IP packets, we forget about TCP. All that we deal with are HTTP requests and responses.<br><br><br>
Requests are gonna be the things that machines that wanna interact with other machines send. And these requests are gonna have a lot of properties defined by the HTTP protocol. The best way to really understand or rather appreciate the power and the rigor that HTTP gives you, is to try to visualize what these request and responses look like. One can think of them as objects with important fields or properties that describe them.<br>For example,<br>
Requests have fields such as url, port, method, headers, body etc.. <br>
Responses have fields such as status code, response body, headers etc.<br>
Headers are a collection of key value pairs that contain important metadata about the request or response.
<br><br><br>
If we go back to IP and TCP, those two protocols were more just for <b>transportation of data</b>. HTTP on the other hand introduces the opportunity to add a lot of <b>business logic</b> which is of course what you're gonna want if you're developing a large scale system or any kind of system to be honest. <br><br>
TP, TCP and HTTP are three very important protocols that basically any modern day system on the internet is gonna be relying on. IP and TCP are very very low level and you're typically not gonna be thinking about them much. HTTP is more relevant to you. 
<br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">10</div>
<h1>Key Terms</h1>
<h2>IP</h2>
Stands for Internet Protocol. This network protocol outlines how almost all machine-to-machine communications should happen in the world. Other protocols like TCP, UDP and HTTP are built on top of IP.
<h2>TCP</h2>
Network protocol built on top of the Internet Protocol (IP). Allows for <b>ordered, reliable</b> data delivery between machines over the public internet by creating a <b>connection</b>.
TCP is usually implemented in the kernel, which exposes sockets to applications that they can use to stream data through an open connection.
<h2>HTTP</h2>
The HyperText Transfer Protocol is a very common network protocol implemented on top of TCP. Clients make HTTP requests, and servers respond with a response.<br><br>
Requests typically have the following schema:<br>
<blockquote>
host: string (example: youtube.com)<br>
port: integer (example: 80 or 443)<br>
method: string (example: GET, PUT, POST, DELETE, OPTIONS or PATCH)<br>
headers: pair list (example: "Content-Type" => "application/json")<br>
body: opaque sequence of bytes
</blockquote><br>
Responses typically have the following schema:<br>
<blockquote>
status code: integer (example: 200, 401) <br>
headers: pair list (example: "Content-Length" => 1238)<br>
body: opaque sequence of bytes
</blockquote><br>
<h2>IP Packet</h2>
Sometimes more broadly referred to as just a (network) packet, an IP packet is effectively the smallest unit used to describe data being sent over IP, aside from bytes. An IP packet consists of:<br>
- an IP header, which contains the source and destination IP addresses as well as other information related to the network<br>
- a payload, which is just the data being sent over the network

<br><br><br><br><br><br><br><br>
<div align="center">11</div>
<h1 id="storage" style="font-size:30px">Storage</h1>
If you think of any system that you might wanna design, you're probably gonna realize that, your system is gonna require some form of storage.<br>
This is where databases come into play.<br><br>
<h2>Database</h2>
A database is a thing that really serves two primary purposes:<br>
- To <b>store/write/set/record</b> data<br>
- To <b>retrieve/read/get/query</b> data<br><br>

Now one common misconception about databases is thinking that a database is this magical opaque box that lives somewhere in the ether. What a database really is, there are of course some exceptions, but what a database almost always is, is just a server. It is just like any other machine/computer.<br><br><br><br>
One very important concept in storage and in databases is <b>persistence</b>.<br>
A lot of people take for granted that if they store data in a database, that data will persist through any kind of issue that might occur in your system. They assume that if you store data in a database and then there's a power outage or a network issue or your database server crashes, once everything is booted back up, that the data will still be there.<br><br>
And while that assumption is often fair because a lot of databases do ensure that data stored in them is gonna persist through outages or issues, it isn't always correct. And this leads us to two fundamental things in storage: Disk and Memory <br><br>
<h3>Writing data to Disk</h3>
If you have a database server, and that database writes data to disk, that <b>data will persist</b> even if the database server goes down. Writing data to disk is basically what happens when you save a file on your computer. If you shut down your computer afterwards or if your computer crashes, that file that you saved is still gonna be there unless there's some catastrophic issue with your hardware or some other exceptional issue that data, that file, is still gonna be there.<br><br><br><br><br><br><br><br><br><br><br>
<div align="center">12</div>
<h3>Writing data to Memory</h3>
In contrast, if your database writes data in memory, and this is what happens when for instance you've got your server code and you have maybe an array or a hash table declared in your server code and you store data in that array or in that hash table if that server goes down, if your database server goes down, and then gets booted back up, the array or the hash table in which you might have stored data is <b>no longer gonna have that data</b>.
That's what it essentially means to store data in memory.<br><br><br><br>
<h3>Q) Why you'd ever want to use memory instead of disk ?</h3>
The simple reason is that reading data from memory or writing data in memory is much faster than reading data from disk or writing to disk.<br><br><br>
You can imagine if your database goes down, because your database is such a critical part of your system, then your entire system effectively goes down. <br>
And so then this brings us to the topic of distributed storage which adds further complexity as we have to maintain consistency throughout. <br><br><br>
There are hundreds of database offerings out there and each of them can give us certain properties or certain gurantees but will tradeoff others. <br><br><br><br> <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">13</div>
<h1>Key Terms</h1>
<h2>DATABASE</h2>
Database is a program that either use disk or memory to do 2 core things: record data and query data. In general, they are themselves servers that are long lived and interact with the rest of your application through network calls, with protocols on top of TCP or even HTTP.
<h2>DISK</h2>
Disk Usually refers to either HDD (hard-disk drive) or SSD (solid-state drive). Data written to disk will persist through power failures and general machine crashes. Disk is also referred to as <b>non-volatile storage</b>.
<h2>MEMORY</h2>
Short for Random Access Memory (RAM). Data stored in memory will be lost when the process that has written that data dies.
<h2>PERSISTENT STORAGE</h2>
Usually refers to disk, but in general it is any form of storage that persists if the process in charge of managing it dies.<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">14</div>
If you've ever experienced lag in a video game, it was most likely due to a combination of high latency and low throughput. And lag sucks.
<h1 id="landt" style="font-size:30px">Latency And Throughput</h1>
Two most important measures of the performance of a system.<br><br>
<h2>Latency</h2>
It is basically<br>
- how long it takes for data to traverse a system.<br>
- how long does it take for data to get from one point in a system, to another point in a system.<br><br>

The latency of a network request is how long does it take for one request to go from a client to a server, and then back from the server to the client. The time that it's gonna take to read data from memory or disk is also gonna be referred to as latency. The most important aspect of latency is the fact that these<br> 
<div align="center"><b><i>
different things in systems have different latencies.
</i></b></div><br><br><br>
Some examples of latencies of various operations : <br>
Reading 1 MB sequentially from memory RAM: &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;250 µs (0.25 ms) <br>
Reading 1 MB sequentially from SSD:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1,000 µs (1 ms) <br>
Transfer 1 MB over 1 GB/s Network: &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;10,000 µs (10 ms) <br>
Reading 1 MB sequentially from HDD:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 20,000 µs (20 ms)<br>
Sending a pakcet(<<1 MB) over network for round trip <br> between California and Netherlands: 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;150,000 µs (150 ms)<br><br>
> When you are gonna be designing systems, you're typically going to optimize those systems, by lowering the overall latencies of the systems.<br><br>

<div align="center"><b>low latency => faster data transfers</b></div>
<br>
<h2>Throughput</h2>
Throughput is how much work a machine can perform in a given period of time.<br><br>
When we talk about throughput, and we talk about this amount of work that a computer or machine can perform in a given amount of time, we're really referring to how much data can be transferred from one point in a system to another point in a system, in a given amount of time.<br>
And so typically, we measure this throughput, in gigabits per second, or kilobits per second, megabits per second.
<br><br><br><br><br>
<div align="center">15</div>
Even though both are related to systems performance, <br>&nbsp;they're not necessarily correlated.<br><br><br><br><br>
<h1>Key Terms</h1>
<h2>LATENCY</h2>
The time it takes for a certain operation to complete in a system. Most often this measure is a time duration, like milliseconds or seconds.
<h2>THROUGHPUT</h2>
The number of operations that a system can handle properly per time unit. For instance the throughput of a server can often be measured in requests per second (RPS or QPS).
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">16</div>
<h1 id="avail" style="font-size:30px">Availability</h1>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">
<h2><i>The content isn't available on this page<br>
Try checking on next page</i></h2>
</div>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">17</div>
One way to think about it is how resistant a system is to failures.<br>
For instance, <br>
- what happens if a server in your system fails?<br>
- What happens if your database fails? <br>
- Is your system gonna completely go down or your system still gonna be operational?

And this is often described as a <b>system's fault tolerance</b>, how fault tolerant is a system ? <br><br><br>
Another way to think about availability is, as the <b>percentage of time in a given period of time</b>, like a month or a year, where the system is at least operational enough such that all of its primary functions are satisfied.<br><br><br>
Availability is a very important thing to think about when evaluating a system.<br>And in this day and age, especially, most systems almost have an implied guarantee of availability.<br><br>
<h2>How do you measure Availability?</h2>
We typically measure availability as the percentage of a system's uptime in a given year.
So, for instance, if a system is up and operational for half of an entire year, then you would say that that system has 50% availability.<br><br>
When we're dealing with availability, we're usually <b>dealing very, very high percentages</b>. Even an availability of 90% isn't really great. If you do the math, it means that your system is gonna be down about 35 or 36 days out of the year. So what that means is that in the industry, most services or most systems aim for really high availabilities and so we often end up measuring availability not exactly in percentages but rather in what we call nines.<br><br><br>
<h2>Nines</h2>
Nines are effectively percentages but they are specifically percentages with the number nine.
If you have a system that has 99% availability, meaning that it is up 99% of the time during a year.
Then, we say that your system has two nines of availability because literally the number nine appears two times in this percentage.<br><br>
If your system has 99.9% availability&nbsp; => three nines of availability. <br>
If your system has 99.99% availability => four nines of availability <br>
... <br>
and so on and so forth. And this is really the standard way that people talk about availability in the industry.
<br><br>
Five nines of availability is typically regarded as the <b>gold standard of availability</b>. If your system has five nines of availability, then we would really say that it is a highly available system (HA).<br><br><br>
<div align="center">18</div>
For certain systems, you don't have an implied guarantee of availability, you have an explicit guarantee of availability. Many service providers out there have SLAs.<br><br>
<h2>Service-Level Agreement (SLA)</h2>
SLA is an agreement between a service provider, basically the people who are behind the service or system that is being sold or provided, and the customers or end users of this service or of this system, an agreement on that system's availability amongst other things. SLAs are taken very serious. And if the service provider fail to do so, they have to payback.<br><br><br>
So many service providers out there have these explicit written SLAs, that basically tell customers<br>
<div align="center">
<b>"Hey, we guarantee you this amount of availability."</b>
</div><br><br>
SLO stands for <b>service-level objective</b>. SLO can be considered as components of SLA. In other words a service-level agreement is made up of service-level objectives. <br><br><br>
When designing systems, you're gonna have to ask yourself: "What parts of my system are absolutely critical?" Well, not necessarily critical but are critical to the point that they require high availability. And what parts of my systems don't actually require high availability? What parts of my systems would be okay to fail? That's gonna be something that you'll have to think about.<br>
<b>Eg:-</b> For payments(stripe), we need high availability.<br><br><br>
<h2>How do you improve Availability?</h2>
Distributed systems became mainstream with large-scale applications solely because, in them, we can eliminate the   <b>single points of failure</b>: Single places in your system that if they fail cause your entire system to fail. <br><br>
And how do you eliminate single points of failure? Answer is Redundancy. Redundancy is basically the act of duplicating or triplicating or multiplying even more certain parts of your system.<br>
Eg:- multiple servers, multiple load balancers etc...<br><br><br>
The point is that you can introduce redundancy in a lot of different parts of your system just by literally adding machines to those parts of your system.
<br><br><br><br><br><br><br><br><br><div align="center">18</div>
<h3>Passive Redundancy</h3>
When you have multiple components at a given layer in your system. And if at any point one of those components dies, nothing's really gonna happen.
The other components are basically gonna be able to continue running smoothly with the increased load.<br>
<b>Eg</b>:- Engines of an aeroplane<br><br>
<h3>Active Redundancy</h3>
Active redundancy is a little bit more complicated.<br>
When you have multiple machines that work together in such a way that only one or few of the machines are gonna be typically handling traffic or doing work. And if one of the ones that is handling traffic or doing work fails, the other machines are gonna somehow know that that other one failed and they're gonna take over.<br><br>
Netflix uses Chaos Monkey, which is responsible for randomly terminating instances in production to ensure that engineers implement their services to be resilient to instance failures. <br><br><br><br><br><br><br><br><br><br> <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><div align="center">21</div>
<h1>Key Terms</h1>
<h2>AVAILABILITY</h2>
The odds of a particular server or service being up and running at any point in time, usually measured in percentages. A server that has 99% availability will be operational 99% of the time (this would be described as having two nines of availability).
<h2>HIGH AVAILABILITY</h2> 
Used to describe systems that have particularly high levels of availability, typically 5 nines or more; sometimes abbreviated "HA".
<h2>NINES</h2>
Typically refers to percentages of uptime. For example, 5 nines of availability means an uptime of 99.999% of the time. Below are the downtimes expected per year depending on those 9s: <br>
- 99% (two 9s): 87.7 hours <br>
- 99.9% (three 9s): 8.8 hours <br>
- 99.99%: 52.6 minutes <br>
- 99.999%: 5.3 minutes<br>

<h2>REDUNDANCY</h2>
The process of replicating parts of a system in an effort to make it more reliable.
<h2>SLA</h2>
Short for "service-level agreement", an SLA is a collection of guarantees given to a customer by a service provider. SLAs typically make guarantees on a system's availability, amongst other things. SLAs are made up of one or multiple SLOS.
<h2>SLO</h2> 
Short for "service-level objective", an SLO is a guarantee given to a customer by a service provider. SLOs typically make guarantees on a system's availability, amongst other things. SLOs constitute an SLA.
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">19</div>
<h1 id="cache" style="font-size:30px">Caching</h1>
Caching is used in a lot of algorithms. The reason is to typically avoid redoing the same operations, especially computationally complex operations that might take a lot of time, multiple times. So caching is used to improve the time complexity of the algorithms, to speed up the algorithms. <br><br><br>
And in the context of systems design, caching is actually pretty similar. To put it simply, caching is used to <b>speed up a system</b>. Caching is used to reduce or to improve the latency of a system.<br><br>
- Caching is going to be a way to design a system in such a way that, if we were originally gonna be using types of operations or data transfers that take a lot of time, like for example, network requests, we're gonna design a system in such a way that we don't have to do those network requests, and we can do different types of operations or different types of data transfers that are going to be faster. <br><br>
- Caching is storing data in a location that's different from the one where the data originally is, such that it's faster to access this data from this new location.<br><br><br>

<div align="center"><b>
Caching is key to the performance of any kind of application.<br> It ensures low latency and high throughput.
</b></div><br><br>
Caching will enable you to make vastly better use of the resources you already have as well as making otherwise unattainable product requirements feasible.<br><br><br>
<h2>Where can we use Caching ? </h2>
Caching can be used at different places in a system. For instance, you can cache at the client level. So that the client caches some data such that it no longer has to go to the server to retrieve it. Similarly, you could cache at the server level. Maybe you need the client to always interact with the server, but maybe the server doesn't always need to go to the database to retrieve data. Maybe it only needs to go to the database once and we can have some form of cache here at the server level.<br><br>
You could also have a cache in-between two components in a system. So maybe you could have a cache in-between a server and a database. In fact, you can even have caching at the hardware level. Now, perhaps this is less important in the context of Systems Design interviews, but it's still good to know about this. There is actually a lot of caching that happens at the hardware level in modern-day computers. For example, there's CPU caches, which are caches, as the name implies, that live at the CPU level, that basically make it faster to retrieve data from memory.
<br><br><br><br><div align="center">25</div>
It is good to know that caching can occur, or occurs by default, at many different levels of a system.<br><br><br>
<b>Note</b>:- Though caching is performed to speed up the slow operations, We can also use it incase of normal operations, not to speed them up individually but to avoid doing them multiple number of times because it might affect your system in other ways like increased load etc...  <br><br><br>
<blockquote><b>
Are <i>Cache</i> and <i>Database</i> the two sources of truth ?
</b></blockquote><br>
<h1>Caching dynamic data</h1>
With caching, we can cache both the static and the dynamic data. Dynamic data changes more often and has an expiry time or a TTL (Time to live). After the TTL ends, the data is purged from the cache, and the newly updated data is stored in it. This process is known as <b>cache invalidation</b>.<br><br>
Though the data TTL should be long enough to make effective use of caching, caching won’t help much if the data changes too often, for instance, the price of a stock, the score of a cricket or a baseball match.<br><br><br><br>
<h1>Editing cache data</h1>
<h2>Write Through Cache</h2>
A type of caching system where when you write a piece of data, your system will write that piece of data both in the cache and in the main source of truth (Database) at the same time, or rather in the same operation.<br> That way the <b>cache and the database are always in sync</b>. (consistency)<br><br>
Now the down side to this is that you end up having to still go to the database.<br>
So, a little latency will be added.<br><br><br>
<h3>Write-around cache</h3>
This technique is similar to write-through cache, but data is written directly to permanent storage, bypassing the cache. This can reduce the cache being flooded with write operations that will not subsequently be re-read, but has the disadvantage that a read request for recently written data will create a “cache miss” and must be read from slower back-end storage and experience higher latency.<br><br><br><br><div align="center">26</div>
<h2>Write Back Cache</h2>
A type of caching system where when you write a piece of data, your system will write that piece of data in the cache only and completion is immediately confirmed to the client.<br>
So now your <b>cache will actually be out of sync with your database</b>.<br><br>
Behind the scenes, your system will asynchronously update the database with the values that are stored in the cache.
And this can be done in different ways. Maybe it's on certain intervals or on cache eviction.<br><br>
One of the downsides here is that if something ever happens to your cache and you lose the data in the cache, for instance, before the database has been updated asynchronously, then you're gonna lose data and that's really bad.<br><br><br>
Lastly,for immutable data, Caching is beautiful.<br>
for mutable data, things gonna get trickier.<br><br><br><br>
<h2>Concept of Staleness</h2>
Say we have a bunch of servers and every server has a cache inside it. If for an operation, the cache of the first server got updated but the cache of the other servers are not updated yet, then the clients dealing with the other servers will be dealing with the stale versions of data. That would not be good. <br><br>
In this particular system (where staleness is considered), a solution would be to move our cache out of the servers and to put our cache, a single cache. Maybe this would be Redis. And all of the servers would hit the cache and we'd have this single source of truth for the caching mechanism.<br><br><br>
Example where staleness of data is considered: Comments on a YouTube video<br>
Example where staleness of data is not considered: Views on a YouTube video<br><br>
<br><br>
<h2>Eviction policy in Caching</h2>
We do not have infinite space, so there is a limit for the amount of data stored in cache. To get rid of that data, we can use Least Recently Used policy (LRU), Least Frequently Used policy (LFU), Last in First out (LIFO), First in First out (FIFO), randomly etc..... depending on the usecase you are designing.
<br><br><br><br><br><br><div align="center">27</div>
<h2>Some important points about Caching</h2>
- It should be implemented wisely. If not, it can cause data inconsistency issues.<br>
- It can be used at any layer of the application, with any component and there are no<br>&nbsp; ground rules as to where it can and cannot be applied.<br>
- <b>Key-value data stores</b> are primarily used to implement caching in web applications.<br>
- The most common usage of caching is database caching.<br>
- It is also the core of the HTTP protocol. We can store user sessions in a cache.<br>

<br><br><br><br>
<h2>Content Delivery Network (CDN)</h2>
Content Delivery (or Distribution) Network's are a kind of cache that comes into play for <b>sites serving large amounts of static media</b>. In a typical CDN setup, a request will first ask the CDN for a piece of static media; the CDN will serve that content if it has it locally available. If it isn’t available, the CDN will query the back-end servers for the file, cache it locally, and serve it to the requesting user.<br><br>
If the system we are building is not large enough to have its own CDN, we can ease a future transition by serving the static media off a separate subdomain (e.g., static.yourservice.com) using a lightweight HTTP server like Nginx, and cut-over the DNS from your servers to a CDN later.<br><br><br><br><br>
<b>What do a punching bag and a cache have in common?</b><br>
They can both take a hit! <br><br><br><br><br><br>
Following links have some good discussion about caching:<br>
[1] <a href="https://en.wikipedia.org/wiki/Cache_(computing)">Cache</a><br>
[2] <a href="https://lethain.com/introduction-to-architecting-systems-for-scale/">Introduction to architecting systems</a> <br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">28</div>
<h1>Key Terms</h1>
<h2>CACHE</h2>
A piece of hardware or software that stores data, typically meant to retrieve that data faster than otherwise.
Caches are often used to store responses to network requests as well as results of computationally-long operations.
<h2>CACHE HIT</h2>
When requested data is found in a cache.
<h2>CACHE MISS</h2>
When requested data could have been found in a cache but isn't. <br>This is typically used to refer to a negative consequence of a system failure or of a poor design choice. For example:
If a server goes down, our load balancer will have to forward requests to a new server, which will result in cache misses.
<h2>CACHE EVICTION POLICY</h2>
The policy by which values get evicted or removed from a cache. Popular cache eviction policies include LRU (least-recently used), FIFO (first in first out), and LFU (least-frequently used).
<h2>CONTENT DELIVERY NETWORK</h2>
A CDN is a third-party service that acts like a cache for your servers. Sometimes, web applications can be slow for users in a particular region if your servers are located only in another region. A CDN has servers all around the world, meaning that the latency to a CDN's servers will almost always be far better than the latency to your servers. A CDN's servers are often referred to as POPs (Points of Presence). Two of the most popular CDNs are Cloudflare and Google Cloud CDN.<br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">23</div>
<h1 id="proxy" style="font-size:30px">Proxies</h1>
When people use the term proxy, they often mean forward proxy.<br><br>
<h2>Forward Proxy</h2>
A forward proxy is a server that sits in between a client or a set of clients and another server or a set of other servers. But more specifically a forward proxy is a server that acts on behalf of the client(s).<br><br>
In practice, what this means is that if a client wants to communicate with a server, assuming the forward proxy has been configured correctly by the client, when the client is gonna issue a request to the server, instead of going directly to the server, it's first gonna go to the forward proxy, which then is gonna forward the request to the server.<br><br><br>
It's almost like the client is saying,<br>
<div align="center"><h3>"hey forward proxy, communicate with the server on my behalf please."</h3></div><br><br>
And when the server responds, it's gonna give its response to the forward proxy and then it will be forwarded to the client<br><br><br>
<h2>Why to use it ?</h2>
A forward proxy can serve as a way to <b>hide the identity of a client</b> that's requesting something from a server. Because the source IP address in the request going to the server is going to be the IP address of forward proxy and not that of the client. <br><br>
This is basically how <b>VPN</b>s work in a simplified way. It's a forward proxy. This means that a client might be able to access restricted servers that it's otherwise not supposed to access because the forward proxy might hide who this client really is. So this is how you might be able to access websites that are unavailable in your country, or that are restricted by your organization using a forward proxy.<br><br><br><br>
In an interaction between a client and a server,<br>
&nbsp;&nbsp;&nbsp;forward proxies act on behalf of clients whereas <br>
&nbsp;&nbsp;&nbsp;reverse proxies act on behalf of a server. <br><br>
<br><br><br><br><br>
<div align="center">23</div>
<div align="center">
<img  src="https://raw.githubusercontent.com/saivault/dsanotes/main/store/forwardreverse.png" height="230" width="500">
</div><br><br>
<h2>Reverse Proxy</h2>
If the client wants to send a request to the server, if the reverse proxy has been configured properly by the server or by the entity that owns the server, then when the client is gonna issue a request to the server, the request is actually gonna go to the reverse proxy. Then the reverse proxy is going to forward the request to the server then the server is gonna return a response to the reverse proxy and finally the reverse proxy is gonna return the response to the client.<br><br>
The key thing here is that client won't know that its request is going to a reverse proxy and thinks that it's interacting with the server. Even the DNS query will return the IP address of the reverse proxy. <br><br><br>
In forward proxy, it's the server that has no idea that the client and the forward proxy are kind of one and the same.<br>
Whereas with the reverse proxy, it's the client that has no idea that the reverse proxy and the server are effectively one and the same. <br><br><br>
<h3>Can a forward proxy act as a reverse proxy?</h3>
Simply put, a forward proxy server cannot act as a reverse proxy server. Even if these proxies concepts may be similar, they are utilized for entirely different purposes.<br><br>
A proxy by itself is not only an IP address. Proxies consist of IP addresses and dedicated software that allows them to operate in the intended manner.<br>
As forward and reverse proxies are used for different tasks, they each have different software to perform smoothly. This is the reason why you cannot use forward proxies as reverse proxies.<br><br><br><br><br>
<div align="center">24</div>
<h2>Uses of Reverse Proxy</h2>
Now reverse proxies are really useful because you can do a lot with them.<br><br>
<ul>
<li><b>Anonymity</b><br> They serve as an additional level of protection for backend servers.</li>
<li><b>Filtering requests</b><br> For instance, you might configure your reverse proxy such that it can filter out requests that you want to ignore.
Maybe for your system you don't want your servers to ever deal with certain kinds of requests so you can have your reverse proxy, kind of filter them out.</li>
<li><b>Logging</b><br> If you wanna log stuff, if you wanna gather metrics, maybe your reverse proxy can do that.</li>
<li><b>Caching</b><br> A reverse proxy is capable of caching data that is commonly requested. Businesses that store a lot of pictures and videos may also speed up the performance of their websites by caching this content and reducing the load on the internet servers.</li>
<li><b>Load Balancer</b><br> One of the best use cases of a reverse proxy. In a sentence, a load balancer is something like a server that is gonna effectively distribute the request load between a bunch of servers.</li>
</ul>

<br><br><br><br><h1>Key Terms</h1>
<h2>FORWARD PROXY</h2>
A server that sits between a client and server and acts on behalf of the client, typically used to mask he client's identity (IP Address). Note that forward proxies are often referred to as just proxies.
<h2>REVERSE PROXY</h2>
A server that sits between clients and servers and acts on behalf of the servers, typically used for logging, load balancing, or caching.
<h2>Nginx</h2>
Pronounced "engine X", not "N jinx". Njinx is a very popular webserver that's often used as a reverse proxy and load balancer. Learn more https://www.nginx.com/
<br><br><br><br>
<div align="center">25</div>
<h1 id="lb" style="font-size:30px">Load Balancers</h1>
Relentlessly distributing network requests across multiple servers, these <b>digital traffic cops</b> act as watchful guardians for your system, ensuring that it operates at peak performance day and night.<br><br><br>
<h2>Understanding Load balancers</h2>
Let's look at a simple use case. <br><br>
For example, let's assume there's a client and a server. The client issues requests and the server responds to the client. Imagine what would happen if our system became a little bit bigger? In other words, imagine instead of having one client issuing a request to our server, we had multiple clients, so maybe 2, 3 or 4 clients, all of them issuing requests to this server.
<br><br> And you could imagine that one of our clients might be issuing more than one request, one of our clients might be issuing a lot of requests. Our single server has limited resources. Our system has limited throughput. Our single server can only handle a limited amount of requests in a given amount of time.<br><br>
So what that means is that the more requests are being sent to the server, the more likely our server is to become overloaded, to receive more requests than it can handle. And that might lead to a failure in our system or maybe it'll just make our system very slow.<br><br><br>
<h3>So how do we handle this?</h3>
Well, the simple answer is, we scale our system.<br>
vertical scaling&nbsp;&nbsp; : increase the power of our single server <br>
horizontal scaling : add more servers to our system. <br><br>
But as you can imagine, vertical scaling is going to be limited, there's only so much that we can do to increase the power or the performance of a single server/machine.<br><br>
So, horizontally scaling our system seems like a pretty obvious solution because if we have, let's say, 4 servers, we can now handle all of the requests from our clients in a balanced way. And assuming that our servers have the same resources, have the same power, our system will be able to handle four times the load that it was previously able to handle with only one server.<br><br>
But of course, this is assuming that all of our clients are going to be issuing requests to our servers in a balanced way. But this begs the question, <br><br><br><br><br>
<div align="center">26</div>
<h3>How did our clients know to issue their requests or rather to direct their requests to the servers in a balanced way?</h3><br>
How come none of the clients issued their requests to the same server leading to the same problem that we had before?
<br>And this is of course where load balancers come into play.<br><br><br>
<h1>Load Balancer</h1>
A load balancer may not be required if a service entertains a few hundred or even a few thousand requests per second. But when millions of requests arrived per second in a typical data center, to serve these requests, servers should work together to share the load of incoming requests with the help of a load balancer.<br><br>
A load balancer is a server that sits in between a set of clients and a set of servers and that basically has the <b>job of balancing workloads across the resources</b>. It is the first point of contact within a data center after the firewall.<br><br>
What would happen in our example with the load balancer is that our clients would be issuing requests, that would go to the load balancer. And then the load balancers' job would be to <b>redirect these requests in a balanced way</b> or in some preconfigured way. So now, the traffic is evenly distributed among the pool of available servers.<br><br>
<br>Here’s an abstract depiction of how load balancers work:
<div align="center" style="padding-bottom:10px">
<img src="https://raw.githubusercontent.com/saivault/dsanotes/main/store/loadbalancer.png" width="480" height="250">
</div><br>
Also with load balancers, our system will become more flexible as we can easily add or remove machines transparently on the fly.<br><br><br><br>
<div align="center">27</div>
However, for increasing client requests, load balancers provide the following capabilities:<br>
<li style="padding-top:10px"><b>Scalability:</b> By adding servers, the capacity of the application/service can be increased seamlessly. Load balancers make such upscaling or downscaling transparent to the end users.</li>
<li style="padding-top:10px"><b>Availability:</b> Even if some servers go down or suffer a fault, the system still remains available. One of the jobs of the load balancers is to hide faults and failures of servers. If a server is not available to take new requests or is not responding or has elevated error rate, LB will stop sending traffic to such a server.</li>
<li style="padding-top:10px"><b>Performance:</b> Load balancers can forward requests to servers with a lesser load so the user can get a quicker response time. This not only improves performance but also improves resource utilization. </li>
</ul><br><br>
<h2>Placing load balancers</h2>
Generally, LBs sit between clients and servers. Requests go through to servers and back to clients via the load balancing layer. However, that isn’t the only point where load balancers are used.<br><br>
Let’s consider the three well-known groups of servers. That is the web, the application, and the database servers. To divide the traffic load among the available servers, load balancers can be used between the server instances of these three services in the following way:<br><br>
- Place LBs between end users of the application and web servers/application gateway.<br>
- Place LBs between the web servers and application servers that run the<br>&nbsp; business/application logic.<br>
- Place LBs between the application servers and database servers.<br><br>

<img src="https://raw.githubusercontent.com/saivault/dsanotes/main/store/allloadbalancers.png" width="680" height="250"><br><br><br>
<div align="center">28</div>
In reality, load balancers can be potentially used between any two services with multiple instances within the design of a system.
<br><br><br>
<h3>As a reverse proxy</h3>
And by the way, you can think of load balancers as types of reverse proxies most of the time because load balancers sit between clients and servers, and they typically act on behalf of these servers, which is exactly what a reverse proxy does.<br><br><br>
<h3>Where can we use load balancing ?</h3>
Load balancing can happen at a lot of different places in the system. For instance, you can have a load balancer between the clients and servers, another one between the servers and databases or when dealing with a website, you might even have load balancing at the DNS layer. Well, it turns out that there's something called DNS Round Robin, which is basically a type of load balancing that happens at the DNS layer, where a single domain name gets multiple IP addresses. And when a DNS query is made to get back IP address of that domain name, the multiple IP addresses that are associated with that domain name are going to be returned in a load balanced way.<br><br><br>
<h3>How does the load balancer choose the backend server?</h3>
Load balancers consider two factors before forwarding a request to a backend server. They will first ensure that the server they choose is actually responding appropriately to requests and then use a pre-configured algorithm to select one from the set of healthy servers. We will discuss these algorithms shortly.<br><br><br>
<h3>Health Checks</h3>
Load balancers should only forward traffic to “healthy” backend servers. To monitor the health of a backend server, “health checks” regularly attempt to connect to backend servers to ensure that servers are listening. If a server fails a health check, it is automatically removed from the pool, and traffic will not be forwarded to it until it responds to the health checks again.<br><br>
Load balancers use the heartbeat protocol to monitor the health and, therefore, reliability of end-servers. The heartbeat protocol is a way of identifying failures in distributed systems. Using this protocol, every node in a cluster periodically reports its health (heartbeat message) to a monitoring service to show that it is still alive and functioning.<br><br><br><br><br><br><br><br><br>
<div align="center">27</div>
<h3>Types of load balancers</h3>
Software load balancers and Hardware load balancers. <br>
Hardware load balancers are literally physical machines that are dedicated to load balancing.
The main difference between hardware load balancers and software load balancers is that you can do more with software load balancers, you have more power over customization and scaling with software load balancers.
With hardware load balancers, you're limited to the hardware that you're given. And hardware is often expensive.<br><br>
We will look at software load balancers and the techniques that software load balancers use to distribute traffic to servers.<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">27</div>
<h1>How to distribute the load ?</h1>
Does it follow a special algorithm? Does it do so randomly?<br>
Firstly, You have to make your load balancer such that when you add a new server or when you remove an old server, it registers /  deregisters itself with the load balancer correspondingly, so that the load balancer knows of its existence.<br><br>
There are a lot of different ways to select servers to send traffic.<br><br>
<h2>1. Pure random redirection</h2>
possible that one server would by chance get overloaded.<br><br><br>
<h2>2. Round Robin approach</h2>
A method that goes through all of your servers in one order. And so as you can imagine, that's pretty nice because you guarantee that you will be evenly distributing traffic across your servers. So this is a slightly preferred way.<br><br>
A slightly more complex type of Round Robin strategy is called a Weighted Round Robin, where you basically place weights on specific servers, meaning you would still follow the order of going to the first one first, then the second one, then the third one. But you might put a weight on, let's say, the second server, which would mean that when your load balancer is redirecting traffic to your second server, it's going to redirect a couple more requests, a little bit more traffic than it redirects to the other servers. And you could imagine that you might want to do that if, let's say, some of your servers are more powerful than the others.<br><br><br>
<h2>3. Based on performance or load</h2>
This strategy is a little bit more involved. Basically, your load balancer performs health checks on your servers to know how much traffic a server is handling at any given time, how long a server is taking to respond to traffic, how many resources a server is using, and based on that, it'll redirect traffic accordingly.<br><br><br>
<h2>4. Based on IP addresses</h2>
Basically, when your load balancer gets requests from clients, it's going to <b>hash</b> the IP address of the clients, and depending on the value of the hash, it will redirect the traffic accordingly.<br><br>
IP-based load balancing can be really useful if you've got for instance, caching going on in your servers.<br><br><br><br>
<div align="center">28</div>
You could imagine that within your system you're caching the results of requests in your servers, it would be very helpful to have requests from a specific client always be redirected to the server in which the response of that particular client's request has been cached.
And that can be accomplished through this IP-based load balancing.
IP-based load balancing can help you maximize cache hits.<br><br><br>
<h2>5. Based on path</h2>
With this strategy, a load balancer basically distributes requests to servers according to the path of the requests.<br>
<b>Eg</b>:- download functionality to a server or a set of servers,<br>
handling payments to a server or a set of servers etc..<br><br><br>
<h2>6. Least connections</h2>
In certain cases, even if all the servers have the same capacity to serve clients, uneven load on certain servers is still a possibility. For example, some clients may have a request that requires longer to serve. Or some clients may have subsequent requests on the same connection. In that case, we can use algorithms like least connections where newer arriving requests are assigned to servers with fewer existing connections.<br><br><br><br>
And you're likely to even have multiple load balancers at the same part of a system because as you might be wondering, <br><br>
<h3>what happens if a load balancer starts to get overloaded? </h3>
Well, this is where you could have a second load balancer or even a third load balancer.
These load balancers could communicate between each other, and depending on that, reroute traffic accordingly.<br>
And each of the load balancers monitors the health of the other.<br><br>
Ultimately, load balancers are very simple, but they're extremely important.<br><br><br><br>
<h3>how does a load balancer even know that it has servers to distribute traffic to?</h3>
When a new server is added, how does it know that this new server is something that it should redirect traffic to ??
<br><br>And this is where basically, the people who are in charge of the system can configure the load balancer to know about the servers. Like registering server with the load balancer when added and deregistering it when removed so that load balances knows of its existence.<br><br><br><br>
<p>Following links have some good discussion about load balancers:<br>
[1] <a href="https://avinetworks.com/what-is-load-balancing/" target="_blank">What is load balancing</a><br>
[2] <a href="https://lethain.com/introduction-to-architecting-systems-for-scale/" target="_blank">Introduction to architecting systems</a><br>
[3] <a href="https://en.wikipedia.org/wiki/Load_balancing_(computing)" target="_blank">Load balancing</a></p>
<br><br><br>
<div align="center">29</div>
<h1>Key Terms</h1>
<h2>LOAD BALANCER</h2>
A type of reverse proxy that distributes traffic across servers. Load balancers can be found in many parts of a system, from the DNS layer all the way to the database layer.
<h2>SERVER-SELECTION STRATEGY</h2>
How a load balancer chooses servers when distributing traffic amongst multiple servers. Commonly used strategies include round-robin, random selection, performance-based selection (choosing the server with the best performance metrics, like the fastest response time or the least amount of traffic), and IP-based routing.
<h2>HOT SPOT</h2>
When distributing a workload across a set of servers, that workload might be spread unevenly. This can happen if your sharding key or your hashing function are suboptimal, or if your workload is naturally skewed: some servers will receive a lot more traffic than others, thus creating a "hot spot".<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">29</div>
<h1 id="hash"  style="font-size:30px">Hashing</h1>
Hashing is an action that you can perform to transform an arbitrary piece of data into a fixed size value, typically an integer value.<br><br><br>
<h2>Where exactly does hashing come into play in a system?</h2>
Well for that, we can look at a pretty simple example.<br>
We've got a fairly simple system consisting of clients, 4 clients in this case C1, C2, C3, C4. These clients are going to be speaking with servers, four servers, A, B, C, and D. But there's gonna be a load balancer in the middle. So when the clients are gonna issue requests, these requests are first gonna go to the load balancer which is then gonna have to reroute them to the four servers.<br><br>
When a load balancer has to redirect or reroute a request from a client to a server, it has to have some sort of server selection strategy (such as ramdom selection of servers, round robin approach etc.) to pick what server to reroute that request to. And while a lot of these server selection strategies are fine at face value, they can introduce some problems depending on your system. Let's assume, requests that are computationally expensive are gonna hit the servers and the servers have to perform very complex operations that take a long time to complete and so these requests are just so expensive.<br><br>
One way to deal with these kinds of requests in a system is to use <b>Caching</b>. So one way to implement caching here would be to have every server store an in-memory cache where every request that goes through a server, the server first checks if that request's response has been cached. If it hasn't been, then it actually performs the operations and gets the response. But if it has been cached, then it skips the operations that it would otherwise have to do and then immediately returns the cache response. That would be a pretty reasonable way to design your system if you knew that these requests were gonna be very computationally expensive.<br><br>
If you've designed your system in such a way that it relies heavily on in-memory caches in its servers, but your load balancer is rerouting requests from clients following a server selection strategy that doesn't guarantee that requests from a single client or the same requests will be rerouted to the same server every time, then your in-memory caching system is gonna fall apart as you're gonna miss a bunch of cache hits when your requests get routed to a server that doesn't have the responses cached.<br><br>
And this is where hashing comes into play.
<br><br><br><br><br><br><br><div align="center">30</div>
With hashing, we can hash the requests that come in to the load balancer and then based on the hash, we can bucket the requests according to the position of the servers by performing a tiny bit of business logic.<br>
Data can be an IP address, username, HTTP request etc...<br><br><br>
<h2>Hashing function</h2>
When you're dealing with a hashing function, it's important that it has <b>uniformity</b>. A good hashing function will evenly distribute your requests no matter how many.<br><br>
In practice, you typically never write your own hashing function. You use a pre-made industry-grade hashing function. A few popular examples are the MD5 hashing algorithm or the SHA-1 hashing algorithm, the Bcrypt hashing function, and you can trust that these hashing functions have that uniformity about them.<br>
So now we will be maximizing our chance of getting cache hits for a client's requests.<br><br><br><br>
<h3>Are simple hashing functions solution for all ?</h3>
<div align="center">
<img src="https://raw.githubusercontent.com/saivault/dsanotes/main/store/simplehash.png" height="250" width="400">
</div>
Consider using a simple hashing function which does mod operation on the number of servers. Then problems arise when a server dies or when a new server gets added, all our existing mappings will be broken as it will change the total number of servers which was used to find the server. All of our in-memory caches that we may have had in your system are no longer useful.<br><br>
<b>How do we solve this problem?</b><br>
Well, this is where consistent hashing and rendezvous hashing come into play.<br><br><br><br><br><br><br>
<div align="center">31</div>
<h1>Consistent Hashing</h1>
This hashing technique ensures that only a small set of clients move to new servers. when servers are added or removed.<br><br>
In here, imagine that you have a big circle and that you've placed your servers on the circle in a sort of evenly distributed way. This circle is not an actual thing, it's more a concept that helps us visualize this strategy better.<br><br><br>
<b>How exactly are we placing these servers on the circle?</b><br>
By using a good hashing function and mapping each server to a point on the circle.<br>
Position your clients on the circle also using a hashing function.<br><br><br>
<b>How do you determine where requests or where clients are going to be routed to?</b><br>
Well, you go to each client and from each client, you move in a clockwise direction and the first server that you encounter is gonna be the server that your load balancer is gonna reroute this client to, or this client's requests to.<br><br>
<b>Note:-</b> the direction can be counter-clockwise too.
<div align="center">
<img src="https://raw.githubusercontent.com/saivault/dsanotes/main/store/che.png" height="300" width="450">
</div>
So as you can see, this is kind of uniformly distributed because we used these hashing functions which provide uniformity to position our servers and our clients.<br><br><br><br><br><br>
<br><br><br><div align="center">32</div>
<h2>But what does this accomplish?</h2><br>
1. <b>Well let's see what happens if one of our servers dies?</b><br>

&nbsp;&nbsp;&nbsp;What if server 4 dies? Remember in the previous example with a simple hashing &nbsp;&nbsp;&nbsp;strategy, like we said, if a server died, we'd have to redo all of our <br>
&nbsp;&nbsp;&nbsp;calculations. We would no longer be able to mod by let's say four if one of our 
&nbsp;&nbsp;&nbsp;servers died, we would have to mod by three.<br>
&nbsp;&nbsp;&nbsp;Here, if one of our servers dies, let's say server 4, we're gonna go back to our 
&nbsp;&nbsp;&nbsp;clients, move in a clockwise direction, and find the closest servers. Server 5 
&nbsp;&nbsp;&nbsp;will take care of the clients served by server 4.<br><br>
&nbsp;&nbsp;&nbsp;=> only one server's cache falls apart inaffecting other servers.<br><br>
2. <b>What happens if we add a new server?</b><br>

&nbsp;&nbsp;&nbsp;We go through our clients, move clockwise.<br>
&nbsp;&nbsp;&nbsp;=> cache misses occur for just few existing clients.<br><br><br>
So as you can see with this system, with this system of putting the servers and the clients on a circle and moving in a clockwise direction, what we accomplish is that if we ever add or remove a server, we actually <b>still maintain most of the previous mappings</b> or associations between clients and servers. Only a few of them change.<br><br>
This is why consistent hashing is so powerful because basically, it maintains some level of consistency between hashes and their target buckets.
What's also cool about consistent hashing is that with this circle concept, you can even more evenly distribute your traffic.<br><br><br><br>
<h3>What if clients are hashed more to a particular region ?</h3>
Maybe a lot of your clients/requests are gonna somehow get hashed in a section of the circle where one of the servers isn't present. Maybe most of your clients and requests are gonna appear on the right side of the circle. So what you can do is you can <b>pass all of your servers through multiple hashing functions and then place all of the hashes that you get for your servers on the circle</b> and so basically each server will have multiple places that are associated with it.<br>
In the below picture, servers 1 and 2 are placed at multiple places on the circle.
<br><br><br><br><br><br><br><br><br><br><br><div align="center">32</div>
<div align="center">
<img src="https://raw.githubusercontent.com/saivault/dsanotes/main/store/hashrepl.png" height="250" width="250" >
</div>
<h3>How to make one server more powerful than the others in here ?</h3>
Imagine at the very beginning of the life of your system, you only had one server, server A, and when your system started to grow, you decided to scale it vertically by making your main server A more and more powerful. Eventually, you decided to scale horizontally by adding servers like B, C, D, and E. But they were all weaker, not as powerful at server A so now you're faced with a situation where you wanna evenly distribute your traffic amongst your servers, but you want A to get a little bit more of the load because it's a more powerful server and you still wanna use this consistent hashing strategy. <br><br>
Well what you can do is you can <b>pass server A through more hashing functions than all the other servers</b> and so what ends up happening is server A will have more locations on the circle. So basically now, there's just a higher likelihood that any given client or request is gonna bump into A when you move clockwise from it. <br><br>
In the above figure, we can say servers 1 and 2 are more powerful than 3<br><br><br>
<h2>Another Usecase</h2>
Consistent Hashing also helps with efficiently partitioning and replicating data.<br>
<b>Partitioning:</b> Distributing data across a set of nodes arranged on a circle.<br>
<b>Replication:</b> Each key is assigned to a particular node which first stores the data locally and then replicates it to N-1 clockwise successor nodes on the circle. In an eventually consistent system, this replication is done asynchronously (in background).<br><br><br>
Amazon’s Dynamo and Apache Cassandra use Consistent Hashing to distribute and replicate data across nodes. So this is consistent hashing and it's very powerful.
<br><br><br><br><br><br><div align="center">33</div>
<h2>Rendezvous Hashing</h2>
So imagine that you've got a bunch of usernames (Username 0, 1, 2, 3, 4, 5, 6, 7, 8, 9) and servers (Server 0, 1, 2, 3, 4, 5). So what the rendezvous hashing strategy is gonna do is for every username, it's going to calculate a score or rather a ranking of the servers. So in this case, it's gonna say hey, for username0, I'm gonna rank these six servers using some formula or some piece of logic, and I'm gonna pick the highest ranking server. Then for username1, I'm gonna do the exact same thing and so on.
So let's say that username0 finds server0 as the highest ranking server for itself. That's the server that it's going to be associated with.<br><br><br>
<h3>What if you remove a server ?</h3>
If username0 had server0 as its highest ranking server, removing server5 isn't gonna do anything and username0 is still gonna map to server0. On the other hand, let's say that username2 mapped to server5 and then you remove server5, then that means that you will naturally have to change the mapping of username2 and you will just take the second highest ranking server.<br><br>
<h3>What if you add a server ?</h3>
The new server's gonna be ranked first for some clients. And only for those clients, there will be one cache miss. And no change is gonna happen for other clients.<br><br><br>

```js
function pickServerSimple(username, servers) {
    const hash = utils.hashString(username);
    return servers[hash % servers.length];
}

function pickServerRendezvous(username, servers) {
    let maxServer = null;
    let maxScore = null;
    
    for (const server of servers) {
        const score = utils.computeScore(username, server);
        if (maxScore == null || score > maxScore) {
            maxScore = score;
            maxServer = server;
        }
    }
    
    return maxServer;
}
```
<br><br><br><br><div align="center">34</div>
So that's how rendezvous hashing works in a nutshell.<br>
And so as you can see, just like with consistent hashing, we maintain <b>some consistency in these mappings</b> / associations. Both of those are fairly interchangeable, they both accomplish kind of the same thing. But the naive hashing strategy, the one where you just mod the hashes by the number of servers is certainly not as good.<br><br>
And if your system is gonna be relying on something like in-memory caching, you're definitely gonna be able to bring up these hashing strategies.<br><br><br>
<h1>Key Terms</h1>
<h2>CONSISTENT HASHING</h2>
A type of hashing that minimizes the number of keys that need to be remapped when a hash table gets resized. It's often used by load balancers to distribute traffic to servers; it minimizes the number of requests that get forwarded to different servers when new servers are added or when existing servers are brought down.
<h2>SHA</h2>
Short for "Secure Hash Algorithms", the SHA is a collection of cryptographic hash functions used in the industry. These days, SHA-3 is a popular choice to use in a system.
<h2>HASHING FUNCTION</h2>
A function that takes in a specific data type (such as a string or an identifier) and outputs a number. Different inputs may have same output. But a good hashing function attempts to minimize those hashing collisions (which is equivalent to maximizing uniformity).<br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><div align="center">35</div>
<h1 id="db">Databases</h1>
<blockquote align="center"><b>
Database is a collection of inter-related data<br>which helps in efficient retrieval, insertion and deletion of data.
</b></blockquote><br>
There are hundreds of databases out there. All of these databases have different properties, they give different guarantees, they're optimized for certain functionalities, they might support specific use cases more than others. And so because of that, it's very difficult to make sweeping or generalizing statements about these databases.
It's hard to categorize these databases into specific buckets. However, there is one database characteristic that we can use to actually categorize all of these databases specifically into two major categories.<br><br>
And that characteristic is the structure that is imposed on the data that you store in these databases.<br><br><br>
<h2>Relational Database</h2>
A relational database is a type of database that imposes a <b>tabular like structure</b> on the data stored in it.<br>
<b>Example</b>:- MySQL <br>
<div align="center">
Tables ~ Relations<br>
Rows   ~ Records<br>
Columns ~ Attributes<br>
<img src="https://raw.githubusercontent.com/saivault/dsanotes/main/store/dbtableeg.png" height="200" width="400">
</div><br>
Every column of the database row has some pre-defined rules for the data that is meant to be persisted in it. With structured data, we know what we are dealing with. Since the <i>name</i> is strictly of string type, we can run string operations on it without worrying about errors or exceptions.<br><br><br><br><br><br><br>
<div align="center">36</div>
Relational databases also ensure <b>saving data in a normalized fashion</b>. In very simple terms, normalized data means an entity occurs in only one place/table in its simplest and atomic form and is not spread throughout the database. This helps maintain consistency in the data.<br><br><br><br>
<h2>Non-Relational Database</h2>
Non relational databases are databases that don't impose a tabular like structure on the data stored in them.<br>
<b>Example</b>:- MongoDB, Redis, Neo4J, Cassandra, Memcache, etc.<br><br>
While non-relational databases do sometimes impose some type of structure on the data stored in them, it's typically not gonna be in the form of tables. It will be a lot more flexible and a lot less rigorous.<br><br><br><br>
<h2>Querying Ability</h2>
Since the data is structured in a relational database, it is typically managed by a query language such as <b>SQL (Structured query language)</b>. SQL is used to perform complex queries in relational databases. So relational databases are often used interchangeably with SQL databases and non-relational databases are often used interchangeably with non-SQL databases.<br><br>
Relational databases are preferred over non-relational databases because of their querying abilities. <br><br><br><br>
<h3>Why to use SQL for querying ?</h3>
Why not Javascript / Python ?
Because they involve loading the data in memory at the start. When we have terrabytes (TB's) of data, doing that will be non-trivial.<br>
SQL allows you to perform queries directly in the database without having to load the data in memory.<br><br><br><br><br>
A <b>transaction</b> is a single logical unit of work which accesses and possibly modifies the contents of a database.<br><br>
An ACID transaction is a transaction in a database, that has four properties.
<br><br><br><br><br><br><div align="center">37</div>
<h1>ACID</h1>
Relational databases also ensure ACID transactions. <br>
<h2>Atomicity</h2>
Atomicity guarantees that each transaction is treated as a single "unit", which either succeeds completely, or fails completely: if any of the statements constituting a transaction fails to complete, the entire transaction gets aborted and the database is left unchanged.
<h2>Consistency</h2>
A database is initially in a consistent state, and it should remain consistent after every transaction.
<h2>Isolation</h2>
Transactions are often executed concurrently. Isolation ensures that concurrent execution of transactions leaves the database in the same state that would have been obtained if the transactions were executed sequentially. 
<h2>Durability</h2>
The changes made by a committed transaction are permanent.<br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><div align="center">38</div>
<h1>Indexing</h1>
Imagine that you want to look for the name of the customer who paid the largest amount of money. You naturally have to go sequentially through the entire database to find the customer, resulting in a linear time operation. Implying a very slow operation when dealing with a large scale distributed system. And really slow, especially if you need to perform these types of operations over and over again.<br><br>
This is where a database index comes into play.<br><br>
Basically, the idea behind a database index is that you can create an auxiliary data structure, an additional data structure in your database that is gonna be optimized for fast searching on specific attribute(s) in a table. <br><br>
So here, you could have a database index that is gonna allow you to search for amounts in your table much faster than you would normally be able to search for them. We can create an additional table which stores amounts in sorted order pointing to relevant records in the main table.<br>
=> we can do binary search here <b>bringing the time down to logarithmic</b>.<br><br><br>
The goal of creating an index on a particular table in a database is to make it faster to search through the table and find the row or rows that we want. Indexes can be created using one or more columns of a database table, providing the basis for both rapid random lookups and efficient access of ordered records.<br><br><br>
<h3>Space - Time tradeoff</h3>
The trade-off to keep in mind when you're thinking about adding a database index is that the <b>auxiliary data structure is gonna take up more space</b>.<br><br>
<blockquote align="center"><b>Space increases, time decreases</b></blockquote>
<br><br><br>
<h3>Effect on reads and writes</h3>
Whenever you write (insert, update, delete) to the database, you're also going to have to write in the database index. So with indexing, write operations will become little slower and read operations become a lot faster. <br><br><br>
<br><br><br><br><br><br><br>
<div align="center">38</div>
<h2>Need for NoSQL databases</h2>
One big limitation with SQL-based relational databases is <b>scalability</b>. Scaling relational databases is not trivial. They have to be sharded, replicated to make them run smoothly. This requires careful planning, human intervention and a skillset. On the contrary, NoSQL databases can add new server nodes on the fly and scale without any human intervention.<br><br>
Today’s websites need fast read-writes. There are billions of users connected with each other on social networks. A massive amount of data is generated every micro second, and we need an infrastructure designed to manage this exponential growth.<br><br><br>
NoSQL databases had to <b>sacrifice strong consistency, ACID transactions</b>, and much more to scale horizontally over a cluster and across the data centers. <br><br>
1. Since the data is not normalized, an entity, since spread throughout the database, has to be updated at all places.
Failing to update at all places makes the data inconsistent. <br>
2.  ACID transactions in these databases are limited to a certain entity hierarchy or a small deployment region (not at global level) where they can lock down nodes to update them.<br><br>

The data with NoSQL databases is more <b>eventually consistent as opposed to being strongly consistent</b>. When a large application is deployed on hundreds of servers spread across the globe, the geographically distributed nodes take some time to reach a global consensus.<br>
Until they reach a consensus, the value of the entity is inconsistent. The value of the entity eventually becomes consistent after a short while. This is what eventual consistency is.<br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><div align="center">38</div>
<h2>Learning curve not so steep and schemaless</h2>
The learning curve of NoSQL databases is less steep than that of relational databases. When working with relational databases, a big chunk of our time goes into learning to design well-normalized tables, setting up relationships, trying to minimize joins, and so on.<br>
Also, one needs to be pretty focused when designing the schema of a relational database to avoid running into issues in the future.<br><br>
NoSql database entities have no relationships. Thus, there is a lot of flexibility, and you can do things your way.
<br><br><br><br>
<h1>Key Terms</h1>
<h2>RELATIONAL DATABASE</h2>
A type of structured database in which data is stored following a tabular format; often supports powerful querying using SQL.<br><br>
<h2>NON-RELATIONAL DATABASEe</h2>
In contrast with relational database (SQL databases), a type of database that is free of imposed, tabular-like structure. Non-relational databases are often referred to as NoSQL databases.<br><br>
<h2>SQL</h2>
Structured Query Language. Relational databases can be used using a derivative of SQL such as PostgreSQL in the case of Postgres.<br><br>
<h2>SQL DATABASE</h2>
Any database that supports SQL. This term is often used synonymously with "Relational Database", though in practice, not every relational database supports SQL.<br><br>
<h2>NoSQL DATABASE</h2>
Any database that is not SQL-compatible is called NoSQL.
<br><br><br><br><br><br><br><br><br><br><div align="center">45</div>
<h2>DATABASE INDEX</h2>
A special auxiliary data structure that allows your database to perform certain queries much faster. Indexes can typically only exist to reference structured data, like data stored in relational databases. In practice, you create an index on one or multiple columns in your database to greatly speed up read queries that you run very often, with the downside of slightly longer writes to your database, since writes have to also take place in the relevant index.<br><br>
<h2>STRONG CONSISTENCY</h2>
Strong consistency usually refers to the consistency of ACID transactions, as opposed to Eventual Consistency.<br><br>
<h2>EVENTUAL CONSISTENCY</h2>
A consistency model which is unlike Strong Consistency. In this model, reads might return a view of the system that is stale. An eventually consistent datastore will give guarantees that the state of the database will eventually reflect writes within a time period (could be 10 seconds, or minutes).
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><div align="center">38</div>
<h1 id="kvstore">Key Value Stores</h1>
Sometimes, the tabular structure imposed by a relational database is actually more cumbersome than usual. Then you might prefer a non-relational database.<br><br>
One of the most popular types of <b>non-relational database</b> is a key value store. It is a type of database that allows you to store data in a "key-value" format. The key serves as an unique identifier and has a value associated with it. The value can be as simple as a string(most often) and as complex as an object graph.<br><br>
You can think of key-value store as a fast, flexible storage machine that resembles a hash table.<br><br>
Some of the popular key-value data stores used in the industry are <b>Redis</b>, Hazelcast, Riak, Voldemort, Memcached.<br>
Microsoft, Citrix uses redis.<br>
Google cloud uses memcached.<br><br><br>
<h2>Features</h2>
1. There's arguably no <b>simpler</b> type of storage atleast from a conceptual point of view than a key-value type of mapping.<br>
2. They are <b>flexible</b> as there is no structure imposed on them. <br>
3. We are accessing the values <b>directly through keys</b> in constant time O(1). There is no query language required to fetch the data. It’s just a simple no-brainer fetch operation. This ensures <b>minimum latency</b>.<br><br><br>

<h2>Use cases</h2> 
1. Due to the minimum latency they ensure, the primary use case for these databases is <b>caching</b> application data.<br>
2. Dynamic configuration: special parameters/constants in your system that different parts of your system can rely on.<br><br><br>

Different key value stores behave differently. Some are in-memory, some are not.<br>
Some might give you strong consistency, others might only give you eventual consistency and so on ....
<br><br><br><br><br><br><br><br><br><br><div align="center">40</div>
<h1>Key Terms</h1>
<h2>Key-Value Store </h2>
A Key-Value Store is a flexible NoSQL database that's often used for caching and dynamic configuration. Popular options include Redis, Amazon DynamoDB and Etcd
<h2>Etcd</h2>
Etcd is a strongly consistent and highly available key-value store that's often used to implement leader election in a system.
<h2>Redis</h2> An in-memory key-value store. Does offer some persistent storage options but is typically used as a really fast, best-effort caching solution. Redis is also often used to implement rate limiting.
<h2>Zookeeper</h2> Zookeeper is a strongly consistent, highly available key-value store. It's often used to store important configuration or to perform leader election.
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><div align="center">41</div>
<h1 id="ssp">Specialized Storage Paradigms</h1>
These cater to usecases that are actually fairly common.<br><br><br>
<h2>1. Blob Store</h2>
It is very common interms of usecases.<br>
Blob stands for <b><i>Binary Large Object.</i></b><br><br>
When someone is using the word 'blob', they are really referring to just some arbitrary piece of unstructured data.<br>
Canonical examples are video file, image file, large text file or maybe a large binary meaning compiled code that's ready to be shipped out to production.<br><br>
<b>Can we store blobs in a SQL database ?</b><br>
It's very unstrucured that doesn't make sense to store in a tabular format.<br><br><br>
As its name suggests, blob store is a storage solution for blobs.<br>
The data contained inside a blob is unstructured and often times very large. Blob store specialises in storing <b>massive amounts of unstructured data</b> (millions of blobs). Most commonly used blob stores are <ul>
<li>Google cloud storage is a blob storage service provided by Google.</li>
<li>Amazon S3 is a blob storage service provided by Amazon through AWS.</li>
<li>Microsoft Azure blob storage etc..</li>
</ul><br><br>
Blob stores are <b>optimised for storing and retrieving</b> massive amounts of unstructured data. So it's not very easy to implement and you almost always rely on popular solution like S3 or GCS.<br><br><br>
<h3>Relation with key value stores</h3>
They sort of behave like key value stores.<br>
<div align="center">blob id/name --> blob</div>
Blob stores function differently from key value stores which are not trained for storing massive amounts of data. Key value store is gonna be more optimised for latency rather than availability and durability.<br><br><br>
<br><br><br><br><br><br><br><br><div align="center">50</div>
<h2>2. Time series DB</h2>
A database specialised for storing time series data. These databases are less encountered as the time series data is even less likely to find. <br><br>
when we got large amounts of <b>data that are of events happened at a given time</b> (say every x ms) or when we have to perform very time series like computations like rolling averages, local maximas and minimas, aggregating data between two time periods, then we have to use a time series database.<br><br>
Some of the very popular usecases are monitoring and stock price data.<br>
Two of the most popular time series databases are InfluxDB, Prometheus.<br><br><br><br>
<h2>3. Graph DB</h2>
For storing a dataset where there are a <b>lot of relationships within the data</b> between individual data points. In such cases, tabular data might not make much sense as the queries will get more and more complicated.<br><br>
Usecases that really lend themselves well to having these databases are social networks.
The most popular graph database out there is Neo4j<br><br>
Cypher graph query language that was originally developed for the Neo4j graph database, but that has since been standardized to be used with other graph databases in an effort to make it the "SQL for graphs".<br><br><br><br>
<h2>4. Spatial DB</h2>
Special type of database optimised for storing spatial data.<br><br>
Spatial data is data that is concerned with geometric space. Canonical example is locations on a map. Some spatial queries are:<br>
1. Finding all locations in the vicinity of a specific location<br>
2. Finding the distance between multiple locations.<br><br><br>

A standard database index might not be optimised for this type of queries or computations. So spatial databases rely on spatial indices. Lots of spatial indices are based on trees. An example is a quad tree where every node has either 0 or 4 children nodes. Conceptually you can think of quad tree as a grid.<br><br><br><br><br><br><br>
<div align="center">51</div>
<h2>Quad Tree</h2>
A tree data structure most commonly used to index two-dimensional spatial data. Each node in a quadtree has either zero children nodes (and is therefore a leaf node) or exactly four children nodes.<br><br>
Typically, quadtree nodes contain some form of spatial data - for example, locations on a map — with a <b>maximum capacity of some specified number n</b>. So long as nodes aren't at capacity, they remain leaf nodes; once they reach capacity, they're given four children nodes, and their data entries are split across the four children nodes.<br><br>
A quadtree lends itself well to storing spatial data because it can be represented as a grid filled with <b>rectangles that are recursively subdivided into four sub-rectangles</b>, where each quadtree node is represented by a rectangle and each rectangle represents a spatial region. Assuming we're storing locations in the world, we can imagine a quadtree with a maximum node-capacity n as follows:<br><br>
<ul>
<li>The root node, which represents the entire world, is the outermost rectangle.</li>
<li>If the entire world has more than n locations, the outermost rectangle is divided into four quadrants, each representing a region of the world.</li>
<li>So long as a region has more than n locations, its corresponding rectangle is subdivided into four quadrants (the corresponding node in the quadtree is given four children nodes).</li>
<li>Regions that have fewer than n locations are undivided rectangles (leaf nodes).</li>
<li>The parts of the grid that have many subdivided rectangles represent densely populated areas (like cities), while the parts of the grid that have few subdivided rectangles represent sparsely populated areas (like rural areas).</li>
</ul><br><br>
Finding a given location in a perfect quadtree is an extremely fast operation that runs in log4(x) time (where x is the total number of locations), since quadtree nodes have four children nodes.<br><br>
<div align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/8/8b/Point_quadtree.svg" height="200" width="300">
</div>
<br><br><br><br>
<div align="center">53</div>
<h1>Key Terms</h1>
<h2>BLOB STORAGE</h2>
Widely used kind of storage, in small and large scale systems. They don't really count as databases per se, partially because they only allow the user to store and retrieve data based on the name of the blob. This is sort of like a key-value store but usually blob stores have different guarantees. They might be slower than KV stores but values can be megabytes large (or sometimes gigabytes large). Usually people use this to store things like large binaries, database snapshots, or images and other static assets that a website might have.<br><br>
Blob storage is rather complicated to have on premise, and only giant companies like Google and Amazon have infrastructure that supports it. So usually in the context of System Design interviews you can assume that you will be able to use GCS or S3. These are blob storage services hosted by Google and Amazon respectively, that cost money depending on how much storage you use and how often you store and retrieve blobs from that storage.<br><br>
<h2>TIME SERIES DATABASE</h2>
A TSDB is a special kind of database optimized for storing and analyzing time-indexed data: data points that specifically occur at a given moment in time. Examples of TSDBS are InfluxDB, Prometheus, and Graphite.<br><br>
<h2>GRAPH DATABASE</h2>
A type of database that stores data following the graph data model. Data entries in a graph database can have explicitly defined relationships, much like nodes in a graph can have edges.
Graph databases take advantage of their underlying graph structure to perform complex queries on deeply connected data very fast.<br><br>
Graph databases are thus often preferred to relational databases when dealing with systems where data points naturally form a graph and have multiple levels of relationships-for example, social networks.<br><br>
<h2>SPATIAL DATABASE</h2>
A type of database optimized for storing and querying spatial data like locations on a map. Spatial databases rely on spatial indexes like quadtrees to quickly perform spatial queries like finding all locations in the vicinity of a region.
<br><br><br><br><br><br><br><br><br>
<div align="center">54</div>

<div align="center" id="repshar"><b>
"A system's performance is often very dependent on its database performance"
</b></div><br><br>
<h1 style="font-size:30px">Replication</h1>
Consider a system having a main database, what if it goes down ?<br>
<b>> Use a secondary database</b><br>
This secondary database is a replica of main database and sort of behaves like a standby for it. This is called replication.<br><br><br>
<h3>How this replica idea works ?</h3>
- The main database handles all the reads and writes coming to it. It also updates the replica such that the replica is effectively the same as the main database.<br>
- The replica would take over if the main database fails. Then it becomes the new main database. And once the original database comes back up, it gets updated by the replica and eventually they can swap roles again when needed.<br>

<br><br>
<h2>What it takes ?</h2>
In order for this to work, 
<ul>
<li>the replica needs to always be <b>exactly upto date</b> with the main database.</li>
<li>All the updates done to the main database must also happen in replica in a synchronous way.</li>
</ul><br>
Whenever there is a write operation to your main database, that operation needs to be synchronously done on the replica as well. If at all a write operation fails on the replica, it should not be completed in the main database as you never want your replica to be out of date with the main database.<br>
&nbsp; => write operations will take longer time as the changes need to be done<br>&nbsp; &nbsp; &nbsp;in two places.<br><br><br>
In this example, we used replication to improve the availability of our database and of our system as a whole. But we can also use replication to improve our database's latency and inturn to improve our system's latency. Let's see an example for it below.<br><br><br><br><br><br><br><br><br><br><br>
<div align="center">54</div>
<h2>Another Usecase</h2>
This is going to be an example where you are fine with having your replicas not be upto date with each other at all times. Ofcourse there are many types of products and services where you do not want that to happen.<br><br>
Imagine that we're designing a system like <i>Linked In</i> where people can write posts and other people can view those posts in their feed. Consider a large number of users from both USA and India.<br>
What we might do is to have two databases, One in the US to serve US users and other in India serving Indian users. That way users of both countries will have low latencies because they are served data from databases located in their region.<br><br><br>
What happens if an US user posts something ?<br>
That post will be initially stored in the US database but now it needs to be replicated in the Indian database too as cross-country connections are very normal. As people(Indian users in this case) don't care about how instantaneously they get the recent posts in their feed, what we can do is to have the US database asynchronously update the Indian database like every min / 5 min/ 10 mins etc... and vice versa. Likewise, both the databases update each other.<br><br>
As we are giving up on replica being upto date, we are able to handle the system by updating only fewer times which inturn reduces the latency of write operations too.<br><br><br><br><br>
<h2>How long can you replicate ?</h2>
Imagine you are having a system with one main database, and that system is serving millions of requests and your main database is starting to get overloaded as it can't handle all this requests at once. This results in an low throughput. How can we improve this ?<br>
1. You can do vertical scaling but there is only so much to do with regards to it.<br>
2. Do horizontal scaling by maintaining good number of replicas and thereby increasing your throughput.<br><br>

What if we have billions of users and huge amounts of data, replicating all of that data across bunch of different servers wont be any optimal. What we can do instead is actually split up the data. In other words, one part of the data would be stored in one database server, another part of the data would be stored in another database server and so on......... This idea of splitting up / partitioning your data is what's known as sharding.<br><br><br><br><br><br>
<div align="center">55</div>
<h1 style="font-size:30px">Sharding</h1>
Splitting the main database into a bunch of little databases called shards (or) data partitions. With this, we increased our throughput and avoided duplicating so much data at so many places.<br>
We will also be employing an additional server to which the requests come and gets distributed into one of the shards which is preferably reverse proxy.
<br><b>PS</b>:- Even individual shards require replicas<br><br><ul>
<li>How to split up the data ?</li>
<li>Where to put certain chunks of data in what shard ?</li>
</ul><br><br>
<h3>Approach</h3>
This can be used while using relational databases. We can store some rows in one shard and some rows in other shard and so on... Based on a colum name, we can split them like customer names starting with A-E can be placed in shard 1, F-J in shard 2 etc... (or) according to the region of the customers.<br><br>
But this can come with problems though. You might have <b>hotspots</b>.<br><br><br><br>
<h2>Hotspots</h2>
Certain shards get a lot more traffic than the other just by the nature of the data they store. If the sharding strategy is not uniform, it is very much possible that all of our data is just concentrated in some few shards called hotspots. In the worst case, we may get all the data into just one shard and it being getting overloaded. Then the entire reason for which we sharded in the first place will be of no use.<br><br><br>
A very reasonable way to split up your data is by using <b>Hashing</b>. We can use a hasing function which can gurantee us uniformity to determine what shard a piece of data gets written into or read from.<br><br>
Depending on the type of data that you are sharding, we have to decide how to split it up in different ways. While designing a real world system, you really have to make sure that your sharding strategy is smart.
<br><br><br><br><br><br><br><br><br><br>
<div align="center">55</div>
<h1>Key Terms</h1>
<h2>REPLICATION</h2>
The act of duplicating the data from one database server to others. This is sometimes used to increase the redundancy of your system and tolerate regional failures for instance. Other times you can use replication to move data closer to your clients, thus decreasing the latency of accessing specific data.<br><br>
<h2>SHARDING</h2>
Sometimes called data partitioning, sharding is the act of splitting a database into two or more pieces called shards and is typically done to increase the throughput of your database. Popular sharding strategies include:<br>
• Sharding based on a client's region<br>
• Sharding based on the type of data being stored (e.g: user data gets stored in one shard, payments data gets stored in another shard)<br>
• Sharding based on the hash of a column (only for structured data)<br><br>
<h2>HOT SPOT</h2>
When distributing a workload across a set of servers, that workload might be spread unevenly. This can happen if your sharding key or your hashing function are suboptimal, or if your workload is naturally skewed: some servers will receive a lot more traffic than others, thus creating a "hot spot".
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">56</div>
Citizens in a society typically elect a leader by voting for their preferred candidate. But how do servers in a distributed system choose a master node? Via algorithms of course!<br>
This form of algorithmic democracy is known as "algorithmocracy".<br><br>
<h1 style="font-size:30px" id="leader">Leader Election</h1>
At any point of a system, if you are using only one machine to do the work, the failure in just this single machine can make our whole system go down. So, the solution is to introduce redundancy in our system.<br><br>
If there are 'n' machine at that point of the system to do the same work, how can we ensure it is done only once ?<br>
Well, this is where Leader Election comes into play.<br><br><br>
Consider a group of machines/servers that are incharge of doing the same thing. Instead of having all of them doing the same thing, (which might not be something that you want to do multiple times) Leader election has the <b>servers elect one of themselves as the leader and that server alone is gonna be the responsible for doing the actions</b>, that all of the servers are kind of meant to be.<br><br>
Leader - only server responsible for doing the business logic.<br>
Followers - Just sit there on standby mode incase something happens to the leader.<br><br><br>
<div align="center">
<img src="https://raw.githubusercontent.com/saivault/dsanotes/main/store/leaderelection.png" height="300" width="450">
</div>
<br><br><br><br>
<div align="center">65</div>
This leader becomes responsible for data replication and can act as the central point for all coordination. The followers only accept writes from the leader and serve as a backup. In case the leader fails, one of the followers can become the leader. In some cases, the follower can serve read requests for load balancing.<br><br><br>
<h2>Is it that easy ?</h2>
All the followers should be aware that which among them is the leader at any given point of time, and capable of re-electing when needed.<br>
Electing a leader is easy. The difficulty is in <b>having multiple machines gain consensus</b> (on who the leader is) or agree upon something together.<br><br><br>
In order to achieve Leader election, we should use <b>consensus algorithms</b>. Consensus algorithms are very complicated and math heavy. They allow multiple nodes in a cluster to reach consensus (or) agree on some single data value.<br>
Some popular ones are PAXOS, RAFT<br><br><br><br>
<h2>How to implement ?</h2>
In the industry, you mostly never have to implement any consensus algorithm and use some third party service that itself might use PAXOS / RAFT under the hood to achieve Leader Election.<br>
ZooKeeper and Etcd are two tools that are not primarily meant for leader election. But that happen to allow you implement Leader Election in a very easy way. Previously in Uber, a lot of internal systems used ZooKeeper to implement Leader Election.<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">66</div>
<h1>Key Terms</h1>
<h2>LEADER ELECTION</h2>
The process by which nodes in a cluster (for instance, servers in a set of servers) elect a so-called "leader" amongst them, responsible for the primary operations of the service that these nodes support. When correctly implemented, leader election guarantees that all nodes in the cluster know which one is the leader at any given time and can elect a new leader if the leader dies for whatever reason.<br><br>
<h2>CONSENSUS ALGORITHM</h2>
A type of complex algorithms used to have multiple entities agree on a single data value, like who the "leader" is amongst a group of machines. Two popular consensus algorithms are Paxos and Raft.<br><br>
<h2>PAXOS & RAFT</h2>
Two consensus algorithms that, when implemented correctly, allow for the synchronization of certain operations, even in a distributed setting.<br><br>
<h2>ETCD</h2>
Etcd is a strongly consistent and highly available key-value store that's often used to implement leader election in a system.<br><br>
<h2>ZOOKEEPER</h2>
Zookeeper is a strongly consistent, highly available key-value store. It's often used to store important configuration or to perform leader election. <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><div align="center">60</div>
<h1 id="peerpeer" style="font-size:30px">Peer to Peer Networks</h1>
Say you're designing a system where you want to transfer large files (~5 GB) to thousands of machines at once repeatedly. Say 5 GBPS network throughput and 1000 machines<br>
&nbsp;&nbsp; => 1000s ~ 17 mins<br>
Say now we use 10 machines instead of one, considering distributed manner<br>
&nbsp;&nbsp; => ~1.7 mins, which isn't much amazing<br><br><br>
As the number of machines required to transfer increase, the number of replicas should also increase. But, making our data replicate over all these replica machines is not a good solution.<br> If we use sharding and store each 250 MB data in a new shard, then we run back into the first issue of whenever we want to tranfer one of the files, then all of the 1000 machines are going to the same machine containing that particular file creating a bottleneck again resulting in a 17 mins operation.<br><br><br>
So far, all of our approaches are problematic.<br>
This is where peer to peer networks come into play.<br>
From now, these 1000 machines are called as peers as they are going to work together towards a common goal.<br><br><br>
<div align="center"><b>
What if instead of sending the entire 5 GB file to each of the machines,<br>we split it up into very small chunks of 5 GB file and then send them<br>to all of the peers and then let peers communicate with one another to grab the missing chunks that they all need to create the final file.
</b></div><br>
Here, every peer is building their own total file.<br><br><br>
<h2>Approach</h2><ul>
<li>Divide the 5 GB file into 1000 chunks of 5 MB size and get them numbered.</li>
<li>Transfer each chunk to a separate machine (1000 chunks to 1000 machines). As the total amount of data transferred is 5 GB, this transfer will take 1 second ignoring the network creation overheads etc...</li>
<li>Let the machines communicate with each other and fill their missing blocks. Each chunk(5 MB) transfer requires 1/1000 seconds.</li>
</ul><br><br><br><br><br><br><br><br>
<div align="center">60</div>
Diving deep,<br>
In the first 0.001s, 1 chunk transfer will happen (main server to M1)<br>
In the second 0.001s, 2 chunk transfers will happen (main server to M2, M1 to Mi)<br>
In the third 0.001s, 4 chunk transfers will happen (from main server, M1, M2 and Mi)<br>
........<br><br><br>
In the normal way, we used to have one chunk transfer in each second. But here we are having 2<sup>n</sup>-1 chunk transfers in the n<sup>th</sup> second. Hope you can now really appreciate how much faster, the peer to peer network solution is.<br><br>
<blockquote align="center"><b>
Naive Solution - connections only with few specified machines (replicas)<br>
Peer to Peer   - connections with every other possible machine (peers)</b>
</blockquote><br><br>
One daily life example of a peer to peer network is <b>torrenting</b>.<br><br>
<h2>Peer Discovery</h2>
In order for this peer to peer network to function properly, our peers should know what peers to talk to next. This creates the topic of peer discovery or peer selection.<br>
- Using central database or some machine as a tracker to find their next peer.<br>
- Gossip protocol or Epidemic protocol. Just talk and figure it out themselves.<br>
- Hash table constucted based on the mapping from ip addresses of peers to chunks they carry.<br><br>

Kraken created at Uber implements this whole distribution very fastly.<br><br><br><br>
<h1>Key Terms</h1>
<h2>PEER-TO-PEER NETWORK</h2>
A collection of machines referred to as peers that divide a workload between themselves to presumably complete the workload faster than would otherwise be possible. Peer-to-peer networks are often used in file-distribution systems. <br><br>
<h2>GOSSIP PROTOCOL</h2>
When a set of machines talk to each other in a uncoordinated manner in a cluster to spread information through a system without requiring a central source of data.
<br><br><br><br><br><br><div align="center">60</div>
<h1 id="pollstream" style="font-size:30px">Polling and Streaming</h1>
Till now, we have dealt with clients and servers communicating with each other. The clients issue requests to the servers and servers respond back to them with responses.<br><br>
<h3>What if our clients want some piece of data that gets updated very regularly ??</h3>
Examples are Monitoring temperatures, Stock prices, Realtime chat application<br>
This is where polling and streaming comes into play.<br><br><br>
<h1>Polling</h1>
The client issues a request for data that it wants on a recurring basis following a set interval (every x seconds).<br><br>
But polling has limitations. When two people are chatting using an application, they want to send and receive messages instantly (the almost live feeling). Let's say if we are using polling for this with an interval of 30 seconds, then that will obviously not lead to an instantaneous experience. Say you want to reduce the interval between requests like every 0.5 second, now it can be acceptable. But this comes with a lot of load(too many requests) on the server if we scale big.
<br>This is where streaming comes into play.<br><br><br>
<h1>Streaming</h1>
Instead of having clients repeatedly requesting for data, you're gonna have your client <b>open a long lived connection</b> and typically this is done through sockets.<br><br>
A socket is basically a file that lives on your computer that your computer can write to and read from to communicate with other computer in a long lived connection way. It is more like a portal. This connection can live until one of the two computers closes or until the network is healthy. The client continuously listens to the server for any data the server pushed to it. Basically, the client is streaming data from the server.<br><br>
In streaming, Client is no longer requesting data from server, it is just <b>listening</b> to it. And it is the job of the server to send data to the client whenever it needs to. Implying the server is no longer passive and proactively sending(pushing) data.<br><br><br><br><br><br><br><br>
<div align="center">60</div>
Though in case of chat application streaming came superior to polling, Streaming is not necessarily better than polling. It depends on the usecase.<br><br>
<blockquote align="center"><b>
data getting updated too frequently - streaming<br>
data not getting  updated too frequently - polling
</b></blockquote><br><br><br><br><br>
<h1>Key Terms</h1>
<h2>POLLING</h2>
The act of fetching a resource or piece of data regularly at an interval to make sure your data is not too stale. <br><br>
<h2>STREAMING</h2>
In networking, it usually refers to the act of continuously getting a feed of information from a server by keeping an open connection between the two machines or processes.<br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><div align="center">64</div>

<h1 id="configuration" style="font-size:30px">Configuration</h1>
Most large scale distributed systems are gonna be relying a lot on configuration.<br>
Configuration is the <b>set of parameters</b> / constants that your system / application is going to use. Instead of having these parameters deeply intertwined in your code, you are going to write or configure them elsewhere in a seemingly <b>isolated file</b>. <br><br>
And configuration files are written in JSON or YAML format. This makes it very easy to read and edit regardless of what language your application is using.<br>
Usually "config" is short for confiuration.<br><br><br>
Example for a config.json file:

```json
{
    "apiKey": "abcd@369"
    "supportedLangauges": {
        "cpp",
        "javascript",
        "python"
    },
    "version": {
        "number": 0,
        "releaseDate": "20-11-2020"
    }
}
```
<br><br><br><br><br>There are two primary types of configuration.
<h2>Static Configuration</h2>
Configuration that's gonna be bundled / packaged with your application code.<br>
- Safer but little slower to see changes related to your configuration happen because you have to wait for your entire application to redeploy.<br>
- proper review and tests will be run.<br><br>

<br><br><br><br><br><br><br><br><div align="center">64</div>
<h2>Dynamic Configuration</h2>
Configuration that is completely separated from your application code.<br>
Here, the changes will take effect in a moment providing our application great power and responsibility.<br>
- Little complex as it naturally has to backed by some sort of database that your application is querying what the current configuration is.<br>
- Somewhat riskier as it wont have proper review or tests.<br><br><br>

And at very large companies like google, you can build complex systems such that when you make a configuration change, it only gets deployed to only 1-10% of its users to make it more safe.<br><br><br><br><br>
<h1>Key Terms</h1>
<h2>CONFIGURATION</h2>
A set of parameters or constants that are critical to a system. Configuration is typically written in JSON or YAML and can be either static, meaning that it's hard-coded in and shipped with your system's application code (like frontend code, for instance) or dynamic, meaning that it lives outside of your system's application code.
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">65</div>
<h1 id="ratelimit" style="font-size:30px">Rate limiting</h1>
This is very important when dealing with large scale systems mainly because it has a lot of ramifications including security ramifications and performance ramifications.<br><br>
<h3>Definition</h3>
Rate limiting is basically setting some sort of threshold on certain operations past which these operations will return errors. (or)<br>
Rate limiting is limiting the number of operations that can be performed in a given amount of time.
<br><br><br>The reason rate limiting is so important is that if you don't rate limit certain operations in a system, you will have the risk of getting your system brought down by malicious actors. A bad actor flooding the system with a lot of traffic bringing the system down is a Denial of Service (DOS) attack. Rate limit can prevent these attacks.<br>
<b>Example:</b> Code execution engine on any coding platform<br><br><br>
We can rate limit on a bunch of different things; on users (headers - auth credentials), on ip addresses, on regions, on your entire system as a whole (like keeping a limit of handling 10k requests totally)<br><br><br>
Rate limiting being very important and effective, isn't the ultimate way to protect from attacks. Though simple DOS attacks can be prevented, if your system becomes the target of a more complicated attack like D-DOS attack, then things will get complicated because a D-DOS attack will try to circumnavigate rate limiting by having a bunch of different machines that might not be identifiable as part of same organization or group.<br><br><br>
For large distributed systems, we can use Redis to properly implement rate limiting.
<br><br><br><br>
<h1>Key Terms</h1>
<h2>RATE LIMITING</h2>
The act of limiting the number of requests sent to or from a system. Rate limiting is most often used to limit the number of incoming requests in order to prevent DoS attacks and can be enforced at the IP-address level, at the user-account level, or at the region level, for example. Rate limiting can also be implemented in tiers; for instance, a type of network request could be limited to 1 per second, 5 per 10 seconds, and 10 per minute.
<br><br><div align="center">66</div>
<h1 id="logmonitor" style="font-size:30px">Logging and Monitoring</h1>
<h2>Logging</h2>
We will log stuff to get more information about your code and to debug issues.<br><br>
<h3>Log Storage</h3>
And when we log, we will be having a system / service in place that is going to collect all of your logs and <b>store them in some kind of database</b> so that you can go to that database and look through the logs at later times <b>to debug issues</b>.<br>
<b>Eg:-</b> Google stack driver<br><br>
When you are writing your application code, you are gonna put log statements in your code to log important information. Things like errors, important operations and requests that your users are performing etc....<br><br><br>
And depending on the language that you are writing your application, you might use a special library to format these logs because we have to make sure that your logs contain as much useful information in them as possible.<br>
Two popular formats of logs that are often used in systems: 
<ul>
<li>syslog</li>
<li>json</li>
</ul><br>
Logging being very simple, is incredibly important because it is what allows you to debug issues at scale when you are dealing with a huge system.<br><br><br>
<h2>Monitoring</h2>
Monitoring is a tool that makes managing a system a lot easier and a lot better.<br><br>
Say you are maintaining a big system. If you want to have visibility into your system's health, performance and general status, then how can you do it ?<br>
By making sure you designed your system in such a way that you gather meaningful metrics and that you have tools to monitor these metrics.<br><br><br>
<h3>How do you gather metrics ?</h3>
A simple way is to build some sort of service or use a prebuilt tool to scrape your logs and get metrics out of them. The disadvantages of this approach are firstly you are limited by your logs as you need to make sure that they contain each and every useful bit of information. Secondly, If at all you want to change your logs, you risk breaking your metric system.<br><br><br><br><br><br>
Another popular way of gathering metrics is to use a time-series database. (a specialised database specifically tailored for data that is related to time or data that might be measured over time)
Some popular time-series databases are InfluxDB, Prometheus and Graphite.<br><br>
You have your servers periodically send metrics to this database. Then you can query that database using a query langauge. You can also use tools like Grafana which goes into a time-series database and creates a graph out of the data stored in it.<br><br><br>
>> When you do have nice monitoring built into your system, you can do <b>alerting</b> which is very useful.<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<h1 id="securityhttps" style="font-size:30px">Security and HTTPS</h1>
<h2>No privacy over HTTP</h2>
When thinking of a client interacting with a server online over HTTP, there is this implied assumption of privacy between the client and the server.<br>
But that would actually be an incorrect assumption.<br><br>
When two machines are communicating over HTTP, a malicious actor can hijack this communication's channel and intercept the IP packets transferred between them and can eavesdrop on them or can even alter them and relay them. This is known as Man In the Middle (MITM) attack.<br>
And we want to prevent any consequences of MITM attack.<br><br>
<blockquote><b>HTTPS is same as HTTP but with "secure"</b></blockquote><br>
<h2>Encryption</h2>
The idea of converting a message into a seemingly random string of characters, something that is <b>illegible</b>. And the encrypted data should be able to convert to the original message through some techniques and not at the first glance.<br><br>
Two primary families or systems of encryption:<br>
<ul>
<li>Symmetric Encryption: Uses a single key for encrypting and decrypting data. Uses Advanced Encryption Standard (AES). Very fast</li>
<li>Asymmetric Encryption: Uses two keys, public key and private key(which are generated together) for encrypting and decrypting data. Messages encrypted through public key can only be decrypted through private key. Bit Slower</li>
</ul><br><br>
<h2>How to make HTTP secure ?</h2>
HTTPS is an extension of HTTP that runs on top of TLS.<br>
Tranport Layer Security (TLS) is a security protocol. Communication is encrypted using TLS. The predecessor protocol to TLS is Secure Sockets Layer (SSL).
When the client and server are communicating through HTTPS, they first establish a TLS handshake to make a secure connection.<br><br><br>
<h2>Steps to make a HTTPS connection</h2>
- The client sends a client "Hello" to server<br>
- The server responds with server "Hello" and SSL certificate to the client. SSL certificate contains the public key.<br>
- The client generates another random string of characters called "premaster secret". It then encrypts the premaster secret using the public key and sends it to the server.<br>
- The server decrypts the premaster secret using the private key.<br><br>

Now, both the client and the server has access to the client hello, the server hello and the premaster secret. Using these, 4 session keys(one symmetric encryption key) can be generated by both. Now they both can communicate for the rest of their communication session using the symmetric encryption key.<br><br>
Then the client and server send messages to each other which is on the lines of "TLS handshake done" and encrypted using the session keys implying a secure connection is established.<br><br><br>
<h3>Why SSL certificate ?</h3>
Instead of directly sending public key in the start, we will send SSL certificate to ensure that the public key is safe and came from the "server".<br><br>
