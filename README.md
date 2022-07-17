# Use GitHub and Git in VScode

These are my notes while learning to use GitHub and Git in VScode. I have copied some of the references and links verbatim to make it easier for me to read, and avoid switching between my notes and the webpages linked to the references.

### References

- [Use Git version-control tools in Visual Studio Code](https://docs.microsoft.com/en-us/learn/modules/use-git-from-vs-code/)
- [Introduction to GitHub in Visual Studio Code](https://docs.microsoft.com/en-us/learn/modules/introduction-to-github-visual-studio-code/)
- [Get started using GitHub to manage Git repositories and collaborate with others](https://docs.github.com/en/get-started/quickstart)
- [How to Rebase](https://gist.github.com/nnja/a1888523ec851c6b94b2647956d5c3b4)

### Making GitHub Contributions

The workflow for making contributions to other people's projects on GitHub requires that you create a fork. A fork is a copy of their GitHub repository in your GitHub account. When you create a fork, you have full permissions to push changes to it, even if you don't have those permissions in the original repository.

A cloned repository is an entire copy of a remote repository on your local machine. From this local copy, you will be able to create commits, branches, and synchronize those changes back to your remote repository.

You can submit your changes to the owner of the original repository by a pull request. After approving of your changes, the owner then merges your changes to the master branch.

### Create a Fork

Forking takes place entirely within the GitHub web interface.

- Login to your GitHub account
- Go to the repository that your want to fork
- Select Fork near the upper right of the webpage
  > ![fork](images/GitHub/fork.png)

### Create a Clone

You want to clone from your own fork. This will configure Git on your computer to push your changes to the fork, where you have permissions to do so.

- Open Command Palette (Ctrl+Shift+P)
- In the Search box, enter **clone**
- Select **Git: Clone**
- At the prompt, enter the URL of the repository
- Select repository location in Windows File Explorer

### Create a Branch

A branch is a pointer to a specific commit. A commit has a parent, and is the parent of subsequent commits.

- Select branch icon on the bottom ribbon, left
  > ![github_branch](images/vscode/github_branch.PNG)
- In the Dialog box, enter the new branch name
  > ![new_branch](images/vscode/new_branch.png)

### Switch Branches

- Select branch icon on the bottom ribbon, left
  > ![github_branch](images/vscode/github_branch.PNG)
- Select branch from the drop down list
  > ![switch_branch](images/vscode/switch_branch.png)

### Delete a Branch

- Switch to a branch that you want to keep
- Select Source Control Management (SCM) icon on the vertical ribbon, left
  > ![SCM](images/vscode/SCM.png)
- Select **ellipsis** on the top SCM ribbon
  > ![SCM_ribbon_ellipsis](images/vscode/SCM_ribbon_ellipsis.png)
- Select **Branch** on the drop down list
- Select **Delete Branch**
- Select the branch to delete

### [Create a Local Repository](https://docs.microsoft.com/en-us/learn/modules/introduction-to-github-visual-studio-code/5-exercise-publish)

- Create a folder on your machine (e.g. demo)
- In Visual Studio Code, select the File menu, and then select **Open Folder**
- Select the folder that you created (e.g. demo)
- Create file README.md
- Create a confidential file that should not be push (such as database connection strings) to GitHub

### [Publish Local Repository to GitHub](https://docs.microsoft.com/en-us/learn/modules/introduction-to-github-visual-studio-code/5-exercise-publish)

- Open the Source Control Management (SCM) view by selecting the SCM icon on the activity bar
  > ![SCM](images/vscode/SCM.png)
- Select Publish to GitHub
  > ![publish_to_github](images/vscode/publish_to_github.png)
- Select **Publish to GitHub public repository**
- **Uncheck confidential files** that should not push to GitHub
- Open **.gitignore**, the confidential file should be listed there
- Add confidential file to **.gitignore** (e.g. /password)

### Delete a Repository

- Delete repository folder in Windows (need to provide administrator permission)
- Open the repository in GitHub
- Select **Settings**
  > ![Settings](images/GitHub/settings.png)
- Scroll down to **Danger Zone**
  > ![delete_repository](images/GitHub/delete_repository.png)
- Select **Delete this repository** and following the instruction

### View Staged and Unstaged Changes

- Select Source Control Management (SCM) icon, shown with pending changes, on the left vertical ribbon

  > ![SCM_pending_changes](images/vscode/SCM_pending_changes.png)

- Under **Changes** are files with unstaged changes. To the right of the file name are four icons:

  - File icon: Select to open and display the file in the main editor pane
  - Counterclockwise arrow icon: Select to discard changes and revert the file to its state in the previous commit
  - Plus sign (+) icon: Select to stage your changes to be committed
  - "M" or "U" icon:

    - "M" Indicates that this file existed previously and has been modified
    - "U" Indicates that this file is untracked
    - "D" Indicates that this file has been deleted

- Under **Staged Changes**, to the right of the file name are **"M"** or **"A"**:
  - "M" Indicates that this file existed previously and has been modified
  - "A" Indicates that this file is added

### Stage and Unstaged Changed File

- [View staged and unstaged changes](#view-staged-and-unstaged-changes)
- Staged changes
  - Select the plus sign (+) to move the file to a new section titled **Staged Changes**
- Unstaged changes
  - Select the minus sign (-) to move the file to a new section titled **Changes**

### [Commit Choices](https://stackoverflow.com/questions/30038999/differences-between-commit-commit-and-push-commit-and-sync)

- To see the commit choices, select Commit drop down

  > ![commit_choices](images/vscode/commit_choices.png)

  - Commit makes a record of your changes on your local machine. It will not mark the change in the remote repository.
  - Commit and Push do the above and push it to the remote repository. The changes are saved to the remote repository.
  - Commit and Sync do three things. First, it commits the change. Second, it performs a pull (grabs the updated information from the remote repository). Finally, it pushes the changes to the remote repository.

### [Create a Commit](https://docs.microsoft.com/en-us/learn/modules/use-git-from-vs-code/5-exercise-stage-commit)

- Select Source Control Management (SCM) icon, shown with pending changes, on the left vertical ribbon

  > ![SCM_pending_changes](images/vscode/SCM_pending_changes.png)

- Add a commit message in the text box below the checkmark icon

- To complete the commit, select Enter or select the checkmark icon

### Synchronize Changes

Synchronize changes in the current branch in your machine and the upstream branch in GitHub.

- Select Synchronize Changes (two clockwise arrows) icon in the Status Bar
  > ![sync_status_bar](images/vscode/sync_status_bar.png)
  > The Status Bar indicates Synchronize Changes will pull 2 and push 1 commits to remote repository

### GitHub Pull Request

[A pull request in GitHub is a request to the maintainer of a repository to pull in some code.](https://www.dummies.com/article/technology/programming-web-design/general-programming-web-design/what-are-github-pull-requests-264741/)
Code changes in the **MERGE CHANGE FROM** branch will merge into the **INTO** branch. The result is both branches in your GitHub repository will be the same after the Pull.

- [Switch to master branch](#Switch-among-branches)
- Open Source Control (Ctrl+Shift+G)
- Select Create Pull Request icon

  > ![create_pull_request](images/vscode/create_pull_request.jpg)

- GitHub Pull Request Panel opens
  > ![create_pull_request_panel](images/vscode/create_pull_request_panel.png)
- URL for the remote repository is displayed on the top rows of the MERGE CHANGES FROM box and the INTO box
- Select a branch to MERGE CHANGES FROM in the drop down list
- Select a branch to merge INTO in the drop down list
- Add Pull Request Description
- Select **Create**
- Pull Request opens
  > ![merge_pull_request](images/vscode/merge_pull_request.png)
- Select **Merge Pull Request**
- Select **Create Merge Commit**

### Merge Local Branches

Merge local branches is similar to [GitHub Pull Request](#github-pull-request), except the merge is done on branches in the local repository, whereas with GitHub Pull Request, the merged done on branches in the GitHub repository.

- Open Command Palette (Ctrl+Shift+P)
- Type: **Git: Merge Branch**
- Select a branch to merge from in the list

- [Dominant branch when doing a merge](https://stackoverflow.com/questions/42099431/what-is-the-dominant-branch-when-doing-a-git-merge/42104116#42104116)

  - Note:

    - **we** is the current branch, also refer to as: HEAD, Current Change
    - **they** is the branch to merge from, also refer to as: incoming branch, Incoming Change
    - **change** not only applies to line number in a file, it also applies to filename

  - If we changed line 1 and they didn't, the merge result is our version.

  - If we didn't change line 1, and they did, the merge result is their version.

  - If we both changed line 1, the merge result is that the merge fails, with a merge conflict. Git writes both lines into the file and stops the merge with an error, and makes us clean up the mess:
    > ![merge_conflict](images/vscode/merge_conflict.png)
    - To abort the merge, from terminal:
      - git merge --abort

- Merge **deletes files** in current branch if the file is deleted in the merge from branch
- Merge ignores uncommitted changes
