<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:2563eb&height=230&section=header&text=Taeyeon%20Kim&fontSize=56&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Backend%20Engineer%20%7C%20System%20Architect&descSize=18&descAlignY=55" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&pause=1000&color=2563EB&center=true&vCenter=true&width=800&lines=Backend+Engineer+%26+System+Architect;Node.js+%7C+NestJS+%7C+TypeScript;Transaction+Management+%7C+Low+Latency+%7C+DevOps;Building+Reliable+Systems+for+Real+Services" />
</p>

<p align="center">
  <a href="mailto:ktyeon92@gmail.com">
    <img src="https://img.shields.io/badge/Email-ktyeon92%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
  <a href="https://hugekite.github.io/myInfo.github.io/">
    <img src="https://img.shields.io/badge/Portfolio-Interactive%20Portfolio-2563EB?style=for-the-badge&logo=githubpages&logoColor=white"/>
  </a>
</p>

---

## About Me

I am a backend engineer focused on building reliable systems beyond simple feature implementation.

My main interests are **data integrity**, **transaction-safe backend architecture**, **low-latency communication**, and **stable production operations**.  
I have experience designing and operating backend systems for metaverse, digital twin, AI streaming, game reward, and closed-network industrial environments.

I focus on backend systems that remain stable even when failures occur in real production environments.

---

## Tech Stack

### Backend

<p>
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white"/>
</p>

### Database & Cache

<p>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>
  <img src="https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white"/>
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white"/>
  <img src="https://img.shields.io/badge/TypeORM-FE0803?style=for-the-badge"/>
</p>

### Infrastructure & DevOps

<p>
  <img src="https://img.shields.io/badge/AWS EC2-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white"/>
  <img src="https://img.shields.io/badge/AWS S3-569A31?style=for-the-badge&logo=amazons3&logoColor=white"/>
  <img src="https://img.shields.io/badge/PM2-2B037A?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white"/>
  <img src="https://img.shields.io/badge/Ubuntu Linux-E95420?style=for-the-badge&logo=ubuntu&logoColor=white"/>
</p>

### Architecture Focus

<p>
  <img src="https://img.shields.io/badge/Transaction Management-0F172A?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/WebSocket Streaming-2563EB?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/TCP%2FIP Socket Communication-1E40AF?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Low Latency Architecture-0F766E?style=for-the-badge"/>
</p>

---

## Architecture Insights

<table>
<tr>
<td width="50%">

### Data Integrity

Prevented data corruption during multi-table updates involving parcels, ownership, inventory, and user rewards.

Applied **atomic transaction rollback** using TypeORM QueryRunner to keep data consistent even when network or server failures occur.

</td>
<td width="50%">

### Low Latency

Improved response delay caused by sequential REST-based AI audio processing.

Migrated the flow to **WebSocket + Smart VAD based real-time bidirectional streaming**, reducing end-to-end delay.

</td>
</tr>

<tr>
<td width="50%">

### High Concurrency

Resolved RDBMS Index Scan I/O bottlenecks during real-time active-user ranking calculation.

Introduced **Redis Sorted Set (ZADD)** based in-memory ranking architecture for faster concurrent processing.

</td>
<td width="50%">

### Fault Tolerance

Designed backend operation with failure scenarios in mind.

Applied **PM2 cluster-based auto-healing** to automatically restart failed processes and reduce service interruption.

</td>
</tr>

<tr>
<td width="50%">

### Probability Engine

Built server-side reward logic for probability-based gacha systems.

Handled user-state validation, secure server-side random branching, and transactional reward distribution.

</td>
<td width="50%">

### Closed Network Communication

Designed communication flow for environments where external networks are restricted.

Implemented **TCP/IP socket communication rules** and mapped data between C# control applications and Node.js servers.

</td>
</tr>
</table>

---

## Core Projects

### Metaverse Platform Backend Development & Refactoring

- Designed backend logic for virtual economy systems, including currency, item rewards, parcels, and inventory ownership.
- Refactored legacy Node.js code into a structured NestJS architecture using Controller, Service, and DTO layers.
- Standardized request/response DTOs to improve communication consistency with Unreal Engine clients.
- Built common logging and exception-handling structures for better maintainability.
- Improved transaction flow to prevent partial reward distribution and inventory inconsistency.

---

### AI Interview Evaluation Platform Data Pipeline Optimization

- Analyzed the limitation of sequential audio processing based on REST API communication.
- Redesigned the audio processing flow into a WebSocket-based bidirectional streaming structure.
- Optimized the pipeline from audio reception to AI analysis and result response.
- Improved real-time processing stability by reducing unnecessary waiting time between request and response stages.

---

### Manufacturing & Maritime Digital Twin Infrastructure

- Implemented data mapping and communication protocol between C# robot control applications and backend servers.
- Designed TCP/IP socket communication flow for industrial and closed-network environments.
- Participated in infrastructure planning for government-backed manufacturing and maritime logistics projects.
- Reviewed deployment structure, server specifications, redundancy, and operational stability.

---

## DevSecOps & Troubleshooting

### DB Connection Pool Leak

Identified active connection leakage caused by unreleased transactions in specific service logic.

- Forced transaction release in finally blocks
- Tuned connection timeout settings
- Improved QueryRunner lifecycle management

---

### Concurrent Update Collision

Resolved deadlock issues caused by multiple reward APIs updating the same row concurrently.

- Reordered business queries consistently
- Reduced unnecessary lock scope
- Applied transaction-safe reward processing flow

---

### Jenkins Pipeline Breakdown

Debugged SSH authentication failures during deployment on Ubuntu server environments.

- Reviewed server-side Git access permissions
- Stabilized PM2 deployment script execution
- Improved deployment script idempotency to reduce repeated failure risk

---

### Production Process Recovery

Handled backend process failures caused by memory pressure and runtime errors.

- Used PM2 process monitoring
- Applied automatic restart strategy
- Reviewed logs to identify failure points and improve recovery flow

---

## GitHub Overview

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=hugekite&show_icons=true&theme=tokyonight&hide_border=true" height="170"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=hugekite&layout=compact&theme=tokyonight&hide_border=true" height="170"/>
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=hugekite&theme=tokyonight&hide_border=true" height="170"/>
</p>

---

## Engineering Principles

```ts
const engineeringPrinciples = {
  reliability: "Design for failure before production failure happens.",
  integrity: "Protect data consistency with transaction-safe architecture.",
  latency: "Reduce unnecessary waiting time in every communication flow.",
  operation: "Build systems that can be monitored, recovered, and maintained.",
  growth: "Refactor legacy systems without stopping real services.",
};
