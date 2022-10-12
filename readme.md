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