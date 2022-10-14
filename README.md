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
## Bundle 2
### Exercice 1
```bash
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout -b ft/bundle-2
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add services.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit -m "adding service page "
[ft/bundle-2 8b6dd56] adding service page
 1 file changed, 12 insertions(+)
 create mode 100644 services.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use
    git push --set-upstream origin ft/bundle-2
To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 487 bytes | 243.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/NNesta/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
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
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add .
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit  
[ft/service-redesign d0a8849] feat: merging with main branch
 1 file changed, 100 insertions(+)
 PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.28 KiB | 653.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
   a8b080f..d0a8849  ft/service-redesign -> ft/service-redesign
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> 
```
## bundle 3
### Exercice 1
```bash

PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout main
Already on 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout -b ft/team-page
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add team.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit -m "feat: adding team.html"
[ft/team-page 12d94c8] feat: adding team.html
 1 file changed, 17 insertions(+)
 create mode 100644 team.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 560 bytes | 186.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/NNesta/Gym-Git-Exercise-Solutions/pull/new/ft/team-page
remote:
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git log
Author: Ngabonziza Nestor <ngabonest@gmail.com>
Date:   Fri Oct 14 08:06:13 2022 +0200

    feat: adding team.html

commit be22b82ddcc6c4770f9fef95013d4d4daa97165f (origin/main, main, ft/contact-page)
Merge: 03f7a29 015ec63
Author: Ngabonziza Nestor <ngabonest@gmail.com>
Date:   Thu Oct 13 17:40:18 2022 +0200

    feat:adding readme file

commit 03f7a2994151c9590f4b251379b68993a9ab4485
Author: Ngabonziza Nestor <ngabonest@gmail.com>
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git cherry-pick 12d94c8bb50881685ec57a992536dc2dec2f6732
If you wish to commit it anyway, use:


Otherwise, please use 'git cherry-pick --skip'
On branch ft/team-page
Your branch is up to date with 'origin/ft/team-page'.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)

nothing to commit, working tree clean
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout ft/contact-page
Switched to branch 'ft/contact-page'
warning: cancelling a cherry picking in progress
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git cherry-pick 12d94c8bb50881685ec57a992536dc2dec2f6732
[ft/contact-page 80ed126] feat: adding team.html
 Date: Fri Oct 14 08:06:13 2022 +0200
 create mode 100644 team.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add team.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit -m "feat: add changes to team.html"
[ft/contact-page c162fe4] feat: add changes to team.html
 1 file changed, 2 insertions(+)
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 817 bytes | 204.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/NNesta/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout -b ft/faq-page
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add faq.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit -m "feat: adding faq.html page"
[ft/faq-page 4f8c5bf] feat: adding faq.html page
 1 file changed, 13 insertions(+)
 create mode 100644 faq.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 576 bytes | 288.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/NNesta/Gym-Git-Exercise-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git log
commit 4f8c5bf291ff392ba8bc9169ca56f087f1b2144e (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: Ngabonziza Nestor <ngabonest@gmail.com>
Date:   Fri Oct 14 08:20:16 2022 +0200

    feat: adding faq.html page

commit c162fe4d4edf98ab46b408fadbf0079cf8d0c339 (origin/ft/contact-page, ft/contact-page)
Author: Ngabonziza Nestor <ngabonest@gmail.com>
Date:   Fri Oct 14 08:15:03 2022 +0200
Author: Ngabonziza Nestor <ngabonest@gmail.com>
Date:   Fri Oct 14 08:20:16 2022 +0200

    feat: adding faq.html page

commit c162fe4d4edf98ab46b408fadbf0079cf8d0c339 (origin/ft/contact-page, ft/contact-page)
Author: Ngabonziza Nestor <ngabonest@gmail.com>
Date:   Fri Oct 14 08:15:03 2022 +0200

commit 80ed1260f8c28b5ef72f5a88d8faaa04f59ff977
Author: Ngabonziza Nestor <ngabonest@gmail.com>
Date:   Fri Oct 14 08:06:13 2022 +0200
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git revert 4f8c5bf291ff392ba8bc9169ca56f087f1b2144e
[ft/faq-page 21ec078] Revert "feat: adding faq.html page"
 1 file changed, 13 deletions(-)
 delete mode 100644 faq.html

PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 265 bytes | 132.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
   4f8c5bf..21ec078  ft/faq-page -> ft/faq-page
 

```
### Exercice 2
```bash
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git switch ft/faq-page
Switched to branch 'ft/faq-page'
Your branch is up to date with 'origin/ft/faq-page'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git branch -D ft/home-page-redesign
Deleted branch ft/home-page-redesign (was 04915f3).
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add .   
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit -m "feat: making some changes on home page"
[main 12c0f92] feat: making some changes on home page
feat: adding faq.html page
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 482 bytes | 241.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
   ceb4d95..12c0f92  main -> main
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git rebase main
error: could not apply 4f8c5bf... feat: adding faq.html page
hint: Resolve all conflicts manually, mark them as resolved with
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
Could not apply 4f8c5bf... feat: adding faq.html page
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add .
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git rebase --continue
[detached HEAD 5eb80b5] feat: adding faq.html page
 1 file changed, 2 insertions(+)
CONFLICT (modify/delete): faq.html deleted in 21ec078 (Revert "feat: adding faq.html page") and modified in HEAD.  Version HEAD of faq.html left in treeerror: could not apply 21ec078... Revert "feat: adding faq.html page"
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
Could not apply 21ec078... Revert "feat: adding faq.html page"
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add .
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git rebase --continue
Successfully rebased and updated refs/heads/ft/home-page-redesign.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add .
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit -m "add some changes on home page"
[ft/home-page-redesign c960616] add some changes on home page
 1 file changed, 1 insertion(+)
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push
fatal: The current branch ft/home-page-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 15, done.
Counting objects: 100% (15/15), done.
Delta compression using up to 4 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (12/12), 1.32 KiB | 269.00 KiB/s, done.
Total 12 (delta 8), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (8/8), completed with 3 local objects.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/NNesta/Gym-Git-Exercise-Solutions/pull/new/ft/home-page-redesign
remote:
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> 

```
## Bundle 4
### Exercice 1
```bash
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git remote add git-copy https://github.com/NNesta/Gym-Git-Exercice-2.git       
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git remote
git-copy
origin
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add home.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit -m "feat: add changes on home page"
[main b8278a3] feat: add changes on home page
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push origin
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 371 bytes | 371.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
   c14e4ff..b8278a3  main -> main
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push git-copy
Enumerating objects: 50, done.
Counting objects: 100% (50/50), done.
Delta compression using up to 4 threads
Compressing objects: 100% (46/46), done.
Writing objects: 100% (50/50), 10.13 KiB | 864.00 KiB/s, done.
Total 50 (delta 19), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (19/19), done.
To https://github.com/NNesta/Gym-Git-Exercice-2.git
 * [new branch]      main -> main
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push
Everything up-to-date
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> 
```
### Exercice 2
```bash
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout -b ft/footer
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add footer.tml
fatal: pathspec 'footer.tml' did not match any files
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add footer.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit -m "feat: adding initial commit on footer page"
[ft/footer 16dc042] feat: adding initial commit on footer page
 1 file changed, 12 insertions(+)
 create mode 100644 footer.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git add footer.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit -m "feat: more content on footer page"
[ft/footer a8dc320] feat: more content on footer page
 1 file changed, 3 insertions(+)
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push
fatal: The current branch ft/footer has no upstream branch.
To push the current branch and set the remote as upstream, use
    git push --set-upstream origin ft/footer

upstream, see 'push.autoSetupRemote' in 'git help config'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push --set-upstream origin ft/footer
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 785 bytes | 196.00 KiB/s, done.
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git merge --squash ft/footer
Updating f9fc0e5..a8dc320
Fast-forward
Squash commit -- not updating HEAD
 footer.html | 15 +++++++++++++++
 1 file changed, 15 insertions(+)
 create mode 100644 footer.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git commit -m "footer changes squashing"
[ft/squashing 33df9d3] footer changes squashing
 1 file changed, 15 insertions(+)
 create mode 100644 footer.html
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git log
Author: Ngabonziza Nestor <ngabonest@gmail.com>
Date:   Fri Oct 14 11:14:27 2022 +0200

    footer changes squashing

commit f9fc0e502e11fd208ed287c97364ca24835918a2 (origin/main, main)
Author: Ngabonziza Nestor <ngabonest@gmail.com>
Date:   Fri Oct 14 10:51:12 2022 +0200
    feat: Updating README.md with bundle4 exercice1

commit b8278a3ee3ad8592e657f49a7c8f6029536bb95b (git-copy/main)
Author: Ngabonziza Nestor <ngabonest@gmail.com>
Date:   Fri Oct 14 10:44:06 2022 +0200

    feat: add changes on home page

commit c14e4fff6ee651e4dfe27b58e85100badbe52484
Author: Ngabonziza Nestor <ngabonest@gmail.com>
Date:   Fri Oct 14 10:06:52 2022 +0200
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push
fatal: The current branch ft/squashing has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/squashing

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions> git push --set-upstream origin ft/squashing
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 492 bytes | 246.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/NNesta/Gym-Git-Exercise-Solutions/pull/new/ft/squashing
remote:
To https://github.com/NNesta/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/squashing -> ft/squashing
branch 'ft/squashing' set up to track 'origin/ft/squashing'.
PS C:\Users\TheGym\Desktop\tutorial-projects\Gym-Git-Exercise-Solutions>
```

