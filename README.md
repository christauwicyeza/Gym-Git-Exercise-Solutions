# Gym-Git-Exercise-Solutions

## bundle 1

### exercise 1

``` bash
PS D:\Gym-Git-Exercise> git init
Reinitialized existing Git repository in D:/Gym-Git-Exercise/.git/
PS D:\Gym-Git-Exercise> git branch -m master main
fatal: a branch named 'main' already exists
PS D:\Gym-Git-Exercise> git branch -m main master
PS D:\Gym-Git-Exercise> git branch -m master main
PS D:\Gym-Git-Exercise> git add .
PS D:\Gym-Git-Exercise> git commit -m 'created new file'  
[main 804890b] created new file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 exercise1.txt
PS D:\Gym-Git-Exercise> git push 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 305 bytes | 305.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/christauwicyeza/Gym-Git-Exercise.git
   c53f93c..804890b  main -> main
PS D:\Gym-Git-Exercise> git branch -c dev
PS D:\Gym-Git-Exercise> git status 
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS D:\Gym-Git-Exercise> git branch
  dev
* main
PS D:\Gym-Git-Exercise> git switch dev
Switched to branch 'dev'
Your branch is up to date with 'origin/main'.
PS D:\Gym-Git-Exercise> git branch 
* dev
  main
PS D:\Gym-Git-Exercise> git branch -c test
PS D:\Gym-Git-Exercise> git branch 
* dev
  main
  test
PS D:\Gym-Git-Exercise> git switch dev
Already on 'dev'
Your branch is up to date with 'origin/main'.
PS D:\Gym-Git-Exercise> git branch -d test
Deleted branch test (was 804890b).
```

### exercise 2

```bash
PS D:\christauwicyeza-Gym-Git-Exercise> git stash save 'new changes'
No local changes to save
PS D:\christauwicyeza-Gym-Git-Exercise> git add .
PS D:\christauwicyeza-Gym-Git-Exercise> git stash save 'new changes'
Saved working directory and index state On dev: new changes
PS D:\christauwicyeza-Gym-Git-Exercise> git add .
PS D:\christauwicyeza-Gym-Git-Exercise> git stash save 'new added changes'
Saved working directory and index state On dev: new added changes
PS D:\christauwicyeza-Gym-Git-Exercise> git add .
PS D:\christauwicyeza-Gym-Git-Exercise> git stash save 'added about new  changes' 
Saved working directory and index state On dev: added about new  changes
PS D:\christauwicyeza-Gym-Git-Exercise> git stash list 
stash@{0}: On dev: added about new changes
stash@{1}: On dev: new added changes
stash@{2}: On dev: new changes
PS D:\christauwicyeza-Gym-Git-Exercise> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q|--quiet] [<stash>]

    -q, --quiet           be quiet, only report errors
    --index               attempt to recreate the index

PS D:\christauwicyeza-Gym-Git-Exercise> 
 *  History restored 

Warning: PowerShell detected that you might be using a screen reader and has disabled PSReadLine for compatibility purposes. If you want to re-enable it, run 'Import-Module PSReadLine'.

PS D:\christauwicyeza-Gym-Git-Exercise> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q|--quiet] [<stash>]

    -q, --quiet           be quiet, only report errors
    --index               attempt to recreate the index

PS D:\christauwicyeza-Gym-Git-Exercise> git stash pop 1        
On branch dev
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped refs/stash@{1} (d262cbbf0c5b5dcddeba37076246e26ab09f4254)
PS D:\christauwicyeza-Gym-Git-Exercise> git stash pop 0
On branch dev
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   team.html

Dropped refs/stash@{0} (9a6d8edb9f5fd8637facb47c1058000d2dac6985)
PS D:\christauwicyeza-Gym-Git-Exercise> git commit -m 'stash'
[dev f78095f] stash
 2 files changed, 20 insertions(+)
 create mode 100644 about.html
 create mode 100644 team.html
PS D:\christauwicyeza-Gym-Git-Exercise> git push 
fatal: The upstream branch of your current branch does not match
the name of your current branch.  To push to the upstream branch
on the remote, use

    git push origin HEAD:main

To push to the branch of the same name on the remote, use

    git push origin HEAD

To choose either option permanently, see push.default in 'git help config'.

To avoid automatically configuring upstream branches when their name
doesn't match the local branch, see option 'simple' of branch.autoSetupMerge
in 'git help config'.

PS D:\christauwicyeza-Gym-Git-Exercise> git push origin HEAD
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 467 bytes | 467.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise/pull/new/dev
remote:
To https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise.git
 * [new branch]      HEAD -> dev
PS D:\christauwicyeza-Gym-Git-Exercise> git stash pop 2  
fatal: log for 'refs/stash' only has 1 entries
PS D:\christauwicyeza-Gym-Git-Exercise> git branch switch dev 
PS D:\christauwicyeza-Gym-Git-Exercise> git stash pop 2        
fatal: log for 'refs/stash' only has 1 entries
PS D:\christauwicyeza-Gym-Git-Exercise> git status 
On branch dev
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
PS D:\christauwicyeza-Gym-Git-Exercise> git stash list 
stash@{0}: On dev: new changes
PS D:\christauwicyeza-Gym-Git-Exercise> git stash pop 0 
On branch dev
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Dropped refs/stash@{0} (32a0fa5a615526254bbd7ca7a5a594a4d451456f)
PS D:\christauwicyeza-Gym-Git-Exercise> git reset HEAD~1
```
## bundle 2

