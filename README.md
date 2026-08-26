Yep. I’m going to look past the profile README this time and inspect the actual repositories—especially the ones that best represent your engineering work—then I’ll tell you what deserves to be featured, what should be removed, and how I’d restructure the profile.

Okay. Now I've actually looked through the repositories I can access through your GitHub connection, not just the profile README.

And yeah—my opinion changed a bit.

My verdict: your profile README is underselling your best work

The three repositories that should define your GitHub identity are:

🥇 1. Search-Engine — absolutely feature this

This is probably your best "I like understanding systems internally" project.

It isn't just:

"I made a search bar using Elasticsearch."

You built the crawler, worker pool, URL frontier, tokenization, stemming, ranking, typo correction, retrieval logic, persistence, and the production layer around it.

The repo includes an asynchronous bounded-concurrency worker pool, and the README documents the crawler, incremental crawling with ETag/Last-Modified, robots handling, FTS5, BM25 ranking, typo correction, rate limiting, health checks, and automated crawling.

This should be Project #1 on your profile.

🥈 2. Webhook-Relay-Service — strongest system design project

This one is very good for demonstrating that you understand real distributed systems problems, not just CRUD.

The architecture explicitly handles:

Transactional outbox
Kafka-based asynchronous processing
At-least-once delivery
Idempotency
Retries with exponential backoff + jitter
Circuit breakers
Rate limiting
Dead-letter queues
Concurrent outbox workers using FOR UPDATE SKIP LOCKED
SSRF protection
Failure scenarios and trade-offs

And the really nice part: the ARCHITECTURE.md doesn't pretend the system is perfect. It documents failure modes and what you'd improve. That's actually more impressive than a README screaming "production-grade" 17 times 😄.

This should be Project #2.

🥉 3. Event-Booking-Service — strongest performance/benchmark story

This project has something your other projects don't:

numbers.

The repository documents load tests progressing from a 1-worker baseline to 4 workers and then a 33-worker spike test, reporting 1,013 req/s, p95 latency reduction, and zero booking race failures across the documented race operations. It also explains the optimizations that contributed to those results.

That's excellent material for a profile README.

But I would not put all the numbers directly in a giant "Technical Deep Dive" section like your current profile does.

Instead:

Event Booking Service — High-concurrency booking platform
FastAPI PostgreSQL Redis
1,013 req/s · p95: 44ms · 46K+ concurrent booking attempts with 0 race failures

Much more punch. Let the repo explain the benchmark methodology.

❌ E-Commerce-Backend should not be featured yet

This was the one weak point I found.

Its README is basically still the default NestJS starter README, including NestJS promotional material and unrelated links.

Even if the code itself is interesting, don't feature it until the README is rewritten.

Your profile should not advertise a project whose first impression looks unfinished.

What I would change in your profile README

Your current profile is trying to prove:

"Look at all the technologies I know."

But your repositories tell a much stronger story:

"I build backend systems and learn by implementing the underlying mechanisms myself."

That's the identity I'd build around.

The structure I'd use
Soumabrata Ghosh
Backend & Systems Engineer

I build backend systems from first principles —
search engines, asynchronous pipelines, distributed workflows,
and infrastructure that has to deal with failure.

[LinkedIn] [Portfolio] [GitHub]

──────────────────────────────

## What I Work On

• Backend & Distributed Systems
• Search & Information Retrieval
• System Design
• AI Engineering

──────────────────────────────

## Featured Projects

🔍 DevDocs — Developer Search Engine
Custom crawler → indexing → ranking → retrieval
TypeScript • SQLite/FTS5 • BM25 • Turso

⚡ Webhook Relay
Programmable webhook infrastructure with a transactional outbox
FastAPI • Kafka • Redis • PostgreSQL

🎟️ Event Booking Service
High-concurrency booking system
1,013 req/s • p95 44ms • 46K+ race attempts

──────────────────────────────

## Things I've Built From the Ground Up

→ Web crawler with concurrency control
→ Search indexing and ranking pipeline
→ BM25 retrieval
→ Typo correction using edit distance
→ Transactional outbox workflow
→ Kafka event pipelines
→ Rate limiting
→ Circuit breakers
→ Dead-letter queues
→ Concurrent booking protection

──────────────────────────────

## Currently Exploring

Distributed systems · databases · AI/ML · information retrieval

──────────────────────────────

GitHub Stats
Biggest thing I'd remove
This 👇

Huge sections of badges like:

