##Git Exercises
###Challenge1 &2
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