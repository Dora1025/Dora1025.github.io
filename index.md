# Dora1025.github.io
## 外网破解pycharm2020专业版（网上很多，随意找）https://zhuanlan.zhihu.com/p/129239551
前提准备：
下载并安装2020专业版  下载jetbrains破解补丁包

1. Pycharm安装过程忽略，打开pycharm，跳过前面一些列提示后，在下面弹窗中，勾选“Evaluate for free”，点击Evaluate，跳转到新页面
2. 鼠标左键按住下载好的补丁压缩包，将其拖到上述的新窗口，松开鼠标即可，点击Restart重启后。将在弹出的JetbrainsAgent配置助手对话框中，选择License server 激活⽅式，点击安装按钮
3. 重启IDE，进入项目中，点击Help->About查看激活情况。如下图已激活

## 使用pipenv安装虚拟环境（外网）
1. 在命令行下运行：pip install pipenv 安装pipenv，手动创建一个本地项目目录存放虚拟环境，进入该目录，再执行pipenv install，成功后会在目录下自动生成两个文件，如下：
（用pipenv安装的虚拟环境，位置一般在 ~/.virtualenvs 目录下，在项目目录下执行pipenv --venv可以查看到具体位置）
2. 激活虚拟环境，在本地项目目录下执行pipenv shell进行激活

## 安装django
进入项目根目录，执行pipenv install django==2.2.3 指定版本安装，安装后测试是否安装成功，命令行输入：pipenv run python可进入虚拟python环境，再输入import django没有报错，输入print(django.get_version())可查看到对应的版本号
## 建立django工程
### 使用命令创建
待完善
### 使用pycharm直接创建  
待完善
## django工程中的settings文件常用
- 语言
LANGUAGE_CODE = 'zh-cn' 
- 时区
TIME_ZONE = 'Asia/Shanghai'
- 数据库的设置
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
    }
}
- 表示你的根 URLconf 的模块名.
ROOT_URLCONF = 'Django1.urls'
- 是否开启调试模式
DEBUG = True
## 熟悉manage命令
- python manage.py runserver：启用Django，默认情况下，服务器运行在IP地址127.0.0.1的8000端口上。
如果要自定义服务器端口和地址，可以接上一个IP地址和端口号。如：python manage.py runserver 127.0.0.1:8080
- python manage.py startapp：创建新的app，默认情况下，会在这个新的app目录下创建一系列文件模版
- python manage.py makemigrations：根据检测到的模型创建新的迁移？
- python manage.py migrate：对数据库的更改？
- python manage.py createsuperuser：创建超级用户，会被提示输入用户名，电子邮件地址，和密码，设置好后重新启动服务器，访问http://127.0.0.1:8000/admin， 可使用用户名和密码登录

## 遇到问题
将setting文件中的语言改为zh-cn后运行会报错，解决：改为zh-hans可正常，参考https://www.imooc.com/article/50638



