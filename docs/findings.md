# Findings & Risk Analysis

## Medium-Risk Findings

### XML-RPC Endpoint Exposure
The XML-RPC endpoint was publicly accessible and processed unauthenticated requests. While no abuse was performed, this increases the application’s attack surface and has historically been targeted for credential-based and amplification attacks.

### User Enumeration via Public Endpoints
Valid usernames were disclosed through publicly accessible WordPress endpoints. This enables targeted authentication attacks if combined with other weaknesses.

---

## Low-Risk Findings

### Outdated WordPress Theme
The active theme was one version behind the latest release. While no exploit was confirmed, outdated components may introduce risk over time.

### Missing HTTP Security Headers
Several recommended browser-side security headers were not enforced, increasing exposure to certain client-side attack classes.

---

## Informational Observations
- Server version disclosure via HTTP headers  
- Public WordPress readme file accessible  
- External WP-Cron execution enabled  

---

## Positive Observations
- WordPress core fully up to date  
- No third-party plugins detected  
- Strong TLS configuration (TLS 1.3, modern cipher suites)  
- Administrative interfaces properly restricted  
