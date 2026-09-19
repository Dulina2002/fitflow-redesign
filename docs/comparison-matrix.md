## Activity 1: Frontend Technology Comparison

| Evaluation Criteria | Flutter | React Native (New Arch) | Kotlin Multiplatform (KMP) | Swift / SwiftUI |
| :--- | :---: | :---: | :---: | :---: |
| **Development Speed** | 4 (0.80) | 5 (1.00) | 3 (0.60) | 2 (0.40) |
| **AI/ML & CV Support** | 3 (0.60) | 4 (0.80) | 3 (0.60) | 5 (1.00) |
| **Maintainability & Cost** | 4 (0.60) | 5 (0.75) | 3 (0.45) | 1 (0.15) |
| **Runtime Performance** | 4 (0.60) | 4 (0.60) | 5 (0.75) | 5 (0.75) |
| **Security & Privacy** | 4 (0.40) | 4 (0.40) | 5 (0.50) | 5 (0.50) |
| **Scalability & Concurrency** | 4 (0.40) | 4 (0.40) | 4 (0.40) | 4 (0.40) |
| **Cross-Platform / Web** | 4 (0.40) | 5 (0.50) | 3 (0.30) | 1 (0.10) |
| **Total Weighted Score (100%)** | **3.80** | **4.45** | **3.60** | **3.30** |

---

## Activity 2: Backend, Database & Authentication Evaluation

### 1. Database Options Comparison

| Evaluation Criteria | PostgreSQL (Relational / SQL) | MongoDB (NoSQL Document) | Firebase Firestore (NoSQL Real-Time) | AWS DynamoDB (Key-Value) |
| :--- | :--- | :--- | :--- | :--- |
| **Scalability** | High (Vertical scaling + Horizontal read replicas & pooling via PgBouncer) | Very High (Native auto-sharding and horizontal replica sets) | Exceptional (Fully managed serverless auto-scaling by Google Cloud) | Exceptional (Seamless automatic partitioning with predictable throughput) |
| **Query Performance** | High (Complex multi-table relational joins, analytical aggregations, JSONB indexing) | High (Fast document reads/writes on hierarchical objects) | Moderate (Fast for shallow queries; slow and limited for multi-field aggregations) | Superior (Single-digit millisecond latency on indexed key lookups) |
| **Health Data Handling & Security** | Superior (Strict ACID compliance, Row-Level Security, transparent column encryption) | Moderate (ACID supported; flexible schema risks data integrity drifts over time) | Moderate (Rules engine exists, but lacks deep healthcare compliance controls) | High (Fine-grained IAM controls, encryption at rest, but complex relational modeling) |
| **Cost & Maintenance** | Low–Moderate (Predictable costs via managed cloud instances like AWS RDS / Supabase) | Moderate (Managed via MongoDB Atlas; costs rise with unindexed memory usage) | Moderate–High (Pay-per-read/write model can produce unexpected cost spikes) | High (Complex capacity planning and read/write unit cost management) |

### 2. Backend Frameworks Comparison

| Framework | Concurrency & Async | AI/ML Tooling | Type Safety | Team Velocity |
| :--- | :--- | :--- | :--- | :--- |
| **Node.js / NestJS** | Non-blocking event loop; high I/O concurrency | Moderate (REST/gRPC to ML service) | Enterprise TypeScript | Very High (Shared frontend TS skills) |
| **Python / FastAPI** | High async performance via Starlette | Native (TensorFlow, PyTorch, OpenCV) | Strong runtime types via Pydantic | High (Rapid ML prototyping) |
| **Go (Golang)** | Superior via lightweight Goroutines | Minimal native AI support | Strict compile-time static types | Moderate (Verbose implementation) |

### 3. Authentication & Authorization Solutions

| Solution | Security & Compliance | Ease of Integration | Cost at Scale |
| :--- | :--- | :--- | :--- |
| **Supabase Auth** | Superior (Native PostgreSQL RLS policies, GDPR compliant) | High (JWTs, OAuth for Google/Apple) | Low–Moderate (Open-source base) |
| **Firebase Auth** | High (Standard OAuth and phone SMS verification) | Very High (Turnkey SDKs) | Moderate (Generous free tier) |
| **AWS Cognito** | Enterprise (HIPAA/GDPR compliant, complex IAM) | Low–Moderate (Steep setup curve) | Low–Moderate |
| **Auth0** | Enterprise (Advanced MFA, threat detection) | High (Pre-built Universal Login) | Very High (Scales steeply per MAU) |

### 4. Recommended Combination for FitFlow
- **Primary Backend:** Node.js (NestJS) for application business logic, progress tracking, and WebSockets.
- **AI & Vision Microservice:** Python (FastAPI) for ML workout recommendations and food image scanning.
- **Database:** PostgreSQL (with Row-Level Security) paired with Redis for caching.
- **Authentication:** Supabase Auth (JWT) integrated with native Apple and Google sign-in.

---

## Activity 3: Weighted Decision Matrix

| Criteria | Weight | Option 1: NestJS + Postgres + FastAPI | Option 2: Pure Python (FastAPI + Django) | Option 3: Full Go + Postgres | Option 4: Pure Serverless (Firebase) |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Development Speed** | 20% | 5 (1.00) | 4 (0.80) | 3 (0.60) | 4 (0.80) |
| **AI/ML Integration** | 20% | 5 (1.00) | 5 (1.00) | 2 (0.40) | 3 (0.60) |
| **Maintainability & Cost** | 15% | 4 (0.60) | 4 (0.60) | 3 (0.45) | 3 (0.45) |
| **Runtime Performance** | 15% | 4 (0.60) | 3 (0.45) | 5 (0.75) | 3 (0.45) |
| **Security & Compliance** | 10% | 5 (0.50) | 4 (0.40) | 5 (0.50) | 3 (0.30) |
| **Scalability & Concurrency** | 10% | 4 (0.40) | 3 (0.30) | 5 (0.50) | 4 (0.40) |
| **Cross-Platform Support** | 10% | 5 (0.50) | 4 (0.40) | 4 (0.40) | 4 (0.40) |
| **Total Weighted Score** | **100%** | **4.60** | **3.95** | **3.60** | **3.40** |
