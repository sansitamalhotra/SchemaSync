<div align="center">

<h1>Schema Sync</h1>
<h3><em>The AI Copilot for Data Integration</em></h3>

<p><strong>Unifying financial data across institutions with intelligence, transparency, and speed.</strong></p>

<!-- Badges (feel free to keep/remove) -->
<a href="http://127.0.0.1:8000/docs"><img alt="FastAPI" src="https://img.shields.io/badge/Backend-FastAPI-009688.svg"></a>
<img alt="Python" src="https://img.shields.io/badge/Python-3.10%2B-3776AB.svg">
<img alt="Frontend" src="https://img.shields.io/badge/Frontend-Next.js%20%2B%20React-000000.svg">
<img alt="License" src="https://img.shields.io/badge/License-MIT-purple.svg">

<p>Built for the <strong>EY Canada Data Integration Challenge – Hack the Valley X 2025</strong></p>
</div>

---

## 🧭 Table of Contents
- [Overview](#-overview)
- [Key Features](#-key-features)
- [Architecture](#-architecture)
- [Quick Start](#-quick-start)
- [API Endpoints](#-api-endpoints)
- [Detailed Workflow](#-detailed-workflow)
- [Outputs & Artifacts](#-outputs--artifacts)
- [Security & Privacy](#-security--privacy)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 🌟 Overview
When two banks merge, **data chaos follows**—each system has its own schema, column names, and formats.  
**Schema Sync** is your AI-powered copilot that **maps, merges, and validates** financial datasets across institutions, producing a **unified schema** and a **full audit trail** in minutes, not days.

> Think **GitHub Copilot**—but for **data mapping** and **schema reconciliation**.

---

## 🎯 Key Features
- **🤖 AI Schema Matching** — Embedding-based NLP (OpenAI/SBERT) for semantic alignment  
- **📂 Multi-Format Uploads** — CSV, Excel (`.xlsx`, `.xls`), JSON  
- **🧩 Visual Mapping Workspace** — Side-by-side schemas with drag-to-match + confidence scores  
- **📈 Analytics Dashboard** — Completeness, overlaps, conflicts, and KPIs  
- **⚙️ Conflict Resolver** — Detects mismatches, missing data, and format inconsistencies  
- **🧾 Report Generation** — Excel/PDF with mappings, confidence, and lineage  
- **🛡️ Local Processing** — No cloud uploads; transparent by design  
- **🎨 Modern UI** — Next.js + Tailwind + shadcn/ui

---

## 🏗️ Architecture

### Backend (FastAPI + Python)
- **Schema Parser** — Reads & normalizes schemas  
- **AI Matcher** — Embedding similarity (SBERT/OpenAI)  
- **Merge Engine** — Builds unified master schema  
- **Analytics Service** — Completeness/overlap/conflicts  
- **Report Generator** — Excel/PDF with audit trail  
- **Storage Layer** — Organized directories per institution

### Frontend (Next.js + React + Tailwind)
- **Guided flow:** Upload → Map → Merge → Analyze → Export  
- **Drag & Drop** for Bank A / Bank B  
- **Live Confidence View** + mapping health  
- **Responsive dashboard** with KPIs & charts

---

## 🚀 Quick Start

### Prerequisites
- Python **3.10+**
- Node.js **18+**
- (Optional) OpenAI API key if using OpenAI embeddings

### 1) Clone
```bash
git clone https://github.com/your-username/schema-sync.git
cd schema-sync
2) Backend (port 8000)
No requirements.txt in this repo—install core deps manually:

bash
Copy code
cd backend
pip install fastapi uvicorn pandas python-multipart sentence-transformers torch openpyxl
uvicorn main:app --reload --port 8000
Docs: http://127.0.0.1:8000/docs

3) Frontend
bash
Copy code
cd ../my-app
npm install
npm run dev
Open: http://localhost:3000

Tip: If you later add an .env, keep secrets there (e.g., OPENAI_API_KEY). This project runs fine without one.

🔌 API Endpoints
Base URL: http://127.0.0.1:8000

Method	Endpoint	What it does
POST	/run-pipeline	Run the full pipeline (parse → map → merge)
POST	/schemas/parse	Parse uploaded schemas (Excel → JSON)
GET	/schemas/list	List available parsed schema JSONs
GET	/schemas/{name}	Read a specific schema JSON
GET	/auto-map	Run AI-based schema matching
POST	/upload	Upload files (schemas/data)

🧪 Detailed Workflow
Stage 1 — Table Mapping
Encode table names with Sentence-BERT, compute cosine similarity

Confidence threshold CONF_THRESHOLD = 73% → Confident Match

Outputs: table_name_mapping.json, bank2_renamed_schema.json

Stage 2 — File → Logical Table Manifest
Normalize filenames and map to canonical table tokens

Output: merge_manifest.json (file → logical table, with bank label)

Stage 3 — Field-Level Mapping
Encode field strings (name + type + sample) and match

Outputs: field_name_mapping.json, unified_schema.json

Stage 4 — Raw Ingestion
Load Excel/CSV → pandas; add bank_origin

Persist to SQLite (merged_banks.db)

Stage 5 — Transform & Merge
Apply column renames from field mapping

Standardize types (dates → YYYY-MM-DD, numerics, identifiers)

Merge A+B; detect conflicts

Stage 6 — Conflict Resolution
Prefer non-nulls; tie-break (e.g., Bank A wins or most-recent timestamp)

Log decisions with lineage

Stage 7 — Reporting
Export unified dataset (CSV/Excel)

Generate Integration Report (PDF) with mappings, confidences, KPIs

📦 Outputs & Artifacts
table_name_mapping.json — table matches + confidence

field_name_mapping.json — column matches + confidence

unified_schema.json — canonical fields + lineage

merge_manifest.json — file → logical table mapping

merged_banks.db — SQLite (raw + unified tables)

IntegrationReport.pdf — summary, KPIs, conflicts

🔒 Security & Privacy
Local-only processing; no data leaves your machine

Strict file validation (type/size)

Optional temp cleanup after export

Logs avoid sensitive content

🧰 Troubleshooting
Issue	Fix
Backend won’t start	Ensure Python 3.10+, reinstall deps; check uvicorn command
Frontend blank page	Clear cache, rerun npm run dev
Mapping errors	Confirm sentence-transformers + torch installed
Excel parsing error	Install openpyxl; keep files under ~50 MB

🤝 Contributing
Fork → git checkout -b feature/your-feature

Commit → git commit -m "Add feature"

Push → git push origin feature/your-feature

Open a Pull Request

