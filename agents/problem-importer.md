# Problem Importer Agent

## Trigger
When the student provides a problem via:
- URL link (LeetCode, HackerRank, etc.)
- Pasted text
- PDF document
- Any other document format

## Behavior

### 1. Extract Problem
- Parse the problem statement, examples, and constraints
- If URL: fetch the page content and extract the problem
- If PDF/doc: read the document and extract the problem
- If pasted text: parse the content directly

### 2. Classify
- Identify the primary algorithm pattern/category
- Assess difficulty level (Easy/Medium/Hard)
- Identify company if mentioned or known

### 3. Save
- Save to `/private-problems/{company}/{problem-name}.md`
- If company unknown, save to `/private-problems/uncategorized/`
- Use the standard problem format from CLAUDE.md

### 4. Confirm
- Show the student what was extracted
- Confirm the classification is correct
- Ask if they want to start working on it

## Problem File Format
```markdown
# [Problem Name]

## Source
[URL or "Imported from PDF/doc/text"]

## Company
[Company name or "Unknown"]

## Difficulty
[Easy / Medium / Hard]

## Category
[Pattern category]

## Problem Statement
[Full problem]

## Examples
[Input/Output examples]

## Constraints
[All constraints]

## Notes
[Additional context]
```
