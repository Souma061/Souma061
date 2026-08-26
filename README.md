<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=2,14,24,30&height=180&section=header&text=Soumabrata%20Ghosh&fontSize=42&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Distributed%20Systems%20%7C%20Backend%20Engineer%20%7C%20Information%20Retrieval&descFontSize=18&descAlignY=62" width="100%" alt="Header Banner" />
</div>

<p align="right">
  <img src="https://komarev.com/ghpvc/?username=Souma061&color=blueviolet&style=flat-square" alt="Profile Views" />
</p>

<div align="center">

<a href="https://github.com/Souma061">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=22&duration=3500&pause=1000&color=58A6FF&center=true&vCenter=true&width=600&lines=Distributed+Systems+Engineer;High-Throughput+Backend+Developer;Search+Engine+%26+IR+Builder;System+Design+Enthusiast" alt="Typing SVG" />
</a>

<p>
  <strong>B.Sc Computer Science Student | Backend & Distributed Systems Engineer | India 🇮🇳</strong>
</p>

<p>
  I design and engineer scalable backend architectures, high-throughput distributed systems, and search infrastructure.<br/>
  Passionate about asynchronous messaging, database internals, transactional resilience, and concurrent systems.
</p>

<p>
  <a href="https://www.linkedin.com/in/soumabrata-ghosh-85862530b/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:soumabrataghosh57@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
  <a href="https://dev.to/souma061" target="_blank">
    <img src="https://img.shields.io/badge/Dev.to-0A0A0A?style=for-the-badge&logo=devdotto&logoColor=white" alt="Dev.to" />
  </a>
  <a href="https://www.instagram.com/itsmesoumabrata/" target="_blank">
    <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram" />
  </a>
</p>

</div>

---

### 📝 Technical Deep Dive & Key Engineering Wins

> Highlights demonstrating backend, search systems, performance tuning, and distributed architectures:

- ⚡ **Scaled Event Booking to 1,013 req/s**: Tuned concurrency with 33 asynchronous workers, achieving a **394% throughput boost** and reducing **p95 latency from 3,100ms down to 44ms**.
- 🔍 **First-Principles Search Engine & Crawler**: Built an asynchronous multi-worker BFS crawler with polite `robots.txt` rate-limiting, SQLite FTS5 inverted indexing, and **Okapi BM25 relevance scoring** serving instant paginated results.
- 🔄 **Transactional Kafka Outbox Pattern**: Implemented resilient event publishing with **PostgreSQL outbox table + Redis caching + spillover handling** for 1,000+ queue overflows.
- 🛡️ **Zero Booking Race Failures**: Handled **46,576 concurrent seat-grab transactions** in rigorous stress testing with **0 race condition anomalies**.
- 🚀 **Non-Blocking Concurrency**: Offloaded CPU-intensive `bcrypt` hashing to thread executors (`run_in_executor`), eliminating Python event loop starvation.

---

### 🚀 Featured & Distributed Systems Projects

