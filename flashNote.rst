Flash工作说明文档
=================


部署外网服务器
--------------
 * **更新swf**
  #.  ``ssh -p 11680 root@221.228.73.10`` 输入密码后登陆成功.
  #.  ``cd /var/www/html/mnj/1.x.x/`` 1.x.x为具体版本目录.
  #.  ``rm -f monNickelodeonJr.swf`` .
  #. 如果是更新monNick.swf，回到本地bash, ``scp -P 11680 LocalSWFPath root@221.228.73.10:/var/www/html/mnj/1.x.x/`` 输入密码(LocalSWFPath为本地SWF路径).
  #. 如果是更新plugin.swf,回到本地bash, ``scp -P 11680 LocalSWFPath root@221.228.73.10:/var/www/html/mnj/1.x.x/player/`` 输入密码(LocalSWFPath为本地SWF路径).
  #. OK.

 * **更新xml** 
  * 简单修改直接到服务器上改.
  #.  ``ssh -p 11680 root@221.228.73.10`` 输入密码后登陆成功.
  #.  ``cd /var/www/html/mnj/1.x.x/`` 1.x.x为具体版本目录.
  #.  ``vim file.xml`` file.xml为Config/Lang xml文件名.
  #. OK.

  * 复杂更新可以删掉服务器上的，再从本地upload上去.
  #.  ``ssh -p 11680 root@221.228.73.10`` 输入密码后登陆成功.
  #.  ``cd /var/www/html/mnj/1.x.x/`` 1.x.x为具体版本目录.
  #.  ``rm -f file.xml`` file.xml为Config/Lang xml文件名.
  #. 回到本地bash, ``scp -P 11680 LocalXMLPath root@221.228.73.10:/var/www/html/mnj/1.x.x/`` 输入密码(LocalXMLPath为本地xml路径).
  #. OK.

 * **更新html/js等等，和更新xml一样.** 

打包Plugin
-----------
#. 共享下载虚拟机 ``\\192.168.20.200\share\clarksun\xp`` .
#. Vmware打开xp虚拟机,用户名 **administrator** ,密码 **123456** .
#. 打开目录 ``c:\alex\flash`` .
#. 右键svn update需要更新的项目.
#. 运行 **buildMyNickJ.bat** .
#. 成功后在release目录找到打包好的Plugin和Player.
