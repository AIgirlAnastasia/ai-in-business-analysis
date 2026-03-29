# Call Analysis Skill

Read all meeting transcripts in the `calls/` folder and produce a structured report.

## Instructions

Look in the `calls/` folder. Read every `.md` file you find there.

For each transcript, extract:

**Decisions made**
- What was decided
- Who proposed it
- Context

**Open questions**
- What is still unresolved
- Who raised it
- Why it matters

**Problems identified**
- What the problem is
- Who is affected
- Estimated impact or cost

**Action items**
- Task description
- Owner
- Deadline (if mentioned)

## Output format

Save the full report to `report.md` in the project root.

Structure it like this:

```
# Meeting Analysis Report
Generated: [date]
Transcripts analyzed: [count]

## Key Decisions
[list]

## Open Questions
[list]

## Problems Identified
[list]

## Action Items
[list with owner and deadline]

## Patterns across calls
[if multiple transcripts: what themes repeat across meetings?]
```

If there is only one transcript, skip the "Patterns" section.

Tell me when the report is saved and give a one-line summary of the most important finding.
