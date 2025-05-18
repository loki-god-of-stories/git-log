# git-log

## track changes

```
loki @ ~/Documents/GitHub/multiverse $ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        earth.txt

nothing added to commit but untracked files present (use "git add" to track)
```

```
loki @ ~/Documents/GitHub/multiverse $ git add earth.txt
loki @ ~/Documents/GitHub/multiverse $ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   earth.txt

```

```
loki @ ~/Documents/GitHub/multiverse $ git commit -m "Start story for New Asgard in earth.txt"
[main 9b26458] Start story for New Asgard in earth.txt
 1 file changed, 1 insertion(+)
 create mode 100644 earth.txt
```

```
loki @ ~/Documents/GitHub/multiverse $ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

```
loki @ ~/Documents/GitHub/multiverse $ git log
commit 9b26458f5d229d48be61023bcb510f8beb3f13db (HEAD -> main)
Author: Loki Odinson <loki.odinson@tva.org>
Date:   Sat May 17 20:18:55 2025 -0400

    Start story for New Asgard in earth.txt

commit f537d84c6ef9b6d988f642400b2017f855f9aaa1 (origin/main, origin/HEAD)
Author: Loki Odinson <loki.odinson@tva.org>
Date:   Sat May 17 18:34:45 2025 -0400

    Initial commit
```

```
loki @ ~/Documents/GitHub/multiverse $ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   earth.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

```
loki @ ~/Documents/GitHub/multiverse $ git diff
diff --git a/earth.txt b/earth.txt
index 0b592c6..d27fc77 100644
--- a/earth.txt
+++ b/earth.txt
@@ -1 +1,2 @@
 Thor defends New Asgard from invaders.
+Thor and Valkyrie coordinate a counterattack.
```

```
loki @ ~/Documents/GitHub/multiverse $ git commit -m "Implement counterattack strategy"
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   earth.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

``
loki @ ~/Documents/GitHub/multiverse $ git add earth.txt
loki @ ~/Documents/GitHub/multiverse $ git commit -m "Implement counterattack strategy"
[main ee67c8b] Implement counterattack strategy
 1 file changed, 1 insertion(+)
```

```
loki @ ~/Documents/GitHub/multiverse $ git diff
diff --git a/earth.txt b/earth.txt
index d27fc77..8938f14 100644
--- a/earth.txt
+++ b/earth.txt
@@ -1,2 +1,3 @@
 Thor defends New Asgard from invaders.
 Thor and Valkyrie coordinate a counterattack.
+Thor reunites with Jane Foster at the sanctuary.
```

```
loki @ ~/Documents/GitHub/multiverse $ git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

```
loki @ ~/Documents/GitHub/multiverse $ git log
commit 2f2d364f559efb1101647591d9fbf2cc30ade8bb (HEAD -> main)
Author: Loki Odinson <loki.odinson@tva.org>
Date:   Sat May 17 20:29:51 2025 -0400

    Complete story with Thor-Jane reunion

commit ee67c8b551612e09be46c97726866d04c7b0d785
Author: Loki Odinson <loki.odinson@tva.org>
Date:   Sat May 17 20:24:35 2025 -0400

    Implement counterattack strategy

commit 9b26458f5d229d48be61023bcb510f8beb3f13db
Author: Loki Odinson <loki.odinson@tva.org>
Date:   Sat May 17 20:18:55 2025 -0400

    Start story for New Asgard in earth.txt

commit f537d84c6ef9b6d988f642400b2017f855f9aaa1 (origin/main, origin/HEAD)
Author: Loki Odinson <loki.odinson@tva.org>
Date:   Sat May 17 18:34:45 2025 -0400

    Initial commit
```

```
loki @ ~/Documents/GitHub/multiverse $ git remote -v
origin  https://github.com/loki-god-of-stories/multiverse.git (fetch)
origin  https://github.com/loki-god-of-stories/multiverse.git (push)
```

```
loki @ ~/Documents/GitHub/multiverse $ git push origin main
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 8 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (9/9), 992 bytes | 992.00 KiB/s, done.
Total 9 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/loki-god-of-stories/multiverse.git
   f537d84..2f2d364  main -> main
