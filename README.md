## Django简易音乐网站

首先:

    在确保计算机环境已经安装好python3以上版本以及虚拟环境的情况下执行：
    mkvirtualenv 虚拟环境名称 -p python3
然后:

    打开项目配置好对应环境的解释器后
    pip3 install requirements.txt
    如果下载报错就手动单个包安装，主要的包也没几个

然后:

```
创建本地mysql数据库：
注意此处数据库名称需要与setting中配置一样，建议自行修改setting配置信息
create database music charset=utf8mb4;
```

然后:

```
数据库迁移完成后，可以本地查看是否成功，若成功无误后，执行：
python manage.py createsuperuser
创建超级管理员账户， 此账户用于admin管理系统的使用
```

然后:

```
终端定位到music项目目录，执行：
python manage.py migrate
数据库迁移版本信息已经生成，这里直接迁移就好， 注意django2.2.5迁移可能会出现报错，解决方法见：
https://www.cnblogs.com/huiyichanmian/p/12142671.html
```

最后:

```
项目迁移完成后，可以执行python manage.py runserver本地测试运行，项目中我个人利用爬虫爬取了一百首歌曲，
相关歌曲存放位置static/songFile, 
相关歌曲图片存放位置static/songImg, 
相关歌曲歌词存放位置static/songLyric
这三个文件夹是静态文件寻址的默认位置，在使用admin管理平台进行添加音乐时，只需要填写 音乐.mp3  图片.jpg 歌词.txt文件名称即可

注意：歌词文件只准备了一首歌的测试文件，只支持lrc文本格式。
```



## 如果想要给自己的音乐网站搬运更多的歌曲详情请见我个人的另外一个网易云音乐爬虫项目，支持批量导入喔！！！

