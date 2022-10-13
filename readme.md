# Git exercice
## Bundle 1
### exercice 1
```bash
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git init                        
Initialized empty Git repository in C:/Users/TheGym/Desktop/tutorial-projects/Gym-Git-Exercise-Solutions/.git/
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git branch -M main
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit -m "initial git project"
 1 file changed, 1 insertion(+)
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git remote add origin https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 245 bytes | 245.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
branch 'main' set up to track 'origin/main'.
Everything up-to-date
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push 
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use


To have this happen automatically for branches without a tracking

Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/NNesta/Gym-Git-Exercise-Solutions/pull/new/dev
remote:
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout -b test
Switched to a new branch 'test'
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/NNesta/Gym-Git-Exercise-Solutions/pull/new/test
remote:
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
 * [new branch]      test -> test
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout dev
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git branch -D test
Deleted branch test (was 78b4987).
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push origin --delete test
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
 - [deleted]         test
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> 
```


### Exercice 2
```bash
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git stash list
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add home.html
Saved working directory and index state WIP on dev: 69fd09a Revert "setup home and about pages"
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git stash list
stash@{0}: WIP on dev: 69fd09a Revert "setup home and about pages"
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add about.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git stash
Saved working directory and index state WIP on dev: 69fd09a Revert "setup home and about pages"
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add team.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git stash
Saved working directory and index state WIP on dev: 69fd09a Revert "setup home and about pages"
stash@{0}: WIP on dev: 69fd09a Revert "setup home and about pages"
stash@{2}: WIP on dev: 69fd09a Revert "setup home and about pages"
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git stash pop 1
On branch dev
Your branch is ahead of 'origin/dev' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)

Dropped refs/stash@{1} (d21fffaba7a595099049e5fa3da6aff5b5a6ad27)
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git stash pop 1
On branch dev
Your branch is ahead of 'origin/dev' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped refs/stash@{1} (0f8a8c51aad0842a0e35eb9aa768532419773a8f)
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add --all
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit "adding about and home files" 
error: pathspec 'adding about and home files' did not match any file(s) known to git
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit -m "adding about and home files" 
[dev 9c3d7d3] adding about and home files
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 648 bytes | 216.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
   860c224..9c3d7d3  dev -> dev
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git stash list
stash@{0}: WIP on dev: 69fd09a Revert "setup home and about pages"
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git stash pop 0
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (eb7050cc0efd1952f1d22d30691d65fc86a6b3d3)
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git reset --hard
HEAD is now at 9c3d7d3 adding about and home files
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> 
```
## Exercice 2
```bash
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git pull
Already up to date.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout -b ft/se
Switched to a new branch 'ft/service-redesign'
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add services.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit -m "adding some changes on services.html"
[ft/service-redesign e0634be] adding some changes on services.html
 1 file changed, 3 insertions(+), 3 deletions(-)
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use
    git push --set-upstream origin ft/service-redesign
upstream, see 'push.autoSetupRemote' in 'git help config'.

Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 398 bytes | 132.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push --set-upstream origin ft/service-redesign
git push --set-upstream origin ft/service-redesign
upstream, see 'push.autoSetupRemote' in 'git help config'.

Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 398 bytes | 132.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add -all
error: did you mean `--all` (with two dashes)?
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add --all
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit -m "feat: add list of services"
[main 17f0774] feat: add list of services
 1 file changed, 7 insertions(+)
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 383 bytes | 191.00 KiB/s, done.
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
   5ddf525..17f0774  main -> main
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git diff
diff --cc services.html
index dfc08ec,187ab2e..0000000
--- a/services.html
+++ b/services.html
@@@ -7,8 -7,15 +7,21 @@@
      <title>Document</title>
  </head>
  <body>
++<<<<<<< HEAD
 +    <h1>New Service Page</h1>
 +    <p>Welcome to service page redesigned</p>
 +   <button>Login here again for the redesigned page</button>
++=======
+     <h1>Service Page</h1>
+     <p>Welcome to service page</p>
+    <ul>
+     <li>Servise 1</li>
+     <li>Servise 2</li>
+     <li>Servise 3</li>
+     <li>Servise 5</li>
+    </ul>
++>>>>>>> main
  </body>
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
   e0634be..a8b080f  ft/service-redesign -> ft/service-redesign
   PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
```

