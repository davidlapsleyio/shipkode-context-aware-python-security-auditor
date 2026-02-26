# Tasks: Context-Aware SQLi Remediation

- [ ] **F2-T1: Domain Models and Type Definitions**
  Define the core data structures for vulnerabilities, remediation patches, and context metadata.
  *Refs: 1, 2*
  - [ ] **F2-T1.1: Define Vulnerability Context Models**
    Define TypeScript interfaces for VulnerabilityContext including framework type, data flow path, and sink location.
  - [ ] **F2-T1.2: Define Patch and Tip Models**
    Define RemediationPatch schema containing the code diff, framework-specific explanation, and educational tips.
- [ ] **F2-T2: LLM Patch Generation Service**
  Implement the LLM wrapper to generate framework-aware code fixes and explanations.
  *Refs: 1, 2, 4*
  - [ ] **F2-T2.1: Framework-Specific Prompt Engineering**
    Develop prompt templates that inject framework context (e.g., TypeORM, Knex, Sequelize) to ensure parameterized output.
  - [ ] **F2-T2.2: Contextual Explanation Generation**
    Implement logic to generate step-by-step data flow explanations based on vulnerability traces.
  - [ ] **F2-T2.3: Secure Coding Tip Integration**
    Incorporate a library of interactive secure coding tips into the LLM generation pipeline.
- [ ] **F2-T3: Remediation Orchestrator Implementation Logic**
  Orchestrate the flow between detection, patch generation, and PR delivery.
  *Refs: 1, 3*
  - [ ] **F2-T3.1: Framework Detection Logic**
    Create a service to map detected codebases to specific web/ORM frameworks.
  - [ ] **F2-T3.2: Remediation Orchestration Logic**
    Coordinate calls to LLMPatchGenerator and format result into a PR-compatible comment or commit.
- [ ] **F2-T4: API and External Adapters**
  Integrate with version control providers to surface the remediation.
  *Refs: 3*
  - [ ] **F2-T4.1: PR Integration Adapter**
    Develop an adapter to post remediation comments and code suggestions directly to GitHub/GitLab PRs.
- [ ] **F2-T5: Integrated Remediation Interface**
  Implement the interactive UI elements for the PR view.
  *Refs: 2, 4*
  - [ ] **F2-T5.1: PR Documentation & Interactive UI Template**
    Design the markdown template for PR comments including 'Accept Fix' buttons and collapsible 'Secure Coding Tips'.
