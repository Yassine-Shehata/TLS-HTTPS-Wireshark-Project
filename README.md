# TLS HTTPS Implementation and Traffic Analysis

## Overview

This project demonstrates the implementation and analysis of secure HTTPS communication using Transport Layer Security (TLS) within a virtualized Linux environment.

A complete Public Key Infrastructure (PKI) was implemented using OpenSSL, including the creation of a Root Certificate Authority (CA), server and client certificate generation, secure HTTPS communication, TLS packet analysis, and TLS traffic decryption using Wireshark.

The project focuses on practical understanding of modern TLS security mechanisms including TLS 1.3, certificate-based authentication, encrypted HTTPS communication, and secure key exchange.

---

# Features

* TLS 1.3 HTTPS communication
* Root Certificate Authority (CA) generation
* Server and client certificate signing
* OpenSSL HTTPS server implementation
* TLS handshake analysis
* Wireshark packet capture and inspection
* TLS traffic decryption using SSLKEYLOGFILE
* HTTPS request and response analysis
* Secure certificate-based authentication

---

# Technologies Used

* Linux Mint
* VMware Workstation Pro
* OpenSSL
* Wireshark
* Firefox

---

# TLS Security Components

| Component        | Description            |
| ---------------- | ---------------------- |
| TLS Version      | TLS 1.3                |
| Cipher Suite     | TLS_AES_256_GCM_SHA384 |
| Key Exchange     | X25519                 |
| Authentication   | RSA Certificates       |
| Encryption       | AES-256 GCM            |
| Traffic Analysis | Wireshark              |

---

# Project Structure

```text
TLS-HTTPS-Wireshark-Project/
│
├── certificates/
│   ├── rootCA.crt
│   ├── server.crt
│   └── client.crt
│
├── captures/
│   ├── tls_client_server_urIDs.pcapng
│   └── tls_decrypted_client_server_urIDs.pcap
│
├── screenshots/
│
├── website/
│   └── index.html
│
├── report/
│
└── README.md
```

---

# TLS Implementation Workflow

1. Root Certificate Authority creation
2. Server and client certificate generation
3. HTTPS TLS server implementation
4. TLS client connection establishment
5. HTTPS communication testing
6. Wireshark TLS packet capture
7. TLS traffic decryption and analysis

---

# Packet Analysis

The captured TLS traffic includes:

* Client Hello
* Server Hello
* Certificate exchange
* Encrypted Application Data
* HTTP GET request
* HTTP response packets

Wireshark was configured with exported TLS session secrets to decrypt encrypted HTTPS traffic successfully.

---

# Security Notes

The browser security warning displayed during testing is expected because the Root Certificate Authority used in this project is self-signed and not trusted by the operating system certificate store.

Private key files are intentionally excluded from the repository for security reasons.

---

# Author

Yassine Hesham Shehata