```

```
loki @ ~/Documents/GitHub/multiverse $ git pull origin main
From https://github.com/loki-god-of-stories/multiverse
 * branch            main       -> FETCH_HEAD
Already up to date.
```

```
loki @ ~/Documents/GitHub/multiverse $ git branch heimdall-aware
loki @ ~/Documents/GitHub/multiverse $ git branch
  heimdall-aware
* main
```

```
loki @ ~/Documents/GitHub/multiverse $ git checkout heimdall-aware
Switched to branch 'heimdall-aware'
loki @ ~/Documents/GitHub/multiverse $ git branch
* heimdall-aware
  main
```

```
loki @ ~/Documents/GitHub/multiverse $ git log --oneline
2f2d364 (HEAD -> heimdall-aware, origin/main, origin/HEAD, main) Complete story with Thor-Jane reunion
ee67c8b Implement counterattack strategy
9b26458 Start story for New Asgard in earth.txt
f537d84 Initial commit
```

```
loki @ ~/Documents/GitHub/multiverse $ git add asgard.txt
loki @ ~/Documents/GitHub/multiverse $ git commit -m "Create asgard.txt detailing Heimdall's awareness of invasion"
[heimdall-aware daf95c3] Create asgard.txt detailing Heimdall's awareness of invasion
 1 file changed, 1 insertion(+)
 create mode 100644 asgard.txt
```

```
loki @ ~/Documents/GitHub/multiverse $ git log --oneline
daf95c3 (HEAD -> heimdall-aware) Create asgard.txt detailing Heimdall's awareness of invasion
2f2d364 (origin/main, origin/HEAD, main) Complete story with Thor-Jane reunion
ee67c8b Implement counterattack strategy
9b26458 Start story for New Asgard in earth.txt
f537d84 Initial commit
```

```
loki @ ~/Documents/GitHub/multiverse $ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
loki @ ~/Documents/GitHub/multiverse $ git branch
  heimdall-aware
* main
loki @ ~/Documents/GitHub/multiverse $ git log --oneline
2f2d364 (HEAD -> main, origin/main, origin/HEAD) Complete story with Thor-Jane reunion
ee67c8b Implement counterattack strategy
9b26458 Start story for New Asgard in earth.txt
f537d84 Initial commit
```

```
loki @ ~/Documents/GitHub/multiverse $ git checkout -b heimdall-blind
Switched to a new branch 'heimdall-blind'
loki @ ~/Documents/GitHub/multiverse $ git branch
  heimdall-aware
* heimdall-blind
  main
```

```
loki @ ~/Documents/GitHub/multiverse $ git log --oneline
2f2d364 (HEAD -> heimdall-blind, origin/main, origin/HEAD, main) Complete story with Thor-Jane reunion
ee67c8b Implement counterattack strategy
9b26458 Start story for New Asgard in earth.txt
f537d84 Initial commit
```

```
loki @ ~/Documents/GitHub/multiverse $ git add asgard.md
loki @ ~/Documents/GitHub/multiverse $ git commit -m "Create asgard.md describing Heimdall's blocked vision"
[heimdall-blind 59b9bab] Create asgard.md describing Heimdall's blocked vision
 1 file changed, 1 insertion(+)
 create mode 100644 asgard.md
