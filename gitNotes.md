### Git Notes

* `git config` - configure git
* `git init` - initialize git repository
* `git status` - check the status of the repository
* `git add` - Track files
* `git commit` - commit tracked files
* `git push` - upload files
* `git pull` - download files
* `git config --list` - shows email and name
*** 

##### Configure your global git account

`git config --global user.name "Jake Ryan"
git config --global user.email jake.eric.ryan@gmail.com`

***

`git init` to create a .git file.  do this inside your project

`git remote add origin https://github.com/jake-ryan0/SoMe_PrOjEcT` this will connect it to the online repo.  ***if you pull from another repo, that will be origin.  try `git remote add github https://github.com/Jake-ryan0/bootstrap_blog.git` ***

`git status` will show branch, commit, and untracked files`

`git add .` this will stage all files
`git commit -am "SoMe MeSsAgE"`
`git push origin master`


***
#### Pulling

`git init`
'git remote add origin https://github.com/Jake-ryan0/Notes.git`
`git pull origin master`
