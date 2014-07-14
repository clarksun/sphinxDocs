Flash工作说明文档
=================


更新外网测试
--------------
外网ip: **221.228.73.10** ，访问地址 ``http://mnjflashtest.ivmall.com/mnj/1.x.x`` .(1.x.x是版本号)

 * **更新版本** 
  #.  ``ssh -p 11680 root@221.228.73.10`` 输入密码后登陆成功.
  #.  ``cd /var/www/html/mnj``
  #.  ``cp -r LAST_VERSION_FOLDER LATEST_VERSION_FOLDER`` 将上一个版本的目录拷贝一份，新目录名字为最新的版本号.
  #. 将新版本的文件按照下面的分类进行更新.
  #. OK.

 * **更新swf**
  #.  ``ssh -p 11680 root@221.228.73.10`` 输入密码后登陆成功.
  #.  ``cd /var/www/html/mnj/1.x.x/`` 1.x.x为具体版本目录.
  #.  ``rm -f monNickelodeonJr.swf`` .
  #. 如果是更新monNick.swf，回到本地bash, ``scp -P 11680 LOCAL_SWF_PATH root@221.228.73.10:/var/www/html/mnj/1.x.x/`` 输入密码.
  #. 如果是更新plugin.swf,回到本地bash, ``scp -P 11680 LOCAL_SWF_PATH root@221.228.73.10:/var/www/html/mnj/1.x.x/player/`` .
  #. OK.

 * **更新xml** 
  * 简单修改直接到服务器上改.
  #.  ``ssh -p 11680 root@221.228.73.10`` 输入密码后登陆成功.
  #.  ``cd /var/www/html/mnj/1.x.x/`` 1.x.x为具体版本目录.
  #.  ``vim CONFIG_XML_FILENAME`` and save.
  #. OK.

  * 复杂更新可以删掉服务器上的，再从本地upload上去.
  #.  ``ssh -p 11680 root@221.228.73.10`` 输入密码后登陆成功.
  #.  ``cd /var/www/html/mnj/1.x.x/`` 1.x.x为具体版本目录.
  #.  ``rm -f CONFIG_XML_FILENAME`` and save.
  #. 回到本地bash, ``scp -P 11680 LOCAL_XML_PATH root@221.228.73.10:/var/www/html/mnj/1.x.x/`` 输入密码.
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


更新SVN给老胡使用
-----------------
#. 测试OK没问题.
#. ``svn co http://192.168.20.200/svn/smit/ivmall/mnj/portal/WebRoot/mnj`` .
#. 将新版本的文件copy覆盖co下来的目录对应的文件.
#. ``svn ci -m 'COMMIT_LOG'`` .

 **注意检查几点** :

#. monNickelodeonJr.swf的文件名需要加上版本号.
#. index.htm，不是index.html.
#. index.htm里面有两处使用monNickelodeonJr.swf的地方，需要跟着版本号一起修改文件名. 
