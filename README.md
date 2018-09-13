# 基于flask的博客系统搭建
- 1.部署的具体网址为http://www.unrealblue.xin/, 360安全浏览器和ie浏览器不兼容
- 2.下载代码到本地，先建立一个virtualenv坏境，我用的是pycharm软件，直接可以建立flask坏境,如下图所示:
![image](https://github.com/happyte/flask-blog/blob/master/images/1.png)
- 3.激活virtualenv环境，`. venv/bin/activate`。安装所有requirements.txt中的模块,`pip install -r requirements.txt`。因为网络的原因可能会其中某几个会安装失败，多安装几次就好。
- 4.导入坏境变量，需要导入以下三个变量
  * export MAIL_USERNAME=<your email@example.com>(开启了smtp服务的邮箱账号，程序里默认使用163邮箱，可以修改成其它类型邮箱)
  * export MAIL_PASSWORD=<password>(不一定是你的邮箱密码，比如163邮箱开启smtp服务会让你设置一个密码，该密码即为password,qq邮箱开启smtp会提示给你一个密码)
  * export FLASK_ADMIN=<admin email>(默认是管理者邮箱，用该邮箱创建账号就是管理者)
- 5.安装数据库迁移。输入以下命令
  * `python manager.py db init` (使用init命令创建迁移仓库)
  * `python manager.py db migrate -m "initial migration"`(migrate命令用来自动创建迁移脚本)
  * `python manager.py db upgrade`(更新数据库，第一次使用该命令会新建一个数据库，可以利用pycharm右侧的Database查看该数据库)
- 6.部署程序，`python manager.py deploy`
- 7.在本地运行程序,`python manager.py runserver`打开http://127.0.0.1:5000端口查看, 按Ctrl+C退出程序。

## 实际运行的效果
![image](https://github.com/happyte/flask-blog/blob/master/images/2.png)


![image](https://github.com/happyte/flask-blog/blob/master/images/3.png)


![image](https://github.com/happyte/flask-blog/blob/master/images/4.png)


![image](https://github.com/happyte/flask-blog/blob/master/images/5.png)