| Project | Description & Architecture | Tech Stack | Links |
| :--- | :--- | :--- | :---: |
| **[`Search-Engine (DevDocs)`](https://github.com/Souma061/Search-Engine)** | Production-grade developer search engine with an asynchronous BFS web crawler, Turso (libSQL FTS5) inverted indexing, Okapi BM25 ranking, and sliding-window rate limiting.<br/><sub>`BFS Crawler` `Inverted Index` `Okapi BM25` `Rate Limiting`</sub> | `TypeScript`<br/>`React 19`<br/>`Turso (libSQL)`<br/>`Vercel` | [🚀 Live Demo](https://searchengine-jade.vercel.app)<br/>[📦 Repo](https://github.com/Souma061/Search-Engine) |
| **[`Event-Booking-Service`](https://github.com/Souma061/Event-Booking-Service)** | High-concurrency event ticketing platform bench-tested to 1,013 req/s with atomic seat reservations, Cashfree payment gateway integration, and Redis distributed locks.<br/><sub>`Distributed Locks` `TTL Cache` `Async Workers` `Load Testing`</sub> | `FastAPI`<br/>`React`<br/>`TypeScript`<br/>`PostgreSQL`<br/>`Redis` | [🚀 Live Demo](https://github.com/Souma061/Event-Booking-Service)<br/>[📦 Repo](https://github.com/Souma061/Event-Booking-Service) |
| **[`kafka-learning`](https://github.com/Souma061/kafka-learning)** | Order, inventory, and notification microservices communicating asynchronously with transactional outbox publishing, leader election, and dead-letter queues.<br/><sub>`Outbox Pattern` `Leader Election` `DLQ` `Idempotency` `Circuit Breaker`</sub> | `FastAPI`<br/>`Apache Kafka`<br/>`Redis`<br/>`PostgreSQL`<br/>`Docker` | [📦 Repo](https://github.com/Souma061/kafka-learning) |
| **[`Webhook-Relay-Service`](https://github.com/Souma061/Webhook-Relay-Service)** | High-performance, self-hostable, decoupled webhook ingestion and payload transformation service with automated retry backoffs and idempotent delivery.<br/><sub>`Event Streaming` `Decoupled Queues` `Retry Engine` `Idempotent Delivery`</sub> | `FastAPI`<br/>`Apache Kafka`<br/>`Docker`<br/>`TypeScript` | [📦 Repo](https://github.com/Souma061/Webhook-Relay-Service) |
| **[`LinguaChat`](https://github.com/Souma061/LinguaChat)** | Real-time bi-directional messaging application with automated on-the-fly language translation across active chat rooms.<br/><sub>`WebSockets` `Bi-directional Messaging` `Room State`</sub> | `Socket.IO`<br/>`Node.js`<br/>`Express`<br/>`React` | [📦 Repo](https://github.com/Souma061/LinguaChat) |

---

### 🔨 Currently Building & Learning

- 🔭 **Distributed Tracing Demo**: Instrumenting Kafka microservices with **OpenTelemetry + Jaeger** for end-to-end distributed transaction tracing.
- ⚡ **Webhook Relay Engine**: Building an ultra-resilient webhook ingestion gateway with automated retry backoffs and signature verification.
- 📚 **System Design Blueprint**: Curating production-ready patterns for rate limiting algorithms, raft consensus, distributed caching, and database sharding.

---

### 💻 Tech Stack & Tooling

<details open>
<summary><b>⚙️ Backend & Distributed Messaging</b></summary>
<br/>
<p align="left">
  <img src="https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Apache%20Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white" alt="Kafka" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express.js" />
  <img src="https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socket.io&logoColor=white" alt="Socket.io" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis" />
  <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" alt="Nginx" />
</p>
</details>

<details open>
<summary><b>🗄️ Databases & Storage</b></summary>
<br/>
<p align="left">
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Turso_(libSQL)-00E699?style=for-the-badge&logo=sqlite&logoColor=black" alt="Turso libSQL" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL" />
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase" />
</p>
</details>

<details>
<summary><b>🎨 Frontend & Mobile</b></summary>
<br/>
<p align="left">
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter" />
  <img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="Dart" />
</p>
</details>

<details>
<summary><b>📊 Observability, Testing & DevOps</b></summary>
<br/>
<p align="left">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white" alt="Prometheus" />
  <img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white" alt="Grafana" />
  <img src="https://img.shields.io/badge/OpenTelemetry-415C9B?style=for-the-badge&logo=opentelemetry&logoColor=white" alt="OpenTelemetry" />
  <img src="https://img.shields.io/badge/Locust-009944?style=for-the-badge&logo=locust&logoColor=white" alt="Locust" />
  <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white" alt="Postman" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
</p>
</details>

<details>
<summary><b>💾 Core Languages</b></summary>
<br/>
<p align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black" alt="C" />
  <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP" />
  <img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="Dart" />
</p>
</details>

---

### 📊 GitHub Activity & Metrics

<div align="center">

  <table border="0" style="border: none;">
    <tr style="border: none;">
      <td style="border: none;" align="center">
        <img src="https://github-readme-stats.vercel.app/api?username=Souma061&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" alt="GitHub Stats" />
      </td>
      <td style="border: none;" align="center">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Souma061&layout=compact&theme=tokyonight&hide_border=true" alt="Top Languages" />
      </td>
    </tr>
  </table>

  <br/>

  <img src="https://github-readme-streak-stats.herokuapp.com?user=Souma061&theme=tokyonight&hide_border=true&date_format=j%20M%5B%20Y%5D" alt="GitHub Streak" />

  <br/><br/>

  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Souma061&custom_title=Contribution%20Graph&bg_color=0D1117&color=58A6FF&line=F8D866&point=FFFFFF&area_color=58A6FF22&title_color=58A6FF&area=true&hide_border=true&radius=12" width="95%" alt="Activity Graph" />

  <br/><br/>

  <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight" alt="Dev Quote" />

</div>

<br/>

<div align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=120&color=gradient&section=footer" alt="Footer Wave" />
</div>
