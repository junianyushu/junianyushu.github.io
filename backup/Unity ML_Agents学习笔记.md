#下载ML-Agents
在https://github.com/Unity-Technologies/ml-agents
下载适合自己的版本，并解压在全英文路径，否则会报错，要根据自己的unity版本和python版本

![Image](https://github.com/user-attachments/assets/ab6c7a33-c66d-436c-b5d0-74099c60f55c)，这里可以查看官方文档
#下载Anaconda
安装过程中将anaconda添加到环境变量，安装完成之后，可以在cmd中运行conda --version如果成功输出版本号，则添加成功；如果发生报错，请手动配置环境变量，在控制面板\系统和安全\系统\高级系统设置\环境变量\用户变量\PATH 中添加 anaconda的安装目录的Scripts文件夹。
#创建虚拟机
以管理员身份运行anaconda Prompt，然后输入conda create -n 【自己命名虚拟机】 python=3.10.12
然后cd /d G:\ml-agents-release_21，如果安装在C盘，则不用/d
然后输入conda -activate 【自己命名虚拟机】
win+r输入cmd
``` C#
pip3 install torch -f https://download.pytorch.org/whl/torch_stable.html
pip3 install -e ./ml-agents-envs
pip3 install -e ./ml-agents
```
进行下载
之后创建一个Unity项目，在packmanager里面选择从磁盘导入包找到\ml-agents-release_21\com.unity.ml-agents\package.json以及\ml-agents-release_21\com.unity.ml-agents-extensive\package.json导入
之后在unity中import官方已经训练好的3Dball模型，即可成功如图

![Image](https://github.com/user-attachments/assets/6a18fd4c-7a3d-4b66-b94c-29f05e76a1da)
之后进入虚拟机 conda -activate uml