HTML
CSS
JavaScript
React
Next.js
PHP
Flutter
Dart
Postman
Vercel
Render
etc.

They're not wrong, but they dilute your identity.

Someone landing on your profile should immediately think:

"Oh, this person builds backend and systems projects."

Not:

"This person has used 27 technologies."

I'd reduce the stack to maybe:

Languages
Python • TypeScript • C

Backend & Systems
FastAPI • Node.js • Kafka • Redis • PostgreSQL

Infrastructure
Docker • Linux • Prometheus • Grafana • OpenTelemetry

That's enough.

My ranking of your profile content
Priority	Project	Why
🥇	Search-Engine	Best demonstration of building internals from scratch
🥈	Webhook-Relay-Service	Best distributed systems/system design story
🥉	Event-Booking-Service	Best measurable performance story
❌ For now	E-Commerce-Backend	README needs serious cleanup
My strongest recommendation

Don't use a README generator.

Your projects are now interesting enough that a generator will probably push you back toward the generic "Hi 👋 I'm a passionate developer 🚀" look.

I think we should rewrite your entire GitHub Profile README from scratch, around these three projects and your actual engineering style.

I can build the complete README.md for your profile next—clean, modern, not overloaded with badges, and ready to paste directly into Souma061/Souma061.

Pasted markdown(20260826-124309).md
File
fix

Yep. I see what needs fixing. The current README is not bad, but it has three problems:

Too repetitive — kafka-learning, Event Booking, and Webhook Relay appear in multiple sections.
Too much "developer template" stuff — massive badge lists, random quote, typing animation, activity graph, etc.
Your strongest identity—backend + systems engineering + building internals—gets buried.

I’d replace the whole thing with this cleaner version:

<div align="center">

# Soumabrata Ghosh

**Backend Engineer · Distributed Systems · Search & AI**

