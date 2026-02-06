A Distributed Denial-of-Service (DDoS) attack is disrupt normal traffic of a targeted server, service, or network by **overwhelming it with a flood of Internet traffic** from multiple compromised sources. <br>

Types of DDoS Attack:
- Volume Based
- Protocol Attacks
- Application Layer

How to prevent ?
---
1. Network Layer
- **CDN + DDos Protection** : `Cloudflare`, `AWS Shield` + `Cloudfront`, `Akamai`, `Azure DDoS protection`
- **Rate-limiting**: `Nginx`, `API Gateway`, `Kubernetes Ingress`, `Cloudflare Roles`

2. Application Layer
- **WAF** ( Web Application Firewall )
- **Captcha**

3. Infrastructure level defenses
- **Autoscaling** - buys a time. wont stop the attack
- **Load balancing** : Never Expose the backend servers

4. OS-Firewall hardening
- **Firewall rules** : Close all ununsed ports
- **SYN** Flood protection ( Linux )

5. Monitoring & Detection:
- **Prometheus & Grafana**
- Watch for patterns and high requests.

6. API  Specific Protection
- JWT Validation ( JSON Web Token )
- Per-key rate limit
- API Keys
- Trottling per endpoint

7. In kubernetes
- Use **ingress** with ratelimit
- Enable **NetworkPolicies**
- Use **Servicemesh**
- Protect **NodePorts**
