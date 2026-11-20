<div align="center">

# 📊 Business Process Modeling

**From business process analysis to low-code applications: an organizational strategy case study of Optima, an industrial CNC equipment manufacturer**

![BPMN](https://img.shields.io/badge/BPMN-2.0-blue)
![OutSystems](https://img.shields.io/badge/OutSystems-ODC-red)
![Status](https://img.shields.io/badge/status-completed-brightgreen)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

</div>

---

## 📖 About

This repository contains the final project for **Organizational Strategy**
(BSc in Computer Engineering, 2025/2026). The case study is **Optima**, a
Portuguese manufacturer of CNC cutting and engraving machines with about
25 employees.

The project covers the full cycle:

1. **Diagnosis:** PEST, Porter's Five Forces, BCG matrix, strategic groups,
   critical success factors, SWOT (external and internal), stakeholder interview
   and value chain analysis.
2. **Process redesign:** two critical processes modeled as **AS-IS / TO-BE**
   and justified against the SWOT and the interview findings.
3. **Strategic alignment:** McFarlan matrices, Balanced Scorecard and strategic
   impact of the proposed solutions.
4. **Implementation:** three working applications built on the **OutSystems
   Developer Cloud (ODC)** low-code platform.

> 🎯 **Why it matters:** process modeling and requirements analysis are the
> foundation of ERP implementations (such as SAP) and of business-oriented
> data analysis.

---

## 🗂️ Repository structure

| Folder | Description |
|---|---|
| [`report/`](./report) | Full report (`EO_Relatorio_Completo_Optima.pdf`, 86 pages, in Portuguese) |
| [`process-bpmn/`](./process-bpmn) | Business process models in BPMN 2.0 (`.bpmn`) |
| [`models-oml/`](./models-oml) | OutSystems application modules (`.oml`) |
| [`diagrams/`](./diagrams) | Exported diagrams and screenshots (`.png`) |

---

## 🖼️ Example: proposal and quotation process

![BPMN business process](./diagrams/ProcessoNegocioBPMN.png)

*Handling of a new project request, from the first customer phone call to the
final award. Three internal areas (Administrative Services, Engineering and
Customer Communication) interact with the customer. The model includes a
parallel gateway (technical feasibility and cost/margin analysis run in
parallel) and decision gateways that can end in a justified refusal.*

---

## 🧩 Main models

### 1. Process redesign (AS-IS → TO-BE)

| Process | Problem found (AS-IS) | Proposed solution (TO-BE) |
|---|---|---|
| **Commercial quotation** | Quotes based on manual estimates; no up-to-date record of part costs; Engineering busy with administrative work | Product configurator integrated with the ERP: Engineering selects technical configurations and the system calculates the final price from current costs and margin |
| **Technical assistance** | No machine history; reactive handling; technicians travel without the right parts | **Digital Machine Dossier**: look up serial number, BOM and fault history before dispatching, plan parts picking, and update the record from mobile after the intervention |

### 2. OutSystems applications (`.oml`)

Each `.oml` file is an OutSystems module containing the data model, server
logic and user interface of one application.

| Application | Purpose | Key features |
|---|---|---|
| **Digital Quotation & Margin Management** | Replaces manual quotation calculations | CRUD of quotes and parts; automatic price: `Final Price = Σ parts + margin %`; role-based security (`Engineering`, `Inserir`) enforced with server-side `CheckRole` logic; commercial dashboard (column and line charts by client and over time) |
| **Digital Machine Dossier** | Technical "identity card" for every machine sold | Machine fleet CRUD (serial number, model, client, sale date); 1:N service history per machine with status (Resolved / Pending); chronological timeline; dashboard of fault rates by model |
| **Spare Parts Requisition** | Moves stock replenishment from reactive to proactive | Critical parts catalog with stock levels; requisition form (part and urgency via dropdown); urgency monitoring dashboard with KPIs and an "order" action |

> 📘 Screens, requirements (RF01–RF03 for each application) and design
> decisions are documented in the **OutSystems** chapter of the
> [full report](./report/EO_Relatorio_Completo_Optima.pdf).

---

## 🛠️ Tools & technologies

- **Process modeling:** BPMN 2.0 (bpmn.io / Camunda Modeler)
- **Low-code platform:** OutSystems Developer Cloud (ODC), Service Studio
- **Strategy frameworks:** PEST, Porter, BCG, SWOT, McFarlan, Balanced Scorecard
- **Documentation:** Microsoft Word

---

## ▶️ How to open the files

- **`.bpmn`:** open in [bpmn.io](https://demo.bpmn.io/) or [Camunda Modeler](https://camunda.com/download/modeler/)
- **`.oml`:** open in OutSystems Service Studio (a free [Personal Environment](https://www.outsystems.com/platform/free-trial/) is enough)
- **Report:** PDF in [`report/`](./report) (written in Portuguese)

---

## 👥 Team

Group project developed with **Rafael Oliveira** and **Guilherme Martins**.
Each team member implemented one of the OutSystems applications.

---


## 👤 Author

**Daniel Duarte Silva**
Computer Engineering student (Information Systems & AI) ·
Medal of Excellence, WorldSkills Portugal

[![GitHub](https://img.shields.io/badge/GitHub-danielsilvaengpt-181717?logo=github)](https://github.com/danielsilvaengpt)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-connect-0A66C2?logo=linkedin)](https://www.linkedin.com/in/YOUR-PROFILE)

---

## 📄 License

Distributed under the MIT License. See [`LICENSE`](./LICENSE).
