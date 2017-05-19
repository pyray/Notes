# 调整Jupyter notebook的启动目录

## 1. 在控制台输入以下命令，检查Jupyter notebook的安装目录

    jupyter notebook --generate-config

如：
    
    
    C:\Users\Administrator>jupyter notebook --generate-config

    # 得到配置文件的地址为： 
    
    C:\Users\Administrator\.jupyter\jupyter_notebook_config.py with default config? [y/N]n    # 选择不替换为默认配置

## 2. 用编辑器打开配置文件，修改默认路径

在配置文件中搜索“_dir”，定位到配置文件的键值 “c.NotebookApp.notebook_dir”，取消前面的注释，将其值更改为所需要的路径。如“u'F:\\10-InforTech'”。

BTW: 也可以在命令行启动jupyter notebook是增加参数，直接指定启动目录。但仅在本次启动中有效（可用jup4yter notebook -h查询帮助）,如：

      jupyter notebook --notebook-dir= F:\10-InforTech

### 以后在命令行打开jupyter notebook时，就会在预设目录打开了。

## 另外的一种方法是在命令行将当前目录调整到需要的目录下，再启动jupyter notebook。此时notebook就直接在当前目录下运行了。

### 以上修改对于在命令行启动jupyter notebook有效。由于在windows中安装Anaconda后，默认生成的jupyter notebook的图标启动命令为

  C:\ProgramData\Anaconda3\python.exe C:\ProgramData\Anaconda3\cwp.py C:\ProgramData\Anaconda3 "C:/ProgramData/Anaconda3/python.exe" "C:/ProgramData/Anaconda3/Scripts/jupyter-notebook-script.py" %USERPROFILE%”

### 参数“%USERPROFILE%”导致其启动目录固定在当前用户目录
