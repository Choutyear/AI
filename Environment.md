# Artificial-Intelligence
### 安装Anaconda

1. 下载Anaconda   

   <https://www.anaconda.com/products/individual>

2. Next -> 选择All Users -> Next -> 选择默认路径:`C:\ProgramData\Anaconda3` -> Next -> 不勾选Add Anaconda to the system Path environment variable，勾选Register Anaconda as the system Python 3.7 -> Install

3. 配置环境变量

   此电脑 -> 属性 -> 高级设置 -> 系统变量中的Path 

   ```
   C:\ProgramData\Anaconda3 （Python需要）
   C:\ProgramData\Anaconda3\Scripts （conda自带脚本）
   C:\ProgramData\Anaconda3\Library\mingw-w64\bin （使用C with python的时候）
   C:\ProgramData\Anaconda3\Library\usr\bin	#未配置
   C:\ProgramData\Anaconda3\Library\bin （jupyter notebook动态库）
   ```

4. 检验是否成功安装

   在cmd中输入`python`检验是否有python环境

   > 在进入python环境后，需要退出python环境再进行下面的步骤。`Ctrl`+`D`

   在cmd中输入`conda --version`查看conda版本

   在cmd中输入`conda info`

   打开Anaconda Navigator

   打开Jupyter Notebook

   

* 安装Anaconda时不能开代理，否则在打开Anaconda Navigator时会报Navigator Error：`check_hostname requires server_hostname`



<br/>

### Anaconda创建虚拟环境 

> 在进入虚拟环境后，进行的操作，都仅和当前虚拟环境有关，与base环境无关

1. `conda env list`查看当前存在哪些环境
2. `conda create -n your_env_name python=x.x` 创建指定版本的Python环境（your_env_name为自己的虚拟环境名）
3. `activate your_env_name`激活虚拟环境
4. `conda deactivate`关闭虚拟环境
5. `pip list`或者`conda list`查看已经安装的库
6. 其他操作

   * 查看当前环境的包`conda list`或者`pip list`
   * 删除虚拟环境`conda remove -n your_env_name --all`
   * 删除环境中的某个包`pip uninstall numpy`
   * 在虚拟环境中安装包：在进入虚拟环境的前提下，可以直接使用pip安装也可以使用conda安装  
```
   pip install numpy==1.16.4 //或者`conda install numpy==1.16.4`
   pip install tensorflow==1.12.0
   pip install keras==2.2.4
   pip install matplotlib==2.2.2
   pip install scikit-learn==0.21.0
```
`pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple`永久更改清华源


<br/>

### Jupyter Notebook中使用创建好的虚拟环境

1. `activate your_env_name`进入环境
2. `conda install ipykernel`安装ipykernel
3. `python -m ipykernel install --user --name your_env_name --display-name your_env_name`将环境写入notebook的kernel中
>`--display-name your_env_name`可有可无
4. 在Jupyter Notebook中打开即可
>此时好像不能直接输入命令打开，自己手动在Anaconda里打开就行了


<br/>

### Jupyter Notebook的快捷键

* 命令行模式（蓝色）（按`Esc`生效）
  * `Shift-Enter`: 运行代码块, 选择下面的代码块
  * `Ctrl-Enter`: 运行选中的代码块
  * `Alt-Enter`: 运行代码块并且在下面插入代码块
  * `M`: 把代码块变成 Markdown
  * `A`: 在上面插入代码块
  * `B`: 在下面插入代码块
  * 
* 编辑模式（绿色）（按`Enter`生效）



<br/>

### 常见问题

1. Python使用：文件必须导入到Python.exe文件所在目录下才能直接import，如果不知道目录，可以先`import sys`,再`print(sys.path)`来查看路径
2. 在删除虚拟环境后，jupyter的kernel有可能不会被删除，这时需要以管理员身份运行`Anaconda Prompt`，然后查看所有内核`jupyter kernelspec list`，最后删除`jupyter kernelspec remove kernel_name`


### 书后资源进入

1. `cd..`退回至根目录
2. `d:`选择D盘
3. `D:\workdata\handson-ml2`输入文件位置
4. `conda activate tf2`在该位置进入虚拟环境
5. `jupyter notebook`开始运行