### exercise 1

```bash
PS D:\christauwicyeza-Gym-Git-Exercise> git branch -c ft/bundle-2
PS D:\christauwicyeza-Gym-Git-Exercise> git switch ft/bundle-2
Switched to branch 'ft/bundle-2'
Your branch is up to date with 'origin/main'.
PS D:\christauwicyeza-Gym-Git-Exercise> git add .
PS D:\christauwicyeza-Gym-Git-Exercise> git commit -m 'added services'
[ft/bundle-2 f0ead48] added services
 4 files changed, 40 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html
 create mode 100644 team.html
PS D:\christauwicyeza-Gym-Git-Exercise> git push 
fatal: The upstream branch of your current branch does not match
the name of your current branch.  To push to the upstream branch
on the remote, use

    git push origin HEAD:main

To push to the branch of the same name on the remote, use

    git push origin HEAD

To choose either option permanently, see push.default in 'git help config'.

To avoid automatically configuring upstream branches when their name
doesn't match the local branch, see option 'simple' of branch.autoSetupMerge
in 'git help config'.
PS D:\christauwicyeza-Gym-Git-Exercise> git push origin HEAD
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise/pull/new/ft/bundle-2
remote:
To https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise.git
 * [new branch]      HEAD -> ft/bundle-2
PS D:\christauwicyeza-Gym-Git-Exercise> 
```

### exercise 2

