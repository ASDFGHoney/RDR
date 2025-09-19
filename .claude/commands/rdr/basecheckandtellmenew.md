# MyBase Update Workflow Prompt
Please execute the MyBase update workflow below from Step 1 to Step 3 in order.
Check the changes in the personal branch, update MyBase/summary/, and
analyze reflection feasibility to provide specific reflection questions.

## Step-by-Step Process

### Step 1: Identify Newly Added Files
```
Check changes in the personal branch to identify newly added files in MyBase.

Execute the following commands for verification:
- git log --oneline -10 (check recent 10 commits)
- git diff --name-only HEAD~5..HEAD (file names changed in recent 5 commits)
- ls -la MyBase/ (check MyBase folder contents)

Please organize a list of newly added files and their types (team chats, presentations, code, etc.).
```

### Step 2: Update MyBase/summary/
```
Based on the identified new files, add content to appropriate summary files in the MyBase/summary/ folder.

Process:
1. Classify activity type of each new file (e.g., team meeting, project presentation, code review, etc.)
2. Check corresponding [activity-name]-summary.md file (create if it doesn't exist)
3. Add summary of new files with **factual information only**
   - Date, participants, main agenda, deliverables, etc.
   - Exclude personal emotions or interpretations

Important notes:
- Never fabricate content
- Write based only on actual file contents
- Maintain neutral and objective tone
```

### Step 3: Reflection Feasibility Analysis and Question Generation
```
Based on the added content, analyze whether immediate reflection is possible and generate specific reflection questions.

Analysis criteria:
- Is it a completed activity? (postpone reflection for ongoing projects)
- Are there meaningful learning or growth elements?
- Is there sufficient information to reflect on personal experiences and emotions?

Example reflection questions:
1. What did you learn most from this experience?
2. What part was most challenging?
3. How would you do things differently if a similar situation arose?
4. How did this experience contribute to your professional development?
5. Were there any impressive moments during collaboration?

Processing based on results:
- Immediate reflection possible: "Ready to create a new reflection file in the reflections/ folder"
- Reflection postponed: Check and update reflections/postponed-projects.md file
  1. Review status of existing postponed items
  2. Add new postponed items (including postponement reason, current status, expected completion date, planned reflection date)
  3. Check next review date according to periodic review schedule
```

## Full Workflow Execution Command

When executing this prompt in Claude Code, request as follows:

```
Please execute the MyBase update workflow above from Step 1 to Step 3 in order.
Check the changes in the personal branch, update MyBase/summary/, and
analyze reflection feasibility to provide specific reflection questions.
```