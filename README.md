🧠 AI-Assisted API Test Orchestration Framework (Postman + Newman + GPT)

📌 Overview
This project demonstrates a Test Architect–grade automation framework where Postman collections are treated as executable specifications, and GPT assists in orchestration, analysis, and decision-making—not execution.
The framework evolves traditional API automation into an AI-assisted testing system capable of:
Context-aware execution
Intelligent skipping
Failure classification
Human-readable summaries
Portfolio-ready architectural clarity
🎯 Core Philosophy
GPT decides. Newman executes. Postman defines intent.
No brittle hardcoding
No AI running tests directly
Clear separation of concerns
Automation designed for scale, auditability, and intelligence
🧱 Architecture at a Glance
Copy code

Postman (Execution Rules + Test Intent)
        ↓
Newman (CLI Execution Engine)
        ↓
Structured JSON Results
        ↓
GPT (Interpretation, Summaries, Next-Step Suggestions)
🧪 Phase Breakdown
✅ Phase 1: Strong Postman Foundation
Objective: Make Postman automation clean, stable, and AI-ready.
Implemented:
Standardized collection & folder structure
Consistent naming conventions
Environment-driven execution context
Business-focused assertions
Newman-compatible execution
Output:
✔️ Production-ready Postman collections
✅ Phase 2: MCP / Tool Design (No Coding)
Objective: Define how GPT can safely interact with test execution.
Designed:
Execution boundaries (GPT never executes tests)
Tool contracts (inputs / outputs)
Result schemas for AI interpretation
Failure classification strategy
Output:
✔️ Clear orchestration and decision-making design
✅ Phase 3: Minimal Orchestrator (MVP)
Objective: Enable intelligent execution without over-engineering.
Implemented:
Collection-level prerequisite script
Metadata-driven skipping logic
Semantic build version comparison
Environment and run-type gating
Structured JSON logging per request
Key Capability:
Tests self-decide whether they should run based on metadata.
Output:
✔️ Working execution control layer
🚧 Phase 4: GPT Integration (In Progress)
Objective: Let GPT analyze—not run—tests.
Current scope:
GPT reads Newman JSON output
GPT summarizes failures
GPT distinguishes:
Expected negatives
Known defects
Environment issues
GPT suggests next actions (rerun, block, raise defect)
Output:
✔️ AI-assisted test orchestration
📄 Documentation Strategy
This framework follows a layered documentation approach, embedding intent directly into Postman—not external documents.
🔹 Collection-Level Documentation
Defines global execution philosophy:
Run type (SMOKE / REGRESSION)
Environment scope
Build applicability
Failure policy
📍 Purpose:
Establishes a single source of truth for the entire suite.
🔹 Folder-Level Documentation
Represents feature or lifecycle boundaries:
Feature-specific execution rules
Shared constraints
Logical grouping
📍 Purpose:
Avoids duplication while maintaining control at scale.
🔹 Request-Level Documentation
Captures business and testing intent:
Test purpose
Positive / negative behavior
Expected status & error codes
Severity & classification
Preconditions & postconditions
📍 Purpose:
Every test is self-describing and auditable, even without reading scripts.
🧠 Execution Metadata Example (Request-Level)
Copy code
Text
TEST_LEVEL: REGRESSION
ENV_ALLOWED: QA
BUILD_INTRODUCED: 4.7.2
EXPECTED_STATUS: 404
ERROR_CODE: USER_NOT_FOUND
SEVERITY: HIGH
CLASSIFICATION: DEFECT
ACTION_ON_FAILURE: LOG_DEFECT
This metadata directly drives:
Execution decisions
Skipping logic
Failure classification
GPT analysis
📊 Sample Structured Result (Newman Output)
Copy code
Json
{
  "request": "Get User – Invalid ID",
  "build": "4.7.1",
  "status": 404,
  "failure": false,
  "classification": "EXPECTED_NEGATIVE",
  "action": "NONE"
}
GPT consumes this—not raw logs.
🧩 Why This Project Stands Out
Treats tests as living specifications
Separates execution from intelligence
Scales without becoming brittle
Aligns with Test Architect / QA Director thinking
Portfolio-ready, interview-ready, real-world applicable
🚀 Future Enhancements (Phase 5 Preview)
Conditional flows (UI → API → DB)
Partial reruns
Environment intelligence
CI/CD triggers
Known-defect learning memory
👤 Author
Prajakta
Automation Test Engineer | Test Architect Track
Focus: API Automation, Data Validation, AI-Assisted Testing