```bash
PS D:\christauwicyeza-Gym-Git-Exercise> git pull 
Updating 634a05b..5f943f4
Fast-forward
 about.html    | 10 ++++++++++
 home.html     | 10 ++++++++++
 services.html | 10 ++++++++++
 3 files changed, 30 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html
PS D:\christauwicyeza-Gym-Git-Exercise> git branch  -c ft/service-redesign
PS D:\christauwicyeza-Gym-Git-Exercise> git switch ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/main'.
PS D:\christauwicyeza-Gym-Git-Exercise> git add services.html
PS D:\christauwicyeza-Gym-Git-Exercise> git commit -m 'added new changes'  
[ft/service-redesign 0251785] added new changes
 1 file changed, 1 insertion(+), 1 deletion(-)
PS D:\christauwicyeza-Gym-Git-Exercise> git push 
fatal: The upstream branch of your current branch does not match
the name of your current branch.  To push to the upstream branch
on the remote, use

    git push origin HEAD:main

To push to the branch of the same name on the remote, use

    git push origin HEAD

To choose either option permanently, see push.default in 'git help config'.

To avoid automatically configuring upstream branches when their name
doesn't match the local branch, see option 'simple' of branch.autoSetupMerge
in 'git help config'.

PS D:\christauwicyeza-Gym-Git-Exercise> git push origin HEAD
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 340 bytes | 340.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:        
remote:      https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise/pull/new/ft/service-redesign
remote:
To https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise.git
 * [new branch]      HEAD -> ft/service-redesign
PS D:\christauwicyeza-Gym-Git-Exercise> git push 
fatal: The upstream branch of your current branch does not match
the name of your current branch.  To push to the upstream branch
on the remote, use

    git push origin HEAD:main

To push to the branch of the same name on the remote, use

    git push origin HEAD

To choose either option permanently, see push.default in 'git help config'.

To avoid automatically configuring upstream branches when their name
doesn't match the local branch, see option 'simple' of branch.autoSetupMerge
in 'git help config'.

PS D:\christauwicyeza-Gym-Git-Exercise> git pull 
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 642 bytes | 321.00 KiB/s, done.
From https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise
   5f943f4..7e5a5c4  main       -> origin/main
Updating 0251785..7e5a5c4
Fast-forward
PS D:\christauwicyeza-Gym-Git-Exercise> git switch main 
Switched to branch 'main'
Your branch is behind 'origin/main' by 2 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
PS D:\christauwicyeza-Gym-Git-Exercise> git add . 
PS D:\christauwicyeza-Gym-Git-Exercise> git commit -m 'created'
[main ec124db] created
 1 file changed, 1 insertion(+), 1 deletion(-)
PS D:\christauwicyeza-Gym-Git-Exercise> git push 
To https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
PS D:\christauwicyeza-Gym-Git-Exercise> git pull
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
PS D:\christauwicyeza-Gym-Git-Exercise> git diff 
diff --cc services.html
index 594f12a,e6baa41..0000000
--- a/services.html
+++ b/services.html
@@@ -5,6 -5,6 +5,10 @@@
      </head>
      <body>
          <h1>services we offer</h1>
++<<<<<<< HEAD
 +        <p>none offered zero </p>
++=======
+         <p>none offered of course</p>
++>>>>>>> 7e5a5c4847fc6f599799c468475751f7a076c608
      </body>
  </html>
PS D:\christauwicyeza-Gym-Git-Exercise> git merge 
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
PS D:\christauwicyeza-Gym-Git-Exercise> git merge 
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
PS D:\christauwicyeza-Gym-Git-Exercise> git push 
To https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
PS D:\christauwicyeza-Gym-Git-Exercise> git pull 
error: Pulling is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
PS D:\christauwicyeza-Gym-Git-Exercise> git merge mainft/service-redesign  
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
PS D:\christauwicyeza-Gym-Git-Exercise> git push 
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 549 bytes | 549.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise.git
   7e5a5c4..e74f2d7  main -> main
```

## bundle 3

### exercise one

