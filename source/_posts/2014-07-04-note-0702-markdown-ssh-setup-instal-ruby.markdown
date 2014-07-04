---
layout: post
title: "Note_0702-Markdown, SSH-setup, Instal-ruby"
date: 2014-07-04 15:30:56 +0800
comments: true
categories: sass
---

[Markdown](http://daringfireball.net/projects/markdown/)
=========  
>Markdown的目標是實現「易讀易寫」, 語法全由標點符號所組成，並經過嚴謹慎選，是為了讓它們看起來就像所要表達的意思, 相較於HTML, 其更容易書寫、閱讀和修改，省去許多非必要的符號，更能專注在內容的編譯。


1. Words size
---------------
 
###※When you write down...
    
`###### H6最小` 

`# H1最大`

`標題`

`======`

`分隔線`

`-------`


###※What you see...

###### H6最小 

# H1最大  

標題
======

分隔線
------


2. Lists
-----------

清單項目標記通常是放在最左邊，但是其實也可以縮排，最多三個空白，項目標記後面則一定要接著至少一個空白或tab

換行時需要多空一行，在內容中才會顯示換行，如果中間無多空一行則會皆在上一行後面，但如果是list則不用刻意多空一行。

###※When you write down...

` 1. 空一格再開始打字`

` 1. 第二行即使不是2.也會按順序顯示`

` * 甚至是星號也可以` 

`+ +也可以`

 `- -也行`

 ` * 如果星號前多一個空格就是圓圈` 

 ` * 並且會接往後對齊`

 `+ +也可以是圓圈`
 
 `- -也行`


###※What you see...
 
1. 空一格再開始打字
1. 第二行即使不是2.也會按順序顯示
* 甚至是星號也可以
+ +也可以
- -也行

  * 如果星號前多一個空格就是圓圈 
  * 並且會接往後對齊
  + +也可以是圓圈
  - -也行

3. Links
-----------
[foo]: http://example.com/  "Optional Title Here"
[foo]: http://example.com/  'Optional Title Here'
[foo]: http://example.com/  (Optional Title Here)

###※When you write down...
 
[輸入欲顯示的內容1]：(網址1)

[輸入欲顯示的內容2]

`[foo]`

`[foo]: 網址foo  "Optional Title Here"`

`[foo]: 網址foo  'Optional Title Here'`

`[foo]: 網址foo  (Optional Title Here)`

[輸入欲顯示的內容2]：網址2

`<http://www.youtube.com/watch?v=6A5EpqqDOdk>`

###※What you see...
[輸入欲顯示的內容1]

[輸入欲顯示的內容2]

[foo]

<http://www.youtube.com/watch?v=6A5EpqqDOdk>
4. Emphasis
------------
星號數量會改變字體型式，內容前後加兩個星號為粗體字, 加一個星號或者底線則為斜體字。
###※When you write down...
 `*斜體字*`

 `_斜體字_`

`**粗體字**`

`***粗體字且粗體字***`

`*沒有任何改變`

`**斜體字*`

`*斜體字**`
###※What you see...
*斜體字*

_斜體字_

**粗體字**

***粗體字且粗體字***

沒有任何改變*

**斜體字*

***斜體字**

5. Image
----------
###※When you write down...
`![任意名稱](http://lh6.ggpht.com/-3EHhpkjOs6w/T6oovnaxF5I/AAAAAAAACY0/5rVys-SX_qU/logo-iShow-2_thumb.jpg?imgmax=800)`


`![picture][任意名稱2]`

`[任意名稱2]:http://lh6.ggpht.com/-3EHhpkjOs6w/T6oovnaxF5I/AAAAAAAACY0/5rVys-SX_qU/logo-iShow-2_thumb.jpg?imgmax=800`

`![picture](http://lh6.ggpht.com/-3EHhpkjOs6w/T6oovnaxF5I/AAAAAAAACY0/5rVys-SX_qU/logo-iShow-2_thumb.jpg?imgmax=800 "任意名稱3")`

###※What you see...
![任意名稱](http://lh6.ggpht.com/-3EHhpkjOs6w/T6oovnaxF5I/AAAAAAAACY0/5rVys-SX_qU/logo-iShow-2_thumb.jpg?imgmax=800)

![picture][任意名稱2]
[任意名稱2]:http://lh6.ggpht.com/-3EHhpkjOs6w/T6oovnaxF5I/AAAAAAAACY0/5rVys-SX_qU/logo-iShow-2_thumb.jpg?imgmax=800

![picture](http://lh6.ggpht.com/-3EHhpkjOs6w/T6oovnaxF5I/AAAAAAAACY0/5rVys-SX_qU/logo-iShow-2_thumb.jpg?imgmax=800 "任意名稱3")


6. Blockquotes
--------
大於符號（>）用來標記引言區塊，這和 Email 裡的使用方式很像，所以你要引用一段文字，讓他看起來有縮排的效果，只要在這段文字的開頭處加上 > 就可以了，像是

>####This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can put Markdown into a blockquote.





Further Explanation
------------
大部分的語法都在[Markdown-Cheatsheet]中說明，若是Windows系統可以下載[markdownpad]來編輯Markdown, 而Mac則是下載[Mou]，其中有些差別，[markdownpad]無法編輯table，而且也無法在文章前後分別用三個 ` 來囊括一段文字(可以選擇不同的程式語言),除此之外大致相同。 
[Mou]:http://mouapp.com/
[Markdown-Cheatsheet]:https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
[markdownpad]:http://markdownpad.com/download.html

SSH setup
=========
[MAC]
-----
>Github可以利用Html和SSH來遠端repo, 使用HTML每次都要輸入信箱和密碼, 
>而SSH會產生一組非對稱金鑰, 就如同鑰匙(private key)和鎖頭(public key), 因此只要在電腦上設定好private key, 就可以免密碼取得repo的內容。

1. 首先，打開git bash且輸入 `cat ~/.ssh/id_rsa.pub` 確認是否已生成SSH key。
2. 若未產生SSH key, 輸入 `ssh-keygen -t rsa(或dsa) -C "your_email@example.com"` ，然後會詢問`存取位置`，
以及是否設定private key的 passphrase (empty for no passphrase)，可依個人需求再次加密。
3. 完成後再次輸入 `cat ~/.ssh/id_rsa` 會出現 private key, 然後再輸入 `cat ~/.ssh/id_rsa.pub` 則會有public key, 例如: `ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAklOUpkDHrfHY17SbrmTIpNLTGK9Tjom/BWDSU
GPl+nafzlHDTYW7hdI4yZ5ew18JH4JW9jbhUFrviQzM7xlELEVf4h9lFX5QVkbPppSwg0cda3
Pbv7kOdJ/MTyBlWXFCR+HAo3FXRitBqxiX1nKhXpHAZsMciLq8V6RjsNAQwdsdMFvSlVK/7XA
t3FaoJoAsncM1Q9x5+3V0Ww68/eIFmb1zuUFljQJKprrX88XypNDvjYNby6vw/Pb0rwert/En
mZ+AW4OZPnTPI89ZPmVMLuayrD2cE86Z/il8b+gw3r3+1nKatmIkjn2so1d01QraTlMqVSsbx
NrRFi9wrf+M7Q== schacon@agadorlaptop.local`
4. 接著到Github上去建立一個SSH, 並且輸入名稱及public key(copy)。
5. 回到commend line輸入 `git remote add origin git@github.com:Iamyuan/Summer-Intern_Note.git` 接著輸入`git push -u origin master` 此動作為設定遠端的位置。
6. 接著在git bash 輸入`ssh -T git@github.com` 並且回答YES即可
6. 往後，如果要取得github上的內容，便輸入 `git clone git@github.com:Iamyuan/Summer-Intern_Note.git`。
7. 如果要上傳的話則是在commit之後輸入`git push `即可。

可以參考[GitHub Help-Generating SSH Keys]或者有[完整的影片]

也可以在[linux中架設GIT並使用SSH KEY]
[linux中架設GIT並使用SSH KEY]:http://www.gtwang.org/2014/02/linux-git-server-using-ssh.html

[GitHub Help-Generating SSH Keys]:https://help.github.com/articles/generating-ssh-keys
[完整的影片]:http://www.youtube.com/watch?v=bBUuHvdROKE


[WINDOWS]
------------


1. 安裝好[git]之後，在[git bash],輸入`ssh-keygen -C “username@email.com” -t rsa`此時c:\Users\yuan\.ssh 裡面有id_rsa 和id_rsa_pub.兩個檔案
2. 就如同上面234步驟，然後也可以繼續按照上述56執行，或者提供另一方法，複製GitHub上的url, 然後回commend line輸入`git clone git@github.com:Iamyuan/Summer-Intern_Note.git`，即表示已設定了remote origin，且同時在c:\Users\yuan\.ssh 也會多一個know_hosts的檔案(裡面是public key的內容)。
3. 也可在git bash輸入`ssh -T git@github.com` 檢查是否通過驗證
1. 往後便可自由pull、push在 GitHub的檔案。

**以上參考[windows使用ssh對GitHub進行操作], 關於產生SSH KEY, 也有其他方法:**
  
 - [PuttyGen]是SSH 安全遠端連線程式
 - [setup a SSH serve in Windows8.1](http://www.youtube.com/watch?v=K1M-QhJAh9E "setup a SSH serve in Windows8.1")
 - [PietTTY]是源自於PuTTY ，修正與完整支援亞洲等多國語系字元、 並在使用界面上大幅改進、易學易用的版本


[PuttyGen]:http://www.ecora.com/ecora/support/putty/puttygen-x86.exe
[git]:http://code.google.com/p/msysgit/downloads/list
[git bash]:http://i.imgur.com/ySLJixK.png
[windows使用ssh對GitHub進行操作]:http://www.dotblogs.com.tw/kirkchen/archive/2013/04/23/use_ssh_to_interact_with_github_in_windows.aspx
[PietTTY]:http://ntu.csie.org/~piaip/pietty/


Install-[Ruby](https://www.ruby-lang.org/en/installation/#homebrew)
============

目前最新的穩定版本是 2.1.2。

安裝順序： XCode → HomeBrew → ROR → etc(SSH...)

1. XCode
-------
Open the Mac App Store to buy and download apps.

[APP介紹](https://itunes.apple.com/us/app/xcode/id497799835?mt=12)


2. HomeBrew(套件管理工具)
--------
在commend line 輸入

`ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go/install)`

安裝Git(版本管理)`brew install git`

安裝wget(抓網路檔案的工具)`brew install wget`

安裝ImageMagick(縮圖用)`brew install imageMagick`

安裝MySQL(DataBase)`brew install mysql`

設定MySQL

3. RVM
--------------------------
管理及切換不同版本的ruby

`$ curl -L https://get.rvm.io | bash -s stable`

接著重開命令列或者重新登入
([rbven]也可以)

4. ROR
--------
安裝ruby`rvm install ruby-版本 `

安裝ruby gem`rvm rubygems current`

安裝rails`gem install rails`

Further Explanation
---------------
  * [Ruby on Rails 開發環境建置 for Mac]


[Ruby on Rails 開發環境建置 for Mac]: http://www.slideshare.net/marsz330/ruby-on-rails-for-mac
[rbven]:https://www.ruby-lang.org/en/installation/#rbenv
