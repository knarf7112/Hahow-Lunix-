# Linux 我來教: CentOS/ RHEL 8 新世代雲端
## [課程官網](https://hahow.in/courses/5e6dd4fe024d690024e3be3e/discussions?item=5e6de2ac024d690024e3c24d)

## 第 1 章 認識與建置 Linux
### 單元 1 - 什麼是 Linux? 有很多種 Linux，特色是什麼？
  * [Linux](https://zh.wikipedia.org/zh-tw/Linux) 1991年誕生, 由UNIX衍生
  * [distrowatch](https://distrowatch.com/)網站提供目前各類Linux發行版本的統計資料
  * 發行版本是基於Linux的核心之外,再加上一些自己合用的套件與安裝的管理介面
  * [CENTOS官方網站](https://www.centos.org/)提供許通版本選擇

### 單元 2 - Linux的國際認證
  * 四大階段
      1. 操作: 懂得活用指令操作並了解知識與原理
      2. 管理: 例如:防火牆, 檔案系統, 帳號, 權限...等等
      3. 服務: 如何控制Linux裡面的服務,如何安裝好套件,如何做好一些安全性規則
      4. 解決問題: 能不能解決Linux裡面發生的一些問題,提出一些解決方案
  * 國際認證: LPIC(Linux Professional Institute), 屬於加拿大非營利單位
      * 101 (Level 1: 筆試)
      * 201,202 (Level 2: 上機考試)
      * 301, 302~306(Level 3: 上機考試):提供解決方案
  * 紅帽的國際認證: RHCSA -> RHCE
 
### 單元 3 - 什麼是光碟映像檔(ISO)?
  * 廠商釋出作業系統時,以檔案的格式釋出開機光碟,此特殊檔案是模擬一張光碟片,所以就稱為映像檔ISO格式.

### 單元 4 - 虛擬機器軟體安裝 VirtualBox : Windows
  * 虛擬機器: 在我們的電腦內安裝一個軟體,用來模擬另外一台機器的一個機制
  * 市面上常見的軟體有 VMware, [VirtualBox](https://www.virtualbox.org/)(由Sun公司發起) 這兩套軟體,點選下載平台(Windows hosts)並安裝![download](https://i.imgur.com/bP68R6q.png)
  * 安裝過程就是一直下一步,可能會需要管理員權限,因為需要設定網路相關的設定![](https://i.imgur.com/uieqT0H.png)
  * 接者下載[CentOS 8](https://www.centos.org/download/)-->x86_64-->找DVD版本(約7gb)
  * 安裝 Red Hat 8 企業版: browser search --> [rhel 8](https://www.redhat.com/en/enterprise-linux-8) --> try it -> 試用企業版需要有帳號 -> id:knock7112@gmail.com pw:g4ru87112

### 單元 5 - 虛擬機器軟體安裝 VirtualBox : MacOS
  * MAC的VM安裝會被安全性所阻擋所以需要設置安全性(允許來自開發者Oracle America.Inc的系統軟體)

### 單元 6 - 安裝 CentOS 8.1 與瞭解磁碟分割區
  1. VirtualBox選單按下"**新增**"按鈕,就可以建立虛擬機器(類型選Linux,版本選Red Hat(64bit)),預設會安裝在C槽Users資料夾下的VirtualBox VMs資料夾內
  2. 設定記憶體至少8GB
  3. 建議硬碟使用預設的"立即建立虛擬硬碟"即可
  4. 使用預設的VDI格式(VirtualBox磁碟映像)
  5. 選擇"動態分配"
  6. 檔案位置和大小建議配置"20GB"硬碟空間
  7. 按下"建立"按鈕,即完成配置
  8. 接者點擊完成配置後的虛擬機器查看硬體配置內容並點擊選單"設定"按鈕 --> 存放裝置 -->控制器IDE (裡面顯示"空的") --> 點擊光碟機右方的光碟片圖示 --> 選擇磁碟檔 --> 設定下載好的ISO檔案 --> CentOS-8.2.2004-x86_64-dvd1.iso --> 點擊"確定"按鈕完成設定ISO檔配置
  9. 點擊選單"啟動"
  10. 當點選虛擬機器內的畫面時,滑鼠控制權會轉移到虛擬機器上,控制權無法離開,會提示要離開虛擬機器畫面需要按下右方的Ctrl才能離開
  * 進入CentOS作業系統的安裝,安裝步驟
      1. 選擇語系: ->台灣 選擇->繁體
      2. 選擇地區: ->台北
      3. 外掛軟體選擇: window檔案伺服器,除錯工具,檔案與儲存伺服器,網路檔案系統,網路伺服器,效能工具,基本網站伺服器,Legacy UNIX相容性,RPM開發工具,科學支援,安全性工具,系統工具
      4. 安裝目的地: 勾選本機標準磁碟(Linux沒有C,D,E潮概念,只有根目錄"/"),儲存裝置組態選擇"自訂" -> 手動處理分割 -> 分割規劃選擇"標準分割區" -> 點案這裡讓系統自動建立 -> 點選"/" -> 欲使用容量改成13GB -> 點選"+"設定"/var"的磁碟配置空間4GB ->完成 ->接受變更
      5. 網路與主機名: 乙太網路點選"開"(預設會使用10.0.2.15/24的配置,使用NAT)
      6. 點擊開始安裝 -> 設定根密碼(root為超級管理員) -> 創建用戶 -> knock -> 勾選讓此使用者成為管理員
      7. 安裝完成後,先將光碟機內的映像檔卸載,再點擊重新開機
  * 登入CentOS系統,使用剛剛設定的帳密,先跳過線上帳號的設定
  * 進入桌面後右側選單較常使用"終端機"來輸入命令,輸入`ifconfig`(這是舊指令,用來顯示目前Linux的網路狀態)或是輸入`ip a`(這是新指令,也是查詢網路狀態用的)
  * 想關機可以選擇右上方的按鈕->點選關機鈕-> "關閉電源"  

### 單元 7 - 安裝 Red Hat 企業版 Linux 8.2 (RHEL)
  * 安裝過程和CentOS幾乎一樣,只有最後要訂閱"RedHat軟體更新服務"不太一樣
  * 教學視訊將軟體全部選擇原本預設的配置,只有"網路部與主機名稱"需要手動按"開"啟
  * 選單多了一個叫做"CONNECT TO RED HAT",點選後進入配置並將在Red Hat官網登入時使用的帳密輸入,完成按register,會開始連到官方,完成訂閱後會以這台主機連結到red hat這個服務
  * "軟體選擇"會跳出來源已變更,再按一次確認
  * 檢查選單的"Connect to Red Hat"顯示"Registered"
  * 按下"開始安裝"並設定root密碼與新創用戶帳密
  * 完成安裝後,按下"重新開機"按鈕前,先將映像檔強制卸載,與CentOS操作一樣
  * 登入作業系統後唯一差異是會有顯示red hat的訂閱服務,完成基本設定後
  * 會有個System Registered的提示,點擊"Register System",會跳出Red Hat的訂閱畫面(這是唯一和CentOS不同的東西,其他全都一樣)

### 單元 8 - VirtualBox 的網路設定與遠端登入
  * 因為使用VirtualBox網路的關係,所以在CentOS的終端機內輸入`ip a`顯示的網路設備叫"enp0s3",ip是"10.0.2.15",像這樣的網址表示VirtualBox對目前的模擬器所使用的網路是NAT,從模擬器內部OS連到外部網路沒問題,但外部網路如果要連到模擬器內的主機是無法的,因為linux處於內部的虛擬網路,先關閉主機電源
  * 打開VirtualBox的設定畫面 -> 點選"網路" -> 目前"附加到"的設定裡面應該顯示"NAT" -> 選擇橋接介面卡(讓VirtualBox去抓實體主機上的網路卡當名稱,外部window的網路介面卡會產生新的設定,都會影響內部Linux抓IP的位置) -> 啟動
  * 再登入一次去終端機輸入`ip a`再檢視一次目前IP位置,應該會改成與外部主機類似的IP"192.168.1.111"(DHCP分配給的)
  * 一般會使用遠端服務連入Linux主機, linux預設會自動啟動一個服務"SSH",是加密的遠端登入工作  
    使用一些工具就可以連線到Linux內,遊覽器輸入pietty來下載,使用SSH客戶端的中文版,解壓並執行  
    輸入Linux的主機IP"192.168.1.111",類型選擇SSH,第一次連線會跳出提示,選擇是會儲存SSH的public key,接下來輸入帳號與密碼登入OS
  * Pietty中文顯示亂碼問題: "選項"->字元編碼->改成Unicode, "選項"->亞洲語系修正->"Unicode亞洲寬符號字元"取消勾選 -> 重開軟體再登入看看
    
## 第 2 章 Linux 基礎操作指令
### 單元 1 - Linux的開機過程
  1. 載入機器裡面的BIOS/UEFI(新式介面)來檢測硬體
  2. 找開機磁碟機的讀取程序"bootloader",硬碟啟動後選擇要載入哪一個分割區的作業系統用的,  
     他會去使用Lnux裡面的GRUB,這是Linux所使用的開機管理程式,  
     若硬碟內有多個作業系統,可提供作業系統的選單,  
     當系統出問題時,也可透過GRUB的一個設定來進入單人模式,進行系統修復,例如:忘了root密碼
  3. 載入**Kernal核心**,就是使用者和電腦之間溝通的重要程式,會在"bootloader"開機時就讀入記憶體中執行
  4. 系統接者自動執行一個服務"system",這是近年來採用的服務名稱,舊linux叫"init"服務.  
     此服務會因為我們設定linux是文字介面或是圖形介面來讀取不同的執行程式,若設定文字介面的開機,就會開在文字介面中,如同Pietty一樣,圖形介面則是由"X-Window"來處理UI上的使用者互動效果  
     CentOS和Red hat使用的圖形介面是叫"GNOME"
  *  當我們在系統中完成一些指令或是管理工作後,記得要使用指令"`logout`"登出系統

### 單元 2 - 指令操作、變身為超級使用者
  * 登入成功之後最重要的是前面的帳號資訊`[knock@localhost ~]$` 這個叫做命令提示字元(prompt)
  * linux的命令提示字元有個特殊情況,就是超級使用者和一般使用者是不一樣的.  
    一般使用者的中括號內的@前面表示登入者帳號,@後面表示主機名稱.  
    而空白後面的波浪符號的位置是目前所在的資料夾位置,在linux中的"~"表示自己的家,也就是家目錄,也就是knock這個使用者的家目錄之下
  * 輸入`pwd`命令(Present Working Directory)可以獲得當前目錄的工作路徑 
    ```bash=
    [knock@localhost ~]$ pwd
    /home/knock
    [knock@localhost ~]$
    ```
  * 有些指令是不會有回應的
  * 切換**超級使用者**輸入`su -`指令(Super user),輸入完按enter後會需要輸入密碼  
    輸入完成後提示字元的@前面會變成root,而原本的"$"字號會變成"#",是在提醒使用者已經切換成超級使用者
    ```bash=
    [knock@localhost ~]$ su -
    password:
    [root@localhost ~]#
    ```
  * 輸入`whoami`指令來查詢我是誰
    ```bash=
    [knock@localhost ~]$ whoami
    knock
    ```
  * 切換回來就輸入`exit`就會回到原來的腳色,可以用`whoami`指令確認當前使用者
  * `su -`也可以省略不輸入空白減號` -`,差異是只輸入`su`會仍然使用"knock"的環境變數,不會切換成"root"自己的環境變數.   
    因為使用者都有他獨特的環境變數,而系統的環境變數大都以全大寫的方式來命名
    ```bash=
    [knock@localhost ~]$ echo $PATH
    /home/knock/.local/bin:/home/knock/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/root/bin
    
    //未使用空白減號 -> 仍然使用knock的環境變數
    [knock@localhost ~]$ su
    password:
    [root@localhost knock]# echo $PATH
    /home/knock/.local/bin:/home/knock/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/root/bin
    
    
    //使用空白減號 -> 使用root的環境變數
    [knock@localhost ~]$ su -
    password:
    [root@localhost ~]# echo $PATH
    /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/root/bin
    ```
  * 清除畫面使用`clear`指令,或是輸入Ctrl+L鍵也可以清除畫面

### 單元 3 - 基礎資料夾切換、列表、別名
  * linux中切換資料夾要輸入`cd `指令,cd後面一定要加空白,因為後面可以接其他參數
  * linux中有兩個特殊符號`.`和`..`,直接輸入`cd .`是沒效果的.
    `.`代表是目前的資料夾,`..`代表是上一層資料夾
    ```bash=
    [knock@localhost ~]$ pwd
    /home/knock
    
    //目錄位置不變
    [knock@localhost ~]$ cd .
    
    
    //(相對位置的切換)切換到上一層資料夾
    [knock@localhost ~]$ cd ..
    [knock@localhost home]$ pwd
    /home
    [knock@localhost home]$ cd ..
    [knock@localhost /]$ pwd
    /
    
    //(絕對位置的切換,開頭使用根目錄"/")直接輸入cd /指定路徑
    [knock@localhost ~]$ cd /var
    [knock@localhost var]$ pwd
    /var
    
    //回到家目錄"~"
    [knock@localhost var]$ cd ~
    [knock@localhost ~]$
    ```
  * `ls`指令會列出目前資料夾下的檔案清單,藍色字體的資料夾,需要知道詳細內容輸入`ls -l`
    ```bash=
    [knock@localhost ~]$ ls
    下載  公共  圖片  影片  文件  桌面  模板  音樂
    [knock@localhost ~]$


    [knock@localhost ~]$ ls -l
    總計 0
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 下載
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 公共
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 圖片
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 影片
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 文件
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 桌面
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 模板
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 音樂
    [knock@localhost ~]$


    // 輸入指令ls -a才會把隱藏檔或是系統檔或隱藏資料夾都顯示出來(命令可以合併`ls -la`)
    [knock@localhost ~]$ ls -l -a
    總計 32
    drwx------. 15 knock knock 4096 10月 11 21:51 .
    drwxr-xr-x.  3 root  root    19 10月 11 20:11 ..
    -rw-------.  1 knock knock   24 10月 11 22:28 .bash_history
    -rw-r--r--.  1 knock knock   18 11月  9  2019 .bash_logout
    -rw-r--r--.  1 knock knock  141 11月  9  2019 .bash_profile
    -rw-r--r--.  1 knock knock  312 11月  9  2019 .bashrc
    drwx------. 11 knock knock  256 10月 11 20:41 .cache
    drwx------. 13 knock knock  250 10月 11 20:41 .config
    -rw-------.  1 knock knock   16 10月 11 20:19 .esd_auth
    -rw-------.  1 knock knock  624 10月 11 21:51 .ICEauthority
    drwx------.  3 knock knock   19 10月 11 20:19 .local
    drwxr-xr-x.  4 knock knock   39 10月 11 20:03 .mozilla
    drwxrw----.  3 knock knock   19 10月 11 20:19 .pki
    -rw-r--r--.  1 knock knock  658  3月 21  2020 .zshrc
    drwxr-xr-x.  2 knock knock    6 10月 11 20:19 下載
    drwxr-xr-x.  2 knock knock    6 10月 11 20:19 公共
    drwxr-xr-x.  2 knock knock    6 10月 11 20:19 圖片
    drwxr-xr-x.  2 knock knock    6 10月 11 20:19 影片
    drwxr-xr-x.  2 knock knock    6 10月 11 20:19 文件
    drwxr-xr-x.  2 knock knock    6 10月 11 20:19 桌面
    drwxr-xr-x.  2 knock knock    6 10月 11 20:19 模板
    drwxr-xr-x.  2 knock knock    6 10月 11 20:19 音樂

    ```
  * linux有準備一個叫`alias`的指令來讓很長一串的指令可以設定成另一個別名來縮短輸入
    ```bash=
    [knock@localhost ~]$ alias
    alias egrep='egrep --color=auto'
    alias fgrep='fgrep --color=auto'
    alias grep='grep --color=auto'
    alias l.='ls -d .* --color=auto'
    alias ll='ls -l --color=auto'
    alias ls='ls --color=auto'
    alias vi='vim'
    alias which='(alias; declare -f) | /usr/bin/which --tty-only --read-alias --read-functions --show-tilde --show-dot'
    alias xzegrep='xzegrep --color=auto'
    alias xzfgrep='xzfgrep --color=auto'
    alias xzgrep='xzgrep --color=auto'
    alias zegrep='zegrep --color=auto'
    alias zfgrep='zfgrep --color=auto'
    alias zgrep='zgrep --color=auto'
    [knock@localhost ~]$
    ```
  * `ls -l /`後方可以輸入指定路徑來依據指定的路徑查詢檔案清單
    ```bash=
    [knock@localhost ~]$ ls -l /
    總計 24
    lrwxrwxrwx.   1 root root    7  5月 11  2019 bin -> usr/bin
    dr-xr-xr-x.   6 root root 4096 10月 11 20:18 boot
    drwxr-xr-x.  19 root root 3140 10月 11 21:50 dev
    drwxr-xr-x. 149 root root 8192 10月 11 21:50 etc
    drwxr-xr-x.   3 root root   19 10月 11 20:11 home
    lrwxrwxrwx.   1 root root    7  5月 11  2019 lib -> usr/lib
    lrwxrwxrwx.   1 root root    9  5月 11  2019 lib64 -> usr/lib64
    drwxr-xr-x.   2 root root    6  5月 11  2019 media
    drwxr-xr-x.   2 root root    6  5月 11  2019 mnt
    drwxr-xr-x.   2 root root    6  5月 11  2019 opt
    dr-xr-xr-x. 248 root root    0 10月 11 21:50 proc
    dr-xr-x---.   5 root root  205 10月 12 00:56 root
    drwxr-xr-x.  47 root root 1340 10月 11 21:51 run
    lrwxrwxrwx.   1 root root    8  5月 11  2019 sbin -> usr/sbin
    drwxr-xr-x.   2 root root    6  5月 11  2019 srv
    dr-xr-xr-x.  13 root root    0 10月 11 21:50 sys
    drwxrwxrwt.  14 root root 4096 10月 12 01:30 tmp
    drwxr-xr-x.  12 root root  144 10月 11 20:03 usr
    drwxr-xr-x.  23 root root 4096 10月 11 20:18 var
    [knock@localhost ~]$

    ```
 
### 單元 4 - Linux主要目錄與辨讀權限
  * Linux的根目錄有幾個主要的目錄是比較重要的,只有root這個權限才能進入作特殊操作
    1. `bin`: 表示可執行檔,也就是內容是binary機器碼的檔案, 對應到usr/bin目錄
    2. `sbin`: 放系統管理相關的可執行檔(super user binary),此為系統管理員專用的執行檔, 例如:關機, 網路管理, 改變磁碟機...
    3. `etc`: 放所有系統設定檔,大都是純文字檔,只有系統管理員可修改這些檔案
    4. `dev`: 放系統設備(device)或裝置相關的檔案
    5. `home`: 所有使用者的家目錄, linux上有多少個帳號,此目錄下就會有多少個使用者目錄
    6. `root`: 系統管理員(超級使用者 super user)root的家目錄
    7. `usr`: 套件軟體(packages)大部分都安裝在此目錄下
    8. `var`: 放變動性高或系統等待排隊處理的檔案, 例如: 登入系統產生的log,連線log, email fail log,資料庫的數據 ...
    9. `opt`: 非linux預設安裝的外來軟體
  * `ls -l /`檔案列表的說明
    ```bash=
    [knock@localhost ~]$ ls -l /
    總計 24
    lrwxrwxrwx.   1 root root    7  5月 11  2019 bin -> usr/bin
    // bin: 表示可執行檔,也就是內容是binary機器碼的檔案, 對應到usr/bin目錄
    dr-xr-xr-x.   6 root root 4096 10月 11 20:18 boot
    drwxr-xr-x.  19 root root 3140 10月 12 12:49 dev
    // dev: 放系統設備(device)或裝置相關的檔案
    drwxr-xr-x. 149 root root 8192 10月 12 12:49 etc
    // etc: 放所有系統設定檔,大都是純文字檔,只有系統管理員可修改這些檔案
    drwxr-xr-x.   3 root root   19 10月 11 20:11 home
    // home: 所有使用者的家目錄, linux上有多少個帳號,此目錄下就會有多少個使用者目錄
    lrwxrwxrwx.   1 root root    7  5月 11  2019 lib -> usr/lib
    lrwxrwxrwx.   1 root root    9  5月 11  2019 lib64 -> usr/lib64
    drwxr-xr-x.   2 root root    6  5月 11  2019 media
    drwxr-xr-x.   2 root root    6  5月 11  2019 mnt
    drwxr-xr-x.   2 root root    6  5月 11  2019 opt
    dr-xr-xr-x. 184 root root    0 10月 12 12:49 proc
    dr-xr-x---.   5 root root  205 10月 12 00:56 root
    // root: 系統管理員(超級使用者 super user)root的家目錄
    drwxr-xr-x.  46 root root 1320 10月 12 12:49 run
    lrwxrwxrwx.   1 root root    8  5月 11  2019 sbin -> usr/sbin
    // sbin: 放系統管理相關的可執行檔(super user binary),此為系統管理員專用的執行檔, 例如:關機, 網路管理, 改變磁碟機...
    drwxr-xr-x.   2 root root    6  5月 11  2019 srv
    dr-xr-xr-x.  13 root root    0 10月 12 12:49 sys
    drwxrwxrwt.  12 root root 4096 10月 12 12:59 tmp
    drwxr-xr-x.  12 root root  144 10月 11 20:03 usr
    // usr: 套件軟體(packages)大部分都安裝在此目錄下
    drwxr-xr-x.  23 root root 4096 10月 11 20:18 var
    [knock@localhost ~]$
    ```
  *  [Linux檔案屬性](http://linux.vbird.org/linux_basic/0210filepermission.php)  
    ![Linux檔案屬性](./pics/Linux檔案屬性.png "Linux檔案屬性")
  * 在linux環境內與機器的互動會有一支shell程序來跟linux作互動叫"bash"
    ![shell](./pics/shell.png)
  * 在linux可執行檔案沒有所謂的附檔名(.exe),而是要看檔案屬性是否有"x"可執行的狀態  
    可執行檔都放在**根目錄的bin**之下
    ```bash=
    [knock@localhost ~]$ ls /bin | more
    [
    ab
    abrt-action-analyze-backtrace
    abrt-action-analyze-c
    abrt-action-analyze-ccpp-local
    abrt-action-analyze-core
    abrt-action-analyze-oops
    abrt-action-analyze-python
    abrt-action-analyze-vmcore
    abrt-action-analyze-vulnerability
    abrt-action-analyze-xorg
    abrt-action-check-oops-for-alt-component
    abrt-action-check-oops-for-hw-error
    abrt-action-generate-backtrace
    abrt-action-generate-core-backtrace
    abrt-action-install-debuginfo
    abrt-action-list-dsos
    abrt-action-notify
    abrt-action-perform-ccpp-analysis
    abrt-action-save-package-data
    abrt-action-trim-files
    abrt-cli
    abrt-dump-journal-core
    ...
    ```
### 單元 5 - 關機與重啟系統，sudo指令
  * 如何查看線上有多少使用者已經登入在系統中可用`w`指令,或用`who`指令
    ```bash=
    [root@localhost ~]# w
    14:02:55 up  1:13,  2 users,  load average: 0.00, 0.02, 0.00
    USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU WHAT
    knock    pts/0    192.168.1.104    13:03    4.00s  0.08s  0.08s -bash
    root     pts/1    192.168.1.104    14:02    0.00s  0.02s  0.00s w
    [root@localhost ~]# who
    knock    pts/0        2020-10-12 13:03 (192.168.1.104)
    root     pts/1        2020-10-12 14:02 (192.168.1.104)
    [root@localhost ~]#
    ```
  * 重新啟動機器的指令是`shutdown`  
    使用系統管理員作關機操作和取消關機操作
    ```bash=
    // -h : (halt)表示直接關機, 10:表示10分鐘後才關機(進入排程), 後面訊息是要廣播的指定內容
    [root@localhost ~]# shutdown -h 10 "please backup your job"
    Shutdown scheduled for Mon 2020-10-12 14:11:51 CST, use 'shutdown -c' to cancel.
    [root@localhost ~]# shutdown -c
    ```
    另一個正在遠端操作的使用者也會收到關機的系統資訊
    ```bash=
    [knock@localhost ~]$
    Broadcast message from root@localhost.localdomain on pts/1 (Mon 2020-10-12 14:10:51 CST):

    please backup your job
    The system is going down for poweroff at Mon 2020-10-12 14:11:51 CST!


    Broadcast message from root@localhost.localdomain on pts/1 (Mon 2020-10-12 14:11:25 CST):

    The system shutdown has been cancelled


    [knock@localhost ~]$
    ```

  * shell程序在輸入指令時可以按tab鍵來快速列出目前符合的指令
    ```bash=
    [root@localhost ~]# shu
    shuf      shutdown
    ```
  * `reboot`指令也可以關機,enter按下去就立即重新開機
  * 若不想切到super user但又需要用super user的身分(前提是user帳號有設定管理員權限),  
    可用`sudo`指令,表示暫時性使用管理者身分來執行操作,第一次執行會需要輸入密碼,之後就不用了  
    ```bash=
    [knock@localhost ~]$ sudo shutdown -h 10

    我們相信您已經從本機系統管理員取得
    日常注意事項。注意事項通常可以歸結為三件事情：

        #1) 尊重他人隱私。
        #2) 輸入指令前先三思。
        #3) 權力越大則責任越大。

    [sudo] knock 的密碼：
    Shutdown scheduled for Mon 2020-10-12 14:33:12 CST, use 'shutdown -c' to cancel.
    ```

### 單元 6 - 基本檔案操作 - 複製、搬移、刪除
  * 檔案複製指令`cp`,後面要帶入兩個參數,第1個是來源路徑,第2個是目的地路徑  
    ```bash=
    // 目的地的參數帶入"."表示目的地是當前目錄之下
    [knock@localhost ~]$ cp /etc/fstab .
    [knock@localhost ~]$ ls -l
    總計 4
    // 這樣就把fstab檔案從 /etc 複製到 /home/knock 之下
    -rw-r--r--. 1 knock knock 709 10月 12 14:43 fstab
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 下載
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 公共
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 圖片
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 影片
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 文件
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 桌面
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 模板
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 音樂
    [knock@localhost ~]$
    ```
  * 當想透過tab快速列出目前可用的檔案時,若檔案過多可連按兩次tab,會跳出提示
    ```bash=
    //當輸入來源路徑並按下 tab 鍵兩次時,因為檔案過多會跳出提示
    [knock@localhost ~]$ cp /etc/
    Display all 293 possibilities? (y or n)
    abrt/                       microcode_ctl/
    adjtime                     mime.types
    aliases                     mke2fs.conf
    alsa/                       modprobe.d/
    alternatives/               modules-load.d/
    anacrontab                  motd
    asound.conf                 motd.d/
    at.deny                     mtab
    audit/                      mtools.conf
    authselect/                 multipath/
    autofs.conf                 my.cnf
    autofs_ldap_auth.conf       my.cnf.d/
    auto.master                 nanorc
    auto.master.d/              ndctl/
    auto.misc                   netconfig
    auto.net                    NetworkManager/
    auto.smb                    networks
    avahi/                      nfs.conf
    bash_completion.d/          nfsmount.conf
    bashrc                      nftables/
    bindresvport.blacklist      nsswitch.conf
    binfmt.d/                   nsswitch.conf.bak
    bluetooth/                  oddjob/
    --More--
    ```
  * 想看純文字內容可以用`cat`指令
    ```bash=
    [knock@localhost ~]$ cat fstab

    #
    # /etc/fstab
    # Created by anaconda on Sun Oct 11 08:02:48 2020
    #
    # Accessible filesystems, by reference, are maintained under '/dev/disk/'.
    # See man pages fstab(5), findfs(8), mount(8) and/or blkid(8) for more info.
    #
    # After editing this file, run 'systemctl daemon-reload' to update systemd
    # units generated from this file.
    #
    UUID=56b7da25-39da-4c31-9f46-35b568c3ea00 /                       xfs     defaults        0 0
    UUID=63546e57-1f65-4aa0-ab1c-0458500b3d83 /boot                   ext4    defaults        1 2
    UUID=a8eba0dc-b546-4229-a51f-7dd27ba620ff /var                    xfs     defaults        0 0
    UUID=1ff081ce-dfcd-41d1-b98c-44766a52dbe7 swap                    swap    defaults        0 0
    [knock@localhost ~]$
    ```
  * 複製檔案內容並重新命名檔案名稱
    ```bash=
    // 把當前目錄內的fstab檔案內容複製到一個新的檔案並且將檔案名稱設定為aaa
    [knock@localhost ~]$ cp fstab aaa
    [knock@localhost ~]$ ls -l
    總計 8
    -rw-r--r--. 1 knock knock 709 10月 12 14:55 aaa
    -rw-r--r--. 1 knock knock 709 10月 12 14:43 fstab
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 下載
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 公共
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 圖片
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 影片
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 文件
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 桌面
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 模板
    drwxr-xr-x. 2 knock knock   6 10月 11 20:19 音樂
    [knock@localhost ~]$
    ```
  * 移動檔案到其他資料夾使用`mv`指令,後面參數帶兩個,第1個示來源檔案,第2個是目的地路徑
    也可用來改變檔案名稱,例如將檔案aaa改成bbb就輸入`mv aaa bbb`
    ```bash=
    // 把檔案aaa從當前目錄複製到/tmp之下
    [knock@localhost ~]$ mv aaa /tmp
    [knock@localhost ~]$ ls -l /tmp
    總計 20
    -rw-r--r--. 1 knock knock  709 10月 12 14:55 aaa
    -rw-r--r--. 1 root  root  1787 10月 11 20:19 anaconda.log
    -rw-r--r--. 1 root  root  2942 10月 11 20:18 dbus.log
    -rw-r--r--. 1 root  root     0 10月 11 20:18 ifcfg.log
    -rwx------. 1 root  root  1379 10月 11 20:12 ks-script-kwyrh_vw
    -rw-r--r--. 1 root  root     0 10月 11 20:18 packaging.log
    -rw-r--r--. 1 root  root   131 10月 11 20:18 program.log
    -rw-r--r--. 1 root  root     0 10月 11 20:18 sensitive-info.log
    -rw-r--r--. 1 root  root     0 10月 11 20:18 storage.log
    drwx------. 3 root  root    17 10月 12 14:19 systemd-private-1a0b73f820574a9fbe803605c05bc57c-colord.service-qUfwa2
    drwx------. 3 root  root    17 10月 12 14:19 systemd-private-1a0b73f820574a9fbe803605c05bc57c-ModemManager.service-4CPf08
    drwx------. 3 root  root    17 10月 12 14:19 systemd-private-1a0b73f820574a9fbe803605c05bc57c-rtkit-daemon.service-0eu9mK
    drwx------. 2 knock knock    6 10月 11 20:20 tracker-extract-files.1000
    [knock@localhost ~]$
    ```
  * 刪除檔案使用`rm`指令
    ```bash=
    [knock@localhost ~]$ rm /tmp/aaa
    [knock@localhost ~]$ ls -l /tmp
    總計 16
    -rw-r--r--. 1 root  root  1787 10月 11 20:19 anaconda.log
    -rw-r--r--. 1 root  root  2942 10月 11 20:18 dbus.log
    -rw-r--r--. 1 root  root     0 10月 11 20:18 ifcfg.log
    -rwx------. 1 root  root  1379 10月 11 20:12 ks-script-kwyrh_vw
    -rw-r--r--. 1 root  root     0 10月 11 20:18 packaging.log
    -rw-r--r--. 1 root  root   131 10月 11 20:18 program.log
    -rw-r--r--. 1 root  root     0 10月 11 20:18 sensitive-info.log
    -rw-r--r--. 1 root  root     0 10月 11 20:18 storage.log
    drwx------. 3 root  root    17 10月 12 14:19 systemd-private-1a0b73f820574a9fbe803605c05bc57c-colord.service-qUfwa2
    drwx------. 3 root  root    17 10月 12 14:19 systemd-private-1a0b73f820574a9fbe803605c05bc57c-ModemManager.service-4CPf08
    drwx------. 3 root  root    17 10月 12 14:19 systemd-private-1a0b73f820574a9fbe803605c05bc57c-rtkit-daemon.service-0eu9mK
    drwx------. 2 knock knock    6 10月 11 20:20 tracker-extract-files.1000
    ```
  * 建立資料夾使用`mkdir`指令, 後面參數表示資料夾名稱
    ```bash=
    [knock@localhost ~]$ mkdir test01
    [knock@localhost ~]$ ls -l
    總計 0
    drwxrwxr-x. 2 knock knock 6 10月 12 15:07 test01
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 下載
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 公共
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 圖片
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 影片
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 文件
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 桌面
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 模板
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 音樂
    ```
  * 刪除資料夾可使用`rmdir`或`rm`指令,但若資料夾內非空的就無法刪除,若要刪除需要帶參數`-f`表示強制刪除, `-r`表示遞迴,就是一層一層跑
    ```bash=
    // rmdir和rm都無法刪除非空的資料夾
    [knock@localhost ~]$ rmdir test01
    rmdir: failed to remove 'test01': 目錄不是空的
    [knock@localhost ~]$ rm test01
    rm: 無法移除 'test01': 是個目錄
    [knock@localhost ~]$ rm -f test01
    rm: 無法移除 'test01': 是個目錄

    // 輸入 -rf 強制刪除test01與裡面所有的內容,不會跳出任何提示或訊息
    [knock@localhost ~]$ rm -rf test01
    [knock@localhost ~]$
    ```

### 單元 7 - 學怎麼用Linux，而不是背指令
  * 思考方式先想要做啥,再來查指令

## 第 3 章 Linux 的檔案系統
### 單元 1 - XFS檔案系統
  * CentOS 6使用的檔案系統是Ext2->Ext3(加上日誌功能)->Ext4  
    因為Ext2版本在停電重開後,需要去掃描目前檔案內的一些變動和狀況,  
    而Ext3把變動資訊都記錄起來,節省傳統需掃描整顆硬碟所要耗費的時間,  
    當停電復工後,只需要掃描日誌內有變動的檔案,效能就會提升  
    Ext4檔案最大可達1EB(1000PB)
  * CentOS 7,8使用的檔案系統是XFS(檔案最大可達8EB)
  * `xfs`相關的指令如下,以下指令只有超級管理員才能執行
    ```bash=
    [knock@localhost ~]$ xfs
    xfs_admin      xfs_estimate   xfsinvutil     xfs_mkfile     xfs_rtcp
    xfs_bmap       xfs_freeze     xfs_io         xfs_ncheck     xfs_spaceman
    xfs_copy       xfs_fsr        xfs_logprint   xfs_quota
    xfs_db         xfs_growfs     xfs_mdrestore  xfs_repair
    xfsdump        xfs_info       xfs_metadump   xfsrestore
    [knock@localhost ~]$ xfs
    ```
### 單元 2 - 認識 inode
  * [檔案資訊紀錄檔"inode"](https://linux.vbird.org/linux_basic_train/centos8/unit06.php#6.1)
    * 記錄檔案的屬性，一個檔案佔用一個inode，同時記錄此檔案的資料所在的 block 號碼
    * 檔名,更動時間,權限與檔案儲存的區塊位置等資料
    * 每個inode都有唯一編號
    * `ls -i`指令可列出inode的編號
        ```bash=
        [knock@localhost ~]$ ls -il
        總計 0
        // 第一個就是inode的編號
        27774161 drwxr-xr-x. 2 knock knock 6 10月 11 20:19 下載
        9651884 drwxr-xr-x. 2 knock knock 6 10月 11 20:19 公共
        3413527 drwxr-xr-x. 2 knock knock 6 10月 11 20:19 圖片
        9651885 drwxr-xr-x. 2 knock knock 6 10月 11 20:19 影片
        18512867 drwxr-xr-x. 2 knock knock 6 10月 11 20:19 文件
        18512866 drwxr-xr-x. 2 knock knock 6 10月 11 20:19 桌面
        3413526 drwxr-xr-x. 2 knock knock 6 10月 11 20:19 模板
        27774162 drwxr-xr-x. 2 knock knock 6 10月 11 20:19 音樂
        ```
    * linux中的inode是有數量限制的,輸入`df -i`指令可查詢目前磁碟上inode的使用狀態  
      當檔案很小又很多就可能耗盡inode,造成磁碟空間足夠但無法寫入
        ```bash=
        [knock@localhost ~]$ df -i
        檔案系統         Inode  I已用   I可用 I已用% 掛載點
        devtmpfs        992667    380  992287     1% /dev
        tmpfs           999738      1  999737     1% /dev/shm
        tmpfs           999738    747  998991     1% /run
        tmpfs           999738     17  999721     1% /sys/fs/cgroup
        /dev/sda2      6815744 152980 6662764     3% /
        /dev/sda5      2096128   8026 2088102     1% /var
        /dev/sda1        65536    309   65227     1% /boot
        tmpfs           999738     23  999715     1% /run/user/42
        tmpfs           999738     11  999727     1% /run/user/0
        tmpfs           999738     11  999727     1% /run/user/1000
        [knock@localhost ~]$
        ```
    ![檔案系統示意圖](./pics/Ext2檔案系統示意圖.png "檔案系統示意圖")

### 單元 3 - 檔案系統相關指令與操作說明
  * 要了解目前檔案系統的掛載狀況使用`cat /etc/fstab`指令查詢fstab檔案內的資訊  
    可以看到根目錄是使用xfs方式來掛載,而/boot目錄使用Ext4,因為boot是放linux的開機核心檔
    ```bash=
    [root@localhost ~]# cat /etc/fstab

    #
    # /etc/fstab
    # Created by anaconda on Sun Oct 11 08:02:48 2020
    #
    # Accessible filesystems, by reference, are maintained under '/dev/disk/'.
    # See man pages fstab(5), findfs(8), mount(8) and/or blkid(8) for more info.
    #
    # After editing this file, run 'systemctl daemon-reload' to update systemd
    # units generated from this file.
    #
    UUID=56b7da25-39da-4c31-9f46-35b568c3ea00 /                       xfs     defaults        0 0
    UUID=63546e57-1f65-4aa0-ab1c-0458500b3d83 /boot                   ext4    defaults        1 2
    UUID=a8eba0dc-b546-4229-a51f-7dd27ba620ff /var                    xfs     defaults        0 0
    UUID=1ff081ce-dfcd-41d1-b98c-44766a52dbe7 swap                    swap    defaults        0 0
    ```
  * 使用`df`指令可查詢目前檔案系統掛載的狀態
    ```bash=
    // 以下數字單位均是kb,需要自己換算成gb
    [root@localhost ~]# df
    檔案系統        1K-區段    已用    可用 已用% 掛載點
    devtmpfs        3970668       0 3970668    0% /dev
    tmpfs           3998952       0 3998952    0% /dev/shm
    tmpfs           3998952    9344 3989608    1% /run
    tmpfs           3998952       0 3998952    0% /sys/fs/cgroup
    /dev/sda2      13621248 5114272 8506976   38% /
    /dev/sda5       4182016  894076 3287940   22% /var
    /dev/sda1        999320  193588  736920   21% /boot
    tmpfs            799788    1180  798608    1% /run/user/42
    tmpfs            799788       4  799784    1% /run/user/0
    tmpfs            799788       4  799784    1% /run/user/1000

    // -h參數表示human readable,會轉換成人類比較易懂的方式
    [root@localhost ~]# df -h
    檔案系統        容量  已用  可用 已用% 掛載點
    devtmpfs        3.8G     0  3.8G    0% /dev
    tmpfs           3.9G     0  3.9G    0% /dev/shm
    tmpfs           3.9G  9.2M  3.9G    1% /run
    tmpfs           3.9G     0  3.9G    0% /sys/fs/cgroup
    /dev/sda2        13G  4.9G  8.2G   38% /
    /dev/sda5       4.0G  874M  3.2G   22% /var
    /dev/sda1       976M  190M  720M   21% /boot
    tmpfs           782M  1.2M  780M    1% /run/user/42
    tmpfs           782M  4.0K  782M    1% /run/user/0
    tmpfs           782M  4.0K  782M    1% /run/user/1000
    ```
  * 使用`man`指令(manual:操作手冊)後面帶入要查詢的指令可以獲得指令的操作手冊,指令的操作手冊在安裝系統時就都放入系統中了
    ```bash=
    DF(1)                                         User Commands                                         DF(1)

    NAME
        df - report file system disk space usage

    SYNOPSIS
        df [OPTION]... [FILE]...

    DESCRIPTION
        This  manual page documents the GNU version of df.  df displays the amount of disk space available
        on the file system containing each file name argument.  If no file name is given, the space avail‐
        able on all currently mounted file systems is shown.  Disk space is shown in 1K blocks by default,
        unless the environment variable POSIXLY_CORRECT is set, in which case 512-byte blocks are used.

        If an argument is the absolute file name of a disk device node containing a mounted  file  system,
        df  shows  the  space  available on that file system rather than on the file system containing the
        device node.  This version of df cannot show  the  space  available  on  unmounted  file  systems,
        because  on  most  kinds  of systems doing so requires very nonportable intimate knowledge of file
        system structures.

    OPTIONS
        Show information about the file system on which each FILE resides, or all file systems by default.

        Mandatory arguments to long options are mandatory for short options too.

        -a, --all
                include pseudo, duplicate, inaccessible file systems

    ```
  * 使用`info`指令且後面帶入要查詢的指令可以獲得指令的簡易說明
    ```bash=
    [root@localhost ~]# info df
    Next: du invocation,  Up: Disk usage

    14.1 ‘df’: Report file system disk space usage
    ==============================================

    ‘df’ reports the amount of disk space used and available on file
    systems.  Synopsis:

        df [OPTION]... [FILE]...

    With no arguments, ‘df’ reports the space used and available on all
    currently mounted file systems (of all types).  Otherwise, ‘df’ reports
    on the file system containing each argument FILE.

    Normally the disk space is printed in units of 1024 bytes, but this
    can be overridden (*note Block size::).  Non-integer quantities are
    rounded up to the next higher unit.

    For bind mounts and without arguments, ‘df’ only outputs the
    statistics for that device with the shortest mount point name in the
    list of file systems (MTAB), i.e., it hides duplicate entries, unless
    the ‘-a’ option is specified.

    With the same logic, ‘df’ elides a mount entry of a dummy pseudo
    device if there is another mount entry of a real block device for that
    mount point with the same device number, e.g.  the early-boot pseudo
    -----Info: (coreutils)df invocation, 248 lines --Top--------------------------------------------------------
    Welcome to Info version 6.5.  Type H for help, h for tutorial.
    ```
  * 使用`du`指令(disk usage)查詢資料夾空間使用狀況
    ```bash=
    [root@localhost ~]# du -h
    4.0K    ./.cache/dconf
    4.0K    ./.cache
    4.0K    ./.dbus/session-bus
    4.0K    ./.dbus
    0       ./.config/ibus/bus
    0       ./.config/ibus
    76K     ./.config/pulse
    76K     ./.config
    120K    .
    [root@localhost ~]#

    // "-d"表示資料夾深度,設1就只會查尋第一層,沒設定-d就會每一層資料夾都列出(很耗資源)
    [root@localhost ~]# du -d 1 -h /
    187M    /boot
    0       /dev
    du: 無法存取 '/proc/14045/task/14045/fd/3': 沒有此一檔案或目錄
    du: 無法存取 '/proc/14045/task/14045/fdinfo/3': 沒有此一檔案或目錄
    du: 無法存取 '/proc/14045/fd/4': 沒有此一檔案或目錄
    du: 無法存取 '/proc/14045/fdinfo/4': 沒有此一檔案或目錄
    0       /proc
    9.2M    /run
    0       /sys
    794M    /var
    30M     /etc
    120K    /root
    4.7G    /usr
    12M     /home
    0       /media
    0       /mnt
    0       /opt
    0       /srv
    28K     /tmp
    5.7G    /
    ```

### 單元 4 - 認識連結(Link) - 符號連結與硬連結
  * 連結允許多個檔案參考到一個檔案,連結是一種指向另一個檔案的特別檔案(類似window的捷徑)
  * Linux連結有兩種(連結也是檔案的一種)
    1. 符號連結 Symbolic link
    2. 硬連結 Hard link
  * 連結使用`ln -s /var myvar`指令, "-s"表示產生符號連結, "/var"表示目標路徑, "myvar"表示連結的檔案名稱.  
    用途是當/var內容有更動,myvar連過去的就是更動過的/var
    ```bash=
    [knock@localhost ~]$ ln -s /var myvar
    [knock@localhost ~]$ ll
    總計 0
    // 建立了一個myvar的link會連結到/var目錄
    lrwxrwxrwx. 1 knock knock 4 10月 12 17:34 myvar -> /var
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 下載
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 公共
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 圖片
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 影片
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 文件
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 桌面
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 模板
    drwxr-xr-x. 2 knock knock 6 10月 11 20:19 音樂

    // 輸入ls myvar/會連結到/var目錄,所以會列出/var下的內容
    [knock@localhost ~]$ ll myvar/
    總計 8
    drwxr-xr-x.  2 root root   19 10月 11 20:08 account
    drwxr-xr-x.  2 root root    6  5月 11  2019 adm
    drwxr-xr-x. 18 root root  233 10月 11 20:20 cache
    drwxr-xr-x.  2 root root    6  4月 25 01:07 crash
    drwxr-xr-x.  3 root root   18 10月 11 20:08 db
    drwxr-xr-x.  3 root root   18 10月 11 20:08 empty
    drwxr-xr-x.  2 root root    6  5月 11  2019 ftp
    drwxr-xr-x.  2 root root    6  5月 11  2019 games
    drwxr-xr-x.  2 root root    6  5月 11  2019 gopher
    drwxr-xr-x.  3 root root   18 10月 11 20:04 kerberos
    drwxr-xr-x. 68 root root 4096 10月 11 20:20 lib
    drwxr-xr-x.  2 root root    6  5月 11  2019 local
    lrwxrwxrwx.  1 root root   11 10月 11 20:03 lock -> ../run/lock
    drwxr-xr-x. 22 root root 4096 10月 12 13:14 log
    lrwxrwxrwx.  1 root root   10  5月 11  2019 mail -> spool/mail
    drwxr-xr-x.  2 root root    6  5月 11  2019 nis
    drwxr-xr-x.  2 root root    6  5月 11  2019 opt
    drwxr-xr-x.  2 root root    6  5月 11  2019 preserve
    lrwxrwxrwx.  1 root root    6 10月 11 20:03 run -> ../run
    drwxr-xr-x. 15 root root  180 10月 11 20:08 spool
    drwxr-xr-x.  4 root root   28 10月 11 20:07 target
    drwxrwxrwt.  6 root root  264 10月 12 16:12 tmp
    drwxr-xr-x.  4 root root   33 10月 11 20:05 www
    drwxr-xr-x.  2 root root    6  5月 11  2019 yp
    ```
  * `ln`指令也可連結到檔案,指定檔案名稱就可以產生對檔案的連結,  
    當連結的檔案被刪除,ls列出的檔案連結會變成紅色,表示有問題的,就變成無效的符號連結
    刪除連結與刪除檔案方式是一樣的`rm slink`  
    ```bash=
    [knock@localhost ~]$ ln -s fstab slink
    [knock@localhost ~]$ ll
    總計 4
    -rw-r--r--. 1 knock knock 709 10月 12 17:43 fstab
    lrwxrwxrwx. 1 knock knock   4 10月 12 17:34 myvar -> /var
    lrwxrwxrwx. 1 knock knock   5 10月 12 17:43 slink -> fstab

    // 這時對slink的操作等同對fstab的檔案作操作
    [knock@localhost ~]$ cat slink
    #
    # /etc/fstab
    # Created by anaconda on Sun Oct 11 08:02:48 2020
    #
    # Accessible filesystems, by reference, are maintained under '/dev/disk/'.
    # See man pages fstab(5), findfs(8), mount(8) and/or blkid(8) for more info.
    #
    # After editing this file, run 'systemctl daemon-reload' to update systemd
    # units generated from this file.
    #
    UUID=56b7da25-39da-4c31-9f46-35b568c3ea00 /                       xfs     defaults        0 0
    UUID=63546e57-1f65-4aa0-ab1c-0458500b3d83 /boot                   ext4    defaults        1 2
    UUID=a8eba0dc-b546-4229-a51f-7dd27ba620ff /var                    xfs     defaults        0 0
    UUID=1ff081ce-dfcd-41d1-b98c-44766a52dbe7 swap                    swap    defaults        0 0

    // 當連結的檔案被刪除,ls列出的檔案連結會變成紅色,表示有問題的,就變成無效的符號連結
    [knock@localhost ~]$ rm fstab
    [knock@localhost ~]$ cat slink
    cat: slink: 沒有此一檔案或目錄
    [knock@localhost ~]$ ls -l
    總計 0
    lrwxrwxrwx. 1 knock knock 4 10月 12 17:34 myvar -> /var
    lrwxrwxrwx. 1 knock knock 5 10月 12 17:43 slink -> fstab    
    ```
  * 硬連結(hard link)指令一樣使用`ln`但參數不需要帶入"-s"  
    符號連結(symbolic link)的inode是不同於原本的,但硬連結(hard link)的inode是相同於原本的檔案.  
    當把來源檔案刪除,符號連結會顯示無效連結,但硬連結仍正常,因為硬連結是複製原本的inode,
    所以操作仍然是正常的,但符號連結無法作任何操作了.
    硬連結的檔案類型與原本的一樣,但符號連結顯示的是"l".   
    硬連結限制很多,**硬連結是無法跨越分割區的**,也就是若要從/var/log/message檔案建立一個硬連結到/home/knock是無法操作的
    ```bash=
    // 建立硬連結
    [knock@localhost ~]$ ln fstab hlink
    
    //
    [knock@localhost ~]$ ll -i
    總計 8
    // hlink的inode與fstab一樣,但與slink不一樣
    9651859 -rw-r--r--. 2 knock knock 709 10月 12 17:51 fstab
    9651859 -rw-r--r--. 2 knock knock 709 10月 12 17:51 hlink
    9651853 lrwxrwxrwx. 1 knock knock   4 10月 12 17:55 myvar -> /var
    9651866 lrwxrwxrwx. 1 knock knock   5 10月 12 17:56 slink -> fstab
    
    // 目錄不允許使用硬連結
    [knock@localhost ~]$ ln /var hvar
    ln: /var: 不允許將實際鏈結 (hard link) 連至目錄

    // 刪除來源檔案
    [knock@localhost ~]$ rm fstab
    [knock@localhost ~]$ ls -li
    總計 4
    // 硬連結顯示看起來正常
    9651859 -rw-r--r--. 1 knock knock 709 10月 12 17:51 hlink
    9651853 lrwxrwxrwx. 1 knock knock   4 10月 12 17:55 myvar -> /var
    // 符號連結會變成無效連結並顯示成紅色
    9651866 lrwxrwxrwx. 1 knock knock   5 10月 12 17:56 slink -> fstab

    //操作檔案讀取時,硬連結仍可正常讀取檔案內容
    [knock@localhost ~]$ cat slink
    cat: slink: 沒有此一檔案或目錄
    [knock@localhost ~]$ cat hlink

    #
    # /etc/fstab
    # Created by anaconda on Sun Oct 11 08:02:48 2020
    #
    # Accessible filesystems, by reference, are maintained under '/dev/disk/'.
    # See man pages fstab(5), findfs(8), mount(8) and/or blkid(8) for more info.
    #
    # After editing this file, run 'systemctl daemon-reload' to update systemd
    # units generated from this file.
    #
    UUID=56b7da25-39da-4c31-9f46-35b568c3ea00 /                       xfs     defaults        0 0
    UUID=63546e57-1f65-4aa0-ab1c-0458500b3d83 /boot                   ext4    defaults        1 2
    UUID=a8eba0dc-b546-4229-a51f-7dd27ba620ff /var                    xfs     defaults        0 0
    UUID=1ff081ce-dfcd-41d1-b98c-44766a52dbe7 swap                    swap    defaults        0 0
    [knock@localhost ~]$

    // 硬連結的建立是無法跨越分割區的
    [knock@localhost ~]$ ln /var/log/messages hlink2
    ln: failed to create hard link 'hlink2' => '/var/log/messages': 不適用的裝置間連結
    ```

### 單元 5 - 執行檔案與PATH環境變數
  * 為什麼輸入指令就可以執行的原因是因為在linux的個人設定一個PATH環境變數紀錄可執行檔路徑,當輸入指令會去每個目錄查看是否有可執行的檔案
    ```bash=
    [knock@localhost ~]$ echo $PATH
    /home/knock/.local/bin:/home/knock/bin:/usr/local/bin:/usr/bin:/usr/local/sbin:/usr/sbin
    ```
  * 如果要讓檔案可執行,使用`chmod`指令(change mode)來改變檔案權限,後面傳入參數`u+x runme`,檔案的九個權限分別是(1)user (2)group (3)others三種身份啦！那麼我們就可以藉由**u, g, o**來代表三種身份的權限  
    設定權限後仍無法直接執行,因為linux針對檔案執行有限制,  
    如果要執行當前目錄下的檔案要在前面加入"./"

    ![chmod](./pics/chmod.png "指令示意圖")

    ```bash=
    // 寫一個檔案叫"runme",內容就是"Hello Linux"
    [knock@localhost ~]$ echo "Hello Linux" > runme

    [knock@localhost ~]$ ls -l
    // "runme"檔案沒有"x"屬性,所以無法執行
    -rw-rw-r--. 1 knock knock 12 10月 12 18:24 runme

    // 執行chmod指令改變權限
    [knock@localhost ~]$ chmod u+x runme

    [knock@localhost ~]$ ls -l
    // 改變後user的權限就變成"x"可執行狀態
    -rwxrw-r--. 1 knock knock 12 10月 12 18:24 runme

    // 執行檔案是失敗的,因為linux有安全性限制,要執行檔案需要在前面加上"./"
    [knock@localhost ~]$ runme
    bash: runme: 找不到指令...
    [knock@localhost ~]$ ./runme
    Hello Linux


    ```


## 第 4 章 檔案編輯與工具

### 單元 1 - 熟悉 vim 文字編輯器

  * 作業 1 - 下載網路文字檔案並編輯
### 單元 2 - 標準輸出入與重導

### 單元 3 - 篩選與管線處理

### 單元 4 - 搜尋檔案

### 單元 5 - 檢視檔案內容