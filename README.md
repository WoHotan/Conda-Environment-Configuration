# 安装 Anaconda 环境

为了方便大家的使用，我们把课程中需要使用的包和库封装成了安装文件，按照如下的方式安装、使用即可。

首先根据操作系统下载并安装 [Miniconda](https://conda.io/miniconda.html)（[Anaconda](https://docs.continuum.io/anaconda/install/) 也可以），然后下载环境我们的环境配置文件，解压文件，然后进行如下操作：

1. 首先移动到对应的路径：

   ```
   # 对于 Mac/Linux 系统，转到下载文件所在的路径
   cd ~/Downloads/Conda-Environment-Configuration 
   ```

   对于 Windows 系统，打开下载的目录，在地址栏里输入 `cmd` 然后按回车，如下图所示：
   ![windows configuration](windows%20configuration.jpg)

2. 对于在国内的同学，可以修改 Conda 的下载源来加速库的下载:

   ```
   # 优先使用清华conda镜像
   conda config --prepend channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
   # 也可选用科大conda镜像
   conda config --prepend channels http://mirrors.ustc.edu.cn/anaconda/pkgs/free/
   ```

3. 然后安装所需的依赖包并激活环境：

   ```
   conda env create -f environment.yml
   source activate mlnd-env # 注意Windows下不需要 source
   ```

4. 运行下面命令以成功打开 Jupyter Notebook，然后浏览器打开 [http://localhost:8888](http://localhost:8888/)（通常会自动打开）就可以相应地查看相关的项目了：

   ```
   jupyter notebook
   ```

5. 更多关于 Anaconda 的知识，可以浏览 [这个论坛帖子](http://discussions.youdaxue.com/t/python-conda-anaconda/43936)。



