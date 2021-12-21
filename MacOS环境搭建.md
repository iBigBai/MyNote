# MacOS环境搭建
## 开发环境搭建
### java环境搭建
#### JDK
- Zulu[官网下载](https://www.azul.com/downloads/?package=jdk#download-openjdk)
- 解压压缩包-->`/Library/Java/JavaVirtualMachines`目录
- 配置环境变量文件`~/.bash_profile`(不存在就新建：`touch ~/.bash_profile`)
```shell
# 编辑 ~/.bash_profile(不存在就新建：touch ~/.bash_profile)
vim ~/.bash_profile
# 插入下面内容（按esc退出，按wq保存）
JAVA_HOME=/Library/Java/JavaVirtualMachines/zulu-8.jdk/Contents/Home
CLASSPAHT=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
PATH=$JAVA_HOME/bin:$PATH:
export JAVA_HOME
export CLASSPATH
export PATH
# 更新文件
source ~/.bash_profile
```
#### tomcat
- [官网下载](https://tomcat.apache.org/download-80.cgi)
- 解压压缩包-->`/Library/Java/Java`目录
#### maven
- 安装路径`/Library/Java/apache-maven-3.8.4`
- 配置环境变量`MAVEN_HOME=/Library/Java/apache-maven-3.8.4`
#### Git
1. 通过homebrew安装   
- 安装homebrew脚本   
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
```bash
# 错误：Failed to connect to raw.githubusercontent.com:443
# 处理：7890 和 789 需要换成你自己的端口
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:789
```
- 安装git脚本   
`brew install git`
#### 