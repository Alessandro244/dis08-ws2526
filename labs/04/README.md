# Version Control Software

Version control systems such as Git are essential tools for collaborative software development and project management. They allow developers to track changes, experiment with new features through branching, and merge contributions from multiple team members. This assignment provides hands-on practice with Git and GitHub, focusing on fundamental operations like creating commits, branching, merging, and resolving conflicts. Additionally, it reinforces the use of the command line by working with files, writing simple scripts, and managing repository contents effectively. By completing these tasks, you will gain practical experience in both individual and collaborative version control workflows.

Getting started with branching and merging, making a first commit
Please visit git visualization tool. Create at least 5 commits, branches and tags there and watch the graph grow. To get started, you could try to simulate a fast-forward merge and a three-way merge that we discussed in the lecture. Hint: You can find all available commands of the web app documented in this repository.
Make a screenshot of your work when you’re finished. Give the screenshot a reasonable filename, for example git-graph.png.
Clone your own (this) repository into your local file system.
Save the screenshot on your machine to this working directory.
On the command line:
navigate to the repository
check your git status
add the new file to git
and commit the change.
Finally, push your changes to the remote repository.
Visit your repository on GitHub to verify that your new file is present.
Committing your progress step-by-step
Download the following file https://librarycarpentry.org/lc-shell/data/shell-lesson.zip

wget https://librarycarpentry.org/lc-shell/data/shell-lesson.zip
Unzip it

unzip shell-lesson
Make sure not to commit these files to the repository. Note: You can also add a .gitignore file and add the folder and file paths there.

In the following, create a bash script called get_info.sh with the commands to get the desired answers to the tasks below. After successfully completing a single task, i.e., writing the correct command, stage the changes,write a reasonable commit message and commit your changes, and push them to the repository. Try to include branches and solve merge conflicts if they should occur. tl;dr Implement the first task, commit changes, implement the second task, commit changes, and so on ...

Note: The objective of this assignment is getting familiar with the use of Git and GitHub, and also to get more experience with the command line interface in general. Some topics and contents of last week's lecture.

How do you get the first three lines of the file 2014-01_JA.tsv?
How do you get the total number of lines in each of the *.tsvfiles?
How do you get the file with the highest number of lines and how many does it have? Can you get the output with a single command line call?
Branching and resolving merge conflicts
The following task helps to get a deeper understanding of branches and how merge conflicts can occur. Please follow the outlined steps.

Create a new branch called feature-bio.
In this branch, add a file called bio.md with a short biography (3–5 sentence, if you do not want to share personal information, you can write a fictional bio).
Make at least two separate commits (e.g., first draft, then an update).
Merge the branch back into main.
Create another branch called feature-facts.
Add a file facts.md with three interesting facts (could be about technology, history, or yourself).
Before merging, simulate a merge conflict:
Edit bio.md on both main and feature-facts in different ways.
Try merging and resolve the conflict.
Document in a file conflict-resolution.md what happened and how you solved it.
Important

By the end of this assignment, you should submit the following items in your GitHub repository:

Git Graph Screenshot (git-graph.png) – A screenshot showing at least 5 commits, branches, and tags created using the Git visualization tool.
Bash Script (get_info.sh) – A script with commands solving the three data-processing tasks:
A bio.md file created and updated on the feature-bio branch, merged back into main.
A facts.md file created on the feature-facts branch.
Conflict Resolution Documentation (conflict-resolution.md) with a short explanation of the merge conflict encountered, involving bio.md, how it was resolved, and the final outcome.
