## <img src="https://user-images.githubusercontent.com/70295997/205208100-c24089a2-6c0c-4ab2-8dd0-e75ceaff9be6.png" width=50/> git, GitHub, Version Control

______

### <img src="https://user-images.githubusercontent.com/70295997/204166483-b49b4645-9088-481c-bea2-a8dab2224150.png" width=30/> Common Git Commands (for newly created repositories)

 - git init

 - echo "# repo_name" >> README.md

 - git add .

 - git commit -m "initial commit"

 - git branch -M master main

 - git status

 - git remote add origin https://github.com/user-name/repo_name.git

 - git push origin main
----------

### What is Version Control / Revision Control / Source Control?

- management of changes made to documents
- is not limited to tracking changes or versions, it can contain a bunch of information about who made those changes, often called *blame* (can blame bugs on someone)
- may contain information about when the change was made and what the actual changes were, down to every single line in a particular document

### Why is Version Control So Important?

1. keeping track of changes
2. ability to go back to a previous working version
3. easily adding someone's work

### Where Can I Use Git Version Control?

- with any code file - JS, CSS, Java, Python, etc.
- any document, like a PDF file
- no limit on what I can track with Git - any type of file

### Why to Use Version Control? How Do Dev Teams Use Version Control?
![image](https://user-images.githubusercontent.com/70295997/204178393-db4ac551-50f4-4a76-bf45-c977013b6fca.png)

### <img src="https://user-images.githubusercontent.com/70295997/204179445-ac89703e-0502-405b-8629-e602cb6769c2.png" width=30/>Always Have a _Working Version_ of the Project!

The reason why a good branch structure is so important is because it enables me to have a working version of my project. It should not matter if I have just implemented a new feature and may have broken some things, because always somewhere I have a working version of my project. Eg., I deploy to my users and go back to my working version to continue working from there.

### How to Add New Code?

<img src="https://user-images.githubusercontent.com/70295997/204187411-a1e126b3-3515-4ebe-8b58-7331523499d1.png" width=900/>

Essentially, I have a __master__ branch, which is created by default when I initialize my Git repository. It's the __master__ branch where I keep my _working version_. I rarely make any commits into this __master__ branch.

Instead, I have a __test__ branch. It is this branch, from which I send commits to the __master__, but only after I have tested that new version. In the __test__ branch I must be entirely sure that this version is working, then I send it to the __master__.

Even before the __test__ branc, I have the __dev__ branch where I make most of the direct commits. I can create a new feature and add it inside of the __dev__ branch. Eventually, when it's ready tho be tested, I send it to the __test__ branch.

The QA/SDET team uses this __test__ branch to test the feature. Once testers make sure that it works, they send it to the __master__.

This is an ideal main structure of my branches.

The __dev__ branch is where most of the interesting things happen, where I add new features.

<img src="https://user-images.githubusercontent.com/70295997/204190181-33050aa3-f78f-438d-b804-7bafcfc8630a.png" width=700/>

It may not be the case that I add those features directly to the __dev__ branch. But I may also create branches that eventually merge into the __dev__ branch (eg., feature-1, feature-2, etc.).
In some scenarios, this may happen in the __test__ branch instead, although it's less commmon. Eg., to quickly fix a bug or add a feature, after I've already merged from the __dev__ branch to the __test__ branch.
A more common scenario is when I merge directly from the __dev__ branch into the __test__ branch, once I have added some features to the __dev__ branch and ready for them to be tested.

### What's the Difference between git and GitHub?

__git__ is a local VCS software that enables developers to save snapshots of their projects over time. It’s generally best for individual use. 

__GitHub__ is a web-based platform that incorporates git’s version control features so they can be used collaboratively.

----------

🔗[Difference Between Git and GitHub](https://www.geeksforgeeks.org/difference-between-git-and-github/)

🔗[Git vs Github: What’s the Difference and How to Get Started with Both](https://kinsta.com/knowledgebase/git-vs-github/)

🔗[Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)

🔗[Git Commands from Atlassian](https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html)

🔗[Git Commands Explained with Cats](https://girliemac.com/blog/2017/12/26/git-purr/)

🔗[Git Merge vs Rebase](https://medium.com/nerd-for-tech/git-merge-vs-rebase)

🔗[How To Structure Your Git Branching Strategy — By A Data Engineer](https://towardsdatascience.com/how-to-structure-your-git-branching-strategy-by-a-data-engineer-45ff96857bb)

🔗[Git Undo Merge – How to Revert the Last Merge Commit in Git](https://www.freecodecamp.org/news/git-undo-merge-how-to-revert-the-last-merge-commit-in-git/)

🔗[Git diff Command – How to Compare Changes in Your Code](https://www.freecodecamp.org/news/git-diff-command/)

🔗[How to Undo Pushed Commits with Git](https://dev.to/github/how-to-undo-pushed-commits-with-git-2pe6)

🔗[How Do I Resolve Merge Conflicts?](https://dev.to/github/how-do-i-resolve-merge-conflicts-5438)
