 # GitHub Copilot Instructions — CafeIteso

This repository contains the **CafeIteso** project used in the Software Requirements Engineering course at ITESO.

Always use `/docs/project-context.md` as the primary source of project context before analyzing or generating project-related content.

## Current Project Stage

The project is currently in the **Requirements Elicitation** stage.

Students are currently collecting and documenting **functional ideas** discovered through different elicitation techniques.

At this stage, functional ideas are NOT yet formal requirements.

## How to Work with Functional Ideas

When working with functional ideas:

- Preserve the original business intent.
- Keep each idea associated with its corresponding Epic.
- Preserve the elicitation source whenever it is known.
- Do not change the meaning of an idea unless explicitly requested.
- Do not silently resolve missing information.
- Clearly identify assumptions.
- Clearly distinguish existing project information from AI-generated suggestions.
- If information is missing, identify it as an open question instead of inventing an answer.
- Use the terminology already established in `/docs/project-context.md`.

## Do Not Move Ahead in the Requirements Process

Unless explicitly requested, do NOT transform functional ideas into:

- User Stories
- Use Cases
- Formal Requirements
- Acceptance Criteria
- Gherkin scenarios
- Business Rules
- Backlog items
- Technical specifications
- Software architecture
- Database designs
- API designs
- UI designs
- Test cases
- Implementation tasks

These artifacts will be introduced progressively later in the course.

## Do Not Refine Automatically

Do not automatically:

- Decompose functional ideas.
- Merge functional ideas.
- Prioritize functionality.
- Rewrite ideas into a more formal requirements format.
- Add detailed behavior.
- Add technical implementation decisions.
- Define validation criteria.
- Infer business rules that have not been documented.
- Expand project scope.

Only perform these activities when explicitly requested.

## Handling Missing Information

When important information is missing:

1. Identify what information is missing.
2. Keep it as an open question.
3. Suggest what stakeholder or elicitation activity could help obtain the information when appropriate.

Do not invent project decisions simply to complete an answer.

## AI-Generated Suggestions

If you propose functionality that is not already documented in the repository:

- Clearly identify it as an **AI suggestion**.
- Do not present it as an approved project decision.
- Do not assume it belongs to the final project scope.

## Project Evolution

The CafeIteso requirements will evolve throughout the semester.

The same GitHub Issues may progressively gain more detail as new Requirements Engineering techniques are introduced.

Always work according to the **current stage of the project**, not according to what could eventually be produced later.
