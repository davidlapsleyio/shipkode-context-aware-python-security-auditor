# Context-Aware SQL Injection Remediation

As a Velocity-Driven Developer I want to receive a contextual explanation and a code fix for a detected SQL injection so that I can remediate the risk in under 15 minutes without external research.

## Actors

- The Velocity-Driven Developer

## Preconditions

- The GitHub repository is integrated with the AI Code Review Bot.
- A PR is opened containing new or modified Python code.

## Main Flow

1. Developer submits a Pull Request containing a new API endpoint.
2. The AI Code Review Bot analyzes the data flow from the request object to the database layer.
3. The bot detects an unparameterized SQL query reachable by user input.
4. The bot posts a comment directly on the problematic line of code with a trace of the data flow.
5. The bot provides a specific remediation example using SQLAlchemy parameterized queries.

## Postconditions

- The developer applies the fix without leaving the IDE or searching external documentation.
- The security vulnerability is blocked from merging into the main branch.

## Acceptance Criteria

- The bot identifies the specific unsanitized entry point and terminal sink in the PR comment.
- The explanation includes a 3-5 line code snippet demonstrating the fix.
- The developer can trigger a re-scan within 60 seconds of pushing a fix.

