<p align="center">
  <img src="banner.png" alt="Atlas Crew" width="100%">
</p>

<p align="center">
  <strong>Consulting services & open-source security platforms.</strong><br>
  Edge defense, adversary emulation, vulnerable targets, and platform infrastructure.
</p>

---

## Atlas Crew Security

<p align="center">
  <img src="img/atlas-crew-security-social.png" alt="Atlas Crew Security" width="100%">
</p>

A platform of five open-source products that close the loop on application security: detect at the edge, emulate adversaries, harden against real attack surfaces.

**Flagship trio** — security tools you'd recommend to peers:

- **Synapse** — Edge WAF + Fleet observability (the default defender; bring-your-own WAF also supported)
- **Chimera** — Vulnerable API targets (480+ endpoints, 25 verticals)
- **Crucible** — Adversary emulation (120+ scenarios, MITRE-mapped)

**Substrate tier** — quieter visual treatment for non-flagship products:

- **Bridge** — Service orchestrator (stands up and manages the lab)
- **Apparatus** — Innovation pipeline for the entire platform (sandbox where ideas prototype before becoming features in existing products, or entirely new ones)

End-to-end exercise: Crucible launches production-grade attack scenarios at Chimera's vulnerable endpoints; Synapse WAF sits in the request path as the default defender (or swap it for any WAF — Crucible and Chimera are WAF-agnostic). Bridge orchestrates the services, Synapse Fleet provides multi-tenant observability of WAF activity, and Apparatus sits alongside as the platform-wide R&D space where new ideas prototype before becoming features or new products.

<p align="center">
  <img src="img/atlas-crew-security-architecture.png" alt="Atlas Crew Security platform architecture: Synapse observes the trio at the top, Crucible exploits Chimera in the middle, Bridge and Apparatus form the substrate at the bottom" width="100%">
</p>

---

## Synapse

<p align="center">
  <img src="img/synapse-banner.png" alt="Synapse — Detect. Decide. Fire." width="100%">
</p>

Embedded edge defense — all detection and blocking decisions happen locally with zero external dependencies. Two products that pair: a high-performance detection sensor and a multi-tenant observability platform.

