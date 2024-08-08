```sh
E:\Lab\devops\devopstest1>git branch develop

E:\Lab\devops\devopstest1>git branch qa

E:\Lab\devops\devopstest1>git branch website

E:\Lab\devops\devopstest1>git branch prod

E:\Lab\devops\devopstest1>git branch
  develop
* main
  prod
  qa
  website

E:\Lab\devops\devopstest1>git branch -r
  origin/main

E:\Lab\devops\devopstest1>git branch -a
  develop
* main
  prod
  qa
  website
  remotes/origin/main

E:\Lab\devops\devopstest1>git push --set-upstream origin develop
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'develop' on GitHub by visiting:
remote:      https://github.com/cgssiva/devopstest1/pull/new/develop
remote:
To https://github.com/cgssiva/devopstest1.git
 * [new branch]      develop -> develop
branch 'develop' set up to track 'origin/develop'.

E:\Lab\devops\devopstest1>git push --set-upstream origin qa     
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'qa' on GitHub by visiting:
remote:      https://github.com/cgssiva/devopstest1/pull/new/qa
remote: 
To https://github.com/cgssiva/devopstest1.git
 * [new branch]      qa -> qa
branch 'qa' set up to track 'origin/qa'.

E:\Lab\devops\devopstest1>git push --set-upstream origin website
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'website' on GitHub by visiting:
remote:      https://github.com/cgssiva/devopstest1/pull/new/website
remote:
To https://github.com/cgssiva/devopstest1.git
 * [new branch]      website -> website
branch 'website' set up to track 'origin/website'.

E:\Lab\devops\devopstest1>git push --set-upstream origin prod   
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'prod' on GitHub by visiting:
remote:      https://github.com/cgssiva/devopstest1/pull/new/prod
remote:
To https://github.com/cgssiva/devopstest1.git
 * [new branch]      prod -> prod
branch 'prod' set up to track 'origin/prod'.

E:\Lab\devops\devopstest1>git branch -a
  develop
* main
  prod
  qa
  website
  remotes/origin/develop
  remotes/origin/main
  remotes/origin/prod
  remotes/origin/qa
  remotes/origin/website

E:\Lab\devops\devopstest1>git checkout develop
Switched to branch 'develop'
Your branch is up to date with 'origin/develop'.

E:\Lab\devops\devopstest1>git status
On branch develop
Your branch is up to date with 'origin/develop'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        testfile3.txt
        testfile4.txt

nothing added to commit but untracked files present (use "git add" to track)

E:\Lab\devops\devopstest1>git commit -m "3 & 4 files added"
On branch develop
Your branch is up to date with 'origin/develop'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        testfile3.txt
        testfile4.txt

nothing added to commit but untracked files present (use "git add" to track)

E:\Lab\devops\devopstest1>git add testfile3.txt

E:\Lab\devops\devopstest1>git add testfile4.txt

E:\Lab\devops\devopstest1>git commit -m "3 & 4 files added"
[develop 4e3598b] 3 & 4 files added
 2 files changed, 2 insertions(+)
 create mode 100644 testfile3.txt
 create mode 100644 testfile4.txt

E:\Lab\devops\devopstest1>git status
On branch develop
Your branch is ahead of 'origin/develop' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

E:\Lab\devops\devopstest1>git push -u origin develop
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 384 bytes | 192.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/cgssiva/devopstest1.git
   0784ea0..4e3598b  develop -> develop
branch 'develop' set up to track 'origin/develop'.

E:\Lab\devops\devopstest1>git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 2 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

E:\Lab\devops\devopstest1>git pull
Updating 0784ea0..47abff8
Fast-forward
 testfile3.txt | 1 +
 testfile4.txt | 1 +
 2 files changed, 2 insertions(+)
 create mode 100644 testfile3.txt
 create mode 100644 testfile4.txt

E:\Lab\devops\devopstest1>git checkout website
Switched to branch 'website'
Your branch is up to date with 'origin/website'.

E:\Lab\devops\devopstest1>git add testfile5.txt

E:\Lab\devops\devopstest1>git commit -m "Adding 5th file in commit"
[website ad3854f] Adding 5th file in commit
 1 file changed, 1 insertion(+)
 create mode 100644 testfile5.txt

E:\Lab\devops\devopstest1>git add testfile6.txt

E:\Lab\devops\devopstest1>git commit -m "Adding 6th file in commit"
[website 686e33d] Adding 6th file in commit
 1 file changed, 1 insertion(+)
 create mode 100644 testfile6.txt

E:\Lab\devops\devopstest1>git checkout qa
Switched to branch 'qa'
Your branch is up to date with 'origin/qa'.

E:\Lab\devops\devopstest1>git cherry-pick ad3854f
[qa 3451b39] Adding 5th file in commit
 Date: Thu Aug 8 15:48:15 2024 +0530
 1 file changed, 1 insertion(+)
 create mode 100644 testfile5.txt

E:\Lab\devops\devopstest1>git cherry-pick 686e33d
[qa 5b43f5f] Adding 6th file in commit
 Date: Thu Aug 8 15:48:49 2024 +0530
 1 file changed, 1 insertion(+)
 create mode 100644 testfile6.txt

E:\Lab\devops\devopstest1>git checkout prod
Switched to branch 'prod'
Your branch is up to date with 'origin/prod'.

E:\Lab\devops\devopstest1>git status
On branch prod
Your branch is up to date with 'origin/prod'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        testfile7.txt

nothing added to commit but untracked files present (use "git add" to track)

E:\Lab\devops\devopstest1>git add testfile7.txt

E:\Lab\devops\devopstest1>git commit -m "Adding 7th file in commit"
[prod 79642d2] Adding 7th file in commit
 1 file changed, 1 insertion(+)
 create mode 100644 testfile7.txt

E:\Lab\devops\devopstest1>git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

E:\Lab\devops\devopstest1>git cherry-pick prod
[main 7113d84] Adding 7th file in commit
 Date: Thu Aug 8 15:53:20 2024 +0530
 1 file changed, 1 insertion(+)
 create mode 100644 testfile7.txt

E:\Lab\devops\devopstest1>git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 306 bytes | 306.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/cgssiva/devopstest1.git
   47abff8..7113d84  main -> main

E:\Lab\devops\devopstest1>git checkout develop
Switched to branch 'develop'
Your branch is up to date with 'origin/develop'.

E:\Lab\devops\devopstest1>git push 
Everything up-to-date

E:\Lab\devops\devopstest1>git checkout qa 
Switched to branch 'qa'
Your branch is ahead of 'origin/qa' by 2 commits.
  (use "git push" to publish your local commits)

E:\Lab\devops\devopstest1>git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 567 bytes | 189.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/cgssiva/devopstest1.git
   0784ea0..5b43f5f  qa -> qa

E:\Lab\devops\devopstest1>git checkout prod
Switched to branch 'prod'
Your branch is ahead of 'origin/prod' by 1 commit.
  (use "git push" to publish your local commits)

E:\Lab\devops\devopstest1>git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 327 bytes | 109.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/cgssiva/devopstest1.git
   0784ea0..79642d2  prod -> prod

E:\Lab\devops\devopstest1>
```
