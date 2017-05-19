# 建立Anaconda的多Python环境

## 1. 检查conda下的Python环境

安装anaconda并设置了路径变量后，在控制台输入以下命令以检查现有的环境：

    conda info -e
    
此时应该看到本机conda下有哪些Python环境。如果仅安装Anaconda的某一个版本，则可能只有一个‘root’

## 2. 在conda下新增一个Python环境

    conda create --name mypy3 python=3  #创建一个名称为mypy3，使用Python3.x版本的环境。conda会搜索，并下载安装最新的Python3.x版

## 3. 检测Python环境

    activate mypy3                      #在windows系统中激活进入mypy3环境，如果是Ubuntu系统，则为 source activate mypy3
    python -V                           #检查该环境下Python的版本。应该是需要的3.x版。此时在命令符模式下输入python即启动相应版本的python编辑器
    deactivate mypy3                    #退出mypy3环境。此时回到默认的Python版本（如果有）
    
## 4. 在Jupyter notebook中增加该环境变量选项
    
    activate mypy3
    conda install ipykernel             #在相应环境中安装ipykernel，由于各环境是独立的，故每一个环境都要分别安装
    python -m ipykernel install --user  #在jupyter notebook 中增加该环境选项。如果在Ubuntu下，可写成mypy3 -m ipykernel install --user
    deactivate mypy3                    #退出mypy3环境。同样，在Ubuntu下，需要在前面增加source
    
重复上述步骤，即可增加更多的不同版本的Python环境。

然后可以在Jupyter notebook中选择新建不同版本Python的notebook文件；也可以在运行是进行核心切换。
    