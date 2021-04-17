## 教你朋友 CLI

CLI 英文名稱叫做 Command Line Interface，中文名稱為命令字元列介面，是透過文字命令與電腦進行溝通的工具。
我們平常習慣的圖形化使用者介面 (Graphical User Interface) 也就是透過點擊圖示，觸發不同及讀取大量的 Command Line 讓電腦可以執行我們要讓它做的事情。
不同的作業系統 (Operation System) 都有自己家不同的 Command Line 指令型態。像是 Windows NT 的預設 CLI 叫做 CMD.EXE，而 MacOS 的預設則是 Zsh (支援 bash 功能)， Linux 系統則是 Bash 。
這樣你大概初步了解甚麼是 CLI 了吧！
今天來教你怎麼用 bash 創建你想要的資料夾名稱和檔案 (如果你的電腦作業系統是 Windows，可以去搜尋怎麼在 Windows 系統環境底下安裝 bash，像是以下這個部落格連結 [Windows 10 運行 Ubuntu Linux 的 Bash Shell 原生執行環境教學](https://blog.gtwang.org/windows/how-to-get-ubuntu-and-bash-running-on-windows-10/) ) 
因為我的電腦作業系統是 Windows ， 所以我選擇依照上面的部落格連結安裝 Ubuntu Linux 以模擬 bash 的 CLI，另外附上微軟官方文件的安裝指南 [Windows 10 上適用於 Linux 的 Windows 子系統安裝指南](https://docs.microsoft.com/zh-tw/windows/wsl/install-win10#manual-installation-steps) 你也可以跟著操作。
操作步驟 :
1. 在 Windows 上搜尋 ubuntu 把它打開
2. 設定絕對路徑到桌面 : cd /mnt/d/desktop ，比較方便觀看你想要的檔案。
3. 建立 wifi 資料夾 : mkdir wifi 
4. 切換路徑至 wifi 資料夾底下 : cd wifi
4. 建立名為 afu.js 的檔案 : touch afu.js

這樣就大功告成啦 !! 

