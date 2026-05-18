# Legacy Project Generation Prompt

## Project identity
- Name: {project-name}
- Domain: {domain}
- Stack: {language} / {frameworks}
- Complexity level: junior / mid / senior

## Business context
{Describe the company, the product, the team situation.
Be realistic. Include pressure, history, constraints.}

## Technical starting point
{Describe the state of the codebase.
What exists, what is broken, what is undocumented.
What debt was accumulated and why.}

## Known technical debt to embed
- {debt item 1}
- {debt item 2}
- {debt item 3}

## What the code must contain
- {feature 1}
- {feature 2}
- {feature 3}

## What the code must NOT contain (intentional gaps)
- {missing feature 1 → user story 1}
- {missing feature 2 → user story 2}

## Constraints
- {naming conventions, package structure, style}
- {what to avoid}

---

# Markdown files to generate

## README.md
- Business context
- Stack and dependencies
- How to run locally
- Known limitations

## docs/ARCHITECTURE.md
- Initial architecture overview
- Why these choices were made (simulated history)
- Known debt and why it exists
- What should be improved and in what order

## docs/BACKLOG.md
- 8 to 12 progressive user stories
- Format: As a / I want / So that
- Acceptance criteria for each
- Difficulty label: starter / intermediate / advanced

## docs/LEARNING_GUIDE.md
- Step by step training path for this project
- What to read before starting
- What to audit first
- Key questions to answer before writing code

## docs/REASONING_FRAMEWORK.md
- 10 to 15 interview-style questions specific to this project
- Each question followed by: what a junior says / what a senior says

## docs/LEARNING_LOG.md
- Empty template
- Sections: date, user story worked on, decisions made, doubts, what I learned

---

# Generation instructions

Generate the full project in the following order:
1. Project structure (tree)
2. All source code files
3. README.md
4. docs/ARCHITECTURE.md
5. docs/BACKLOG.md
6. docs/LEARNING_GUIDE.md
7. docs/REASONING_FRAMEWORK.md
8. docs/LEARNING_LOG.md

For the source code:
- Write realistic code, not tutorial code
- Include comments that simulate a real team (some helpful, some outdated, some wrong)
- Include at least one non-obvious bug or design smell per layer
- Do not over-engineer. Match the complexity level specified above.
