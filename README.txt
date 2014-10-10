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
　<form action="http://ブログのURL/cgi-bin/htaccess/encrypt.cgi" method="post" target="_blank">  
　<fieldset>  
　<legend>パスワードを入れてください</legend>  
　<input type="text" name="pass" id="pass" size="20" />  
　<input type="submit" id="encrypt-btn" name="encrypt-btn" value="暗号化 &amp;gt;" />  
　<code id="encrypted-pass" style="font-size:medium;">&amp;nbsp;</code>  
　</fieldset>  
　</form>  
  
コピーしたHTMLソースでウェブページを作成します。  
その際、1行目のaction属性のURLを「1.」のURLで書き換えます。  
　→<form action="http://ブログのURL/cgi-bin/htaccess/encrypt.cgi" method="post" target="_blank">  
また、ウェブページのフォルダに「htaccess」を選択してください。  

3.  
--
ブログを再構築して準備完了です。  
