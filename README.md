<h1 align="center">João Curcino</h1>

<p align="center">
Software Engineer • <strong>Python &amp; RPA</strong> • Financial &amp; Accounting Automation
</p>

<p align="center">
<a href="https://joaopec.com" target="_blank" rel="noopener noreferrer">🌐 Portfolio</a> •
<a href="mailto:joaopecurcino.dev@gmail.com">📩 Email</a> •
<a href="https://www.linkedin.com/in/jo%C3%A3o-curcino-490601262" target="_blank" rel="noopener noreferrer">💼 LinkedIn</a>
</p>

---

I take over **financial and accounting routines** that are still done by hand: order × payment reconciliation, billing and receivables, report generation, and the thankless layer between systems that were never designed to talk to each other — ERPs, banks, government portals, spreadsheets and legacy REST/SOAP APIs.

The default stack for that is **Python** (stdlib first, idempotent, tested), **Playwright** when the only interface available is a web page, and SQL when the data has to be trustworthy. Full-stack engineer at **Infocraft** (2024–) and **NewChase** (2026–), with a background in payment systems (PIX, boleto, card), event-driven architecture (**Kafka**) and production products in **NestJS, Flutter, Next.js and Laravel**.

---

## ⚙️ What an automation from me looks like

These run unattended at month-end. So the requirements are not "it works" — they are "it works again next month, on data nobody cleaned":

- **Idempotent** — persistent state (SQLite) so re-running the same input never duplicates a record or a payment.
- **Deterministic rules** — tie-breaking is explicit and ordered (`invalid data → duplicate payment → missing payment → reconciled → partial / overpaid`), not an accident of `if` order nobody remembers.
- **Config, not code** — tolerance (`R$ 0.01`) and eligible order statuses live in `config.toml`, so finance changes it without a deploy.
- **LGPD by default** — CPF/CNPJ validated by check digits and never written to an output file or a log line.
- **Operable** — semantic exit codes (`0` ok / `1` bad input / `2` bad config), per-job logging and a local panel for whoever doesn't live in a terminal.
- **Tested against real mess** — duplicate IDs, conflicting records, values in the wrong locale format, already-processed records. All of it covered.

## 🚀 Selected work

| | |
|---|---|
| **🔁 Order × payment reconciliation** — Python automation that classifies every order, isolates the divergences and publishes `conciliacao.csv` / `erros.csv` / `resumo.json`. Stdlib only, 37 tests, idempotent by design. *(private — NewChase technical challenge)* | **🧥 [Vistta](https://vistta.app)** — C2C marketplace for second-hand fashion. **NestJS** backend, **Next.js** web and **Flutter** mobile. Real-time chat, listings & transactions. |
| **👻 [FormPhantom](https://formphantom.vercel.app)** — Chrome extension that auto-fills job application forms. Persistent profile, PDF extraction and smart field matching (LinkedIn, Gupy, Greenhouse, Lever…). | **📈 [Markowitz](https://github.com/JoaoPec/Fronteira-de-Markowitz)** — B3 portfolio optimization in Python: efficient frontier, risk vs return, financial modeling. |

---

## 🧠 Stack

**Automation** ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) ![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat&logo=playwright&logoColor=white) ![RPA](https://img.shields.io/badge/RPA-4B5563?style=flat) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white) ![Excel](https://img.shields.io/badge/Excel%20%2F%20CSV-217346?style=flat&logo=microsoftexcel&logoColor=white)

**Backend** ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white) ![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat&logo=nestjs&logoColor=white) ![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=flat&logo=laravel&logoColor=white) ![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)

**Frontend & Mobile** ![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white) ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white) ![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)

**Data & Infra** ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat&logo=postgresql&logoColor=white) ![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=flat&logo=mongodb&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black) ![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)

---

<p align="center">
  <sub>Open to automation, RPA and backend work — <a href="mailto:joaopecurcino.dev@gmail.com">joaopecurcino.dev@gmail.com</a></sub>
</p>

<!-- Stats ocultados — descomente para reativar
---

<p align="center">
  <img width="48%" src="https://github-readme-stats-bice-iota-27.vercel.app/api/top-langs/?username=JoaoPec&layout=compact&theme=tokyonight&hide=javascript,blade,vue,html,css,scss,lua,shell&count_private=true" />
  <img width="48%" src="https://github-readme-streak-stats.herokuapp.com/?user=JoaoPec&theme=tokyonight&mode=weekly" />
</p>
-->
