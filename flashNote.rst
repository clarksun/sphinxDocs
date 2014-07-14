Flash交接说明
===============


部署外网服务器
--------------
 * 更新swf
  #.  ``ssh -p 11680 root@221.228.73.10`` 输入密码后登陆成功
  #.  ``cd /var/www/html/mnj/1.x.x/`` 1.x.x为具体版本目录
  #.  ``rm -f monNickelodeonJr.swf`` 
  #. 回到本地bash, ``scp -P 11680 LocalSWFPath root@221.228.73.10:/var/www/html/mnj/1.x.x/`` 输入密码。（LocalSWFPath为本地SWF路径）
  #. OK.

 * 更新xml
  * 简单修改直接到服务器上改
  #.  ``ssh -p 11680 root@221.228.73.10`` 输入密码后登陆成功
  #.  ``cd /var/www/html/mnj/1.x.x/`` 1.x.x为具体版本目录
  #.  ``vim file.xml`` file.xml为Config/Lang xml文件名
  * 复杂更新可以删掉服务器上的，再从本地upload上去
  #.  ``ssh -p 11680 root@221.228.73.10`` 输入密码后登陆成功
  #.  ``cd /var/www/html/mnj/1.x.x/`` 1.x.x为具体版本目录
  #.  ``rm -f file.xml`` file.xml为Config/Lang xml文件名
  #. 回到本地bash, ``scp -P 11680 LocalXMLPath root@221.228.73.10:/var/www/html/mnj/1.x.x/``输入密码。（LocalXMLPath为本地xml路径）
