#### The Windows User's Walkthrough of GitHub

Github provides a lot of great support for Windows users that you might not be aware of, from GitHub Desktop and Git Shell to the VS Extension. If you've ever wanted to see the forest for the trees in getting started on GitHub or you're looking to grow beyond those 5 Git commands you use every day, or you're curious what some of the newest GitHub features are, swing by for a walkthrough of GitHub from the Windows user's perspective!

#### Poll
- New to git and github?
- Know the basics?
- Never have to delete the .git folder?

#### GitHub Cheatsheet
- https://education.github.com/git-cheat-sheet-education.pdf

#### GitHub Desktop
- https://desktop.github.com/
- For no other reasons: Install for authentication and .gitattribute files to handle file ending 

- DEMO
 - How to setup your preferred git shell 
 - How to setup your credentials and not pass in your email address

- DEMO

  1. Open Desktop - Changes tab
  2. Create a branch off of Master via UI
  3. Open in explorer - open Program.cs in notepad. Call it the "vi of windows"
  4. Switch to master
		
- Visualization DEMO (merge a branch into Master)
 - Create a new repo and add file1
 - Create branch1. On branch create file2
 - On Master create file3
 - Show merging updates from Master into branch1 - "to keep branch up-to-date to reduce merge conflicts"
 - Now merge branch1 into Master
	
- Staging by line DEMO
 - Add a couple of console.writelines and a console.read()
 - Similar to git add --patch and git add --interactive
		
#### Git Shell 
 - Stop using the command prompt, especially if you have 2FA (and you should)
 - DEMO
   - How to specify which shell

#### Visual Studio extension
 - Maintainer workflow scenarios 
 - DEMO
		- DemoApplication - updated program.cs with message
 - Mention Start Page roaming profile

#### Unity plugin

found at http://unity.github.com

#### GitHub Features I wished I had known about
 - Pull Requests are start of a conversation. You can still update the PR by updating the branch at any time.
 - Use '?' to see keyboard shortcuts
 - How to add a Readme and/or license
 - Gists https://gist.github.com/
	
#### GitHub Features
 - Pull request reviewers, requests, and filters - https://github.com/blog/2306-filter-pull-request-reviews-and-review-requests
   - DEMO 
     - Have drofaras leave a pull request
     - DemoApplication - Pull Request - Show the filter "awaiting reviews by you"
	   - Show how you can leave feedback in the review and inline
   - Search commit messages - https://github.com/blog/2299-search-commit-messages
     - How to search commits - https://help.github.com/articles/searching-commits/
   - DEMO 
     - Show the github extension "author:shana merge:true"
- Resolve merge conflicts 
  - Remember the only way to do merges is via a Pull Request
- GitHub Pages 
	- https://saraford.net/2017/02/18/how-to-use-git-io-to-shorten-github-urls-and-create-vanity-urls-049/

#### More git

- http://git-school.github.io/visualizing-git/
- http://ohshitgit.com/
- https://services.github.com/on-demand/git-trouble/
- https://services.github.com/on-demand/github-desktop/

- Demo the bash script from "git-trouble" - page 2
 - https://services.github.com/on-demand/git-trouble/git-set-up

- Demo "oh no! I accidentally committed on master instead of a branch"
 - Commit, commit, commit on master
 - Create a new branch but don't change to it
  - Git reset --hard HEAD~
  - Git checkout branch
	- Then demo on the visualizing-git

- Demo reflog and how if you accidentally did a git reset --hard and your files are gone. How to get them back
  - git reset --hard <file4 sha> - Oh nos!
  - git reflog
  - git reset --hard <file 6 sha>
  - Rinse and repeat using the visualizing-git

- Cherry-pick changes the commit id, but "git reset --hard <id>" keeps it
	
- The interactive rebase via cherry-pick (note: no interactive on the visualizing-git)
 - Git init
 - Create a readme
 - Git add .
 - Git commit -m "readme"
 - Use the bash script
 - Git reset --hard <readme> // on master
 - Git checkout -b some-branch
 - Git reflog //to get ids for the files
 - git cherry-pick <file4 sha>
 - git cherry-pick <file6 sha>
 - git cherry-pick <file5 sha>
 - git checkout master
 - git cherry-pick 1, 2, 3		
 - Git checkout some-branch
 - Git rebase -i master //note it's flipped unlike command line, so you want 4, 5, 6
 - Git checkout master
 - Git merge some-branch

I am a random edit :) 
