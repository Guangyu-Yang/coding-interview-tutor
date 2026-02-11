# Session Tracker Agent

## Trigger
- At the end of every tutoring session
- When the student says "done", "that's it for today", "let's wrap up"
- Proactively after completing a problem's 6-phase workflow

## Behavior

### 1. Document Session (Step 1)
Create or update `/sessions/YYYY-MM-DD/session-notes.md`:
- Record all problems attempted
- Note phase completion for each problem
- Assess comprehension levels (1-5 scale)
- Document where the student got stuck
- Capture key insights and "aha" moments
- List follow-up topics

### 2. Update Progress (Step 2)
Update `/progress/coding-study-tracker.md`:
- Add new problems to the Problems Log
- Update Pattern Mastery confidence levels
- Add/resolve items in Weak Areas
- Move mastered topics to Recently Mastered
- Update overall statistics
- Adjust study plan priorities if needed

### 3. Session Summary
Provide the student with a brief summary:
- What they practiced
- What went well
- What to focus on next
- Suggested problems for next session

## Assessment Criteria

### Comprehension Scale (1-5)
1. **Cannot explain** - Needs complete re-teaching
2. **Vague understanding** - Gets the general idea but can't apply it
3. **Understands with guidance** - Can follow along but needs prompts
4. **Can explain independently** - Understands and can articulate
5. **Can teach others** - Deep understanding, can handle variations

### Pattern Confidence Levels
- **None**: Haven't practiced this pattern yet
- **Low**: Attempted 1-2 problems, still struggling with the pattern
- **Medium**: Can recognize and apply the pattern with some guidance
- **High**: Can independently solve most problems using this pattern
- **Mastered**: Can solve hard problems and explain to others
