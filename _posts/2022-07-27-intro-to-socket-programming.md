---
layout: post
title: Intro To Socket Programming
tags: [socket programming,python]
thumbnail: "assets/img/intro-to-socket-programming/socket.svg"
excerpt_separator: <!--more-->
---
In this article, I will discuss socket programming and how sockets are used to establish a connection between processes.
<!--more-->
# Socket Programming

{% include aligner.html images="intro-to-socket-programming/socket.svg" %}
- Most network application consits of two programms the server program and client program these programs resides on separate end systems.Web applications that use the [HTTP/HTTPS](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol) protocol are common examples of client-server architecture.

- When these two programmes want to communicate with each other, they use sockets. Creating sockets and establishing a connection between processes is called **`socket programming`**.

# What is Socket ?

- Sockets are logical end points which allow communication between two processes.
> program in execution is called process.
- As we know, the Internet uses the [TCP/IP](https://www.ibm.com/docs/en/aix/7.2?topic=protocol-tcpip-protocols) model, where each layer has its own functionalities and provides services to the above and below layers.
> - The process lies in the Application layer of the TCP/IP model.
> - The Transport layer resides in the OS.
- If one process wants to communicate with another process, the sender(process) sends the message to the below layer, which is the Transport layer. But, this transfer does not occur directly. Here, we use `sockets` as an interface between the Application layer and the Transport layer.

So, when the two processes want to communicate, they write the data they want to send to their sockets. You can think of a socket as a file. The below layers are responsible for sending data to the correct destination.

In the next post, we will see how to create socket in Python.

---