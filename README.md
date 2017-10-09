# Java配置----JDK开发环境搭建及环境变量配置

## 1. 安装JDK开发环境

![cmd-markdown-logo](http://images.cnitblog.com/blog/641601/201406/141837064202858.png)

![cmd-markdown-logo](http://images.cnitblog.com/blog/641601/201406/141837118586696.png)

![cmd-markdown-logo](http://images.cnitblog.com/blog/641601/201406/141837135613909.png)

开始安装JDK：

![cmd-markdown-logo](http://images.cnitblog.com/blog/641601/201406/141837152804351.jpg)

修改安装目录如下：

![cmd-markdown-logo](http://images.cnitblog.com/blog/641601/201406/141837169365577.jpg)

确定之后，单击“下一步”。

## 1. 配置环境变量

对于Java程序开发而言，主要会使用JDK的两个命令：javac.exe、java.exe。路径：C:\Java\jdk 1.7.0 _09\bin。但是这些命令由于不属于windows自己的命令，所以要想使用，就需要进行路径配置。 

单击“计算机-属性-高级系统设置”，单击“环境变量”。在“系统变量”栏下单击“新建”，创建新的系统环境变量。

![cmd-markdown-logo](http://images.cnitblog.com/blog/641601/201406/141837183747806.png)

(1)新建->变量名"JAVA_HOME"，变量值"C:\Java\jdk1.8.0_05"（即JDK的安装路径）

(2)编辑->变量名"Path"，在原变量值的最后面加上“;%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin”

(3)新建->变量名“CLASSPATH”,变量值“.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar”


如：JAVA_HOME环境变量的操作如下：

![cmd-markdown-logo](http://images.cnitblog.com/blog/641601/201406/141837213112074.png)

![cmd-markdown-logo](http://images.cnitblog.com/blog/641601/201406/141837222804145.jpg)


## 3. 确认环境配置是否正确：

在控制台分别输入java，javac，java -version 命令，出现如下所示的JDK的编译器信息，包括修改命令的语法和参数选项等信息。

java命令：

![cmd-markdown-logo](http://images.cnitblog.com/blog/641601/201406/141837234679916.png)

![cmd-markdown-logo](http://images.cnitblog.com/blog/641601/201406/141837245308258.png)

javac命令：

![cmd-markdown-logo](http://images.cnitblog.com/blog/641601/201406/141837262642929.png)

java -version命令：

![cmd-markdown-logo](http://images.cnitblog.com/blog/641601/201406/141837281081398.png)


[^code]: 代码高亮功能支持包括 Java, Python, JavaScript 在内的，**四十一**种主流编程语言。

[1]: https://www.zybuluo.com/mdeditor?url=https://www.zybuluo.com/static/editor/md-help.markdown
[2]: https://www.zybuluo.com/mdeditor?url=https://www.zybuluo.com/static/editor/md-help.markdown#cmd-markdown-高阶语法手册
[3]: http://weibo.com/ghosert
[4]: http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference

