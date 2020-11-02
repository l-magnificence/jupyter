## jupyter
服务器jupyter notebook配置
#mamba 安装jupyter
```
conda create -n jupyter
conda activate jupyter
mamba install jupyter
```
#生成登陆密码
```
python
from notebook.auth import passwd
password()
```
#输入两次密码
```
Enter password: 
Verify password: 
Out[2]: '密文（后面要用）'
quit()
```
#配置jupyter notebook file
```
jupyter notebook --generate-config
```
将会在home目录下生成一个隐藏文件夹.jupyter，该文件夹中有一个jupyter的配置文件
#修改文件
```
vi jupyter_notebook_config.py
i
c.NotebookApp.ip='服务器IP地址'
c.NotebookApp.allow_root = True
c.NotebookApp.open_browser = False
c.NotebookApp.port = 9999 # 这里的端口可以自己定义，是之后连接的时候需要设定的
c.NotebookApp.password = ‘上面生成的密文’
esc
:wq
```
#启动
```
jupyter notebook
```
#本地浏览器上
输入ip地址:9999
输入密码





