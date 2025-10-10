
Here’s a **most-used `curl` command set for cybersecurity work** in **Obsidian.md** format — concise, with practical hacker-style use cases so you can paste and reference quickly in your vault.

---

## #it/curl #it/cybersecurity #it/hacking/pentesting #cheatsheet

### **Basic GET request**

```bash
curl http://target.com
```

Fetch a webpage (default method: GET).

---

### **Follow redirects**

```bash
curl -L http://target.com
```

Useful for testing chains of `301/302` redirects.

---

### **Verbose output (full HTTP request/response)**

```bash
curl -v http://target.com
```

Shows request headers, response headers, TLS handshake details.

---

### **Include headers in output**

```bash
curl -i http://target.com
```

Useful for quick header inspection.

---

### **Send custom header**

```bash
curl -H "X-Forwarded-For: 127.0.0.1" http://target.com
```

Spoof headers for testing WAF or bypass logic.

---

### **Specify HTTP method**

```bash
curl -X POST http://target.com
```

Force a method regardless of defaults.

---

### **Send POST data**

```bash
curl -d "username=admin&password=pass" http://target.com/login
```

Default `Content-Type` is `application/x-www-form-urlencoded`.

---

### **Send JSON payload**

```bash
curl -X POST -H "Content-Type: application/json" \
-d '{"username":"admin","password":"pass"}' \
http://target.com/api/login
```

Common in API pentesting.

---

### **Send cookies**

```bash
curl -b "SESSIONID=abcd1234" http://target.com
```

Simulate authenticated requests.

---

### **Save cookies**

```bash
curl -c cookies.txt http://target.com
```

Store cookies for later replay.

---

### **Load cookies from file**

```bash
curl -b cookies.txt http://target.com
```

---

### **Change User-Agent**

```bash
curl -A "Mozilla/5.0 (X11; Linux x86_64)" http://target.com
```

Bypass simple bot detection.

---

### **Timeout**

```bash
# -m
curl --max-time 10 http://target.com
```

Stops hanging connections.

---

### **Test HTTPS / ignore SSL cert errors**

```bash
curl -k https://insecure-ssl-site.com
```

Good for self-signed certs in lab environments.

---

### **Get only HTTP headers**

```bash
curl -I http://target.com
```

Quick check for server info, content type, redirects.

---

### **Upload file**

```bash
curl -F "file=@/path/file.txt" http://target.com/upload
```

Test file upload endpoints.

---

### **HTTP Basic Auth**

```bash
curl -u admin:password http://target.com
```

For endpoints protected by basic auth.

---

### **Proxy support**

```bash
curl -x http://127.0.0.1:8080 http://target.com
```

Route traffic via Burp/Squid/etc.

---

### **Tor proxy**

```bash
curl --socks5 127.0.0.1:9050 http://target.onion
```

Access `.onion` services.

---

### **Save output to file**

```bash
curl -o output.html http://target.com
```

---
```bash
# --silent
curl -s http://example.com
```
