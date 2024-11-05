# Reverting Changes in Git

This document outlines the steps taken to revert changes introduced by the `mfa_feature` branch in the `main` branch of a Git repository.

## Prerequisites

- Ensure you have Git installed on your machine.
- You should have access to the repository where the changes need to be reverted.

## Steps to Revert Changes

### 1. Checkout the Main Branch

Switch to the `main` branch to prepare for the revert operation.

```bash
git checkout main
```
### 2. Fetch the latest changes from the remote repository and merge them into your local main branch.

```bash
git fetch origin
git merge origin/main
```
#### 3. Revert the Merge Commit
Identify the merge commit that introduced the changes from the mfa_feature branch. In this case, the commit hash is e714a71. Use the following command to revert the merge commit:

```bash
git revert -m 1 e714a71
```
The -m 1 option specifies that you want to keep the first parent of the merge commit.

### 4. Resolve Any Conflicts (if necessary)
If there are any conflicts during the revert, Git will notify you. You will need to resolve these conflicts manually. After resolving conflicts, stage the changes:

bash
Insert Code
Edit
Copy code
git add <file_with_conflicts>
git revert --continue
5. Push the Changes to Remote
Once the revert is complete, push the changes to the remote main branch:

bash
Insert Code
Edit
Copy code
git push origin main
Verification
After performing the revert, you can verify the success of the operation using the following commands:

Check the Commit History
View the commit history to ensure that a new revert commit has been created:

```bash
git log --oneline

```
Check the Content of main.txt
Verify that the content of main.txt reflects the expected state after the revert:
```bash
cat main.txt
```