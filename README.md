# NGINX Research Documentation

This repository contains **research and practical implementations** of NGINX features, covering core functionalities like reverse proxy, load balancing, SSL/TLS, security, caching, PHP integration, and more. It is designed for **educational and research purposes**.

---

## **Prerequisites**

- **Docker** (Installed and running)
- **Docker Compose** (For managing multi-container setups)
- Basic familiarity with **terminal commands**
- A text editor (e.g., VS Code, Sublime Text)

---
## **Tasks Performed**

### **Core NGINX Features**
- **Serve static content** using `root` and `index` directives.
- **Configure reverse proxy** with `proxy_pass` and custom headers (`Host`, `X-Real-IP`, `X-Forwarded-For`).
- **Set up load balancing** with:
  - Round Robin (default)
  - `least_conn` (least connections)
  - `ip_hash` (session persistence)

### **Security & Performance**
- **Enable SSL/TLS** using self-signed certificates.
- **Implement security headers**:
  - HSTS (`Strict-Transport-Security`)
  - CSP (`Content-Security-Policy`)
  - XSS Protection (`X-XSS-Protection`)
  - Frame Options (`X-Frame-Options`)
  - MIME-Type Options (`X-Content-Type-Options`)
- **Add basic authentication** for restricted areas.
- **Implement rate limiting** and **connection limits** to control traffic.
- **Set up proxy caching** with `proxy_cache` and validate cache hits/misses.

### **Dynamic Content & Advanced Routing**
- **Integrate PHP** using PHP-FPM and `fastcgi_pass`.
- **Add WebSocket support** through proxy configuration (`Upgrade` and `Connection` headers).
- **Configure URL rewriting and redirects** for clean and maintainable URLs.
- **Create custom error pages** (e.g., 404, 500) for better user experience.

### **Multi-Site & Logging**
- **Host multiple sites** with subdomains and separate server blocks.
- **Use NGINX variables** like `$host`, `$remote_addr`, and `$request_uri` for dynamic configurations.
- **Modify `nginx.conf`** using the `include` directive to organize configurations.
- **Customize access logs** for detailed request tracking.

---

## **How to Use**

1. **Clone the repository** (or create the directory structure manually).
2. **Update configurations** as needed for your use case.
3. **Run the services**:
   ```bash
   docker-compose up -d
4. **Stop the services**:
   ```bash
   docker-compose down -v
