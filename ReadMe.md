## Git Exercises
### Challenge1 &2
```

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices
$ git init
Initialized empty Git repository in C:/Users/Admin/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices/.git/
Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (master)
$ git branch -m main

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ touch test{1..4}.md
git add test1.md && git commit -m "chore: Create initial file"
git add test2.md && git commit -m "chore: Create another file"
git add test3.md && git commit -m "chore: Create third and fourth files"
[main (root-commit) 930faf0] chore: Create initial file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md
[main 83c6338] chore: Create another file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
[main 0ffd2fb] chore: Create third and fourth files
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test4.md

nothing added to commit but untracked files present (use "git add" to track)

commit 0ffd2fb07d804aa5dbd02f73e4645bc45efc4b6c (HEAD -> main)
Author: Munezero26200 <alinemunezero920@gmail.com>
Date:   Mon Jul 21 18:02:50 2025 +0200

    chore: Create third and fourth files

commit 83c6338085b17da0674aed639b3e4772a779e82f
Author: Munezero26200 <alinemunezero920@gmail.com>
Date:   Mon Jul 21 18:02:50 2025 +0200

    chore: Create another file

commit 930faf04557e20a25cae355c8a0251613f794a72
Author: Munezero26200 <alinemunezero920@gmail.com>
Date:   Mon Jul 21 18:02:49 2025 +0200      

    chore: Create initial file

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git add test4.md

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git --amend
unknown option: --amend
e] [--bare] [--git-dir=<path>]
           [--work-tree=<path>] [--namespace=<name>] [--config-env=<name>=<envvar>]
           <command> [<args>]

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$
 *  History restored 


Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i HEAD~2
hint: Waiting for your editor to close the file...


error: invalid command 'B'
error: invalid line 1: B
You can fix this with 'git rebase --edit-todo' and then run 'git rebase --continue'.
Or you can abort the rebase with 'git rebase --abort'.

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main|REBASE)
$ git rebase abort
fatal: It seems that there is already a rebase-merge directory, and
I wonder if you are in the middle of another rebase.  If that is the
case, please try
        git rebase (--continue | --abort | --skip)
If that is not the case, please
        rm -fr ".git/rebase-merge"
and run me again.  I am stopping in case you still have something
valuable there.


Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main|REBASE)
$ git rebase --abort

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git status
On branch main
nothing to commit, working tree clean

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git log --oneline
773ae60 (HEAD -> main) chore: Create third and fourth files
83c6338 chore: Create another file
930faf0 chore: Create initial file

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i 930faf0
Stopped at 83c6338...  chore: Create another file
You can amend the commit now, with

  git commit --amend

Once you are satisfied with your changes, run

  git rebase --continue

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main|REBASE 1/2)
$ git commit --amend
[detached HEAD 81d9eb0] chore: Create second file
 Date: Mon Jul 21 18:02:50 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main|REBASE 1/2)
$  git rebase --continue
Successfully rebased and updated refs/heads/main.
fb08b14 (HEAD -> main) chore: Create third and fourth files
81d9eb0 chore: Create second file
930faf0 chore: Create initial file
```
### Challenge 3
```
$
 *  History restored 


Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i HEAD~2
hint: Waiting for your editor to close the file...


error: invalid command 'B'
error: invalid line 1: B
You can fix this with 'git rebase --edit-todo' and then run 'git rebase --continue'.
Or you can abort the rebase with 'git rebase --abort'.

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main|REBASE)
$ git rebase abort
fatal: It seems that there is already a rebase-merge directory, and
I wonder if you are in the middle of another rebase.  If that is the
case, please try
        git rebase (--continue | --abort | --skip)
If that is not the case, please
        rm -fr ".git/rebase-merge"
and run me again.  I am stopping in case you still have something
valuable there.


Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main|REBASE)
$ git rebase --abort

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git status
On branch main
nothing to commit, working tree clean

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git log --oneline
773ae60 (HEAD -> main) chore: Create third and fourth files
83c6338 chore: Create another file
930faf0 chore: Create initial file

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i 930faf0
Stopped at 83c6338...  chore: Create another file
You can amend the commit now, with

  git commit --amend

Once you are satisfied with your changes, run

  git rebase --continue

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main|REBASE 1/2)
$ git commit --amend
[detached HEAD 81d9eb0] chore: Create second file
 Date: Mon Jul 21 18:02:50 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main|REBASE 1/2)
$  git rebase --continue
fb08b14 (HEAD -> main) chore: Create third and fourth files
81d9eb0 chore: Create second file
930faf0 chore: Create initial file

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git add .

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git commit -m "Here is codes for challenge 1&2 in readme file"
[main c8ba4cf] Here is codes for challenge 1&2 in readme file
 1 file changed, 133 insertions(+)
 create mode 100644 ReadMe.md

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$  git push --set-upstream origin main
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 2 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (10/10), 2.18 KiB | 203.00 KiB/s, done.
Total 10 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), done.
To https://github.com/Munezero26200/Git-Practices.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$
 *  History restored 


Admin@MunezeroPC MINGW64 ~/Documents/Thegym-

codes for challenge 1&2 in readme file
fb08b14 chore: Create third and fourth files
codes for challenge 1&2 in readme file      
fb08b14 chore: Create third and fourth files
81d9eb0 chore: Create second file
930faf0 chore: Create initial file

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i HEAD 
HEAD          ORIG_HEAD     
main          origin/main

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i HEAD 
HEAD          ORIG_HEAD     
main          origin/main

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i HEAD 
HEAD          ORIG_HEAD     
 (main)
$ git rebase -i HEAD
 (main)
$ git rebase -i HEAD
HEAD          ORIG_HEAD
main          origin/main

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i HEAD~3
error: cannot rebase: You have unstaged changes.
error: Please commit or stash them.

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git add .

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git commit -m "Here is the change on format of ReadMe file."
[main 2dfb256] Here is the change on format of ReadMe file.
 1 file changed, 2 insertions(+), 2 deletions(-)

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
lenge 1&2 in readme file
fb08b14 chore: Create third and fourth files
lenge 1&2 in readme file
fb08b14 chore: Create third and fourth files
81d9eb0 chore: Create second file
930faf0 chore: Create initial file

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i HEAD~3
hint: Waiting for your editor to close the fi
Successfully rebased and updated refs/heads/main.

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase --abort
fatal: no rebase in progress

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
enge 1&2 in readme file
fb08b14 chore: Create third and fourth files
enge 1&2 in readme file
fb08b14 chore: Create third and fourth files 
81d9eb0 chore: Create second file
930faf0 chore: Create initial file

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i HEAD~3
hint: Waiting for your editor to close the fi
Successfully rebased and updated refs/heads/main.

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
enge 1&2 in readme file
fb08b14 chore: Create third and fourth files
enge 1&2 in readme file
fb08b14 chore: Create third and fourth files 
81d9eb0 chore: Create second file
930faf0 chore: Create initial file

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i HEAD~4
hint: Waiting for your editor to close the fi
Successfully rebased and updated refs/heads/main.

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase --abort
fatal: no rebase in progress

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i HEAD~5
fatal: invalid upstream 'HEAD~5'

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git log --oneline
2dfb256 (HEAD -> main) Here is the change on format of ReadMe file.
c8ba4cf (origin/main) Here is codes for challenge 1&2 in readme file
fb08b14 chore: Create third and fourth files 
81d9eb0 chore: Create second file
930faf0 chore: Create initial file

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git branch
* main

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i HEAD~5
fatal: invalid upstream 'HEAD~5'

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rev-list --count HEAD
5

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase --abort
fatal: no rebase in progress

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i HEAD~5
fatal: invalid upstream 'HEAD~5'

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i 930faf0 chore: Create initial file
usage: git rebase [-i] [options] [--exec <cmd>] [--onto <newbase> | --keep-base] [<upstream> [<branch>]]
   or: git rebase [-i] [options] [--exec <cmd>] [--onto <newbase>] --root [<branch>]      
   or: git rebase --continue | --abort | --skip | --edit-todo

    --[no-]onto <revision>
                          rebase onto given branch instead of upstream
    --[no-]keep-base      use the merge-base of upstream and branch as the current base   
    --no-verify           allow pre-rebase hook to run
    --verify              opposite of --no-verify
    -q, --[no-]quiet      be quiet. implies --no-stat
    -v, --[no-]verbose    display a diffstat of what changed upstream
    -n, --no-stat         do not show diffstat of what changed upstream
    --stat                opposite of --no-stat
    --[no-]signoff        add a Signed-off-by trailer to each commit
    --[no-]committer-date-is-author-date     
                          make committer date match author date
    --[no-]reset-author-date
                          ignore author date and use current date
    -C <n>                passed to 'git apply'
    --[no-]ignore-whitespace
                          ignore changes in whitespace
    --[no-]whitespace <action>
                          passed to 'git apply'
    -f, --[no-]force-rebase
                          cherry-pick all commits, even if unchanged
    --no-ff               cherry-pick all commits, even if unchanged
    --ff                  opposite of --no-ff
    --continue            continue
    --skip                skip current patch and continue
    --abort               abort and check out the original branch
    --quit                abort but keep HEAD where it is
    --edit-todo           edit the todo list during an interactive rebase
    --show-current-patch  show the patch file being applied or merged
    --apply               use apply strategies to rebase
    -m, --merge           use merging strategies to rebase
    -i, --interactive     let the user edit the list of commits to rebase
    --[no-]rerere-autoupdate
                          update the index with reused conflict resolution if possible    
    --empty (drop|keep|stop)
                          how to handle commits that become empty
    --[no-]autosquash     move commits that begin with squash!/fixup! under -i
    --[no-]update-refs    update branches that point to commits that are being rebased    
    -S, --[no-]gpg-sign[=<key-id>]
                          GPG-sign commits   
    --[no-]autostash      automatically stash/stash pop before and after
    -x, --[no-]exec <exec>
                          add exec lines after each commit of the editable list
    -r, --[no-]rebase-merges[=<mode>]
                          try to rebase merges instead of skipping them
    --[no-]fork-point     use 'merge-base --fork-point' to refine upstream
    -s, --[no-]strategy <strategy>
                          use the given merge strategy
    -X, --[no-]strategy-option <option>      
                          pass the argument through to the merge strategy
    --[no-]root           rebase all reachable commits up to the root(s)
    --[no-]reschedule-failed-exec
                          automatically re-schedule any `exec` that fails
    --[no-]reapply-cherry-picks
                          apply all changes, even those already present upstream


Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i 930faf0^
fatal: invalid upstream '930faf0^'

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git branch --contains 930faf0
* main

Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git rebase -i --root
hint: Waiting for your editor to close the fihint: Waiting for your editor to close the fi
[detached HEAD c3056f1] chore: Create initial and second  file
 Date: Mon Jul 21 18:02:49 2025 +0200        
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md
 create mode 100644 test2.md
adme file
1ead9a4 chore: Create third and fourth files
c3056f1 chore: Create initial and second  file
```
### Challenge 4
```

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

Admin@MunezeroPC MINGW64 ~/Documents/Thegym-works(projects)/Works/Advanced-Git-Practices (main)
orks(projects)/Works/Advanced-Git-Practices (main)
$ git push origin main
Everything up-to-date
```