**[Synapse WAF](https://github.com/atlas-crew/synapse)** — Edge detection sensor built on Rust/Pingora. 237 WAF rules, 25 DLP patterns, campaign correlation, bot detection, behavioral analysis. Single binary, sub-10 microsecond detection latency at 72K req/s.

**[Synapse Fleet](https://github.com/atlas-crew/synapse)** — Multi-tenant fleet intelligence hub and SOC platform. Live threat map, campaign visualization, impossible-travel detection, war room, sensor management. Self-hosted or SaaS.

### Quick Install

```bash
# Synapse WAF
docker run -p 6190:6190 -p 6191:6191 nickcrew/synapse-waf

# Synapse Fleet
docker run -p 3100:3100 \
  -e DATABASE_URL=postgresql://user:pass@host:5432/synapse-fleet \
  nickcrew/synapse-fleet
```

### Packages

| Component              | Install                              | Registry                                                       |
| ---------------------- | ------------------------------------ | -------------------------------------------------------------- |
| **Synapse WAF**        | `docker pull nickcrew/synapse-waf`   | [Docker Hub](https://hub.docker.com/r/nickcrew/synapse-waf)    |
| **Synapse Fleet**      | `docker pull nickcrew/synapse-fleet` | [Docker Hub](https://hub.docker.com/r/nickcrew/synapse-fleet)  |
| **Synapse Fleet**      | `npm i -g @atlascrew/synapse-fleet`  | [npm](https://www.npmjs.com/package/@atlascrew/synapse-fleet)  |
| **Synapse CLI**        | `npm i -g @atlascrew/synapse-client` | [npm](https://www.npmjs.com/package/@atlascrew/synapse-client) |
| **Synapse API Client** | `npm i @atlascrew/synapse-api`       | [npm](https://www.npmjs.com/package/@atlascrew/synapse-api)    |

### Links

|               |                                                             |
| ------------- | ----------------------------------------------------------- |
| Repository    | [atlas-crew/synapse](https://github.com/atlas-crew/synapse) |
| Documentation | [synapse.atlascrew.dev](https://synapse.atlascrew.dev)      |
| Website       | [atlascrew.dev/synapse](https://atlascrew.dev/synapse)      |
| License       | AGPL-3.0                                                    |

---

## Chimera

<p align="center">
  <img src="img/chimera-banner.png" alt="Chimera — Vulnerable Targets" width="100%">
</p>

A vulnerable API platform at roughly 10× the scale of any comparable open-source lab. 480+ endpoints across 25 industry verticals, 12 of them wrapped in branded production-style web apps (healthcare, banking, e-commerce, SaaS, government, telecom, and six others). Business-logic flaws the generic OWASP labs don't touch. Guided exploit tours walk learners through the full kill chain. The X-Ray Inspector ties every vulnerability to the exact line of source and the fix. Not toy CTF puzzles — real attack surfaces authored with remediation built in.

### Quick Install

```bash
pip install chimera-api && chimera-api --port 8880 --demo-mode full
```

### Packages

| Component   | Install                   | Registry                                      |
| ----------- | ------------------------- | --------------------------------------------- |
| **Chimera** | `pip install chimera-api` | [PyPI](https://pypi.org/project/chimera-api/) |

Also available as `nickcrew/chimera` on Docker Hub.

### Links

|               |                                                             |
| ------------- | ----------------------------------------------------------- |
| Repository    | [atlas-crew/Chimera](https://github.com/atlas-crew/Chimera) |
| Documentation | [chimera.atlascrew.dev](https://chimera.atlascrew.dev)      |
| Website       | [atlascrew.dev/chimera](https://atlascrew.dev/chimera)      |
| License       | MIT                                                         |

---

## Crucible

<p align="center">
  <img src="img/crucible-banner.png" alt="Crucible — Adversary Emulation" width="100%">
</p>

The production-grade adversary emulation engine. 120+ attack scenarios authored against Chimera's specific vulnerabilities, with a DAG execution engine, live WebSocket simulation, and pass/fail assessment against ground-truth assertions. Every scenario knows what should work, what shouldn't, and where in the target it's exploiting. Point it at Chimera (with Bridge orchestrating the services) for the full integrated run, or bring your own targets.

### Quick Install

```bash
npm install -g @atlascrew/crucible && crucible start
```

### Packages

| Component           | Install                               | Registry                                                        |
| ------------------- | ------------------------------------- | --------------------------------------------------------------- |
| **Crucible**        | `npm i -g @atlascrew/crucible`        | [npm](https://www.npmjs.com/package/@atlascrew/crucible)        |
| **Crucible CLI**    | `npm i -g @atlascrew/crucible-cli`    | [npm](https://www.npmjs.com/package/@atlascrew/crucible-cli)    |
| **Crucible Client** | `npm i -g @atlascrew/crucible-client` | [npm](https://www.npmjs.com/package/@atlascrew/crucible-client) |

Also available as `nickcrew/crucible` on Docker Hub.

### Links

|               |                                                               |
| ------------- | ------------------------------------------------------------- |
| Repository    | [atlas-crew/Crucible](https://github.com/atlas-crew/Crucible) |
| Documentation | [crucible.atlascrew.dev](https://crucible.atlascrew.dev)      |
| Website       | [atlascrew.dev/crucible](https://atlascrew.dev/crucible)      |
| License       | MIT                                                           |

---

## Bridge

<p align="center">
  <img src="img/bridge-banner.png" alt="Bridge — Service Orchestrator" width="100%">
</p>

Single-binary service orchestrator for security labs. Stands up Crucible, Chimera, and any custom services in a coordinated graph; manages dependencies, health checks, and teardown. Substrate-tier — quieter branding than the flagship trio because Bridge is the platform you build security work on, not the security work itself.

### Quick Install

```bash
npm install -g @atlascrew/bridge && bridge up
```

### Packages

| Component  | Install                      | Registry                                               |
| ---------- | ---------------------------- | ------------------------------------------------------ |
| **Bridge** | `npm i -g @atlascrew/bridge` | [npm](https://www.npmjs.com/package/@atlascrew/bridge) |

### Links

|            |                                                           |
| ---------- | --------------------------------------------------------- |
| Repository | [atlas-crew/bridge](https://github.com/atlas-crew/bridge) |
| Website    | [atlascrew.dev/bridge](https://atlascrew.dev/bridge)      |
| License    | MIT                                                       |

---

## Apparatus

<p align="center">
  <img src="img/apparatus-banner.png" alt="Apparatus — Cybersecurity Simulation Lab" width="100%">
</p>

The platform-wide innovation pipeline. Where new ideas prototype before they're absorbed as features in existing products (Synapse, Crucible, Chimera, Bridge) or shipped as entirely new products. Provides scenario builder, traffic generation, JWT/MTD modules, supply-chain attack simulation, timeline visualization, and red-team validation — experimental tooling that overlaps with what Crucible does, but in research form. Not production-grade like Crucible; it's the lab where everything in the platform first takes shape. Substrate-tier visually, sibling to Bridge.

### Quick Install

```bash
npm install -g @atlascrew/apparatus && apparatus
```

### Packages

| Component         | Install                             | Registry                                                      |
| ----------------- | ----------------------------------- | ------------------------------------------------------------- |
| **Apparatus**     | `npm i -g @atlascrew/apparatus`     | [npm](https://www.npmjs.com/package/@atlascrew/apparatus)     |
| **Apparatus CLI** | `npm i -g @atlascrew/apparatus-cli` | [npm](https://www.npmjs.com/package/@atlascrew/apparatus-cli) |

Also available as `nickcrew/apparatus` on Docker Hub.

### Links

|               |                                                                 |
| ------------- | --------------------------------------------------------------- |
| Repository    | [atlas-crew/Apparatus](https://github.com/atlas-crew/Apparatus) |
| Documentation | [apparatus.atlascrew.dev](https://apparatus.atlascrew.dev)      |
| Website       | [atlascrew.dev/apparatus](https://atlascrew.dev/apparatus)      |
| License       | MIT                                                             |

---

## Facet

<p align="center">
  <img src="img/facet-github-banner.png" alt="Facet — Same diamond. Different face." width="100%">
</p>

AI-powered career platform. Build a deep model of who you are professionally, then let it find the right jobs, assemble targeted materials, and prep for interviews. The system gets smarter with every interaction.

**The Loop** — Research → Pipeline → Build → Letters → Prep. Five workspaces that feed each other: AI-inferred job search, opportunity tracking, targeted resume generation, cover letters from pipeline context, and interview prep decks. Results feed back into Research to improve targeting.

Separate from the security platform, same engineering principles. Hosted or self-hosted.

### Try It

```bash
# Hosted (free tier available)
open https://demo.myfacets.cv

# Self-host
git clone https://github.com/atlas-crew/Facet
cd Facet && docker compose up
```

### Links

|            |                                                         |
| ---------- | ------------------------------------------------------- |
| Repository | [atlas-crew/Facet](https://github.com/atlas-crew/Facet) |
| Live Demo  | [demo.myfacets.cv](https://demo.myfacets.cv)            |
| Website    | [atlascrew.dev/facet](https://atlascrew.dev/facet)      |
| License    | AGPL-3.0                                                |

---

## About Atlas Crew

Atlas Crew is the name the work above is published under. Available for SDLC modernization, platform engineering, AI integration, and developer experience work.

[**atlascrew.dev/about**](https://atlascrew.dev/about) · [nick@atlascrew.dev](mailto:nick@atlascrew.dev) · [LinkedIn](https://linkedin.com/in/ncferguson)
