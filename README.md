<h1 align="center">Hi, I'm Rob 👋</h1>
<p align="center">
  <strong>Senior SRE • AI Reliability • Open Source</strong><br/>
  Creator of the <a href="https://github.com/rsionnach/opensrm">OpenSRM</a> ecosystem
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Role-Senior%20SRE-4B9CD3?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Open%20Source-Maintainer-4BCF93?style=for-the-badge" />
  <img src="https://img.shields.io/badge/GasTown-Contributor-E85D2C?style=for-the-badge" />
</p>

---

## 💡 The Thesis

Reliability engineering and AI are on a collision course, and both sides need each other.

Traditional SRE gave us SLOs, error budgets, and deployment gates for deterministic systems. But AI agents make decisions that can't be validated with unit tests. A code review bot with 99.9% availability can still approve PRs with critical security vulnerabilities dozens of times a day, and nobody's tracking that.

Meanwhile, AI systems are being deployed into production without the reliability practices that every other critical service takes for granted. No SLO contracts. No dependency math. No deployment gates based on decision quality.

I'm building the tooling that connects these two worlds: bringing SRE discipline to AI systems, and extending SRE for the judgment-quality problems that AI introduces.

I wrote about this: **[Your AI Agent Is Available, Fast, and Making Terrible Decisions](https://dev.to/rsionnach/your-ai-agent-is-available-fast-and-making-terrible-decisions-54ac)** (judgment SLOs), **[OpenSRM: An Open Specification for Service Reliability](https://dev.to/rsionnach/opensrm-an-open-specification-for-service-reliability-44bi)**, and **[Shift-Left Reliability](https://dev.to/rsionnach/shift-left-reliability-4poo)**.

---

## 🔧 The OpenSRM Ecosystem

**[OpenSRM](https://github.com/rsionnach/opensrm)** is an open specification for declaring service reliability requirements as code, including judgment SLOs for AI decision quality. The spec is the shared contract that every component reads.

Five independent tools compose through the spec without depending on each other:

**[NthLayer](https://github.com/rsionnach/nthlayer)** — Generate your entire monitoring stack from a single YAML manifest. Prometheus rules, Grafana dashboards, PagerDuty configs, deployment gates. Deterministic, no AI required.

**[Arbiter](https://github.com/rsionnach/arbiter)** — Universal quality measurement for AI agent output. Point it at your agents, it tells you which ones are producing good work and which are silently degrading. Tracks per-agent quality trends, self-calibrates through human correction signals, and governs agent autonomy.

**[SitRep](https://github.com/rsionnach/sitrep)** — Situational awareness at enterprise scale. Pre-correlates millions of observability signals continuously so that when something breaks, the correlated picture is already built. Seconds to a situation snapshot, not minutes of manual dashboard correlation.

**[Mayday](https://github.com/rsionnach/mayday)** — AI-coordinated incident response. Specialised agents handle triage, investigation, communication, and remediation under human supervision. Findings flow back into the ecosystem so the system learns from every incident.

Each tool works alone. Together they form a complete reliability lifecycle: define (OpenSRM) → generate (NthLayer) → measure (Arbiter) → correlate (SitRep) → respond (Mayday) → learn (back to OpenSRM).

---

## 🏗️ GasTown Contributions

The ecosystem's quality measurement concepts were proven inside [GasTown](https://github.com/steveyegge/gastown) (Steve Yegge's multi-agent workspace manager):

- **[Guardian](https://github.com/steveyegge/gastown/pull/2263)** — Quality-review layer for the internal merge pipeline, implemented as a Deacon plugin. Scores per-worker output, tracks quality trends, alerts on degradation. Fix-merged to main by Steve Yegge.
- **[Feed problems view refactor](https://github.com/steveyegge/gastown/pull/1583)** — Replaced tmux scraping with structured beads-based health detection. Merged via dual-model review (5 iteration passes).

---

## 🧭 Architecture Principles

**Zero Framework Cognition (ZFC):** Transport is code. Judgment is model. Code handles deterministic transformation. The model handles interpretation. Every component in the ecosystem follows this boundary.

**The spec is the integration layer:** Components don't import each other's code. They all read OpenSRM manifests and emit OTel telemetry following shared semantic conventions. Adopt one tool or all five.

**Independence is the feature:** Unlike platforms where you must adopt everything to get value, each component solves a complete problem alone.

---

## 📫 Connect

- **OpenSRM Ecosystem:** [github.com/rsionnach/opensrm](https://github.com/rsionnach/opensrm)
- **Articles:** [Judgment SLOs](https://dev.to/rsionnach/your-ai-agent-is-available-fast-and-making-terrible-decisions-54ac) • [OpenSRM Spec](https://dev.to/rsionnach/opensrm-an-open-specification-for-service-reliability-44bi) • [Shift-Left Reliability](https://dev.to/rsionnach/shift-left-reliability-4poo)
- **LinkedIn:** [rob-fox-29a29024](https://www.linkedin.com/in/rob-fox-29a29024/)
- **GasTown Discord:** Active contributor in the Wasteland community
