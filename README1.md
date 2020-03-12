# ssrgood

安装手册  宝塔安装
yum install -y wget && wget -O install.sh http://download.bt.cn/install/install_6.0.sh
&& sh install.sh

选择初始环境安装， 【mysql5.7+php7.3】 ,其余保持默认值就行，等待5分钟左右完成安装
wget https://baiyue.one/latte_sspanel;bash latte_sspanel.数据库对接或迁移

宝塔左侧打开数据库，复制数据库密码，然后到 网站目录下/config/.confing.php 文件下修改数据


进入网站根目录后执行命令:【记得替换 latte.com 为自己的域名】

cd /www/wwwroot/latte.om/
php xcat creatAdmin
如果提示添加成功，则代表整个过程安装顺利。其他情况均为不正常。
旧站迁移(适合旧机场)
必要准备：数据库备份+配置文件 .config.php 备份。
基本过程同上。数据库对接后，请打开宝塔左侧，数据库管理，然后选中数据库执行SQL语句 UPDATE
user SET theme='latte' 用来更新用户的主题模板。
配置文件：打开新站的 .config.php 文件，然后对比本地备份的 config.php 文件,分块对照填写，
注意新旧不能直接copy粘贴，新版参数开头为 $ENV ,旧版为 $system
