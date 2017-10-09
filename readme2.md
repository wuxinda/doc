# Maven的安装与环境配置

  想要安装 Apache Maven在Windows 系统上, 需要下载 Maven 的 zip 文件，并将其解压到你想安装的目录，并配置 Windows环境变量。
  所需工具 ：
  1.JDK
  2.Maven
  3.Windows 7
  注:Maven 3.2 要求 JDK 1.6 或以上版本, 而 Maven 3.0/3.1 需要 JDK 1.5 或以上。
  ## 1.JDK 和 JAVA_HOME
  确保已安装JDK，并 将“JAVA_HOME” 变量已加入到 Windows 环境变量中。
  
  ![cmd-markdown-logo](http://images2015.cnblogs.com/blog/915951/201612/915951-20161205105219585-470223969.png)
  
  我们可以打开Windows的命令行，运行如下的命令来检查Java的安装：
  
  ![cmd-markdown-logo](http://images2015.cnblogs.com/blog/915951/201612/915951-20161206201047226-878818071.png)
  
  上述命令首先检查环境变量JAVA_HOME是否指向了正确的JDK目录，然后运行了java命令，如果无法执行命令，或者无法找到JAVA_HOME环境变量，就需要检查Java是否安装了，或者环境变量是否设置正确。

  ## 2.下载Apache Maven
  下载地址：http://maven.apache.org/download.html，打开后找到下载链接，如图：
  
  ![cmd-markdown-logo](http://images2015.cnblogs.com/blog/915951/201612/915951-20161205110034288-179704586.png)
  
  以前下载的3.2.2的版本，用着也没什么问题，所以也懒得下载最新的版本，这里大家可以下载最新的版本下来用。当然，如果你对Maven的源代码感兴趣并想自己构建Maven，也可以下载apache-maven-3.3.9-src.zip。将下载的安装包解压到特定的目录下，假设你解压缩到文件夹 –  D:\apache-maven-3.2.2，如图：
  
  ![cmd-markdown-logo](http://images2015.cnblogs.com/blog/915951/201612/915951-20161206222455538-1077285607.png)
  
  ## 3.添加 M2_HOME 和 MAVEN_HOME
  
  打开系统属性面板（右击“计算机”>"属性"），单击高级系统设置，再单击环境变量，在系统变量中新建一个变量，变量名为M2_HOME，变量值为Maven的安装目录，如图：
  ![cmd-markdown-logo](http://images2015.cnblogs.com/blog/915951/201612/915951-20161206221927601-334023765.png)
  
  M2_HOME 或 MAVEN_HOME
  Maven 说只是添加 M2_HOME , 但一些项目仍引用 Maven 的文件夹 MAVEN_HOME, 因此，为了安全也把它添加进去。
  
  ## 4.添加到环境变量 - PATH
  
  编辑 PATH 变量，添加 Maven bin 文件夹到 PATH 的最后，如： %M2_HOME%\bin, 这样就可以在命令中的任何目录下运行Maven 命令了。
  
  ![cmd-markdown-logo](http://images2015.cnblogs.com/blog/915951/201612/915951-20161205110840116-2073862741.png)
  
  ## 5.验证
  
  在命令行中输入：echo %M2_HOME%以及mvn –version或-v,出现下面这个界面，说明我们的maven已经安装成功。
  
  ![cmd-markdown-logo](http://images2015.cnblogs.com/blog/915951/201612/915951-20161206222825366-1543269603.png)
  
  第一条命令echo %M2_HOME%用来检查M2_HOME是否指向了正确的Maven安装目录，mvn -v用来检查Windows是否能够找到正确的mvn执行脚本。
  
  ## 6.升级
  
  在Windows上更新Maven非常简单，只需要下载新的文件解压至本地目录，然后更新M2_HOME环境变量指向的目录即可，降级也是同理，不做过多介绍。
  
  