```bash
PS D:\christauwicyeza-Gym-Git-Exercise> git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
PS D:\christauwicyeza-Gym-Git-Exercise> git add team.html
PS D:\christauwicyeza-Gym-Git-Exercise> git commit -m "Add team.html and make changes"
[ft/team-page 794e4ff] Add team.html and make changes
 1 file changed, 10 deletions(-)
 delete mode 100644 team.html
PS D:\christauwicyeza-Gym-Git-Exercise> git push origin ft/team-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 257 bytes | 128.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise/pull/new/ft/team-page
remote: 
To https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise.git
 * [new branch]      ft/team-page -> ft/team-page
PS D:\christauwicyeza-Gym-Git-Exercise> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS D:\christauwicyeza-Gym-Git-Exercise> git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
PS D:\christauwicyeza-Gym-Git-Exercise> git checkout ft/contact-page
Already on 'ft/contact-page'
PS D:\christauwicyeza-Gym-Git-Exercise> git cherry-pick <commit-hash>
At line:1 char:17
+ git cherry-pick <commit-hash>
+                 ~
The '<' operator is reserved for future use.
    + CategoryInfo          : ParserError: (:) [], ParentContainsErrorRecordExcepti
   on
    + FullyQualifiedErrorId : RedirectionNotSupported       

PS D:\christauwicyeza-Gym-Git-Exercise> git cherry-pick commit-hash
fatal: bad revision 'commit-hash'
PS D:\christauwicyeza-Gym-Git-Exercise> git log --oneline   
e74f2d7 (HEAD -> ft/contact-page, main) Merge branch 'main' of https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise
ec124db created
7e5a5c4 (ft/service-redesign) Merge pull request #1 from christauwicyeza/ft/service-redesign
0251785 (origin/ft/service-redesign) added new changes      
5f943f4 updated services
f0ead48 added services
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
error: could not apply ec124db... created
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git cherry-pick --continue".
hint: You can instead skip this commit with "git cherry-pick --skip".
hint: To abort and get back to the state before "git cherry-pick",
hint: run "git cherry-pick --abort".
PS D:\christauwicyeza-Gym-Git-Exercise> git add .
PS D:\christauwicyeza-Gym-Git-Exercise> git cherry-pick --continue
The previous cherry-pick is now empty, possibly due to conflict resolution.
If you wish to commit it anyway, use:

created

# Conflicts:
#       services.html
#
# It looks like you may be committing a cherry-pick.
# If this is not correct, please run
#       git update-ref -d CHERRY_PICK_HEAD
# and try again.


# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# Date:      Thu May 18 19:35:15 2023 +0200
#
# On branch ft/contact-page
    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'
On branch ft/contact-page
You are currently cherry-picking commit ec124db.
  (all conflicts fixed: run "git cherry-pick --continue")

Otherwise, please use 'git cherry-pick --skip'
On branch ft/contact-page
You are currently cherry-picking commit ec124db.
  (all conflicts fixed: run "git cherry-pick --continue")   
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)

nothing to commit, working tree clean
[ft/contact-page 5034e4a] created
 Date: Thu May 18 19:35:15 2023 +0200
PS D:\christauwicyeza-Gym-Git-Exercise> he file...
PS D:\christauwicyeza-Gym-Git-Exercise> git add .
PS D:\christauwicyeza-Gym-Git-Exercise> git commit -m "Add changes for contact page"
On branch ft/contact-page
nothing to commit, working tree clean
PS D:\christauwicyeza-Gym-Git-Exercise> git push origin ft/contact-page
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 209 bytes | 209.00 KiB/s, done.Total 1 (delta 0), reused 0 (delta 0), pack-reused 0        
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise/pull/new/ft/contact-page
To https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise.git
   bb32b37..d419602  ft/faq-page -> ft/faq-page
PS D:\christauwicyeza-Gym-Git-Exercise> git revert <commit-hash>
At line:1 char:12
To https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise.git
   bb32b37..d419602  ft/faq-page -> ft/faq-page
PS D:\christauwicyeza-Gym-Git-Exercise> git revert <commit-hash>
At line:1 char:12
+ git revert <commit-hash>
+            ~
The '<' operator is reserved for future use.
fatal: Exiting because of an unresolved conflict.
U       services.html
PS D:\christauwicyeza-Gym-Git-Exercise> git add .
PS D:\christauwicyeza-Gym-Git-Exercise> git revert --continue
[ft/faq-page 54cc72a] Revert "created"
 1 file changed, 1 insertion(+), 1 deletion(-)
PS D:\christauwicyeza-Gym-Git-Exercise> git push origin ft/team-page
Everything up-to-date
PS D:\christauwicyeza-Gym-Git-Exercise>
```
### exercise two
```bash
PS D:\christauwicyeza-Gym-Git-Exercise> git checkout -b ft/home-page-redesign ft/faq-page
Switched to a new branch 'ft/home-page-redesign'
PS D:\christauwicyeza-Gym-Git-Exercise> git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 4 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
PS D:\christauwicyeza-Gym-Git-Exercise> git pull 
Updating e74f2d7..99585b8
Fast-forward
 team.html | 10 ----------
 1 file changed, 10 deletions(-)
 delete mode 100644 team.html
PS D:\christauwicyeza-Gym-Git-Exercise> git checkout main
Already on 'main'
Your branch is up to date with 'origin/main'.
PS D:\christauwicyeza-Gym-Git-Exercise> git add .
PS D:\christauwicyeza-Gym-Git-Exercise> git commit -m "Make changes on main branch"
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS D:\christauwicyeza-Gym-Git-Exercise> git push origin main

Everything up-to-date
PS D:\christauwicyeza-Gym-Git-Exercise> git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
PS D:\christauwicyeza-Gym-Git-Exercise> git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.
PS D:\christauwicyeza-Gym-Git-Exercise> git add .
PS D:\christauwicyeza-Gym-Git-Exercise> git commit -m "Add changes to home page"
On branch ft/home-page-redesign
nothing to commit, working tree clean
PS D:\christauwicyeza-Gym-Git-Exercise> git push origin ft/home-page-redesign
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 8 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (9/9), 864 bytes | 216.00 KiB/s, done.
Total 9 (delta 6), reused 0 (delta 0), pack-reused 0        
remote: Resolving deltas: 100% (6/6), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise/pull/new/ft/home-page-redesign
remote:
To https://github.com/christauwicyeza/christauwicyeza-Gym-Git-Exercise.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
PS D:\christauwicyeza-Gym-Git-Exercise> 
```

