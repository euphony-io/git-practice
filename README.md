# git-practice
Git Practice repository  
All content is taken from https://github.com/github/docs.  
Fork this repository and practice!  



$ git checkout -b conflict_branch2 origin/conflict_branch2
$ git merge modify_about_merge
# conflict resolve
$ git add .
$ git commit -m "conflict resolve"
$ git push origin conflict_branch2
```


$ git log --pretty=oneline # check commit history
$ git rebase -i a5909f529078f558156297977d851d1d458fd233
pick 166267a squash commit 1
s f93aa5b squash commit 2
s 5a9ad96 squash commit 3
s 5d2909a squash commit 4
s d86c1a8 squash commit 5
$ git log --pretty=oneline  # check squash result
a3ae723519d4c38b49c7f4189e87152ec4f4067a (HEAD -> squash_branch2) squash commit 1~5
a5909f529078f558156297977d851d1d458fd233 (master) add github contents
f20a4725e5374c6d7cb6b4a50d97d008fdd98aca Initial commit
$ git push -f origin squash_branch2
```


```
$ git branch -r | grep -v '\->' | while read remote; do git branch --track "${remote#origin/}" "$remote"; done
$ git fetch --all
$ git pull --all
```
