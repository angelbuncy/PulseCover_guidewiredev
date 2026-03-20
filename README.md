# PulseCover: AI-Powered Parametric Insurance

**PulseCover** is a cutting-edge, full-stack insurance platform designed specifically for the gig economy. By leveraging AI-driven risk assessment and automated parametric triggers, we provide delivery workers with seamless "no-claims-filing" income protection that activates instantly during adverse conditions.



##  Requirement & Persona-Based Scenarios

Traditional insurance is too slow for the gig economy. PulseCover automates financial recovery for workers whose earnings are tied to their ability to be on the road.

### User Personas
* **The Delivery Partner (e.g., Rohit):** Works 10+ hours daily. His income drops by **40%** during monsoons or heat waves. He needs affordable, automated coverage without the headache of manual paperwork.
* **The Platform Admin:** Needs to monitor total portfolio exposure, identify high-risk zones, and manage fraud queues efficiently using AI-generated insights.

### Application Workflow
1.  **Onboarding:** The worker connects their profile and selects a coverage zone.
2.  **AI Quote:** The system calculates a personalized premium based on historical weather patterns and worker risk profiles.
3.  **Active Monitoring:** The backend continuously polls environmental data (Weather APIs/IoT).
4.  **Automatic Trigger:** If a threshold is met (e.g., Rainfall > 50mm), a claim is instantly "triggered."
5.  **Instant Payout:** Funds are disbursed to the worker’s wallet, compensating for projected "missed shifts" automatically.


##  Weekly Premium & Parametric Model

### The Weekly Subscription Strategy
PulseCover operates on a **Weekly Subscription** model. This aligns with the weekly payout cycles of delivery platforms (Swiggy, Zomato, UberEats), making it cash-flow friendly. It allows workers to opt-in during volatile seasons and opt-out during stable periods.

### Parametric Triggers
Claims are not based on subjective "loss assessment" but on **pre-defined parameters**:
* **Precipitation:** Rainfall exceeding a specific threshold (mm/hr) that makes biking unsafe.
* **Temperature:** Extreme heat (e.g., >42°C) triggers "Heat Stress" compensation.
* **Disruption Index:** High-impact local events (protests, road closures) detected via API.

### Platform Choice: Web-First Responsive (React)
We chose a **Web platform** with a mobile-first **Glassmorphism** UI because:
* **Frictionless Access:** Workers can access their dashboard via a link in their delivery app without downloading a heavy APK.
* **Rapid Deployment:** Allows for instant updates to ML models and UI during high-velocity growth.


##  AI/ML Integration

PulseCover uses a dual-engine ML approach to ensure sustainability and security:

| Feature | Model | Purpose |
| :--- | :--- | :--- |
| **Dynamic Pricing** | **Random Forest** | Analyzes historical volatility and geographic risk to generate fair, risk-adjusted premiums. |
| **Fraud Detection** | **Logistic Regression** | Detects "Location Drift"—flagging claims if a worker's GPS doesn't match the triggered weather zone. |
| **Risk Meter** | **Predictive Analytics** | Provides workers with a real-time "Risk Score" to help them decide when to purchase coverage. |



##  Tech Stack & Development Plan

### The Stack
* **Frontend:** React.js, Tailwind CSS, Framer Motion (Animations).
* **Backend:** FastAPI (Python), Pydantic (Data Validation).
* **Database:** MongoDB (Scalable Policy Storage) with In-Memory fallback for demo stability.
* **ML Engine:** Scikit-Learn, Pandas, NumPy.

### Development Roadmap
* **Phase 1:** Core API, Auth, and "Deterministic" Trigger simulation.
* **Phase 2:** Integration of the Random Forest model for live, dynamic quoting.
* **Phase 3:** Real-world Weather API integration (replacing `USE_MOCK_EXTERNALS`).
* **Phase 4:** Advanced Admin Analytics for portfolio risk management.

---

##  Folder Structure
```text
DevTrails-GuideWire/
|-- backend/          # FastAPI, ML Models, & DB Logic
|   |-- app/          # Core Application Logic
|-- frontend/         # React + Tailwind Responsive UI
|   |-- src/          # Components, Pages, & State
`-- README.md         # Documentation
