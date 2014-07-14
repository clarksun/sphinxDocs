Flash交接说明
===============


部署外网服务器
--------------
*更新swf
  *.  ``ssh -p 11680 root@221.228.73.10`` 输入密码后登陆成功
  *.  ``cd /var/www/html/mnj/1.x.x/`` 
  *.  ``rm -f monNickelodeonJr.swf`` 
  *. 回到本地服务器bash, ``scp -P 11680 LocalSWFPath root@221.228.73.10:/var/www/html/mnj/1.x.x/`` 输入密码后开始复制

Inline Markup
-------------
Words can have *emphasis in italics* or be **bold** and you can define
code samples with back quotes, like when you talk about a command: ``sudo`` 
gives you super user powers!
