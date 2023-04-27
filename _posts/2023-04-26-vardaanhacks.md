---
toc: true
layout: post
badges: true
comments: true
author: Khalid farah
categories: [fastpages, markdown]
title: Vardaan group hacks 
---

# hacks 
- KASM hacks 
1. Virtual desktops allow users to access a complete desktop environment remotely, without the need for physical hardware. KASM is a security feature that isolates each virtual machine from others, providing enhanced security. In an AP CSP environment, virtual desktops can be utilized to provide students with access to a consistent and secure computing environment, allowing them to complete coursework and practice coding without needing to install software or worry about hardware limitations.

- AWS Database hacks 

QUIZ 1
Q1: What is the main difference between relational and non-relational databases?

Correct - C. Relational databases are based on tables and use SQL, while non-relational databases are based on collections and use JSON-like documents.

Q2: Which AWS database service is best suited for applications that require low-latency speed?

Correct - A. Amazon ElastiCache

Q3: What is the purpose of the code example provided in the lesson?

Correct - C. To provide an example of how to connect to a database instance in RDS using Python.

QUIZ 2

Q1: Which of the following is not an AWS database option?

Correct - C. SQLite

Q2: Which of the following is a file-based, lightweight RDBMS?

Correct - D. SQLite

Q3: Which AWS service enables you to store and query highly connected datasets?

Correct - C. Amazon Neptune

- DUCK DNS
![]({{site.baseurl}}/images/Screenshot 2023-04-26 211144.png)
Duck DNS is an essential part of the internet infrastructure that translates human-readable domain names like www.khalidfarah.com into IP addresses that computers can understand. We use DNS to access websites, send emails, and connect to other online services. DNS allows us to remember domain names easily and eliminates the need to remember IP addresses.

DuckDNS is a free dynamic DNS service that allows users to assign a custom domain name to their public IP address, making it easier to access their home network devices remotely. DuckDNS works by running a client script on a device connected to the network that periodically sends the current IP address to DuckDNS servers, which then update the DNS record with the new IP address. DuckDNS is unique in that it does not require users to register or provide any personal information to use the service, and it supports multiple subdomains per account.

DuckDNS is useful for our projects because it enables us to access our home network devices remotely without having to remember the IP address or perform complex configurations. We can use DuckDNS to access our Raspberry Pi servers, cameras, and other IoT devices securely and conveniently from anywhere in the world.

Here is how you set up Duck DNS in a few steps

Go to the DuckDNS website and sign up for an account.
Choose a custom subdomain name for your account.
Install the DuckDNS client script on a device connected to your network.
Configure the client script to run periodically and send the current IP address to the DuckDNS servers.
Update your router’s port forwarding settings to forward traffic to the appropriate device on your network.
Test your setup by accessing your custom domain name from a remote location.

- 4 
I did not do deployment for my Group last tri.
- 6
![]({{site.baseurl}}/images/Screenshot 2023-04-26 211259.png)

- Cerbot hacks
attempted didnt work inshallah next time

OpenSSL and LibreSSL are both popular open-source cryptographic libraries used for secure communication on the Internet. While both libraries share many similarities in their security features, there are some differences between the two. OpenSSL is a widely used library that supports a variety of cryptographic algorithms, including SSL/TLS protocols, PKI, and cryptographic hashing. It also provides a comprehensive set of features for secure communication, such as support for hardware acceleration, session resumption, and perfect forward secrecy. OpenSSL has been the subject of various security vulnerabilities over the years, including Heartbleed, DROWN, and more recently, the “ChaCha20-Poly1305 zero-length padding” vulnerability. both OpenSSL and LibreSSL provide a wide range of security features for secure communication on the Internet. However, LibreSSL has been developed with a focus on security and simplicity, and it has improved on some of the vulnerabilities present in OpenSSL. While both libraries may still be vulnerable to future security issues, it’s important to keep them updated to their latest versions to ensure maximum security.


