---
author: <a href="https://www.linkedin.com/in/naman2001/"> Naman Lakhwani</a>
categories:
- Google Summer of Code
- Open Source
- CNCF
- Thanos
- GoLang
- TLS
- 2021
comments: true
date: "2021-08-19T00:00:00Z"
published: true
title: TLS in brief
---

Namaste! :pray:

I am Naman Lakhwani, an undergraduate student at the Indian Institute of Information Technology, Gwalior, India. I worked on the Thanos project over the summer as part of the Google Summer of Code program 2021. In this blog, I would be sharing my learnings on TLS and mutual TLS.

### :point_right: What is Transport Layer Security (TLS)? 
Transport Layer Security (TLS) is an encryption protocol in wide use on the Internet. 
TLS authenticates the server in a client-server connection and encrypts communications between client and server 
so that external parties cannot spy on the communications.

There are three important things to understand about how TLS works: 
1. Public key and private key \
TLS works using a technique called public key encryption, which relies on a pair of keys — a public key and a private key. 
- Anything encrypted with the public key can be decrypted only with the private key
- Anything encrypted with the private key can be decrypted only with the public key 
2. Tls certificate \
A TLS certificate is a data file that contains important information for verifying a server's or device's identity, including the public key, a statement of who issued the certificate (TLS certificates are issued by a certificate authority), and the certificate's expiration date.

3. TLS handshake \
TLS handshake is responsible for the authentication and key exchange necessary to establish secure sessions.  The TLS handshake accomplishes 3 main things:
- Exchanging cipher suites   
- Authenticating one or both parties
- Creating/Exchanging symmetric session keys

First of all, the client and server agree on the exact encryption methods they will use, based on their capabilities – this is called a cipher suite. And then the authentication part takes place as follows:
- Client sends the “clientHello” message to the server.
- Server responds back with the “serverHello '' message, TLS certificate which also contains the public key.
- Client verifies the certificate, encrypts the session key with the server public key and sends it to the server.
- Server decrypts the received message using it’s private key.
- Voila! Now both client and server can communicate securely using the shared symmetric session keys .

### :point_right: What is mutual TLS (mTLS)?
Mutual TLS, or mTLS for short, is a method for mutual authentication. mTLS ensures that the parties at each end of a network connection are who they claim to be by verifying that they both have the correct private key. E.g if you go to any website and if it’s TLS encrypted (like https://www.google.com) then you are sure that the response is from the authenticated server and you can verify it by clicking the lock icon in the address bar of your browser, however the server doesn’t know your identity at all, also it’s not possible for any public server to verify the identity of each client. Although the request and response would be fully encrypted in a TLS connection (without mTLS) using the shared symmetric session keys.

### :point_right: How does mTLS work?
Normally in TLS, the server has a TLS certificate and a public/private key pair, while the client does not. The typical TLS process works like as we saw above.\
In mTLS, however, both the client and server have a certificate, and both sides authenticate using their public/private key pair. Compared to regular TLS, there are additional steps in mTLS to verify both parties:
- Client connects to server
- Server presents its TLS certificate
- Client verifies the server's certificate
- Client presents its TLS certificate
- Server verifies the client's certificate
- Server grants access
- Client and server exchange information over encrypted TLS connection

### :point_right: Certificate authority in mTLS
All trusted TLS certificates are issued by a Certificate Authority (CA), which is a company that has been approved to issue digital certificates. \
However, in the case of mutual TLS, the organization implementing mTLS acts as its own certificate authority. This is different from standard TLS, in which the certificate authority is an external organization that checks if the certificate owner legitimately owns the associated domain.\
However, A "root" TLS certificate is necessary for mTLS; This enables an organization to be their own certificate authority. The certificates used by authorized clients and servers have to correspond to this root certificate. The root certificate is self-signed, meaning that the organization creates it themselves.

### :point_right: Why use mTLS?
mTLS helps ensure that traffic is secure and trusted in both directions between a client and server. This provides an additional layer of security for the users. mTLS prevents various kinds of attacks, including:\
On-path attacks, Credential stuffing, Brute force attacks, Phishing attacks, etc.

### :point_right: Thinking that websites already use TLS, so why is mTLS not used on the entire Internet?
For everyday purposes, one-way authentication provides sufficient protection. The goals of TLS on the public Internet are 1) to ensure that people do not visit spoofed websites, 2) to keep private data secure and encrypted as it crosses the various networks that comprise the Internet, and 3) to make sure that data is not altered in transit. One-way TLS, in which the client verifies the server's identity only, accomplishes these goals.\
Besides, distributing TLS certificates to all end user devices would be extremely difficult. Generating, managing, and verifying the billions of certificates necessary for this is a near-impossible task. But on a smaller scale, mTLS is highly useful and quite practical for individual organizations.

### :point_right: Curious to read and learn more about TLS? 
Head over to this awesome [article](https://www.thesslstore.com/blog/explaining-ssl-handshake/) on TLS.

Until then…

