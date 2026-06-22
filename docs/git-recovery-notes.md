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

Added note to git-recovery-notes.md.

### Repository state

modified: git-recovery-notes.md
File staged and commited with poor commit message.

### What I wanted to preserve

I need to fix the commit message for git-recovery-notes.md commit.

### What I wanted to undo

Change the commit to a better commit message.

### Command or method used

git commit --amend -m "docs: add Git recovery rule.

### Why it was appropriate

It fixed the poor commit message with one that explains the file change better.

### Result

Commit has a better descriptive message.

---

## Scenario D: Undo local commit while preserving the work

### What I changed

Added temporary code to index.html, and staged and committed the file.

### Repository state

index.html was committed properly

### What I wanted to preserve

Undo commit without losing the changes in index.html

### What I wanted to undo

Undo the index.html file commit.

### Command or method used

git reset --soft HEAD~1

### Why it was appropriate

It removed the commit without changing the index.html file changes.

### Result

Commit was removed from the commit list.

---

## Scenario E: Correct a pushed mistake safely

### What I changed

Added incorrect information in README.md and pushed to repository

### Repository state

file was pushed properly.

### What I wanted to preserve

Keep the incorrect commit message and fix and push the corrected version

### What I wanted to undo

Add the correct information to README.md and push the corrected version to the repository, without removing the incorrect version.

### Command or method used

git revert COMMIT_ID

### Why it was appropriate

I was able to add the updated commit without removing the incorrect version.

### Result
