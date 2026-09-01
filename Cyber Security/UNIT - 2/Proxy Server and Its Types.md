# Proxy Server and Its Types – 13 Mark Answer

## 1. Introduction

A **proxy server** acts as a **gateway between a user's device and the Internet**. Instead of connecting directly to the destination server, the user's request first goes through the proxy server. It can **hide the user's IP address, improve privacy, filter traffic, control Internet usage and improve network performance**. 

---

## 2. How a Proxy Server Works

The working of a proxy can be explained in the following steps:

1. **Client → Proxy:** The client sends the request to the proxy instead of directly accessing the Internet.
2. **Proxy Decision:** The proxy checks its rules, filters and cache.
3. **Cache Check:** If the requested content is already cached, the proxy sends it directly to the client.
4. **Request Forwarding:** If it is not cached, the proxy forwards the request to the target server.
5. **Response Handling:** The target server sends the response to the proxy.
6. **Client Delivery:** The proxy sends the response back to the client.

During this process, the proxy can **hide the client's real IP, filter or block requests, log activities and improve performance through caching**. 

### Simple Diagram

**Client → Proxy Server → Internet/Target Server**

**Target Server → Proxy Server → Client**

---

# 3. Types of Proxy Servers

The PDF describes **12 types of proxy servers**.

### 1. Forward Proxy

A **forward proxy** is placed between the client and the Internet. It sends requests to the target server on behalf of the client. The target server sees the **proxy's IP address** instead of the client's.

**Uses:**

* Content filtering
* Hiding user's IP
* Monitoring employee Internet usage 

---

### 2. Transparent Proxy

A **transparent proxy** intercepts communication without requiring configuration on the client. It can **log traffic and enforce policies**, but it does not hide the client's original IP address.

**Uses:**

* Caching
* Monitoring user activities
* Optimizing bandwidth by ISPs 

---

### 3. Anonymous Proxy

An **anonymous proxy** hides the client's IP address from the destination server but identifies itself as a proxy.

**Uses:**

* Maintaining online privacy
* Preventing website tracking
* Avoiding targeted advertising 

---

### 4. High-Anonymity Proxy (Elite Proxy)

A **high-anonymity proxy** hides both the user's IP address and the fact that a proxy is being used. Therefore, it is difficult for the destination server to detect the proxy.

**Uses:**

* Maximum privacy
* Bypassing geo-restrictions and censorship
* Avoiding IP bans 

---

### 5. Distorting Proxy

A **distorting proxy** hides the real IP address and provides a **fake IP address** to the target server. It can therefore make the request appear to come from a different location.

**Uses:**

* Accessing region-restricted content
* Hiding the actual geographical location 

---

### 6. Data Center Proxy

A **data center proxy** uses IP addresses provided by data centers rather than residential Internet service providers. They are generally **fast and inexpensive**, but websites can detect and block them more easily.

**Uses:**

* High-speed data retrieval
* Large-scale automated requests
* Web scraping 

---

### 7. Residential Proxy

A **residential proxy** uses IP addresses assigned by real ISPs to residential users. Therefore, requests appear to come from actual home devices and are harder to detect.

**Uses:**

* Web scraping
* Accessing geo-restricted websites
* Reducing the possibility of being blocked 

---

### 8. Public Proxy

A **public proxy** is freely available for anyone to use, usually without authentication. Since many users share it, it can be **slow, overloaded and insecure**.

**Uses:**

* Basic anonymity
* Bypassing minor restrictions

It is **not recommended for sensitive activities**. 

---

### 9. Shared Proxy

A **shared proxy** is used by multiple clients at the same time. Users share the same IP address, which may cause performance problems or IP blocking.

**Uses:**

* Affordable privacy
* Light browsing
* Non-sensitive work 

---

### 10. SSL (HTTPS) Proxy

An **SSL proxy** uses SSL encryption to protect communication between the client and proxy and between the proxy and target server.

**Uses:**

* Protecting banking and other sensitive transactions
* Securing data over public Wi-Fi 

---

### 11. Rotating Proxy

A **rotating proxy** automatically changes its IP address at fixed intervals or for every request. This makes tracking and IP-based blocking more difficult.

**Uses:**

* Large-scale web scraping
* Avoiding rate limits
* Avoiding IP bans 

---

### 12. Reverse Proxy

A **reverse proxy** is placed between the Internet and a web server. It receives client requests and forwards them to the actual backend server. The client does not directly communicate with the backend server.

**Uses:**

* Protecting backend servers from direct attacks
* Load balancing
* Caching content
* Improving performance 

---

# 4. Uses of Proxy Servers

Proxy servers are commonly used for:

1. **Privacy and Anonymity** – Hides the client's real IP address.
2. **Security** – Acts as a barrier between internal networks and external threats.
3. **Content Filtering** – Blocks unwanted websites or categories.
4. **Load Balancing** – Distributes requests across multiple servers.
5. **Caching** – Stores frequently accessed content to improve speed.
6. **Bypassing Geo-Restrictions** – Allows access to region-specific content.
7. **DDoS Protection** – Filters massive traffic before it reaches the actual server.
8. **Monitoring and Logging** – Records network activities for security and compliance. 

---

## 5. Conclusion

A **proxy server** provides an intermediate layer between clients and the Internet. It can improve **privacy, security, filtering, performance and network control**. Different types such as **Forward, Transparent, Anonymous, High-Anonymity, Distorting, Data Center, Residential, Public, Shared, SSL, Rotating and Reverse proxies** are used according to specific requirements.

**For exam:** Draw the simple diagram **Client → Proxy Server → Internet → Target Server** and then explain the **12 types with definition + one or two uses**. This is enough to make a strong 13-mark answer.
