# Git 

1. **Initialize a Git Repository**  
   ```bash
   git init
   ```
   Use this command to start a new Git repository in your project folder. It creates a `.git` folder to keep track of changes.

2. **Check Repository Status**  
   ```bash
   git status
   ```
   This command shows the status of your working directory and staging area, including untracked and modified files.

3. **Add Files to Staging Area**  
   ```bash
   git add <file_name>   # Add a specific file
   git add .             # Add all files in the directory
   ```
   Staging files lets Git know which changes you want to include in your next commit.

4. **Commit Changes**  
   ```bash
   git commit -m "Your commit message"
   ```
   This saves your staged changes to the repository with a message describing what changes were made.

5. **Push Changes to Remote Repository**  
   ```bash
   git push origin main  # Push to the main branch
   ```
   Pushing updates the remote repository with your local changes. Replace `main` with the branch name you’re working on if it’s different.

6. **Pull Updates from Remote Repository**  
   ```bash
   git pull origin main  # Pull updates from the main branch
   ```
   This fetches and merges updates from the remote repository to keep your local branch in sync.

7. **Create a New Branch**  
   ```bash
   git branch new-branch-name
   ```
   Creating branches lets you work on new features or data analysis experiments without affecting the main codebase.

8. **Switch to a Branch**  
   ```bash
   git checkout new-branch-name
   ```
   Use this command to switch to a different branch.

9. **Merge Changes from Another Branch**  
   ```bash
   git checkout main              # Switch to main branch
   git merge new-branch-name      # Merge new-branch-name into main
   ```
   Merging combines changes from different branches.

10. **Clone a Remote Repository**  
    ```bash
    git clone <repository-url>
    ```
    This command copies a remote repository to your local machine, ideal for starting a project from an existing Git repository.
