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

   > 在进入python环境后，需要退出python环境再进行下面的步骤。

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

5. `pip list`查看已经安装的库

6. 其他操作

   * 删除虚拟环境
   * 删除环境中的某个包
   * 在虚拟环境中安装包：在进入虚拟环境的前提下，直接使用pip安装   
   * `pip install numpy==1.16.4`
   * `pip install tensorflow==1.12.0`
   * `pip install keras==2.2.4`    
   * `pip install matplotlib==2.2.2`
   * `pip install scikit-learn==0.21.0`



<br/>

### Jupyter Notebook中使用创建的虚拟环境

1. `activate myenv`进入环境
2. `source activate your_env_name`
3. `python -m ipykernel install --user --name=your_env_name`将环境写入notebook的kernel中
4. 在Jupyter Notebook中打开即可



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

## 常用函数



### Matplotlib






