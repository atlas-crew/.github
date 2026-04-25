<p align="center">
  <img src="banner.png" alt="Atlas Crew" width="100%">
</p>

<p align="center">
  <strong>Consulting services & open-source software.</strong><br>
  Edge protection, security testing, and career intelligence platforms.
</p>

---

## Synapse Edge Defense

<p align="center">
  <img src="img/synapse-social.png" alt="Synapse Edge Defense" width="100%">
</p>

Embedded intelligence for API security and application defense. All detection and blocking decisions happen locally at the edge — zero external dependencies.

**[Synapse WAF](https://github.com/atlas-crew/synapse)** — High-performance edge detection sensor built on Rust/Pingora. 237 WAF rules, 25 DLP patterns, campaign correlation, bot detection, behavioral analysis. Single binary, sub-10 microsecond detection latency at 72K req/s.

**[Synapse Fleet](https://github.com/atlas-crew/synapse)** — Multi-tenant fleet intelligence hub and SOC platform. Live threat map, campaign visualization, impossible travel detection, war room, and sensor management. Self-hosted or SaaS.

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
| **SynapserFleet**      | `docker pull nickcrew/synapse-fleet` | [Docker Hub](https://hub.docker.com/r/nickcrew/horizon)        |
| **Synapse Fleet**      | `npm i -g @atlascrew/synapse-fleet`  | [npm](https://www.npmjs.com/package/@atlascrew/synapse-fleet)  |
| **Synapse CLI**        | `npm i -g @atlascrew/synapse-client` | [npm](https://www.npmjs.com/package/@atlascrew/synapse-client) |
| **Synapse API Client** | `npm i @atlascrew/synapse-api`       | [npm](https://www.npmjs.com/package/@atlascrew/synapse-api)    |

### Links

|               |                                                             |
| ------------- | ----------------------------------------------------------- |
| Repository    | [atlas-crew/synapse](https://github.com/atlas-crew/synapse) |
| Documentation | [synapse.atlascrew.dev](https://horizon.atlascrew.dev)      |
| Website       | [atlascrew.dev/synapse](https://atlascrew.dev/synapse)      |
| License       | AGPL-3.0                                                    |

---

## Inferno Lab

<p align="center">
  <img src="infernolab-hero.png" alt="Inferno Lab — Two Tools. One Platform." width="100%">
</p>

Open-source security testing suite — attack simulation, vulnerability research, and compliance assessment. Three tools, one platform.

**[Chimera](https://github.com/atlas-crew/Chimera)** — Chimera is a vulnerable API platform at roughly 10x the scale of any comparable open-source lab. 480+ endpoints across 25 industry verticals, 12 of them wrapped in branded production-style web apps (healthcare, banking, e-commerce, SaaS, government, telecom, and six others). Business-logic flaws the generic OWASP labs don't touch. Guided exploit tours walk learners through the full kill chain. The X-Ray Inspector ties every vulnerability to the exact line of source and the fix. Not toy CTF puzzles. Real attack surfaces authored with remediation built in.

**[Crucible](https://github.com/atlas-crew/Crucible)** — Crucible is the adversary emulation engine. 120+ attack scenarios authored against Chimera's specific vulnerabilities, with a DAG execution engine, live WebSocket simulation, and pass/fail assessment against ground-truth assertions. Every scenario knows what should work, what shouldn't, and where in the target it's exploiting. Point it at Apparatus plus Chimera for the full integrated run, or bring your own targets.

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

| Component         | Install                             | Registry                                                      |
| ----------------- | ----------------------------------- | ------------------------------------------------------------- |
| **Apparatus**     | `npm i -g @atlascrew/apparatus`     | [npm](https://www.npmjs.com/package/@atlascrew/apparatus)     |
| **Apparatus CLI** | `npm i -g @atlascrew/apparatus-cli` | [npm](https://www.npmjs.com/package/@atlascrew/apparatus-cli) |
| **Crucible**      | `npm i -g @atlascrew/crucible`      | [npm](https://www.npmjs.com/package/@atlascrew/crucible)      |
| **Chimera**       | `pip install chimera-api`           | [PyPI](https://pypi.org/project/chimera-api/)                 |

All three are also available as Docker images: `nickcrew/apparatus`, `nickcrew/crucible`, `nickcrew/chimera`.

### Links

| Product       | Repository                                                      | Documentation                                              |
| ------------- | --------------------------------------------------------------- | ---------------------------------------------------------- |
| **Apparatus** | [atlas-crew/Apparatus](https://github.com/atlas-crew/Apparatus) | [apparatus.atlascrew.dev](https://apparatus.atlascrew.dev) |
| **Chimera**   | [atlas-crew/Chimera](https://github.com/atlas-crew/Chimera)     | [chimera.atlascrew.dev](https://chimera.atlascrew.dev)     |
| **Crucible**  | [atlas-crew/Crucible](https://github.com/atlas-crew/Crucible)   | [crucible.atlascrew.dev](https://crucible.atlascrew.dev)   |

---

## Facet

<p align="center">
  <img src="img/facet-github-banner.png" alt="Facet — Same diamond. Different face." width="100%">
</p>

AI-powered career platform. Build a deep model of who you are professionally, then let it find the right jobs, assemble targeted materials, and prep for interviews. The system gets smarter with every interaction.

**The Loop** — Research → Pipeline → Build → Letters → Prep. Five workspaces that feed each other: AI-inferred job search, opportunity tracking, targeted resume generation, cover letters from pipeline context, and interview prep decks. Results feed back into Research to improve targeting.

Separate from the security suite, same engineering principles. Hosted or self-hosted.

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
