<p align="center">
  <img src="banner.png" alt="Atlas Crew" width="100%">
</p>

Product engineering and open-source security tools.

## Horizon Security Platform

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
| Website | [atlascrew.dev](https://atlascrew.dev) |
| License | AGPL-3.0 |

## Inferno Lab

Open-source security testing suite — attack simulation, vulnerability research, and compliance assessment.

**[Apparatus](https://github.com/inferno-lab/Apparatus)** — Cybersecurity simulation lab with 58+ features spanning deception, chaos engineering, red team automation, and multi-protocol support.

**[Crucible](https://github.com/inferno-lab/Crucible)** — Attack simulation and compliance assessment engine with 80+ scenarios, visual editor, real-time execution, and pass/fail scoring.

**[Chimera](https://github.com/inferno-lab/Chimera)** — Intentionally vulnerable application with 456+ endpoints across 25+ industry verticals for WAF testing and security education.

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
| **Apparatus** | [inferno-lab/Apparatus](https://github.com/inferno-lab/Apparatus) | [apparatus.atlascrew.dev](https://apparatus.atlascrew.dev) |
| **Crucible** | [inferno-lab/Crucible](https://github.com/inferno-lab/Crucible) | [crucible.atlascrew.dev](https://crucible.atlascrew.dev) |
| **Chimera** | [inferno-lab/Chimera](https://github.com/inferno-lab/Chimera) | [chimera.atlascrew.dev](https://chimera.atlascrew.dev) |
