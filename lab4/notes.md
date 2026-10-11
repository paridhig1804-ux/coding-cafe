1. The --global flag saves the username and email settings across the entire user account meaning every Git project I make from then on will automatically know who I am. If I left it out, Git would only apply those details to the specific folder I am currently working in, and any new projects I start later would throw an error asking me to identify yourself.
2. The hidden .git folder showed up because files and folders starting with a dot are hidden by default in Linux. Inside it are all the behind-the-scenes tracking files, configuration settings, and history logs that Git uses to manage the project's version control.
3. Git offers to track thousands of files, mostly tucked away inside the .venv/ and __pychache__/ directories. None of those files were written by me, they are pre-packaged python libraries, virtual environment dependencies, and compiled bytecode generated automatically by your system.
4. The entire .venv/ folder and all the thousands of supporting dependency files completely vanished from the untracked files list because .gitignore told Git to look away from them.
5. .gitignore definitely needs to be committed to the repository. Since everyone collaborating on the project needs to follow the exact same rules about what files to leave out, that configuration file has to be tracked and shared.
6. It shifted from Untracked files over to changes to be committed. In terms of Git's three-places model, it moved out of the working directory and into the staging area getting it ready to be saved permanently.
7. It shifted from Untracked files to Changes to be committed. In terms of Git's three-places model, it moved out of your working directory and into the staging area getting it ready to be saved permanently.
8. They are called the short commit hash, which acts as a convenient, unique ID tag to pinpoint and reference that specific snapshot of the project's history without needing to type out the full 40-character code.
9. Inow have two commits. 

 Make or edit files in the working folder.

 Check the project state using git status.

 Stage the modifications using git add.

 Save the snapshot permanently using git commit.

10.  Platforms like GitHub specifically look for a README.md file to automatically render as the front landing page of the repository, giving visitors an immediate overview of what the project is about.
11. It securely authenticated the terminal with GitHub using a token stored on the machine, acting as a trusted credential helper so Git can communicate with the remote server safely without prompting for a password every time.
12. The beautifully formatted content of the README.md file appears right on the main page because GitHub is designed to automatically detect and display it as the welcoming project description.
13. No, pushing didn't change anything about the local timeline. It simply uploaded a mirrored copy of the existing commits up to the remote server on GitHub.
14. A private repository lives safely in the cloud with its full history intact, but access is locked down strictly to me and whoever you choose to invite. If a repository doesn't exist on GitHub at all, there is no online backup anywhere the code lives entirely on the personal machine and is completely invisible to anyone else.