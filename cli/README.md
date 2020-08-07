# cli-作業回答
# 前言
相信大家看過很多電影裡面的帥氣駭客們，總是在黑底白字的介面前面輸入指令操控著電腦。 身為一個工程師，我們當然也要立志當帥氣的工程師，既然如此就得好好學學怎麼使用這烏漆抹黑的介面。

# 推薦學習資源
[鳥哥的 Linux 私房菜](https://linux.vbird.org/linux_basic/centos7/)

# 問題

### 名詞解釋

- GUI vs CLI
  - GUI
    - Graphical User Interface -> 圖形化用戶介面，比較直觀 
  - CLI
    - Command Line Interface -> 命令行介面，比較精準
  - 比較 
    - CLI比GUI更早出現，因前者技術上更容易實現。GUI於1980年首次出現。1983 Apple公司是第一家使用GUI的商品化電腦(Apple Lisa)
  ; 1985 Windows推出基於DOS的GUI作業系統(Windows1.0)。 
  - Resources:
    - [名詞解釋wiki](https://zh.m.wikibooks.org/zh-tw/Ubuntu/GUI%E4%B8%8ECLI%E4%B9%8B%E4%BA%89)
    - [GUI vs CLI](http://www.cnitblog.com/addone/archive/2008/01/08/38581.html) 

- terminal
  - 用來與電腦溝通的橋樑。用來輸入、輸出資料。 
  - [Resources](https://www.wikiwand.com/en/Computer_terminal)
  - [Why terminal](https://dev.to/nrobinson2000/why-you-need-terminal-bpd)

- shell
    - bash
      - Bourne Again Shell
        - Improved sinced its first release 1989
        - The default shell of most linux distributions
    - zsh
      - Z shell
      - Created by Paul Falstad in 1990
    - even more: Tcsh, Ksh, Fish
    - Resources:
      - [Resources-1](https://www.tecmint.com/different-types-of-linux-shells/)
      - [Resources-2](https://www.howtogeek.com/68563/htg-explains-what-are-the-differences-between-linux-shells/)
- Terminal vs console vs shell
  - Terminal 是輸入/輸出的環境(從硬體借過來的說法)，透過terminal去操作shell
  - console 是實體的terminal
  - shell 命令列解釋器
  - 用法e.g.
    - 開啟terminal來執行shell
  - Resources
    - [Resources-1](https://askubuntu.com/questions/506510/what-is-the-difference-between-terminal-console-shell-and-command-line)
    - [Resources-2](https://www.hanselman.com/blog/WhatsTheDifferenceBetweenAConsoleATerminalAndAShell.aspx)

### 請解釋下方 CLI 的指令作用
    
- `cat` 
  - 用來連結與印出檔案 

- `cd` 
  - 切換路徑

- `chgrp`
  - 改變團體
  - `chgrp -R jeff /usr/jeff14994`
    - 將/usr/jeff14994及其子目錄下的所有文件用戶改為jeff 

- `chown`
  - 更改檔案使用者與團體
  - `sudo chown jeff myfile`
    - 將myfile擁有者改為jeff
  - `sudo chown :mygroup myfile`
    - 將myfile的群組改為mygroup

- `chmod`
  - 改變檔案模式或存取權限

- `cp` 
  - 複製檔案
  - `cp -R ./source_file ~/destination_file`
    - 將底下所有的檔案複製到destination_file 

- `curl` 
  - 傳送URL

- `less` 
  - less 是 more加上更多優點
  - [Resources](https://unix.stackexchange.com/questions/81129/what-are-the-differences-between-most-more-and-less)
- `ls` 
  - 顯示檔案內容
  - 搭配xargs可以從文件輸出吃參數
    - `find /sbin -perm +700 | xargs ls -l`
- `man`
  - format and display online manual pages
- `mkdir` 
  - 新建空資料夾    
- `mv` 
  - 移動資料夾與更改資料夾名稱

- `grep` 
  - 資料夾規律搜尋

- `|` 
  - 管線命令
  - 上一個指令的輸出可以變成下一個指令的輸入

- `pwd` 
  - 顯示當前的使用者在哪一個資料夾

- `rm` 
  - 刪除資料
  - `rm -rf `
    - 用來刪除資料夾 
- `touch` 
  - 新建檔案
- `vim` 
  - 檔案編輯器
  - vi 的增強版(vim: vi improved)
  - nvim 是vim 的更加強版(nvim: new vim)
- 小時候整理的linux指令
  - https://imgur.com/Qu4gU0Z
### 請說明以下 Linux file system structure 

- [Resources](https://www.tldp.org/LDP/intro-linux/html/sect_03_01.html)

- `/` 
  - 根目錄

- `/bin` 
  - 存放可執行檔的地方

- `/etc` 
  - 系統配置檔

- `/home` 
  -  使用者目錄

- `/lib` 
  - 函式庫

- `/var` 
  - 存放執行時資訊的地方
- `/sbin` 
  - 系統執行檔

- `/srv` 
  - 包含特定網站的訊息
  - [Resources](https://www.tldp.org/LDP/Linux-Filesystem-Hierarchy/html/srv.html)
- `/tmp`
  - 暫存區
  - 所有人都有權存取
- `/usr`
  - 存放許多Linux系統檔案
