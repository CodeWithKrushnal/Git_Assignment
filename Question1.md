# 1. What is cherry-pick? Explain the use case of it and also write steps to do it.

Cherry Pick is a command used to apply a selective commit from some other branch to the current branch, instead merging the branches.

**Usecases:**

1. To apply a single commit to different branch

2. Fix a minor bug in multiple branches

3. Isolation of specific change.

**Stepes:**

1. **Identify the commit hash of the commit.**

Commit Hashes could be noted with help of following command:

```
git log
```
2. **Checkout**** the Target Branch:**

Switch to the Branch  where you want to apply the commit.

```
git checkout main
```
3. **Cherry-Pick the Commit**

Run the command followed by the commit hash you want to apply

```
git cherry-pick <commit-hash>
git cherry-pick <start_commit_hash>^..<end_commit_hash> //for range of commits
```
**Operation logs:** \


```
krush@Ultron MINGW64 /d/Git_Assignment (feature2)
$ git log
commit f93e9b40922b59513d86f19777614e23f425c270 (HEAD -> main, origin/main)
Author: CodeWithKrushnal <krushnal.patil@joshsoftware.com>
Date:   Sun Jan 5 13:52:03 2025 +0530

    Change files

commit c64c6c8cc30236369eef2fe37fea6c87500573a4
Author: CodeWithKrushnal <krushnal.patil@joshsoftware.com>
Date:   Sun Jan 5 13:24:34 2025 +0530

    Modify the gitignore again

commit 0755bc9b68b97324b1d982c26f45cb3eafa103ed
Author: CodeWithKrushnal <krushnal.patil@joshsoftware.com>
Date:   Sun Jan 5 13:23:13 2025 +0530

    Modify the gitignore again

commit 731f436434a8254d6c5e50393fdb2643f4ac90b1
Author: CodeWithKrushnal <krushnal.patil@joshsoftware.com>
Date:   Sun Jan 5 13:22:19 2025 +0530


krush@Ultron MINGW64 /d/Git_Assignment (main)
$ git branch
  feature1
  feature2
* main

krush@Ultron MINGW64 /d/Git_Assignment (main)
$ git log
commit f93e9b40922b59513d86f19777614e23f425c270 (HEAD -> main, origin/main)
Author: CodeWithKrushnal <krushnal.patil@joshsoftware.com>
Date:   Sun Jan 5 13:52:03 2025 +0530

    Change files

commit c64c6c8cc30236369eef2fe37fea6c87500573a4
Author: CodeWithKrushnal <krushnal.patil@joshsoftware.com>
Date:   Sun Jan 5 13:24:34 2025 +0530

    Modify the gitignore again

commit 0755bc9b68b97324b1d982c26f45cb3eafa103ed
Author: CodeWithKrushnal <krushnal.patil@joshsoftware.com>
Date:   Sun Jan 5 13:23:13 2025 +0530

    Modify the gitignore again

commit 731f436434a8254d6c5e50393fdb2643f4ac90b1
Author: CodeWithKrushnal <krushnal.patil@joshsoftware.com>
Date:   Sun Jan 5 13:22:19 2025 +0530

    Modify .gitignore

commit 5262c1b45bc70ad96d9daefa9b773f52df5d417a
Author: CodeWithKrushnal <krushnal.patil@joshsoftware.com>
Date:   Sun Jan 5 12:13:51 2025 +0530

    Add main.txt to main branch

krush@Ultron MINGW64 /d/Git_Assignment (main)
$ git switch feature1
Switched to branch 'feature1'
Your branch is up to date with 'origin/feature1'.

krush@Ultron MINGW64 /d/Git_Assignment (feature1)
$ git cherry-pick 5262c1b45bc70ad96d9daefa9b773f52df5d417a
[feature1 5d3b40e] Add main.txt to main branch
 Date: Sun Jan 5 12:13:51 2025 +0530
 1 file changed, 1 insertion(+)
 create mode 100644 main.txt

krush@Ultron MINGW64 /d/Git_Assignment (feature1)
$ git status
On branch feature1
Your branch is ahead of 'origin/feature1' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

krush@Ultron MINGW64 /d/Git_Assignment (feature1)
$ git push origin feature1
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 320 bytes | 320.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com-codewithkrushnal:CodeWithKrushnal/Git_Assignment.git
   5c43db6..5d3b40e  feature1 -> feature1
```