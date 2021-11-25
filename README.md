# CS_NOTE
@Git的特點:


1.免費、開源


2.速度快、檔案體積小


3.分散式系統，強調個體


4.公共服務器壓力和數據量都不會太大


5.離線工作


@Linux的特點:

1.穩定的系統

2.免費或少許費用

3.獨立作業

4.安全性、漏洞的修補

5.多工、多使用者

6.使用者與群組的規劃

7.相對比較不耗資源的系統

8.適合需要小核心程式的嵌入式系統
![image](https://user-images.githubusercontent.com/91462920/142958406-e14895e8-a47c-455f-a0d4-bef8521b57b7.png)



@Linux背景知識-發展與線上升級:

  開發時分為兩種版本:

   1.開發中版本範例(主次版本為奇數)：2.5.x

   2.穩定版本範例(主次版本為偶數)：2.6.x
   
 『線上升級』機制:
 
  透過此機制可以在第二次使用之後,從網路上取得任何有關原開發商的軟體
  
@Linux背景知識-檔案命名原則、副檔名:
 
1.區分英文字元的大小寫，基本以小寫為主

2.檔名長度至多256個字元，可包刮字母、數字、"."(點)、"_"(下劃線)和"-"(連字元)

3.檔名不可使用的字元："?"(問號),"*"(星號), " "(空格), "$"(貨幣符), "&", 擴號, "/" (斜線)，"." , ".." 

@Linux介紹指令及實做:

@絕對路徑&相對路徑:

絕對路徑：路徑的寫法『一定由根目錄 / 寫起』，例如： /usr/share/doc 這個目錄。

相對路徑：路徑的寫法『不是由 / 寫起』，例如由 /usr/share/doc 要到 /usr/share/man 底下時，寫成： 『cd ../man』，相對路徑意指『相對於目前工作目錄的路徑！』

@指令:

cd 	變換目錄
 
pwd	顯示目前的目錄

mkdir 建立一個新目錄

rmdir 刪除一個裡面是空的空目錄

cp 複製

mv 移動

ls 顯示目錄下的所有內容

cat 查看檔案內容

@編輯文檔:

nano 

Ctrl C：顯示游標所在

Ctrl W：查詢命令，按下後會跳轉到末行的反白位置，輸入要查詢的內容在回車及可。

vi/vim(vim相當於vi的升級版)

一般模式：可使用上下左右進行游標宜動、刪除字元及複製貼上檔案資料。

編輯模式：編輯文字
 
 (i鍵即可進入編輯模式)
 
![image](https://user-images.githubusercontent.com/91462920/142965162-7a2fd20c-17e1-4e16-be41-80eacd01e786.png)

    (Esc鍵退出編輯模式)
    
![image](https://user-images.githubusercontent.com/91462920/142965175-c9002e36-16b0-4c87-bde6-9644ace86e72.png)

vi/vim(vim相當於vi的升級版)
命令列模式



Linux背景知識

使用者與群組

關於身份：

身份分類：

user (owner)	
group			
others			

群組 (group) 的主要用意：

將帳號歸類，有助於類似專案開發；

每個使用者均可加入多個群組。

關於身份類別：

系統管理員： root

一般帳號：

系統帳號 (用於系統帳號的工作)

一般使用者帳號 (用於一般使用者登入用。)

![image](https://user-images.githubusercontent.com/91462920/143457863-f71d87d3-38e0-46a6-b0a9-80858a80e437.png)

![image](https://user-images.githubusercontent.com/91462920/143458104-99724b95-817f-4b54-846e-bd1a2dbc9f2f.png)

chmod可控制檔案如何被他人調用→ chmod [-cfvR] [--help] [--version] mode file…

mode許可權設定字串 → [ugoa...][[+-=][rwxX]...][,...]

檔案 file1.txt 設為所有人皆可讀取 :
chmod ugo+r file1.txt

將檔案 file1.txt 與 file2.txt 設為該檔案擁有者，與其所屬同一個群體者可寫入，但其他以外的人則不可寫入 :

chmod ug+w,o-w file1.txt file2.txt

將 ex1.py 設定為只有該檔案擁有者可以執行 :

chmod u+x ex1.py

將目前目錄下的所有檔案與子目錄皆設為任何人可讀取 :

chmod -R a+r *

chmod a=rwx file == chmod 777 file

chmod ug=rwx,o=x file ==  chmod 771 file

@Linux背景知識-壓縮檔案

為什麼要壓縮檔案呢？


備份資料的時候，方便整理。

將檔案變小，節省電腦硬碟的空間。(但圖片、音訊、視訊等多媒體檔案壓縮率低，並不能有效節省空間)

將無數個散亂的檔案打包成一個較小的檔案，亦方便資訊在網路上流通。(可將永久免費版之付費軟體輕鬆分享)

壓縮檔案時，可以視情況進行加密。

壓縮檔案的概念？
使用的電腦系統是使用bytes單位計量的，但事實上電腦最小的計量單位應該是 bits (1 byte = 8 bits)。因此將許多閒置的空間釋出，即可將檔案占用的空間減少。

將重複的資料進行統計記錄。EXAMPLE：如果資料為『111....』共有100個1時， 那麼壓縮技術會記錄『100個1』而不是真的有100個1的位元存在。

@Linux背景知識-各壓縮的差別

需要在記憶體很小的機器（如小於 128MB）上解壓縮時，則選擇 gzip 格式。


需要在很簡單、沒有什麼工具可用的機器解壓縮時，則選擇 gzip 格式。

需要節省網路頻寬、縮短下載所需要的時間時，則選擇 xz 格式。

需要有最好的壓縮率時，則選擇 tar.xz  格式。

考慮的因素


壓縮率（compression ratio），能夠將檔案壓到多小。

解壓縮所需的時間，也就是需要的 CPU 計算量。

解壓縮所需的記憶體空間。

相容性（compatibility），即解壓縮程式的普遍性，是不是大部分人都有辦法解壓縮這種格式？

gzip

壓縮：gzip FileName

解壓縮：

gunzip FileName.gz

gzip -d FileName.gz

xz
 
壓縮：xz -z FileName

解壓縮：xz -d FileName.xz

tar.gz

壓縮：tar -zcvf FileName.tar.gz DirName

解壓縮：tar -zxvf FileName.tar.gz

@Linux介紹指令及實做-檔案搜尋

find [path] [option] [action] filename

option

-size EX：找出大於500M的檔案→-size +500M

-name EX：找出為照片的檔案→-name "*.jpg"

-type EX：-type f→一般檔案;-type d→一般目錄

-user EX：同時找兩個擁有者的檔案→-user user1 -o -user user2

action -exec

ls

print

which filename

-n<文件名长度>指定文件名長度，指定的長度必須大於或等於所有文件中最長的文件名。

-p<文件名長度>與-n参數相同，但此處的<文件名長度>包括了文件的路徑。

-w指定輸出欄位的寬度。

-V顯示版本訊息。

cat  從第一行顯示檔案內容、形成新檔案

cat -n file1 > file2→把file1的檔案內容加上行號後輸入file2檔案

-n→由1開始對所有輸出的行數編號

>→將多個文件覆蓋到目標文件中

>>→將多個文件追加到目標文件中

tac  從最後一行開始顯示

tac -r -s 'x\|[^x]' test.log→一個接著一個字符的反轉一個文件

-r→將分隔符作為基礎正規表達是處理

-s→使用String作為分隔符代替默認的換行![image](https://user-images.githubusercontent.com/91462920/143459799-206e0c1f-b736-4a50-8dd7-f7ec69367832.png)

more 一頁一頁的顯示檔案內容

more +20 testfile→從第20行開始顯示testfile的文檔內容

ENTER：向下n行(default為1行)

Ctrl+F/SPACE：向下滾動一屏

Ctrl+B：返回上一屏

less 與 more 類似，顯示檔案室允許用戶既可以向前又可以向後翻頁閱讀檔案

ps -ef |less→ps查看進程信息並通過less分頁顯示	

j→下一行

k→上一行

G→移動到最後一行

g→移動到第一行

head/tail 只看頭/尾巴幾行

head -n 20 state.txt | tail -10→顯示11~20行的內容



















  


