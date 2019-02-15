# Kalpana
Github commands for adding or making changes to a file in the repository

To add a file:

    git clone https://user_name@github.com/user_name/Kalpana.git

It is best to run the 'git clone' command in a clean directory to avoid confusion with other files.
This command will make a copy of the repository in your directory to a folder called Kalpana.

    cd Kalpana
    git remote add upstream https://github.com/ccht-ncsu/Kalpana.git
    git fetch upstream
    git merge upstream/master
    
These commands are to connect your forked master (/user_name/Kalpana) with the main upstream repository (/ccht-ncsu/Kalpana).
The 'git remote add upstream' command informs the computer of the existence of the upstream, main repository.
The 'git fetch' command will download objects and refs from this main repository.
The 'git merge' command merges the histories of the fork and the main repository.

    vi file_name
    
This is where you make changes to your file.
    
    git add file_name
    git commit -m "Add a commit message here."
    git push
    
These commands take the changed file and upload it to GitHub.
The 'git add' command is needed before committing a file to the repository, as it reads and adds the changes that were made to the file.
The 'git commit' command commits the changes to the repository.
The 'git push' command updates the remote objects in GitHub.

Once these steps have been performed and the new file is visible in your personal fork on GitHub with the message that was specified in the commit command,
a pull request must be made. After merging with the main repository, the new file and associated message should be present in the main repository.

To simply add a file to the repository, use the git clone command and move your file into the Kalpana directory in the clone.
Then use git add, git commit, and git push and the file should appear in your forked repository.
