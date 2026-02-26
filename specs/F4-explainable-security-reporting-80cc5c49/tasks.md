# Tasks: Explainable Security Reporting

- [ ] **F4-T1: Domain Models & Type Definitions**
  Define the core structures for representating vulnerability insights, including data-flow nodes, exploit vectors, and remediation guidance.
  *Refs: 1, 2, 3, 5*
  - [ ] **F4-T1.1: Vulnerability Schema Definition**
  - [ ] **F4-T1.2: Data-Flow Graph Model**
  - [ ] **F4-T1.3: Remediation & Educational Metadata Types**
- [ ] **F4-T2: LLM Explanation Adapter Implementation**
  Implement the integration with LLM services to generate human-readable summaries and educational content based on raw analysis results.
  *Refs: 1, 5*
  - [ ] **F4-T2.1: Natural Language Summary Generator**
  - [ ] **F4-T2.2: Educational Guidance Prompt Engineering**
- [ ] **F4-T3: Security Reporting Use Case Logic**
  Core logic to aggregate analysis data, map flows to source code, and format the final security report.
  *Refs: 2, 3, 5*
  - [ ] **F4-T3.1: Exploit Vector Path Mapper**
  - [ ] **F4-T3.2: Visual Data-Flow Orchestrator**
  - [ ] **F4-T3.3: Report Assembly Service**
- [ ] **F4-T4: PR Resident Reporting Integration**
  Integrate reporting with the Pull Request workflow, ensuring reports are comments/pinned to specific code lines and PR metadata.
  *Refs: 4*
  - [ ] **F4-T4.1: PR Comment/Pinning Adapter**
  - [ ] **F4-T4.2: Line-Specific Vector Annotation Logic**
- [ ] **F4-T5: Visual Reporting Components**
  Implement the visual rendering logic for the security report inside the developer's environment (Markdown/HTML for PRs).
  *Refs: 2*
  - [ ] **F4-T5.1: Markdown Graph Visualization Renderer**
  - [ ] **F4-T5.2: Interactive Remediation UI Components**
