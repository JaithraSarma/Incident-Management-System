# Infrastructure / SRE Intern Assignment Submission

**Candidate:** Jaithra Sarma Karlapalam
**Role:** Infrastructure / SRE Intern

---

## GitHub Repository Link

**Mandatory Link:** [https://github.com/JaithraSarma/ims-zeotap](https://github.com/JaithraSarma/ims-zeotap)

---

## Assignment Overview

The repository contains the complete implementation of the Mission-Critical Incident Management System (IMS). 

### Key Deliverables Included:
1. **Running Application:** A fully functional distributed application with a React SPA frontend and a Node.js/Express backend, orchestrated via Docker Compose.
2. **Codebase Structure:** A single repository containing both `/backend` and `/frontend` cleanly separated.
3. **Data Handling:** Intelligent separation of data stores using PostgreSQL (transactional), MongoDB (audit/timeseries), and Redis (caching/pub-sub).
4. **Resilience & Backpressure:** Engineered to handle bursts of 10,000 signals/sec using a 3-layer defense mechanism (Rate Limiter → Ring Buffer → Debouncer).
5. **Design Patterns:** Strict adherence to software design principles, implementing the **Strategy Pattern** for dynamic alert classification and the **State Pattern** for strict incident lifecycle management.
6. **Documentation:** A comprehensive `README.md` with an Architecture Diagram, Setup Instructions, and a dedicated Backpressure strategy explanation.
7. **Prompt Engineering:** All AI interaction logs and iterative prompts are checked into the repository (`prompt.md`, `/docs`).

### Non-Functional Enhancements (Bonus Points)
- **Security:** Implemented Express Rate Limiting against DDoS, parameterized SQL queries to prevent SQL injection, and CORS constraints.
- **Performance:** Implemented `O(1)` drop-oldest ring buffers ensuring the ingestion engine never blocks or crashes, and Redis caching for sub-millisecond dashboard reads.
- **Testing:** Comprehensive test suite with 33 passing unit tests verifying state transitions, RCA validation, and memory management edge cases.
- **UI/UX:** Added a real-time WebSocket dashboard, a visual status timeline, automated MTTR calculation, and an in-UI Signal Simulator to easily trigger failure scenarios.

*Please refer to the README.md in the GitHub repository for full setup and architecture details.*
