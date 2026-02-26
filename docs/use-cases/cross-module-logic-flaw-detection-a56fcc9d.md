# Cross-Module Logic Flaw Detection

As a Velocity-Driven Developer I want to understand complex logic vulnerabilities that span multiple files so that I can improve my secure coding skills while shipping features.

## Actors

- The Velocity-Driven Developer
- The Overwhelmed Security Architect

## Main Flow

1. Developer implements a complex custom authentication decorator.
2. The bot performs a cross-module analysis to see how the decorator is applied to sensitive views.
3. The bot identifies a logic bypass where certain exception handlers return a 200 OK without validating the session.
4. The bot explains the logic flaw in plain English, comparing the current state to a secure state.

## Postconditions

- The developer refactors the logic to close the bypass.
- The security knowledge is captured in the PR history for future training reference.

## Acceptance Criteria

- The bot identifies logic flaws that span across 2 or more separate Python modules.
- The summary provides an 'Impact Score' based on the sensitivity of the data handled in the logic flow.
- The SDE II developer reports an 'increased understanding' of the flaw via a feedback button on the PR.

