<p align="right">
  <img src="https://komarev.com/ghpvc/?username=Souma061&color=blueviolet" alt="Profile views for Souma061" />
</p>

<div align="center">

# Soumabrata Ghosh

### Backend Engineer · Distributed Systems · Search & AI

I build systems to understand how they work — from crawlers and search engines
to asynchronous pipelines, distributed workflows, and high-concurrency backend services.

<p>
  <a href="https://www.linkedin.com/in/soumabrata-ghosh-85862530b/">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://www.soumabrata.me">
    <img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" />
  </a>
  <a href="mailto:soumabrataghosh57@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>

</div>

---

## 🧠 What I Work On

- ⚙️ **Backend & Distributed Systems**
- 🔍 **Search & Information Retrieval**
- 🗄️ **Databases & Storage Systems**
- 🤖 **AI & RAG Systems**
- 🏗️ **System Design**

I enjoy building things from the ground up and understanding the
mechanisms behind the abstractions I use.

---

# 🚀 Featured Projects

### 🔍 [Search Engine](https://github.com/Souma061/Search-Engine)

A developer-focused search engine built around a custom crawling,
indexing, and retrieval pipeline.

`TypeScript` · `Crawler` · `SQLite FTS5` · `BM25` · `Ranking`

**Built:**
Concurrent crawling · robots.txt handling · incremental crawling ·
indexing · BM25 ranking · typo correction · rate limiting

---

### ⚡ [Webhook Relay Service](https://github.com/Souma061/Webhook-Relay-Service)

A self-hostable webhook infrastructure for reliable asynchronous
event processing and delivery.

`FastAPI` · `Kafka` · `PostgreSQL` · `Redis` · `Docker`

**Architecture:**

```text
Webhook
   │
   ▼
FastAPI Gateway
   │
   ▼
PostgreSQL + Transactional Outbox
   │
   ▼
Kafka
   │
   ├──► Transform Worker
   │
   └──► Delivery Worker
              │
              ▼
       Retry / Circuit Breaker / DLQ
