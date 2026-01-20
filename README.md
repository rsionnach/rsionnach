<h1 align="center">Hi, I'm Rob 👋</h1>

<p align="center">
  <strong>Senior SRE • Shift-Left Reliability • Open Source</strong><br/>
  Creator & Maintainer of <a href="https://github.com/rsionnach/nthlayer">NthLayer</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Role-Senior%20SRE-4B9CD3?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Open%20Source-Maintainer-4BCF93?style=for-the-badge" />
  <img src="https://img.shields.io/github/stars/rsionnach/nthlayer?label=NthLayer%20Stars&style=for-the-badge" />
</p>

---

**[NthLayer](https://github.com/rsionnach/nthlayer)** — Shift-left reliability for platform teams.

**NthLayer** is an open-source **Operations-as-Code engine** that generates the entire observability and reliability stack from a single YAML file.

Most reliability decisions happen too late — after deployment, during incidents, in postmortems. NthLayer moves them earlier:

| Problem | NthLayer Solution |
|---------|-------------------|
| SLOs set in isolation | Validate against dependency chains |
| Alert when budget exhausted | Predict exhaustion with drift detection |
| Missing metrics found in incidents | Enforce before deployment |
| "Is this ready?" = opinion | "Is this ready?" = deterministic CI check |

```bash
pip install nthlayer
nthlayer check-deploy --service payment-api
```

**→ [github.com/rsionnach/nthlayer](https://github.com/rsionnach/nthlayer)**

---

## 💡 The Thesis

Reliability has a timing problem. We've invested heavily in incident response — better alerting, faster recovery, thorough postmortems. But when in a service's lifecycle do we *define* reliability? 

GitHub gave us version control for code. Terraform gave us version control for infrastructure. Security has shift-left. **Reliability should too.**

I wrote about this: **[Shift-Left Reliability](https://dev.to/rsionnach/shift-left-reliability-4poo)**

---

## 🔭 Current Work & Focus

- **Drift detection** — Predict SLO exhaustion before it happens
- **Dependency intelligence** — Calculate what SLO targets are actually achievable
- **CI/CD gates** — Block deploys when error budget is exhausted
- **Metric enforcement** — Validate OpenTelemetry conventions before production

---

## 📫 Connect

- **NthLayer:** [github.com/rsionnach/nthlayer](https://github.com/rsionnach/nthlayer)
- **Article:** [Shift-Left Reliability](https://dev.to/rsionnach/shift-left-reliability-4poo)
- **LinkedIn:** [rob-fox-29a29024](https://www.linkedin.com/in/rob-fox-29a29024/)
