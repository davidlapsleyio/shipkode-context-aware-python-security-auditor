# Tasks: CI/CD Orchestration Layer

- [ ] **F0c-T1: Domain Data Models and Typings**
  Define the core domain entities for Git events, vulnerability findings, and remediation suggestions.
  *Refs: 1, 2, 3, 5*
  - [ ] **F0c-T1.1: Define Git Provider Event Schemas**
    Define payload structures for PR events from multiple providers (GitHub, GitLab, Bitbucket).
    *Refs: 1, 4*
  - [ ] **F0c-T1.2: Define Finding and Remediation Models**
    Define the VulnerabilityFinding and RemediationPatch data classes ensuring support for rich-text explanations.
    *Refs: 2, 5*
- [ ] **F0c-T2: Core Orchestration Service Logic Logic**
  Implement the core business logic for processing scans and filtering results.
  *Refs: 1, 2, 3, 5*
  - [ ] **F0c-T2.1: High-Fidelity Reachability Filter**
    Implement logic to evaluate data paths and discard non-exploitable vulnerabilities.
    *Refs: 3*
  - [ ] **F0c-T2.2: Remediation Synthesis Engine**
    Build the logic to pair a detected vulnerability with its corresponding contextual explanation and code fix.
    *Refs: 2, 5*
  - [ ] **F0c-T2.3: Property Test: Feedback Completeness**
    Write property tests to ensure every SQL injection finding results in a non-empty explanation and code fix.
    *Refs: 2*
- [ ] **F0c-T3: Git Provider Adapters**
  Implement adapters for interacting with Git provider APIs (webhook reception and PR commenting).
  *Refs: 1, 4*
  - [ ] **F0c-T3.1: Webhook Interception Layer**
    Implement handlers for incoming PR webhooks to trigger scan flows.
    *Refs: 1, 4*
  - [ ] **F0c-T3.2: Git Provider Feedback Publisher Interface**
    Implement the mechanism to post rich-text/markdown feedback and code suggestions back to the PR.
    *Refs: 2, 5*
