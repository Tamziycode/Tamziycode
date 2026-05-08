<div align="center">

<img src="header.svg" width="100%" alt="Tamilore Banner">

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tamilore-afolabi)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:tamziyafolabi@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-FF2D1F?style=for-the-badge&logo=firefoxbrowser&logoColor=white)](https://tamziy.vercel.app)


</div>

---

## `whoAmI`

```json
{
  "name": "Tamilore Afolabi",
  "alias": "Tamziy",
  "role": "Full-Stack Software Engineer",
  "location": "Ibadan, Nigeria",
  "focus": [
    "Backend systems that scale",
    "Auth flows that can't be bypassed",
    "Transactions that stay consistent under concurrency",
    "APIs built for the long run"
  ],
  "stack": {
    "backend": ["Java", "Spring Boot", "Node.js", "Express"],
    "frontend": ["React", "Vite", "HTML", "CSS"],
    "databases": ["MySQL", "PostgreSQL", "MongoDB"],
    "security": ["JWT", "bcrypt", "RBAC", "Spring Security"]
  },
  "currently": "Mastering Spring Boot — layered architecture, JPA/Hibernate, Spring Security",
  "philosophy": "I don't just ship features. I engineer the layer underneath them."
}
```

---

## `[ TECH_STACK ]`

**Languages & Core**

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

**Frameworks & Runtimes**

![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)

**Databases**

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)

**Security & Auth**

![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)
![bcrypt](https://img.shields.io/badge/bcrypt-003087?style=for-the-badge&logoColor=white)

**Tools**

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white)

**In Progress**

