# Agent Instructions: Issue Analysis & Use Case Generation Workflow

## Objective

The goal of this workflow is to analyze open functional idea issues in the repository, identify missing use cases for issues, refine those use cases collaboratively with the user, and ultimately create them as formal subissues in the repository upon approval.

## Workflow Overview

[Phase 0: Discovery & Reading]
           │
           ▼
[Phase 1: Candidate Proposal & Refinement]
           │
           ▼
[Phase 2: Draft Elaboration & Review]
           │
           ▼
[Phase 3: Subissue Generation]


## Phase 0: Discovery & Comprehension

**Use the available project context**: Read the project context located in the project-context.md.

**Read Issues:** Read all open issues in the repository. Treat each open issue as a Functional Idea.

**Analyze Existing Subissues:**

Some issues will already have subissues attached.

Use these existing subissues as the canonical examples for the required structure, fields, and formatting expected for a full use case.

**Execution Mode:** Read-only. Do not make any updates, modifications, or creations during this phase.

## Phase 1: Candidate Proposal (Per-Issue Basis)

**Scope:** Execute this phase only for open issues that are requested to be analyzed and you need to be told explicitly which ones to process. Process one issue at a time. Remember to read any existing subissues for the issue to understand the context and avoid duplication.

**Analyze Functional Idea:** Read and evaluate the issue description.

**Core Definitions & Considerations for Candidates:**
- **System:** The product or service with defined functionality.
- **Goal:** The purpose or objective users reach with a system’s features.
- **Use Case:** A task that an actor needs to perform with the help of the system.
- **Actor:** A user of a system in a particular role. An actor can be anything exhibiting behavior that interacts with a system, such as a single user, a team, or another piece of software.
- **Actor Role vs. Individual:** An actor is a role, not an individual person (e.g., a librarian can have many distinct roles).
- **Actor Naming Rule:** In naming actors, choose specific names that describe the role—never generic names such as "user" or "client".

**Brainstorm Candidates:** Identify potential use case candidates that break down the main functional idea. Do this through detection of separate actor goals to build off them as multiple use cases if applicable. Identify missing or ambiguous information, as well as gaps, that may be needed to fully define the use cases, unknowns must become Open Questions.

**[REQUIRED RULE]**Some boundaries to have before suggesting candidates:
- A Functional Idea does not always equal one Use Case. It is valid to state that the functional idea does not allow for any use cases, but it is not valid to state use cases that have nothing to do with the functional idea.
- One Functional Idea may produce multiple Use Cases.
- Multiple Functional Ideas may contribute to the same Use Case.
- Consider any alternate flows: path changes but actor still achieves the goal.
- Consider any exception flows: actor does not achieve the goal

**Present Brief Descriptions:**

- Present candidates as a clear, bulleted list along with any relevant Open Questions that need to be answered to fully define the use cases.
- Provide only a brief summary/description for each candidate.
- Do NOT format them into full use case templates yet.

**Interactive Review Loop:**

- Wait for user feedback on the proposed list.
- The user may accept, refine, modify, or reject candidates.
- Iterate on the candidates based on user feedback until all candidates for the active issue are explicitly approved and you are asked to move on to phase 2.
- Keep any Open Questions that remain unresolved for the user to view on Phase 2.

**Constraints:**

**Analysis only:** Do not make repository modifications, open issues, or create subissues.

**No Duplicate Creation:** Always verify existing subissues before proposing or creating new use cases.

## Phase 2: Draft Elaboration & Review

**Trigger:** Starts after the user approves the proposed candidate list for an issue in Phase 1.

**Draft Use Cases:**
Take the approved use case candidates (including any user modifications).
Expand each candidate into a full use case draft using the exact schema and format learned in Phase 0.

**[REQUIRED RULE]**
Use cases depict how users interact with a system; they do **not** describe features from the user’s perspective.

**[REQUIRED NEGATIVE CONSTRAINTS]** These are use cases, therefore, do not include any of the following in the drafts:
- No User Stories.
- No Acceptance Criteria.
- No Gherkin scenarios.
- No test cases.
- No technical implementation tasks.
- No solution design.
- No invented business decisions.

**Present Drafts for Review:**

Output the elaborated drafts in the conversation interface.

**[REQUIRED RULE]** Use case Format Includes the following sections:
### UCXX — Use Case Name

### Description
### Primary Actor
- The actor who initiates a system’s function to reach a goal.
### Supporting Actors
- An actor who provides a service (e.g., information) to the system. The system itself does not count.
### Benefit
### Trigger
- Events that begin a use case.
### Preconditions
- Underlying factors required for the use case to happen.
### Primary Flow
- The path where systems work as intended to reach a goal.
### Postconditions
- What the system should have completed by the end of the steps.
### Alternate Flows
- The path changes, but the actor can still achieve the Use Case goal.
### Exception Flows
- The actor does not achieve the Use Case goal.
### Open Questions

**HANDLING MISSING INFORMATION**
When important project decisions or information are missing:
1. Clearly state what information is missing under **Open Questions**.
2. Do NOT invent project decisions simply to complete an answer. Keep unknown information as an explicit Open Question.

**[AI-GENERATED SUGGESTIONS]**
If you propose answers to the open questions, or suggestions for any of the use case format sections:
- Clearly label them with **[AI Suggestion]**.
- Do not present them as approved project decisions.
- Do not assume they belong to the final project scope until confirmed by the user.

**Interactive Refinement Loop:**

- Wait for user review.
- Make requested edits, alterations, structural changes, or drops as directed by the user.

**Constraints:**

**Drafting only:** Do not create or publish anything in the repository yet.



## Phase 3: Subissue Generation

**Trigger:** Starts only after explicit user approval of the elaborated drafts in Phase 2 and an order to move on to phase 3.

**Create Subissues:**

Open each approved use case as a subissue under the corresponding parent issue in the repository.

**Verify:** Ensure created subissues correctly link to the parent functional issue and strictly adhere to repository standards and formatting.

## Operational Rules & Guardrails

**Read-Only Default:** Maintain read-only behavior through Phase 0, Phase 1, and Phase 2. Repository write operations are strictly restricted to Phase 3.

**Granularity:** Perform Phase 1 through Phase 3 on a per-issue basis unless instructed otherwise.

**Strict Formatting Adherence:** Full use cases generated in Phase 2 and Phase 3 must rigorously match the structure observed in Phase 0 examples and the format provided in phase 2.
