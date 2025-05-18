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