```

```
loki @ ~/Documents/GitHub/multiverse $ git log --oneline
59b9bab (HEAD -> heimdall-blind) Create asgard.md describing Heimdall's blocked vision
2f2d364 (origin/main, origin/HEAD, main) Complete story with Thor-Jane reunion
ee67c8b Implement counterattack strategy
9b26458 Start story for New Asgard in earth.txt
f537d84 Initial commit
```

```
loki @ ~/Documents/GitHub/multiverse $ git checkout heimdall-aware
Switched to branch 'heimdall-aware'
loki @ ~/Documents/GitHub/multiverse $ git push
fatal: The current branch heimdall-aware has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin heimdall-aware

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
```

```
loki @ ~/Documents/GitHub/multiverse $ git push -u origin heimdall-aware
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 406 bytes | 406.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'heimdall-aware' on GitHub by visiting:
remote:      https://github.com/loki-god-of-stories/multiverse/pull/new/heimdall-aware
remote: 
To https://github.com/loki-god-of-stories/multiverse.git
 * [new branch]      heimdall-aware -> heimdall-aware
branch 'heimdall-aware' set up to track 'origin/heimdall-aware'.
```

```
loki @ ~/Documents/GitHub/multiverse $ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
loki @ ~/Documents/GitHub/multiverse $ git log --oneline
2f2d364 (HEAD -> main, origin/main, origin/HEAD) Complete story with Thor-Jane reunion
ee67c8b Implement counterattack strategy
9b26458 Start story for New Asgard in earth.txt
f537d84 Initial commit
```

```
loki @ ~/Documents/GitHub/multiverse $ git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 952 bytes | 476.00 KiB/s, done.
From https://github.com/loki-god-of-stories/multiverse
   2f2d364..976b48e  main       -> origin/main
Updating 2f2d364..976b48e
Fast-forward
 asgard.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 asgard.txt
```

```
loki @ ~/Documents/GitHub/multiverse $ git log --oneline
976b48e (HEAD -> main, origin/main, origin/HEAD) Merge pull request #1 from loki-god-of-stories/heimdall-aware
daf95c3 (origin/heimdall-aware, heimdall-aware) Create asgard.txt detailing Heimdall's awareness of invasion
2f2d364 Complete story with Thor-Jane reunion
ee67c8b Implement counterattack strategy
9b26458 Start story for New Asgard in earth.txt
f537d84 Initial commit
```

```
loki @ ~/Documents/GitHub/multiverse $ git branch -d heimdall-aware
Deleted branch heimdall-aware (was daf95c3).
```

```
loki @ ~/Documents/GitHub/multiverse $ git branch -d heimdall-blind
error: The branch 'heimdall-blind' is not fully merged.
If you are sure you want to delete it, run 'git branch -D heimdall-blind'.
loki @ ~/Documents/GitHub/multiverse $ git branch -D heimdall-blind
Deleted branch heimdall-blind (was 59b9bab).
```

```
loki @ ~/Documents/GitHub/multiverse $ git branch loki-twist
loki @ ~/Documents/GitHub/multiverse $ git add earth.txt
loki @ ~/Documents/GitHub/multiverse $ git commit -m "Add invaders retreat"
[main a521b20] Add invaders retreat
 1 file changed, 1 insertion(+)
```

```
loki @ ~/Documents/GitHub/multiverse $ git log --oneline
a521b20 (HEAD -> main) Add invaders retreat
976b48e (origin/main, origin/HEAD) Merge pull request #1 from loki-god-of-stories/heimdall-aware
daf95c3 (origin/heimdall-aware) Create asgard.txt detailing Heimdall's awareness of invasion
2f2d364 Complete story with Thor-Jane reunion
ee67c8b Implement counterattack strategy
9b26458 Start story for New Asgard in earth.txt
f537d84 Initial commit
```

```
loki @ ~/Documents/GitHub/multiverse $ git checkout loki-twist
Switched to branch 'loki-twist'
loki @ ~/Documents/GitHub/multiverse $ git branch
* loki-twist
  main
loki @ ~/Documents/GitHub/multiverse $ git add earth.txt
loki @ ~/Documents/GitHub/multiverse $ git commit -m "Add twist ending with Loki as mastermind"
[loki-twist 7b972b4] Add twist ending with Loki as mastermind
 1 file changed, 1 insertion(+)
