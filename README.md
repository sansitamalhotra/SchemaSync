# 🔄 Schema Sync

<div align="center">

![Schema Sync Banner](https://img.shields.io/badge/Schema%20Sync-AI%20Integration-00D9B8?style=for-the-badge&logo=database&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-0.115.5-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-15-000000?style=for-the-badge&logo=next.js&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?style=for-the-badge&logo=typescript&logoColor=white)

### 🤖 *The AI Copilot for Data Integration* 🚀

**Unifying financial data across institutions with intelligence, transparency, and speed**

[🏆 Built for EY Canada - Hack the Valley X 2025](#)

</div>

---
---

## 🎯 About This Project

**Schema Sync** was built in **24 hours** at **Hack the Valley X 2025** (University of Toronto's premier hackathon) for the **EY Canada Data Integration Challenge**.

This repository is my personal version of the project, cleaned up and documented for portfolio purposes. The original collaborative version can be found [here](https://github.com/[original-repo-if-you-want-to-link-it]).

**My Contributions:**
- Full-stack development (React frontend + FastAPI backend)
- AI schema matching implementation using Sentence-BERT
- Real-time analytics dashboard with data visualization
- Conflict resolution and data transformation logic

---

## 📸 Screenshots

<div align="center">

### 🏠 Landing Page
![Landing Page](screenshots/landing.jpg)

### 🗺️ Schema Mapping Workspace
![Schema Mapping](screenshots/mapping.jpg)

### 📊 Unified Data Output
![Unified Data](screenshots/unified.jpg)

### 📈 Analytics Dashboard
![Analytics](screenshots/analytic.jpg)

</div>

---

## 💡 The Problem

When two banks merge, **data chaos follows**:
- ❌ Each system has different schemas, column names, and formats
- ❌ Manual mapping takes **days or weeks**
- ❌ No transparency in the reconciliation process
- ❌ High risk of errors and data loss

**Schema Sync solves this** by automating schema mapping with AI.

---

## ✨ What Schema Sync Does

### 🎯 Key Features

- 🤖 **AI-Powered Matching** - Semantic field alignment using Sentence-BERT embeddings
- 📂 **Multi-Format Support** - CSV, Excel (.xlsx, .xls), JSON
- 🗺️ **Visual Mapping Workspace** - Side-by-side schemas with confidence scores
- 📊 **Analytics Dashboard** - Real-time KPIs: completeness, overlaps, conflicts
- ⚙️ **Conflict Resolution** - Smart handling of mismatches and missing data
- 📄 **Audit Trail** - Full lineage tracking for compliance
- 🛡️ **Local Processing** - No cloud uploads; your data stays secure
- 🎨 **Modern UI** - Next.js + Tailwind + shadcn/ui

---

## 🛠️ Tech Stack

### Backend
![FastAPI](https://img.shields.io/badge/FastAPI-0.115.5-009688?style=flat-square&logo=fastapi)
![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python)
![Sentence Transformers](https://img.shields.io/badge/SBERT-3.3.1-FF6F00?style=flat-square)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-EE4C2C?style=flat-square&logo=pytorch)

### Frontend
![Next.js](https://img.shields.io/badge/Next.js-15-000000?style=flat-square&logo=next.js)
![React](https://img.shields.io/badge/React-18.3.1-61DAFB?style=flat-square&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?style=flat-square&logo=typescript)
![Tailwind](https://img.shields.io/badge/Tailwind%20CSS-3.4-38B2AC?style=flat-square&logo=tailwind-css)

---

## 🚀 Quick Start

### Prerequisites
```bash
# Python 3.10+
python --version

# Node.js 18+
node --version
```

### Installation

**1️⃣ Clone the repository**
```bash
git clone https://github.com/sansitamalhotra/SchemaSync.git
cd SchemaSync
```

**2️⃣ Backend Setup**
```bash
cd backend
pip install -r requirements.txt
```

**3️⃣ Run the Backend**
```bash
uvicorn main:app --reload --port 8000
```

Backend runs at: `http://127.0.0.1:8000`  
API docs available at: `http://127.0.0.1:8000/docs`

**4️⃣ Frontend Setup**

Open a new terminal:
```bash
cd my-app
npm install
npm run dev
```

Frontend runs at: `http://localhost:3000`

---

## 🎯 How It Works

### Stage 1: Table Mapping
- Encode table names using **Sentence-BERT**
- Compute **cosine similarity** between schemas
- Confidence threshold: **73%** for auto-match

### Stage 2: Field-Level Mapping
- Semantic matching of field names, types, and sample data
- AI suggests mappings with **confidence scores**
- Human-in-the-loop for approval

### Stage 3: Merge & Transform
- Apply column mappings
- Standardize data types (dates, numbers, IDs)
- Detect and resolve conflicts

### Stage 4: Analytics & Export
- Generate KPIs and quality metrics
- Export unified schema and data
- Create full audit trail report

---

## 📂 Project Structure
```
SchemaSync/
├── backend/
│   ├── main.py                    # FastAPI application
│   ├── ai_mapping.py              # AI schema matching
│   ├── schema_parser.py           # Schema extraction
│   ├── merge_banks.py             # Data merging logic
│   ├── transform_unified.py       # Data transformation
│   ├── requirements.txt           # Python dependencies
│   └── BankA/ BankB/              # Sample data
│
├── my-app/
│   ├── app/                       # Next.js pages
│   ├── components/                # React components
│   ├── lib/                       # Utilities
│   └── package.json
│
├── screenshots/
│   ├── landing.jpg
│   ├── mapping.jpg
│   ├── unified.jpg
│   └── analytic.jpg
│
└── README.md
```

---

## 🏆 Accomplishments

- ✅ Built full-stack AI-powered schema reconciliation system
- 🤖 Implemented semantic field matching with 85%+ accuracy
- 📊 Created real-time analytics dashboard with data quality metrics
- 🎨 Designed intuitive mapping workspace with confidence visualization
- 🚀 Reduced manual schema mapping time from **days to minutes**

---

## 🔮 Future Roadmap

### Phase 1: Enhanced AI
- [ ] 🧠 Multi-model support (OpenAI, Cohere, local models)
- [ ] 📈 Confidence calibration and active learning
- [ ] 🔍 Anomaly detection in merged data

### Phase 2: Enterprise Features
- [ ] 🔐 Role-based access control
- [ ] 📝 Version control for schema mappings
- [ ] 🔄 Incremental merge support
- [ ] 📧 Email notifications and webhooks

### Phase 3: Scale
- [ ] ☁️ Cloud deployment (AWS/GCP/Azure)
- [ ] 🗄️ Support for SQL databases (PostgreSQL, MySQL)
- [ ] 🌐 Multi-tenant SaaS platform
- [ ] 📱 Mobile app for approval workflows

---

## 🧪 API Endpoints

Base URL: `http://127.0.0.1:8000`

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/run-pipeline` | Run full pipeline (parse → map → merge) |
| `POST` | `/schemas/parse` | Parse uploaded schemas |
| `GET` | `/schemas/list` | List available schemas |
| `GET` | `/auto-map` | Run AI schema matching |
| `POST` | `/upload` | Upload files |

---

## 🔒 Security & Privacy

- 🛡️ **Local-only processing** - No data sent to cloud
- 🔐 **File validation** - Type and size checks
- 🗑️ **Auto cleanup** - Temporary files deleted after export
- 📝 **Audit logging** - Full lineage tracking

---

## 🐛 Troubleshooting

| Issue | Solution |
|-------|----------|
| Backend won't start | Check Python 3.10+, reinstall dependencies |
| Frontend blank page | Clear cache, `npm run dev` |
| AI mapping errors | Verify `sentence-transformers` + `torch` installed |
| Excel parsing fails | Install `openpyxl`, check file size < 50MB |

---

## 📄 License

This project was built for **Hack the Valley X 2025** - EY Canada Data Integration Challenge.

All rights reserved.

---

<div align="center">

**Built with ❤️ for Hack the Valley X 2025**

⭐ Star us on GitHub if you found this project interesting!

[![GitHub stars](https://img.shields.io/github/stars/sansitamalhotra/SchemaSync?style=social)](https://github.com/sansitamalhotra/SchemaSync)

</div>
