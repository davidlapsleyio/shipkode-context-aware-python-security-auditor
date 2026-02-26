# Requirements: Context-Aware SQLi Remediation

## Introduction

Context-Aware SQLi Remediation is a core capability of CodeGuard AI designed to eliminate the manual effort involved in fixing SQL Injection vulnerabilities. The feature analyzes the developer's specific Python framework (e.g., Django, Flask, SQLAlchemy) and provides localized code patches that replace vulnerable string formatting with secure parameterized queries. Beyond simple fixes, it provides educational context through risk explanations and interactive secure coding tips, ensuring developers understand the 'why' behind the vulnerability and the 'how' of the remediation.

## Requirements

### F2-R1: Framework-Specific Patch Generation

- **Priority:** must
- **Type:** event_driven

> As a Velocity-Driven Developer I want to receive a framework-specific code fix for a detected SQL injection so that I can apply the remediation without manual syntax adjustment.

**Acceptance Criteria:**
- WHEN a SQLi vulnerability is detected, THE system SHALL identify the specific Python database framework or library in use.
- THE system SHALL generate a code patch using the native parameterization syntax of the detected framework.

### F2-R2: Contextual Risk Explanation

- **Priority:** must
- **Type:** ubiquitous

> As a Velocity-Driven Developer I want to see a contextual explanation of the vulnerability so that I can understand the data flow that makes the code exploitable.

**Acceptance Criteria:**
- WHEN a code patch is proposed, THE system SHALL provide a line-by-line comparison between the vulnerable code and the suggested fix.
- THE system SHALL include a Python-commented explanation of the data-flow path leading to the exploit.

### F2-R3: Integrated Remediation Workflow

- **Priority:** should
- **Type:** state_driven

> As a Velocity-Driven Developer I want the code fix to be available directly in my Pull Request so that I can remediate the risk in under 15 minutes without leaving my code review environment.

**Acceptance Criteria:**
- IF the SQL injection is detected in a CI/CD Pull Request, THEN THE system SHALL post the remediation snippet as a suggested change.
- THE system SHALL provide an 'Apply Fix' button that automatically commits the suggested patch to the branch.

### F2-R4: Interactive Secure Coding Tips

- **Priority:** could
- **Type:** optional

> As a Velocity-Driven Developer I want to access interactive secure coding tips so that I can improve my security skills while shipping features.

**Acceptance Criteria:**
- THE system SHALL provide a 'Learn More' section for every SQLi detection containing secure coding principles.
- IF a user interacts with the remediation prompt, THEN THE system SHALL offer alternative secure coding patterns (e.g., ORM usage vs. raw SQL).

