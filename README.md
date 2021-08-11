# git-practice
git command practice repository

all content is taken from https://github.com/github/docs.

## GIT PRACTICE
1. Pull Request without conflict  
[modify_about_merge] -> [master]  

2. Pull Request with conflict (resolve with web editor)  
[conflict_branch] -> [modify_about_merge]  

3. Pull Request with conflict (resolve with command line)  
[conflict_branch2] -> [modify_about_merge]  
```
$ git fetch origin
$ git checkout -b conflict_branch2 origin/conflict_branch2
$ git merge modify_about_merge
# conflict resolve
$ git add .
$ git commit -m "conflict resolve"
$ git push origin conflict_branch2
```

4. Sqaush practice (with web editor)  
[squash_branch] -> [master]  

5. Squash practice (with command line)  
[squash_branch2] -> [master]  
![image](https://user-images.githubusercontent.com/10149398/128968477-0f2bdc45-b879-43ee-ac28-2f07f4797fb0.png)
```
$ git pull origin master
$ git checkout squash_branch2
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

6. Commit amend practice
[amend_branch] -> [master]
```
$ git checkout amend_branch
# modify configuring-commit-rebasing-for-pull-requests.md file
$ git add .
$ git commit --amend
$ git push -f origin amend_branch
```

## Useful git commands  
1. Git pull all from remote  
```
$ git branch -r | grep -v '\->' | while read remote; do git branch --track "${remote#origin/}" "$remote"; done
$ git fetch --all
$ git pull --all
```