## bundle four 

### Exercise one 
```bash
PS D:\christauwicyeza-Gym-Git-Exercise> git checkout main   
Switched to branch 'main'
Your branch is behind 'origin/main' by 4 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
PS D:\christauwicyeza-Gym-Git-Exercise> git pull
Updating 99585b8..d24ecac
Fast-forward
 faq.html      | 10 ++++++++++
 services.html |  2 +-
 2 files changed, 11 insertions(+), 1 deletion(-)
 create mode 100644 faq.html
PS D:\christauwicyeza-Gym-Git-Exercise> git remote add git-copy https://github.com/cherror: failed to push some refs to 'https://github.com/christauwicyeza/GYM-exercise_2.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
PS D:\christauwicyeza-Gym-Git-Exercise> git pull git-copy main
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 607 bytes | 11.00 KiB/s, done.
From https://github.com/christauwicyeza/GYM-exercise_2
 * branch            main       -> FETCH_HEAD
 * [new branch]      main       -> git-copy/main
fatal: refusing to merge unrelated histories
PS D:\christauwicyeza-Gym-Git-Exercise> 
PS D:\christauwicyeza-Gym-Git-Exercise> git push git-copy main 
Enumerating objects: 37, done.
Counting objects: 100% (37/37), done.
Delta compression using up to 8 threads
Compressing objects: 100% (34/34), done.
Writing objects: 100% (37/37), 5.73 KiB | 419.00 KiB/s, done.
Total 37 (delta 19), reused 3 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (19/19), done.
To https://github.com/christauwicyeza/GYM-exercise_2.git
 + 2388af2...96c8554 main -> main (forced update)
PS D:\christauwicyeza-Gym-Git-Exercise> 
```

## exercise two


```bash
 git checkout -b ft/footer
  63 git add .
  64 git commit -m "Add initial changes to footer"
  65 # Make the necessary changes
  66 git add .
  67 git commit -m "Add additional changes to footer"
  68 git push origin ft/footer
  69 git checkout main
  70 git checkout -b ft/squashing
  71 git merge --squash ft/footer
  72 git commit -m "footer changes squashing"
  73 git push origin ft/squashing 
```

### Bundle 5

## Exercise one 