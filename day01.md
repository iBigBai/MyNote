## 常见WIN_DOS命令

`d`  回车	盘符切换  
`dir` 列出当前目录下的文件以及文件夹(directory)  
`cd` 改变指定目录(进入指定目录)(change directory)  
`cd..`   退回到上一级目录  
`cd\(cd/)`   退回到根目录  
`cls `  清屏(clear screen)  
`exit`   退出dos命令行  
`md`   创建目录(make directory)  
`rd `  删除目录(remove directory)  
`del `  删除文件,删同一类型的文件*.txt  (delete)  
`notepad`   创建文件  
删除带内容的文件夹
`rd + /s`	文件夹名称(询问是否删除)  
`rd + /q + /s `文件夹名称(直接删除)  

## JDK目录详解
 * bin目录：该目录用于存放一些可执行程序。
 >如javac.exe（java编译器）、java.exe(java运行工具)，jar.exe(打包工具)和* javadoc.exe(文档生成工具)等。
* db目录：db目录是一个小型的数据库。
> 从JDK 6.0开始，Java中引用了一个新的成员JavaDB，这是一个纯Java实现、开源的数据库管理系统。这个数据库不仅轻便，而且支持JDBC 4.0所有的规范，在学习JDBC 时，不再需要额外地安装一个数据库软件，选择直接使用JavaDB即可。
* jre目录："jre"是 Java Runtime Environment 的缩写，意为Java程序运行时环境。
>此目录是Java运行时环境的根目录，它包括Java虚拟机，运行时的类包，Java应用启动器以及一个bin目录，但不包含开发环境中的开发工具。
* include目录：由于JDK是通过C和C++实现的，因此在启动时需要引入一些C语言的头文件
> 该目录就是用于存放这些头文件的。
* lib目录：lib是library的缩写，意为 Java 类库或库文件
> 开发工具使用的归档包文件。
* src.zip文件：src.zip为src文件夹的压缩文件
 >src中放置的是JDK核心类的源代码，通过该文件可以查看Java基础类的源代码。

## 命名规则
* 包名：
`com.qq.main`域名倒序书写，并且**所有字母小写**
* 类名&接口名：
`Demo`一个单词**首字母大写**
`MyDemo`多个单词**每个单词首字母大写**
* 方法名&变量名：
`main()`一个单词**全部小写**
`getString`	多个单词**第二个起单词首字母大写**
* 常量：
`ONE`一个单词**所有字母大写**
`ONE_TWO`多个单词**所有单词大写并用_间隔单词**