![JUnit5](https://img.shields.io/badge/JUnit_5-25A162?style=for-the-badge&logo=junit5&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)

---

## `[ ACTIVE_PROCESSES ]`

- **Spring Boot:** Mastering layered architecture — service/repository separation, JPA entity relationships, Spring Security. Migrating from Node.js-first thinking to proper enterprise patterns
- **DSA:** Daily problem-solving focused on pattern recognition, time complexity, and solutions that hold up under scale — arrays, linked lists, recursion, DP
- **Systems thinking:** Concurrency control, data integrity under load, and access control architecture

---

## `[ FLAGSHIP_SYSTEM ]` — Learnova

> Production-grade e-learning platform with dual user roles, end-to-end JWT auth, email verification, and a custom dark-mode design system. Built across four deliberate phases.

**System Architecture**

```mermaid
graph TD
    Client["React 19 Frontend"] -->|HTTPS| API["Express 5 REST API"]
    API --> AuthMW["JWT Auth Middleware"]
    AuthMW -->|Valid token| RoleMW["Role Guard Middleware"]
    RoleMW -->|Student| SC["Student Controllers"]
    RoleMW -->|Instructor| IC["Instructor Controllers"]
    SC --> DB[("MySQL Database")]
    IC --> DB
    DB -->|WHERE instructor_id = ?| IC
    API -->|Signup trigger| Email["Resend API"]
    Email -->|32-byte token| Inbox["User Inbox"]
    Inbox -->|/verify| API

    style Client fill:#0c1018,color:#61DAFB,stroke:#61DAFB
    style API fill:#0c1018,color:#339933,stroke:#339933
    style AuthMW fill:#0c1018,color:#ff2d1f,stroke:#ff2d1f
    style RoleMW fill:#0c1018,color:#ff2d1f,stroke:#ff2d1f
    style SC fill:#0c1018,color:#e8edf5,stroke:#263044
    style IC fill:#0c1018,color:#e8edf5,stroke:#263044
    style DB fill:#0c1018,color:#4479A1,stroke:#4479A1
    style Email fill:#0c1018,color:#EA4335,stroke:#EA4335
    style Inbox fill:#0c1018,color:#8a95a8,stroke:#263044
```

**Engineering Breakdown**

| Layer | What was built | Why it matters |
|---|---|---|
| **Auth** | JWT stateless sessions + bcrypt (cost 10). Signup triggers branded email with 32-byte cryptographic token | Accounts locked at API level until confirmed — not just a UI gate |
| **RBAC** | Three independent layers: React route guard → Express middleware → SQL ownership check | No client-side bypass can reach data — unauthorised access is structurally impossible |
| **Session** | AuthContext handles token expiry and invalid tokens as separate cases | No broken states served — redirect fires before stale data renders |
| **Content** | YouTube URL parser handles watch / youtu.be / embed / Shorts | Search + filter state in URL params — every filtered view is directly linkable |
| **Prod** | Error boundaries, skeletons, typed token error responses, CORS locked to origin | ~30 files, 1,200+ line CSS design system, responsive to 320px |

### `>> Exception Handling & Edge Cases`
* **Stale State Rejection:** If a user’s JWT expires while they are filling out a form, the API rejects the submission and the React `AuthContext` catches the 401, clears local storage, and preserves the user's input state while forcing a re-auth.
* **Concurrent Video Tracking:** Handles edge cases where a user opens the same course in two tabs; progress tracking enforces a "latest timestamp wins" rule to prevent database deadlocks.

### `>> Performance Benchmarks (Local)`
* **Auth Overhead:** Custom JWT middleware adds `<15ms` latency to protected routes.
* **Query Optimization:** Indexed `instructor_id` foreign keys dropped course-fetching queries from `O(n)` table scans to `O(log n)`, averaging `120ms` response times in local testing.

> *[Insert screenshot of Postman test suite passing or API logs blocking an unauthorized request here]*

<br/>

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

[![GitHub Repo](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Tamziycode/learnova)
[![Live Demo](https://img.shields.io/badge/Live-Demo-FF2D1F?style=for-the-badge&logo=firefoxbrowser&logoColor=white)](https://learnova-omega.vercel.app)

---

## `[ ANCILLARY_SYSTEMS ]`

<table border="0">
<tr>
<td width="50%" valign="top">

### // GigConnect
**Escrow-Backed Service Marketplace** &nbsp;·&nbsp; *Hackathon*

Financial trust engineered into the architecture — not bolted on.

- **Interswitch API escrow** — funds held until both parties confirm completion, no mediator needed
- Webhook handler + idempotency key validation — prevents double-charging on retries
- Community price index aggregates rates platform-wide — anti-exploitation against gouging
- Geolocation routing to nearest available professional
- Strict MVC — auth, job lifecycle, chat in independent testable modules

<br/>

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![Interswitch](https://img.shields.io/badge/Interswitch-003087?style=flat-square&logoColor=white)

[![Repo](https://img.shields.io/badge/GitHub-View-181717?style=flat-square&logo=github)](https://github.com/Tamziycode/gigconnect)

</td>
<td width="50%" valign="top">

### // Library Management API
**Enterprise REST API &nbsp;·&nbsp; Concurrency Focus**

Built for correctness under pressure. Architecture prioritises data integrity over convenience.

- **Pessimistic locking** on borrow transactions — concurrent requests for the last copy cannot both succeed
- **Transactional Rollback:** If an inventory decrement succeeds but the borrow record insert fails, the entire SQL transaction rolls back to prevent phantom missing books
- **JWT RBAC** — admin (inventory write) vs patron (borrow/view), enforced at middleware layer
- **Performance:** Paginated and indexed search endpoints maintain `<80ms` response times even when simulating 10,000+ mock book records

<br/>

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)

[![Repo](https://img.shields.io/badge/GitHub-View-181717?style=flat-square&logo=github)](https://github.com/Tamziycode/Library_API)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### // Computerized Exam System
**Browser-Level Security**

Anti-cheat logic in a middleware layer — no UI action trusted at face value.

- Visibility API + fullscreen lock + input interception — tab switches caught before reaching the DOM
- Session state serialised on each answer — recovers in under 1s after interruption, no answer loss
- Violations logged with timestamp and event type — tamper evidence, not just prevention
- MongoDB for flexible session document storage — exam snapshots without rigid schema constraints

<br/>

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)

[![Repo](https://img.shields.io/badge/GitHub-View-181717?style=flat-square&logo=github)](https://github.com/Tamziycode/exam-system)

</td>
<td width="50%" valign="top">

### // DSA & Algorithms
**Daily Practice**

Solving problems that hold up under scale — not just ones that pass test cases.

- Arrays, linked lists, stacks, queues — core patterns and implementation
- Recursion and DP — memoisation, tabulation, state transitions
- Binary search, two pointers, sliding window as standard toolkit
- Time and space complexity analysis on every solution

<br/>

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)

[![LeetCode](https://img.shields.io/badge/LeetCode-Active-FFA116?style=flat-square&logo=leetcode&logoColor=black)](https://leetcode.com/u/Tamziycode/)

</td>
</tr>
</table>

---

## `[ TELEMETRY ]`

<div align="center">

<img height="175em" src="https://github-readme-stats.vercel.app/api?username=Tamziycode&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&hide_border=true&bg_color=080b0f&title_color=2d8fff&icon_color=ff2d1f&text_color=e8edf5"/>
&nbsp;
<img height="175em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Tamziycode&layout=compact&hide_border=true&bg_color=080b0f&title_color=2d8fff&text_color=e8edf5&langs_count=6"/>

<br/>
<br/>

![Streak](https://streak-stats.demolab.com?user=Tamziycode&theme=tokyonight&hide_border=true&background=080b0f&stroke=2d8fff&ring=ff2d1f&fire=ff2d1f&currStreakLabel=2d8fff&sideLabels=e8edf5&dates=8a95a8&currStreakNum=e8edf5&sideNums=e8edf5)

</div>

---

## `[ EDUCATION ]`

| | Institution | Degree | Status |
|---|---|---|---|
| `*` | University of Ibadan | B.Sc. Computer Science | Penultimate Year |

---

## `[ INITIATE_HANDSHAKE ]`

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tamilore-afolabi)
[![Email](https://img.shields.io/badge/Email-tamziyafolabi%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:tamziyafolabi@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-FF2D1F?style=for-the-badge&logo=firefoxbrowser&logoColor=white)](https://tamziy.vercel.app)

*Open to backend and full-stack roles where real engineering problems exist.*

<br/>
<br/>

<img src="footer.svg" width="100%" alt="Footer">

</div>
