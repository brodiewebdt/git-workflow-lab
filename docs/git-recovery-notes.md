# Git Recovery Practice

## Recovery rule

Always inspect the state of a change before choosing an undo command.

## Scenario A: Discard an unstaged change

### What I changed

I replaced the page heading with different content

### Repository state

modified: index.html
using git diff shows the page heading change.

### What I wanted to preserve

Return to the original page heading content.

### What I wanted to undo

Change the page heading back to the orginal content.

### Command or method used

I didn't need to run a command. I just changed the page heading back to the original content, and that cleared the issue.

### Why it was appropriate

The file wasn't staged, so no commands were necessary to clear the issue.

### Result

Page cleared of any git status issues.

---

## Scenario B: Unstage a file

### What I changed

I changed the README.md and css/styles.css files.

### Repository state

README.md and css/styles.css files showed as modified in Git status.
I used Git add to stage the two files.

### What I wanted to preserve

I wanted to remove css/styles.css from the staging area while staging the README.md file.

### What I wanted to undo

Remove the css/styles.css file from the staging area.

### Command or method used

git restore --staged css/styles.css.

### Why it was appropriate

The restore command removed the css/styles.css file from the staging area, and allowed me to commit the README.md file.

### Result

README.md file was committed and the css/styles.css file was removed from the staging area.

---

# Git Recovery Practice

## Scenario C: Correct most recent local commit

### What I changed

### Repository state

### What I wanted to preserve

### What I wanted to undo

### Command or method used

### Why it was appropriate

### Result

---

## Scenario D: Undo local commit while preserving the work

### What I changed

### Repository state

### What I wanted to preserve

### What I wanted to undo

### Command or method used

### Why it was appropriate

### Result

---

## Scenario E: Correct a pushed mistake safely

### What I changed

### Repository state

### What I wanted to preserve

### What I wanted to undo

### Command or method used

### Why it was appropriate

### Result