```

```
loki @ ~/Documents/GitHub/multiverse $ git log --oneline
7b972b4 (HEAD -> loki-twist) Add twist ending with Loki as mastermind
976b48e (origin/main, origin/HEAD) Merge pull request #1 from loki-god-of-stories/heimdall-aware
daf95c3 (origin/heimdall-aware) Create asgard.txt detailing Heimdall's awareness of invasion
2f2d364 Complete story with Thor-Jane reunion
ee67c8b Implement counterattack strategy
9b26458 Start story for New Asgard in earth.txt
f537d84 Initial commit
```

```
loki @ ~/Documents/GitHub/multiverse $ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
loki @ ~/Documents/GitHub/multiverse $ git branch
  loki-twist
* main
```

```
loki @ ~/Documents/GitHub/multiverse $ git merge loki-twist
Auto-merging earth.txt
CONFLICT (content): Merge conflict in earth.txt
Automatic merge failed; fix conflicts and then commit the result.
```

```
loki @ ~/Documents/GitHub/multiverse $ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   earth.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

```
loki @ ~/Documents/GitHub/multiverse $ git log
commit c5c81b35d7631b4aa9c7d71d06253c593cbaf644 (HEAD -> main)
Merge: a521b20 7b972b4
Author: Loki Odinson <loki.odinson@tva.org>
Date:   Sat May 17 21:36:55 2025 -0400

    Merge branch 'loki-twist'

commit 7b972b4d86972ddfbacac225c5c84c8b4a5609ff (loki-twist)
Author: Loki Odinson <loki.odinson@tva.org>
Date:   Sat May 17 21:27:20 2025 -0400

    Add twist ending with Loki as mastermind

commit a521b20ef97343b49b3b25717e485b360fcb8d64
Author: Loki Odinson <loki.odinson@tva.org>
Date:   Sat May 17 21:25:13 2025 -0400

    Add invaders retreat
```

```
loki @ ~/Documents/GitHub/multiverse $ git checkout loki-twist
Switched to branch 'loki-twist'
loki @ ~/Documents/GitHub/multiverse $ git add earth.txt
loki @ ~/Documents/GitHub/multiverse $ git commit -m "Add Thor's knowing reaction to Loki's scheme"
[loki-twist 959f09c] Add Thor's knowing reaction to Loki's scheme
 1 file changed, 1 insertion(+)
```

```
loki @ ~/Documents/GitHub/multiverse $ git merge loki-twist
Auto-merging earth.txt
hint: Waiting for your editor to close the file... code --wait: code: command not found
error: There was a problem with the editor 'code --wait'.
Not committing merge; use 'git commit' to complete the merge.
```

```
loki @ ~/Documents/GitHub/multiverse $ git status
On branch main
Your branch is ahead of 'origin/main' by 5 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

```
loki @ ~/Documents/GitHub/multiverse $ git log --oneline
b965aa1 (HEAD -> main) Merge branch 'loki-twist' again
959f09c (loki-twist) Add Thor's knowing reaction to Loki's scheme
c5c81b3 Merge branch 'loki-twist'
7b972b4 Add twist ending with Loki as mastermind
a521b20 Add invaders retreat
976b48e (origin/main, origin/HEAD) Merge pull request #1 from loki-god-of-stories/heimdall-aware
daf95c3 (origin/heimdall-aware) Create asgard.txt detailing Heimdall's awareness of invasion
2f2d364 Complete story with Thor-Jane reunion
ee67c8b Implement counterattack strategy
9b26458 Start story for New Asgard in earth.txt
f537d84 Initial commit
```

```
loki @ ~/Documents/GitHub/multiverse $ git push
Enumerating objects: 17, done.
Counting objects: 100% (17/17), done.
Delta compression using up to 8 threads
Compressing objects: 100% (15/15), done.
Writing objects: 100% (15/15), 1.42 KiB | 1.42 MiB/s, done.
Total 15 (delta 10), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (10/10), completed with 1 local object.
To https://github.com/loki-god-of-stories/multiverse.git
   976b48e..b965aa1  main -> main
```
