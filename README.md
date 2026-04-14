# Hi, I'm Tamilore 👋

I build systems that actually work under pressure — auth flows, payment logic, access control, the full stack.
Based in Ibadan, Nigeria. Computer Science student. Shipping real things.

**Java · Spring Boot · Node.js · Express · React · MySQL · PostgreSQL**

---

### 🚀 What I'm working on

- **Spring Boot:** Rebuilding backend services in Java — REST APIs, Spring Security, JPA/Hibernate with PostgreSQL.
- **Algorithms:** Daily problem-solving focused on optimization and pattern recognition (arrays, linked lists, recursion, DP).
- **Systems thinking:** Concurrency, data integrity under load, and access control architecture across full-stack projects.

---

### 💻 Tech Stack

**Languages:** Java · JavaScript · SQL · HTML/CSS
**Frameworks & runtimes:** Spring Boot · React · Node.js · Express
**Databases:** MySQL · PostgreSQL
**Tools:** Git · Postman · VS Code

---

### 🛠️ Featured Project

#### Learnova — Full-Stack E-Learning Platform
> Production-grade learning platform with dual user roles, end-to-end JWT auth, email verification, and a custom CSS design system. Built across four deliberate phases — auth foundation, core features, design polish, production hardening.

**Auth & Security**
- JWT stateless sessions + bcrypt (cost 10). Signup triggers a branded verification email with a 32-byte cryptographic token. Accounts stay locked until confirmed at the API level — not just the UI.
- The frontend AuthContext decodes the JWT on load and handles token expiry separately from invalid tokens, clearing localStorage and redirecting rather than serving broken state.

**Role-Based Access Control**
- Enforced in three independent layers: React route guard, Express middleware, and the SQL query itself.
- No client-side bypass can reach the database — unauthorized access is structurally impossible, not just conditionally blocked.

**Course & Content System**
- YouTube URL parser handles all formats (watch, youtu.be, embed, Shorts) and renders responsive 16:9 iframes automatically.
- Search and filter state lives in URL query params — every filtered view is directly linkable.

**Production Hardening**
- Error boundaries, loading skeletons, custom 404, typed token-expiry vs invalid-token responses, CORS locked to deployed frontend.
- ~30 files across frontend and backend. Custom CSS design system exceeding 1,200 lines. Fully responsive to 320px.

**Stack:** React 19 · Vite · Node.js · Express 5 · MySQL · JWT · Nodemailer
**GitHub:** [repo link] | **Live Demo:** [deployed link]

---

### 🔧 Other Projects

#### GigConnect — Escrow-Backed Service Marketplace *(Hackathon)*
- Integrated Interswitch API to hold payments in escrow during active jobs — funds release only on mutual completion, eliminating dispute risk without a human mediator.
- Built a community-driven price index that aggregates average service costs across the platform — an anti-exploitation layer against price gouging.
- Geolocation-based matching routes clients to the nearest available professional, reducing response time and logistics overhead.
- Strict MVC backend separates auth, job lifecycle, and chat across independent, testable modules.
— no client-side action is trusted.
  
**Stack:** Node.js · Express · MySQL · Interswitch API

---

#### Enterprise Library Management API
- Fail-safe database transactions for borrow/return operations — concurrent requests cannot cause race conditions or corrupt inventory counts.
- JWT-based RBAC with distinct permission scopes: admin (inventory management) vs patron (browsing and borrowing) — enforced at middleware level.
- Paginated, filtered REST endpoints designed for scale — response times stay predictable as the catalogue grows.

**Stack:** Node.js · Express · MySQL · JWT

---

#### Computerized Exam System
- Enforced exam integrity using the Visibility API, fullscreen locking, and input interception — tab switching and copy/paste blocked at the browser event level.
- Persistent session state recovers in-progress exams after unexpected interruptions without data loss.
- Anti-cheat middleware sits between UI events and exam logic — no client-side action is trusted.

**Stack:** JavaScript · Node.js

---

### 📫 Let's connect

- **LinkedIn:** https://www.linkedin.com/in/tamilore-afolabi
- **Email:** tamziyafolabi@gmail.com
- **Portfolio:** 
