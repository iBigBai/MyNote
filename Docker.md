### Docker百科
 * Docker官网：<https://www.docker.com>
 * 仓库地址：<https://hub.docker.com>
### Docker安装
#### MacOS
* 使用 Homebrew 安装
[Homebrew](https://brew.sh/) 的 [Cask](https://github.com/Homebrew/homebrew-cask) 已经支持 Docker Desktop for Mac，因此可以很方便的使用 Homebrew Cask 来进行安装：
`$ brew install --cask docker`
### Docker原理
### Docker命令
### Docker镜像
### 容器数据卷
### DockerFile
### Docker网络原理
### IDEA整合Docker
### Docker Compose（集群）
### Docker Swarm
### CUI/CD Jenkins（持续集成/部署）
* Homebrew 错误信息
``` shell
      

Error: 

 homebrew-core is a shallow clone.

 homebrew-cask is a shallow clone.

To \`brew update\`, first run:

 git -C /usr/local/Homebrew/Library/Taps/homebrew/homebrew-core fetch --unshallow

 git -C /usr/local/Homebrew/Library/Taps/homebrew/homebrew-cask fetch --unshallow

These commands may take a few minutes to run due to the large size of the repositories.

This restriction has been made on GitHub's request because updating shallow

clones is an extremely expensive operation due to the tree layout and traffic of

Homebrew/homebrew-core and Homebrew/homebrew-cask. We don't do this for you

automatically to avoid repeatedly performing an expensive unshallow operation in

CI systems (which should instead be fixed to not use shallow clones). Sorry for

the inconvenience!

  

 **失败 去下面文章看一下第二部分的常见错误解决办法**

 **https://zhuanlan.zhihu.com/p/111014448**

 **如果没有解决，把运行脚本过程截图发到 cunkai.wang@foxmail.com**
```
