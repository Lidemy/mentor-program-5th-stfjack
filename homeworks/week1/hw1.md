## 交作業流程

# 步驟
1. 打開 Huli 老師的鋰學院網址 [Lidemy](https://lidemy.com/) 
2. 如果你已經是第五期學生，找到 [MTR05 程式導師實驗計畫第五期](https://lidemy.com/courses/1360789/lectures/31705020) 這個課程
3. 點開**寫作業與交作業流程**中的**如何交作業**教學影片
4. 至最上方整理之網址 [GitHub Classroom](https://classroom.github.com/a/yNNrtNyW) 接受建立作業資料庫的邀請
5. 安裝版本控制軟體 [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) 
6. 打開 Git bash ，設定好自己想要存放作業的地方，創立作業用資料夾:`mkdir lidemy repository` 。
7. 切換指令作用位置:`cd lidemy repository`
8. 至剛剛於 Git classroom 開通在 lidemy 底下的個人 repository [Lidemy/mentor-program-5th-stfjack](https://github.com/Lidemy/mentor-program-5th-stfjack) 遠端複製(clone)檔案到本地主機:`git clone https://github.com/Lidemy/mentor-program-5th-stfjack.git`
9. 切換資料夾位置至下載好的子目錄:`cd mentor-program-5th-stfjack`
10. 初始化 Git 進行版本控制:`git init`
11. 檢查是否有 untracked file :`git status`
12. 如果有，則添加檔案:`git add file name` 或是 `git add ..`添加全部至staged版本控制狀態。
11. 創立一個新的 branch :`git branch week1`
12. 將主幹從 master 轉移至 branch :`git checkout week1`
13. 打開 week1 內的 hw 檔案做作業。
14. 當取得階段性的目標完成，提交 commit 新版本:，參照此網站 [連猴子都能懂的 Git 入門指南](https://backlog.com/git-tutorial/tw/reference/basic.html#sec2) :`git commit -am'hw1_finished'`
15. 提交作業前先檢查 commit 狀態:`git log`
16. 提交作業前先檢查 branch 狀態是否在 week1 分支:`git branch -v`
17. 從本地主機提交作業 ( push )至 Github (步驟 8 列出的網址上):`git push origin week1`
18. 重新整理步驟 8 的網站
19. 點選 Pull Requests (在 git hub 上把 week1 的 branch merge 到 master) ，可以leave a comment ，確認沒問題就 Create pull request 。
20. 如果要修改內容，可以在本地主機的檔案進行修改並且主要 branch 一樣在 week1 中進行，然後 push 到 Github 就可以完成修正。
21. 發 PR 到 lidemy 學習系統的課程總覽上每一周進行繳交作業 ， 網址就是lidemy底下的個人 repository 的 pull requests [https://github.com/Lidemy/mentor-program-5th-stfjack/pulls] (https://github.com/Lidemy/mentor-program-5th-stfjack/pulls)
22. 在學習系統上的作業列表，檢查作業是否繳交成功。

