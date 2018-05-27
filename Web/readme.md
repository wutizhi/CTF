/Web-1:source code\
題目:
 - 網站有許多漏洞，從底下的登入網址，你認為有幾種方式可以入侵?
 - 提示1 : 如何看到網站的原始碼?
 - 提示2 : 如何從網站的原始碼看到你所需要的資訊?
 - 提示3 : 答案格式 BreakALLCTF{xxxxxxxxxxx}
 - 請連結以下網址:
 - http://120.114.62.89:1001/ 
 - 解:\
打開網址後,按F12看網頁原始碼,會發現能直接看到flag,此flag即為答案\
![image](https://github.com/daniel-chang1260/CTF/blob/master/note/Photo/Web/2018-05-27%20(18).png)
/web-2:Robots.txt\
題目:
- robots.txt是一種文字檔案，它告訴網路搜尋引擎此網站中的哪些內容是不應被搜尋引擎的搜尋到的，哪些是可以被搜尋引擎搜尋到的。 但駭客卻常透過robots.txt來知道哪些網頁目錄含有重要或是隱私資訊。
- 本題任務是請你找到robots.txt並因此找到flag。
- 提示1 : robots.txt的存放放置
- 提示2 : 相關hex to string及base64 編碼
- 請連結以下網址:
- http://120.114.62.89:2001/ 
- 解:\
1.開啟網址後,在網址後方加上"/robots.txt"
![image](https://github.com/daniel-chang1260/CTF/blob/master/note/Photo/Web/2018-05-27%20(2).png)
2.進入後網站後,根據我們僅有的線索,將網址斜線後方改成"secret"
![image](https://github.com/daniel-chang1260/CTF/blob/master/note/Photo/Web/2018-05-27%20(3).png)
3.進入網址後,打開"flag.txt",並得到"516e4a6c595774425445784456455a374e31463053304979546a5655624846425155563651334a36546b3939"此串數字
![image](https://github.com/daniel-chang1260/CTF/blob/master/note/Photo/Web/2018-05-27%20(4).png)
![image](https://github.com/daniel-chang1260/CTF/blob/master/note/Photo/Web/2018-05-27%20(5).png)
4.將此數字進行hex to string及base64 編碼,即得到答案
![image](https://github.com/daniel-chang1260/CTF/blob/master/note/Photo/Web/2018-05-27%20(6).png)
![image](https://github.com/daniel-chang1260/CTF/blob/master/note/Photo/Web/2018-05-27%20(7).png)
![image](https://github.com/daniel-chang1260/CTF/blob/master/note/Photo/Web/2018-05-27%20(9).png)
/web-3:Curl-1\
題目:
- 網址重新導向(URL redirection)的技術 請到wiki上看看URL redirection的原理及用途 https://zh.wikipedia.org/wiki/網域名稱轉址 
- 提示1 : 如何從網站的原始碼找到你所需要的資訊?
- 提示2 : 本題可以使用curl工具輕鬆解題
- 請連結以下網址進行解題: 
- http://120.114.62.89:2014/ 
- 解:\
1.打開網址後,在GO上按右鍵檢查,查看index.php得到http://120.114.62.89:2014/index.php
![image](https://github.com/daniel-chang1260/CTF/blob/master/note/Photo/Web/2018-05-27%20(19).png)
2.在Linux中開啟終端機,輸入"curl http://120.114.62.89:2014/index.php", 即得到flag
![image](https://github.com/daniel-chang1260/CTF/blob/master/note/Photo/Web/2018-05-27%20(11).png)
![image](https://github.com/daniel-chang1260/CTF/blob/master/note/Photo/Web/2018-05-27%20(13).png)
![image](https://github.com/daniel-chang1260/CTF/blob/master/note/Photo/Web/2018-05-27%20(14).png)
![image](https://github.com/daniel-chang1260/CTF/blob/master/note/Photo/Web/2018-05-27%20(15).png)
![image](https://github.com/daniel-chang1260/CTF/blob/master/note/Photo/Web/2018-05-27%20(17).png)
