# Tasks: Deep-Context Taint Tracker

- [ ] **F0b-T1: Domain Models and Types**
  Define core data structures for taint tracking including Source, Sink, Sanitizer, and TaintPath models.
  *Refs: 1*
  - [ ] **F0b-T1.1: Define Taint Graph Models**
    Implement Pydantic models for TaintNode and TaintGraph to represent cross-file data flows.
  - [ ] **F0b-T1.2: Define Sanitizer Schemas**
    Define standard and custom sanitizer registry schemas.
- [ ] **F0b-T2: Taint Propagation Engine Logic Core**
  Implement the core engine responsible for walking the AST and tracking data flow across module boundaries.
  *Refs: 1, 5*
  - [ ] **F0b-T2.1: Cross-File AST Walker**
    Develop logic to track variable propagation across function calls and file imports.
  - [ ] **F0b-T2.2: Sanitizer Logic Integration**
    Implement logic to prune paths when a recognized sanitizer function is encountered in the call stack.
- [ ] **F0b-T3: Exploitability Verifier Service**
  Develop the verification service that filters paths by attempting to prove reachability and exploitability.
  *Refs: 2*
  - [ ] **F0b-T3.1: Reachability Analysis Service**
    Validate that a path from a user-controlled source leads to a dangerous sink without mitigation.
  - [ ] **F0b-T3.2: Exploitability Filtering Logic**
    Filter out paths where data types or constraints prevent exploitability (e.g., integer casting before SQL sink).
- [ ] **F0b-T4: Automated Remediation Service**
  Implement automated code generation for fixing detected vulnerabilities.
  *Refs: 3*
  - [ ] **F0b-T4.1: Remediation Generator Logic Factory**
    Generate context-aware remediation code snippets based on the specific sink type (e.g., parameterized queries for SQLi).
- [ ] **F0b-T5: Integration Adapters and API**
  Create the adapters for CI/CD integration and PR feedback.
  *Refs: 4*
  - [ ] **F0b-T5.1: CI/CD CLI Adapter**
    Develop a CLI wrapper to execute the engine and export results in SARIF/JSON format for CI pipelines.
  - [ ] **F0b-T5.2: PR Feedback Adapter**
    Implement a GitHub Action / GitLab MR comment generator to post findings directly to PRs.
