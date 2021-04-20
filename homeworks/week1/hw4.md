## 跟你朋友介紹 Git

Hello，菜哥你好。我嘗試整理了一下如何使用 Git。前些時候你跟我聊天，問我甚麼是 Git，然後要怎麼幫你的笑話進行版本控制，我嘗試簡單介紹 Git 並且教你如何學會操作。
 
# 一. Git 可以幫你解決甚麼問題

1.不用建立好幾個不同版本的檔案，像是 笑話 01 笑話 02 笑話 03 。只要把你想加入版本控制的資料夾或檔案加入 Git，就可以運用程式幫你完成這些惱人的工作。而且還可以隨時切換呢！

# 二. 安裝 Git

[Git程式連結](https://git-scm.com/)

裝好之後，點開使用命令列操作介面的 Git Bash 就算開啟成功了。

# 三. 版本控制文件步驟

我以自身在使用的 windows 作業系統來做示範。

首先要設定作用 Git Bash 的路徑。查看自己當前目錄的路徑。( pwd : print working directory ) 
```
$ pwd
/c/Users/USER
```

切換目錄到想要存放你個人工作目錄的地方，先存到我的桌面好了。( cd : change directory )
```
$ cd /d/desktop
```

為笑話集建立一個工作目錄。( mkdir : make directory )
```
$ mkdir my_joke_collection
```

切換 Git Bash 作用目錄到笑話集裡面。
```
$ cd my_joke_collection
```

建立一個笑話集的 .txt 檔案，叫做 my_joke.txt。
```
$ touch my_joke.txt
```

我先打開文件新增一個笑話之後當版本控制舉例。

笑話 1 :有一天有個帥哥走在路上，一個阿嬤突然上前搭訕說「帥哥，你超會搭耶」，然後帥哥就冒煙了。

使用 git 做版本控制前要先設定使用者名稱和 email ，因為當你提交版本的時候，它會需要記錄這些資料。
```
$ git config --global user.name "你的使用者名稱"
$ git config --global user.email "你的 Email"
```

查看 git 設定狀態
```
$ git config --list
```

將 git 版本控制文件初始化到工作目錄。( init : initialization )
```
$ git init
Initialized empty Git repository in D:/desktop/my_joke_collection/.git/
```

使用 git status 檢查 git 當前版本控制狀態。
```
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        my_joke.txt

nothing added to commit but untracked files present (use "git add" to track)
```

上面顯示我們的 my_joke.txt 檔案還沒被加入 git 控制內 (untrack file)，所以我們使用 git add 把它加進去。(track)
```
$ git add my_joke.txt
```

再次確認此工作目錄底下 git 作用的狀態。
```
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   my_joke.txt
```

當檔案從 Untracked files 變成 Changes to be committed ，就可以準備提交第一個笑話集版本了。(輸入 -m " " 給這個版本一個訊息名稱) 
```
$ git commit -m "my_joke_version_01"
On branch master
nothing to commit, working tree clean
```

用 git log 查看目前版本控制 commit 狀態
```
$ git log
commit 6fc1ef4aa1494fd64ad796c8330c68386b126ad6 (HEAD -> master)
Author: Aom_Jack <jack00601@gmail.com>
Date:   Tue Apr 20 09:22:24 2021 +0800

    my_joke_version_01
```

6fc1e 後面一堆亂數是這個版本的亂數號，確保它的版本名稱不會跟其他檔案重複。

假如說你今天打開文件新增了一個笑話，想要再度使用 git 提交新版本的話，步驟跟上面一樣，但我們這次跳過 add ，把它簡化在 commit -am 一起提交 ( 但此操作不適用新創的檔案 )。

笑話 2 : 有一天小明他爸很渴，就叫小明幫他倒水，但小明遲遲沒去倒。小明爸就說：「你是要逼爸渴死嗎？」，於是小明就開始 B Box 了。

一樣先檢查 git 作用狀態
```
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   my_joke.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

輸入 git commit -am "my_joke_version_02" 
```
$ git commit -am "my_joke_version_02"
[master c6a77cd] my_joke_version_02
 1 file changed, 3 insertions(+), 1 deletion(-)
```

再次 git log 查看 
```
$ git log
commit c6a77cdd52053e4fdfe52005403063bdf7bb6872 (HEAD -> master)
Author: Aom_Jack <jack00601@gmail.com>
Date:   Tue Apr 20 14:41:21 2021 +0800

    my_joke_version_02

commit 6fc1ef4aa1494fd64ad796c8330c68386b126ad6
Author: Aom_Jack <jack00601@gmail.com>
Date:   Tue Apr 20 09:22:24 2021 +0800

    my_joke_version_01
```

這樣就簡單新創了另一個版本了 !

如果要切換版本，使用 git checkout "輸入亂碼列" 。 
```
$ git checkout 6fc1ef4aa1494fd64ad796c8330c68386b126ad6
Note: switching to '6fc1ef4aa1494fd64ad796c8330c68386b126ad6'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 6fc1ef4 my_joke_version_01
```

這樣就切換到了第一個 my_joke_version_01 的版本了。了解上面的操作，你只要建立一個檔案就好，而 git 會幫你完成切換版本的功能，你就不用再創立很多個檔案了。

如果後續有任何問題請再跟我說，很樂意幫你解決。










 




