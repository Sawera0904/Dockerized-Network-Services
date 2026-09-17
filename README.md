# Dockerized-Network-Services
This project demonstrates the deployment of essential network infrastructure services — DNS, DHCP, and HTTP Proxy — as isolated Docker containers, showcasing containerization as a lightweight alternative to traditional dedicated network servers.

✨ Features ✅ DNS Service

🌐 BIND9 configured as an authoritative name server 📁 Custom zone (csne.vcct.com) resolving to the local subnet 🔍 Verified with dig from both server and client ✅ DHCP Service

📡 ISC-DHCP-Server issuing dynamic leases (192.168.8.130–160) 🌍 Configured with gateway, subnet mask, and DNS options ✅ Handshake tested (DISCOVER → OFFER → REQUEST → ACK) ✅ Proxy Service

🧭 Squid proxy handling HTTP traffic on port 3128 📦 Caching enabled with access restricted to the local subnet 📊 Verified via curl with cache-hit confirmation ✅ Image Distribution

🐳 All images built from custom Dockerfiles ☁️ Pushed to Docker Hub (sawera2001) for pull & redeploy 🔁 Redeployment tested end-to-end from remote pull ✅ Orchestration

🧩 Docker Compose file managing all three services together 
▶️ Single-command startup for the full stack

✅ Technologies Used
🐧 Ubuntu 22.04 (host) / Ubuntu 24.04 (containers) 
🐳 Docker CE & Docker Compose 
🌐 BIND9 (DNS) 
📡 ISC-DHCP-Server (DHCP) 
🧭 Squid (Proxy) 
☁️ Docker Hub (image registry)

🚀 Setup Overview 
1️⃣ Install Docker and Docker Compose on Ubuntu host
2️⃣ Build DNS, DHCP, and Proxy images from their Dockerfiles
3️⃣ Run containers individually or via docker-compose up -d
4️⃣ Push images to Docker Hub for versioning and sharing
5️⃣ Join a client machine to test DHCP leasing and DNS resolution
6️⃣ Validate proxy caching and connectivity with curl

💡 Key Takeaways Lightweight virtualization of critical network services using containers Reproducible, version-controlled infrastructure via Dockerfiles and Docker Hub Simplified multi-service orchestration with Docker Compose End-to-end validation from server build through live client testing
