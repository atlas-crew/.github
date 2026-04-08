<p align="center">
  <img src="banner.png" alt="Atlas Crew" width="100%">
</p>

<p align="center">
  <strong>Consulting services & open-source software.</strong><br>
  Edge protection, security testing, and career intelligence platforms.
</p>

---

## Horizon Security Platform

<p align="center">
  <img src="img/edge-protection-banner.png" alt="Horizon Security Platform" width="100%">
</p>

Embedded intelligence for API security and application defense. All detection and blocking decisions happen locally at the edge — zero external dependencies.

**[Synapse WAF](https://github.com/atlas-crew/horizon-security-platform)** — High-performance edge detection sensor built on Rust/Pingora. 237 WAF rules, 25 DLP patterns, campaign correlation, bot detection, behavioral analysis. Single binary, sub-10 microsecond detection latency at 72K req/s.

**[Signal Horizon](https://github.com/atlas-crew/horizon-security-platform)** — Multi-tenant fleet intelligence hub and SOC platform. Live threat map, campaign visualization, impossible travel detection, war room, and sensor management. Self-hosted or SaaS.

### Quick Install

```bash
# Synapse WAF
docker run -p 6190:6190 -p 6191:6191 nickcrew/synapse-waf

# Signal Horizon
docker run -p 3100:3100 \
  -e DATABASE_URL=postgresql://user:pass@host:5432/signal_horizon \
  nickcrew/horizon
```

### Packages

| Component | Install | Registry |
| --- | --- | --- |
| **Synapse WAF** | `docker pull nickcrew/synapse-waf` | [Docker Hub](https://hub.docker.com/r/nickcrew/synapse-waf) |
| **Signal Horizon** | `docker pull nickcrew/horizon` | [Docker Hub](https://hub.docker.com/r/nickcrew/horizon) |
| **Horizon** | `npm i -g @atlascrew/horizon` | [npm](https://www.npmjs.com/package/@atlascrew/horizon) |
| **Synapse CLI** | `npm i -g @atlascrew/synapse-client` | [npm](https://www.npmjs.com/package/@atlascrew/synapse-client) |
| **Synapse API Client** | `npm i @atlascrew/synapse-api` | [npm](https://www.npmjs.com/package/@atlascrew/synapse-api) |

### Links

| | |
|---|---|
| Repository | [atlas-crew/horizon-security-platform](https://github.com/atlas-crew/horizon-security-platform) |
| Documentation | [horizon.atlascrew.dev](https://horizon.atlascrew.dev) |
| Website | [atlascrew.dev/horizon](https://atlascrew.dev/horizon) |
| License | AGPL-3.0 |

---

## Inferno Lab

<p align="center">
  <img src="img/infernolab-social.png" alt="Inferno Lab — Three Tools. One Platform." width="100%">
</p>

Open-source security testing suite — attack simulation, vulnerability research, and compliance assessment. Three tools, one platform.

**[Apparatus](https://github.com/atlas-crew/Apparatus)** — Cybersecurity simulation lab built around a 13-protocol echo server. Multi-protocol traffic generation, deception, chaos engineering, and AI red team automation. Build, attack, and observe realistic environments.

**[Chimera](https://github.com/atlas-crew/Chimera)** — Intentionally vulnerable application with 450+ endpoints across 25+ industry verticals. 12 web apps representing real-world attack surfaces, plus an X-Ray inspector, guided exploit tours, WAF visualization, and LLM kill chain tracking.

**[Crucible](https://github.com/atlas-crew/Crucible)** — Attack simulation and compliance assessment engine with 120+ scenarios mapped to MITRE ATT&CK. Composable scenario chains, adaptive AI testing, and automated reporting against NIST 800-53, CIS Controls, PCI DSS, and HIPAA.

### Quick Install

```bash
# Apparatus
npm install -g @atlascrew/apparatus && apparatus

# Crucible
npm install -g @atlascrew/crucible && crucible start

# Chimera
pip install chimera-api && chimera-api --port 8880 --demo-mode full
```

### Packages

| Component | Install | Registry |
| --- | --- | --- |
| **Apparatus** | `npm i -g @atlascrew/apparatus` | [npm](https://www.npmjs.com/package/@atlascrew/apparatus) |
| **Apparatus CLI** | `npm i -g @atlascrew/apparatus-cli` | [npm](https://www.npmjs.com/package/@atlascrew/apparatus-cli) |
| **Crucible** | `npm i -g @atlascrew/crucible` | [npm](https://www.npmjs.com/package/@atlascrew/crucible) |
| **Chimera** | `pip install chimera-api` | [PyPI](https://pypi.org/project/chimera-api/) |

All three are also available as Docker images: `nickcrew/apparatus`, `nickcrew/crucible`, `nickcrew/chimera`.

### Links

| Product | Repository | Documentation |
| --- | --- | --- |
| **Apparatus** | [atlas-crew/Apparatus](https://github.com/atlas-crew/Apparatus) | [apparatus.atlascrew.dev](https://apparatus.atlascrew.dev) |
| **Chimera** | [atlas-crew/Chimera](https://github.com/atlas-crew/Chimera) | [chimera.atlascrew.dev](https://chimera.atlascrew.dev) |
| **Crucible** | [atlas-crew/Crucible](https://github.com/atlas-crew/Crucible) | [crucible.atlascrew.dev](https://crucible.atlascrew.dev) |

---

## About Atlas Crew

Atlas Crew is the consulting practice of [Nick Ferguson](https://linkedin.com/in/ncferguson). Available for SDLC modernization, platform engineering, AI integration, and developer experience work — the open source above is the proof of work.

[**atlascrew.dev/consulting**](https://atlascrew.dev/consulting) · [nick@atlascrew.dev](mailto:nick@atlascrew.dev) · [LinkedIn](https://linkedin.com/in/ncferguson)
