mt-theme-mtzevent_template
==========================
MT三昧 イベント告知の使い方
http://www.mtzanmai.com/mtzevent/

.htaccessのパスワードの暗号化はfutomi's CGI Cafe様の下記ページのスクリプトを利用させていただいています。
http://www.futomi.com/lecture/htaccess/htpasswd.html

マニュアル作成中（下記にメモ書きしていきます。後日、まとめる予定）

1.  
--
ブログ直下のcgi-binディレクトリの中に「encrypt.html」と言うファイルがあります。このファイルの拡張子を「.cgi」に変更します。  
ブログURL/cgi-bin/htaccess/encrypt.html  
↓  
ブログURL/cgi-bin/htaccess/encrypt.cgi  

2.  
--
パスワードの暗号化用のウェブページを作成します。  
下記の「enc-pass.html」というファイルに書いてあるHTMLをコピーします。  
ブログURL/files/enc-pass.html  
  
ファイルの中身は下記のHTMLソースになります。  
　&lt;form action="http://ブログのURL/cgi-bin/htaccess/encrypt.cgi" method="post" target="_blank"&gt;  
　&lt;fieldset&gt;  
　&lt;legend&gt;パスワードを入れてください&lt;/legend&gt;  
　&lt;input type="text" name="pass" id="pass" size="20" /&gt;  
　&lt;input type="submit" id="encrypt-btn" name="encrypt-btn" value="暗号化 &amp;gt;" /&gt;  
　&lt;code id="encrypted-pass" style="font-size:medium;"&gt;&amp;nbsp;&lt;/code&gt;  
　&lt;/fieldset&gt;  
　&lt;/form&gt;  
  
コピーしたHTMLソースでウェブページを作成します。  
その際、1行目のaction属性のURLを「1.」のURLで書き換えます。  
　→&lt;form action="http://ブログのURL/cgi-bin/htaccess/encrypt.cgi" method="post" target="_blank"&gt;  
また、ウェブページのフォルダに「htaccess」を選択してください。  

3.  
--
ブログを再構築して準備完了です。  
