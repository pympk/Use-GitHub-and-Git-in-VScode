# Use GitHub and Git in VScode

These are my notes while learning to use GitHub and Git in VScode.

References

- [Use Git version-control tools in Visual Studio Code](https://docs.microsoft.com/en-us/learn/modules/use-git-from-vs-code/)
- [Introduction to GitHub in Visual Studio Code](https://docs.microsoft.com/en-us/learn/modules/introduction-to-github-visual-studio-code/)
- [Get started using GitHub to manage Git repositories and collaborate with others](https://docs.github.com/en/get-started/quickstart)

Create a branch

- Select branch icon on the bottom ribbon, left
  > ![github_branch](images/vscode/github_branch.PNG)
- Type the new branch name into the dialog box
  > ![new_branch](images/vscode/new_branch.png)

Switch branch

- Select branch icon on the bottom ribbon, left
  > ![github_branch](images/vscode/github_branch.PNG)
- Select branch from the drop down list
  > ![switch_branch](images/vscode/switch_branch.png)

Delete a branch

- Switch to a branch that you want to keep
- Select Source Control Management (SCM) icon on the vertical ribbon, left
  > ![SCM](images/vscode/SCM.png)
- Select **ellipsis** on the top SCM ribbon
  > ![SCM_ribbon](images/vscode/SCM_ribbon.png)
- Select **Branch** on the drop down list
- Select **Delete Branch**
- Select the branch to delete

[Create a repository](https://docs.microsoft.com/en-us/learn/modules/introduction-to-github-visual-studio-code/5-exercise-publish)

- Create a folder on your machine (e.g. **mslearn-demo**)
- In Visual Studio Code, select the File menu, and then select **Open Folder**
- Select the **mslearn-demo** folder that you created
- Create **README.md**
- Create .env file type (e.g. **.env.development**) that's confidential and should not push (such as database connection strings) to GitHub.

[Publish repository to GitHub](https://docs.microsoft.com/en-us/learn/modules/introduction-to-github-visual-studio-code/5-exercise-publish)

- Open the Source Control Management (SCM) view by selecting the SCM icon on the activity bar
  > ![SCM](images/vscode/SCM.png)
- Select Publish to GitHub
  > ![publish_to_github](images/vscode/publish_to_github.png)
- Select **Publish to GitHub public repository**
- **Uncheck confidential files** that should not push to GitHub
- Open **.gitingore**, the confidential file (e.g. **.env.development**) is listed there.
- Add confidential file to **.gitingore** by preceding the filename with **"/"** (e.g. **/.env.development**)

Delete a repository

- Delete repository folder in Windows (need to provide administrator permission)
- Open the repository in GitHub
- Select **Settings**
  > ![Settings](images/GitHub/settings.png)
- Scroll down to **Danger Zone**
  > ![delete_repository](images/GitHub/delete_repository.png)
- Select **Delete this repository** and following the instruction

[Clone an existing repository](https://docs.microsoft.com/en-us/learn/modules/introduction-to-github-visual-studio-code/6-lesson-clone)

- Open a new window (Ctrl+Shift+N)
- Select **Explorer** (Ctrl+Shift+E)
- Select **Clone Repository**
  > ![clone_repository](images/vscode/clone_repository.png)
- Provide repository URL in dialog box
- Select repository location in Windows File Explorer

[Create a fork of an open-source project in GitHub](https://docs.microsoft.com/en-us/learn/modules/use-git-from-vs-code/3-exercise-clone-branch)

- Navigate to open-source project repository in GitHub
- Select **Fork** near the upper right of the webpage
  > ![fork](images/GitHub/fork.png)