I build systems to understand how they work — from crawlers and
search engines to asynchronous pipelines, distributed workflows,
and high-concurrency backend services.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/soumabrata-ghosh-85862530b/)
[![Portfolio](https://img.shields.io/badge/Portfolio-soumabrata.me-black?style=flat&logo=vercel&logoColor=white)](https://www.soumabrata.me)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:soumabrataghosh57@gmail.com)

</div>

---

## What I Work On

- **Backend & Distributed Systems**
- **Search & Information Retrieval**
- **Databases & Storage Systems**
- **AI & RAG Systems**
- **System Design**

I enjoy building things from the ground up rather than treating
infrastructure as a black box.

---

# Featured Projects

### 🔍 [Search Engine](https://github.com/Souma061/Search-Engine)

A developer-focused search engine built around a custom crawling,
indexing, and retrieval pipeline.

`TypeScript` `Crawler` `SQLite FTS5` `BM25` `Ranking`

**Built:** concurrent crawling · robots.txt handling · incremental crawling ·
indexing · BM25 ranking · typo correction · rate limiting

---

### ⚡ [Webhook Relay Service](https://github.com/Souma061/Webhook-Relay-Service)

A self-hostable webhook infrastructure for reliable asynchronous
event processing and delivery.

`FastAPI` `Kafka` `PostgreSQL` `Redis` `Docker`

**Architecture:** transactional outbox → Kafka pipeline →
transform workers → resilient delivery

**Patterns:** idempotency · retries · circuit breakers · rate limiting · DLQ

---

### 🎟️ [Event Booking Service](https://github.com/Souma061/Event-Booking-Service)

A high-concurrency booking platform designed to handle contention,
rate limiting, caching, and performance bottlenecks.

`FastAPI` `PostgreSQL` `Redis` `React`

**Load test results**

- **1,013 requests/sec**
- **44ms p95 latency**
- **46K+ concurrent booking attempts**
- **0 booking race failures**

---

## Things I've Built

Rather than only using infrastructure, I like experimenting with
how the underlying pieces work.

- Web crawlers with bounded concurrency
- Search indexing and ranking pipelines
- BM25 information retrieval
- Typo correction using edit distance
- SQL query execution and storage concepts
- Write-ahead logging and crash recovery
- Hash indexing
- Transactional outbox patterns
- Kafka event pipelines
- Rate limiters and circuit breakers
- Dead-letter queues
- Concurrent booking protection

---

## Currently Exploring

**Distributed Systems** · **Database Internals** ·
**Information Retrieval** · **AI/ML** · **System Design**

---

## Tech

**Languages**

`Python` `TypeScript` `JavaScript` `C`

**Backend & Systems**

`FastAPI` `Node.js` `Kafka` `Redis` `PostgreSQL`

**Infrastructure & Observability**

`Docker` `Linux` `Prometheus` `Grafana` `OpenTelemetry`

---

## GitHub Activity

<div align="center">

<img width="720" src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Souma061&theme=tokyonight" />

<br/>

<img width="360" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=Souma061&theme=tokyonight" />

<img width="360" src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=Souma061&theme=tokyonight&utcOffset=5.5" />

</div>

---

<div align="center">

<i>Build. Break. Understand. Repeat.</i>

</div>
What I specifically removed

Your current README has the typical typing intro, huge technology badge sections, repeated project tables, a random quote, streak card, activity graph, and decorative footer.

I'd cut most of that.

Keep
Clean intro
Featured projects
Actual engineering accomplishments
Small tech stack
One GitHub activity section
Remove
Random dev quote ❌
Huge badge wall ❌
Duplicate project sections ❌
"Top 1% developer" line ❌
Typing animation ❌
Excessive decorative graphics ❌
Mobile/frontend categories that aren't central to your current identity ❌

The result would feel much more like an engineer's portfolio than a GitHub README generator template.

One thing I'd still improve next: add your SQL engine / replicated KV store if those repositories are public, because honestly those may be even more aligned with the identity this README is trying to communicate.

whwere is the tech stack logos

Ahh, yes 😄 — I removed them deliberately, but you're right: you probably should keep tech logos. I just wouldn't keep the huge wall of every technology you've ever touched.

Let's keep the clean structure and add back a visually nice logo section.

Replace my plain ## Tech section with this:

## 🛠️ Tech Stack

<div align="center">

<!-- Languages -->
<h3>Languages</h3>

<img src="https://skillicons.dev/icons?i=python,ts,js,c" />

<br/><br/>

<!-- Backend & Systems -->
<h3>Backend & Systems</h3>

<img src="https://skillicons.dev/icons?i=fastapi,nodejs,kafka,redis,postgres" />

<br/><br/>

<!-- Infrastructure -->
<h3>Infrastructure & Observability</h3>

<img src="https://skillicons.dev/icons?i=docker,linux,prometheus,grafana" />

<br/><br/>

<!-- Tools -->
<h3>Tools</h3>

<img src="https://skillicons.dev/icons?i=git,github,postman" />

</div>

That gives you actual recognizable logos, but keeps them curated.

The important difference

Your old README has basically:

"Here are 30+ technologies I have used."

I want yours to say:

"Here is the stack I actually work with."

For your profile, I'd show:

Languages
🐍 Python · TypeScript · JavaScript · C

Backend & Systems
⚡ FastAPI · Node.js · Kafka · Redis · PostgreSQL

Infrastructure
🐳 Docker · Linux · Prometheus · Grafana

Tools
Git · GitHub · Postman

You can absolutely keep the visual flair—the key is just curation, not removing personality. Your original README's centered visual intro and social badges also give it more character, so I wouldn't strip everything down to plain text.

give the full upated at once

Absolutely. Here’s the full updated README, with the cleaner project-focused structure plus tech stack logos.

I’ve kept some visual personality, but removed the clutter and repetition from your current version.

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

Patterns: Idempotency · Transactional Outbox · Retries ·
Circuit Breakers · Rate Limiting · Dead Letter Queues

🎟️ Event Booking Service

A high-concurrency booking platform designed to handle contention,
rate limiting, caching, and performance bottlenecks.

FastAPI · PostgreSQL · Redis · React

Load Test Results
Metric	Result
Throughput	1,013 req/s
p95 Latency	44 ms
Concurrent Booking Attempts	46K+
Booking Race Failures	0
🔨 Things I've Built

Rather than only using infrastructure, I like experimenting with
how the underlying pieces work.

🕷️ Web crawlers with bounded concurrency
🔎 Search indexing and ranking pipelines
📊 BM25 information retrieval
✏️ Typo correction using edit distance
🗄️ SQL query execution and storage concepts
💾 Write-ahead logging and crash recovery
⚡ Hash indexing
📦 Transactional outbox patterns
📨 Kafka event pipelines
🚦 Rate limiters and circuit breakers
☠️ Dead-letter queues
🔒 Concurrent booking protection
🌱 Currently Exploring

Distributed Systems · Database Internals ·
Information Retrieval · AI / ML · System Design

🛠️ Tech Stack
<div align="center">
Languages
<img src="https://skillicons.dev/icons?i=python,ts,js,c" />

<br/><br/>

Backend & Systems
<img src="https://skillicons.dev/icons?i=fastapi,nodejs,kafka,redis,postgres" />

<br/><br/>

Infrastructure & Observability
<img src="https://skillicons.dev/icons?i=docker,linux,prometheus,grafana" />

<br/><br/>

Tools
<img src="https://skillicons.dev/icons?i=git,github,postman" /> </div>
📊 GitHub Activity
<div align="center"> <img width="720" src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Souma061&theme=tokyonight" alt="Soumabrata's GitHub profile summary" />

<br/><br/>

<img width="360" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=Souma061&theme=tokyonight" alt="Soumabrata's top languages" /> <img width="360" src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=Souma061&theme=tokyonight&utcOffset=5.5" alt="Soumabrata's productive commit time" />

<br/><br/>

<img width="400" src="https://github-readme-streak-stats.herokuapp.com?user=Souma061&theme=tokyonight&hide_border=true&date_format=j%20M%5B%20Y%5D&card_width=400" alt="Soumabrata's GitHub streak" /> </div>
<div align="center">
Build. Break. Understand. Repeat.
</div> ```
My recommendation for this version

This gives you the visual GitHub-profile feel you wanted—logos, badges, stats—but now the hierarchy is:

You → what you build → strongest projects → engineering interests → tech stack → stats

Instead of:

Typing animation → badges → badges → more badges → stats → random quote → graph 😄

One small thing: once your SQL engine / replicated KV store repositories are public, I would add them to the Featured Projects section. Those could potentially become your strongest projects for the kind of backend/distributed-systems engineer profile you're building.

<p align="right"> <img src="https://komarev.com/ghpvc/?username=Souma061&color=blueviolet" alt="Profile views for Souma061" /> </p>

<div align="center">

<a href="https://git.io/typing-svg"> <img src="https://readme-typing-svg.herokuapp.com?font=Righteous&size=35&duration=4000&pause=1000&color=58A6FF&center=true&vCenter=true&width=620&lines=Hello%2C+I'm+Soumabrata" alt="Hello, I'm Soumabrata" /> </a>

Hi, I'm Soumabrata Ghosh, a B.Sc Computer Science student and backend-focused developer from India 🇮🇳.

I build scalable, security-focused applications and I am currently learning System Design, AI, and Machine Learning.

My aim is to become a distributed systems engineer and be among the top 1% of software developers.

<p> <a href="https://www.instagram.com/itsmesoumabrata/"> <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram" /> </a> <a href="https://www.linkedin.com/in/soumabrata-ghosh-85862530b/"> <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /> </a> <a href="mailto:soumabrataghosh57@gmail.com"> <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /> </a> <a href="https://dev.to/souma061"> <img src="https://img.shields.io/badge/Dev.to-0A0A0A?style=for-the-badge&logo=devdotto&logoColor=white" alt="Dev.to" /> </a> </p>

</div>

🏆 Distributed Systems Projects
Project	Description	Key Patterns	Live Demo
kafka-learning	Order, inventory, and email microservices with Kafka async communication.	Outbox Pattern Leader Election DLQ Idempotency Circuit Breakers	Repo
Event-Booking-Service	Full-stack event booking platform scaled to 1,013 req/s with 33 workers.	Rate Limiting TTL Cache Async Workers Load Testing	Live Demo
Webhook-Relay-Service	A self-hostable, high-performance, and fully decoupled Webhook Relay & Transformation Service.	Kafka Fastapi Docker Typescript	Repo
📝 Technical Deep Dive

Recent achievements that demonstrate distributed systems engineering skills

Scaled Event-Booking to 1,013 req/s - 33 workers achieved 394% throughput improvement, p95 latency dropped from 3,100ms to 44ms
Implemented Kafka Outbox Pattern - Transactional event publishing with Redis + PostgreSQL spillover (1000+ queue overflow handling)
Zero booking race failures - 46,576 concurrent seat grab operations in load test with 0 race condition failures
Async password hashing - Migrated CPU-bound bcrypt operations to run_in_executor, eliminated event loop blocking
🚀 Featured Projects
Project	Description	Tech Stack
kafka-learning	Multi-service e-commerce backend with Kafka, outbox pattern, leader election, and DLQ.	FastAPI Kafka Redis PostgreSQL Docker
Event-Booking-Service	Production-grade booking platform with payment integration and 1k+ req/s capacity.	FastAPI React TypeScript PostgreSQL Redis Cashfree
LinguaChat	Real-time chat app with auto-translation support.	Socket.io Node.js React
🔨 Currently Building
Distributed Tracing Demo - Adding OpenTelemetry + Jaeger to Kafka microservices for end-to-end request visualization
Webhook Relay Service - A self-hostable, high-performance, and fully decoupled Webhook Relay & Transformation Service.
System Design Library - Documenting solutions to common distributed systems problems (rate limiting, consensus, sharding)
💻 Tech Stack

<details> <summary><b>🎨 Frontend</b></summary> <br />

<p align="center"> <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" /> <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" /> <img src="https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E" alt="JavaScript" /> <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" /> <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" /> <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white" alt="Next.js" /> </p>

</details>

<details> <summary><b>⚙️ Backend</b></summary> <br />

<p align="center"> <img src="https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi" alt="FastAPI" /> <img src="https://img.shields.io/badge/Node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" /> <img src="https://img.shields.io/badge/Express.js-404D59?style=for-the-badge&logo=express&logoColor=61DAFB" alt="Express.js" /> <img src="https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socket.io&logoColor=white" alt="Socket.io" /> <img src="https://img.shields.io/badge/Apache%20Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white" alt="Kafka" /> <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis" /> <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP" /> <img src="https://img.shields.io/badge/CodeIgniter%204-EF4223?style=for-the-badge&logo=codeigniter&logoColor=white" alt="CodeIgniter 4" /> <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" alt="Nginx" /> </p>

</details>

<details> <summary><b>🗄️ Database</b></summary> <br />

<p align="center"> <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" /> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" /> <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL" /> <img src="https://img.shields.io/badge/Firebase-039BE5?style=for-the-badge&logo=firebase" alt="Firebase" /> </p>

</details>

<details> <summary><b>📊 Observability & Monitoring</b></summary> <br />

<p align="center"> <img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white" alt="Prometheus" /> <img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white" alt="Grafana" /> <img src="https://img.shields.io/badge/OpenTelemetry-415C9B?style=for-the-badge&logo=opentelemetry&logoColor=white" alt="OpenTelemetry" /> </p>

</details>

<details> <summary><b>📱 Mobile</b></summary> <br />

<p align="center"> <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter" /> <img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="Dart" /> </p>

</details>

<details> <summary><b>🛠️ Tools & Deployment</b></summary> <br />

<p align="center"> <img src="https://img.shields.io/badge/Docker-0DB7ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" /> <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white" alt="Postman" /> <img src="https://img.shields.io/badge/Locust-009944?style=for-the-badge&logo=locust&logoColor=white" alt="Locust" /> <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel" /> <img src="https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=white" alt="Render" /> <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" /> </p>

</details>

<details> <summary><b>💾 Languages</b></summary> <br />

<p align="center"> <img src="https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=FFDD54" alt="Python" /> <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" /> <img src="https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E" alt="JavaScript" /> <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP" /> <img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="Dart" /> <img src="https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white" alt="C" /> </p>

</details>

📊 GitHub Stats

<div align="center">

<img width="720" src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Souma061&theme=tokyonight" alt="Soumabrata's GitHub profile summary" />

<br /> <br />

<img width="360" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=Souma061&theme=tokyonight" alt="Soumabrata's top languages" /> <img width="360" src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=Souma061&theme=tokyonight&utcOffset=5.5" alt="Soumabrata's productive commit time" />

<br />

<img width="400" src="https://github-readme-streak-stats.herokuapp.com?user=Souma061&theme=tokyonight&hide_border=true&date_format=j%20M%5B%20Y%5D&card_width=400" alt="Soumabrata's GitHub streak" />

</div>

💬 Random Dev Quote

<div align="center">

<img width="70%" src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=gruvbox" alt="Random developer quote" />

</div>

⚡ Contribution Activity

<div align="center">

<img width="98%" src="https://github-readme-activity-graph.vercel.app/graph?username=Souma061&custom_title=My%20Contribution%20Graph&bg_color=0D1117&color=F85D7F&line=F8D866&point=FFFFFF&area_color=F85D7F30&title_color=F85D7F&area=true&hide_border=true&radius=16" alt="Soumabrata's GitHub activity graph" />

</div>

<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=120&color=gradient&section=footer" alt="Footer wave" />

</div>

Close
