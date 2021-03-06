## 基本概念
* 仓库：`Repository`
> 用来存放项目代码，每个项目对应一个仓库，多个开源项目则有第一个仓库
* 收藏：`Star`
> 收藏项目，方便下次查看
* 复制/克隆：`Fork`
> 该fork的项目是独立存在的
* 发起请求：`Pull Request`
> 基于Fork，其他人做了改进，希望合并到原项目中，简称（PR）
>详细步骤：
>* fork项目
>* 修改自己仓库项目代码
>* 创建Pull Request请求
>* 等待作者操作（合并：`Merge`，代码审查）
* 关注：`Watch`
> 关注某个项目，会收到更新提醒
* 问题卡片：`Issue`
> 关于项目到问题可以进行讨论
* Github主页
* 仓库主页
* 个人主页
## Git使用
### Git提交原理
* Git Repository（Git仓库）
> 最终确定的文件保存到仓库，成为一个新版本，并且对他人可见
* 暂存区
> 暂存已经修改的文件，最后统一提交到git仓库中
* Working Directory（工作区）
> 添加，编辑，修改文件的动作
``` mermaid
graph LR
A[工作区]-->|git add|B[暂存区index]
B-->|git commit -m|C[Git仓库head]
C-->|git push|D[github]
```
### Git常用命令
* 常用命令  
`git status`：查看文件当前状态  
`git branch -vv`：查看分支详细信息  
`git add test.java`：提交test文件到暂存区  
`git rm test.java`：删除Git文件  
`git commit -m '提交描述'`：提交文件到Git仓库  
`git push`：将本地Git仓库代码提交到远程Github  
`git remote add origin 项目地址`：将本地项目连接到github远程仓库  
`git checkout head test.java`：恢复本地误删文件,忽略工作区修改将文件还原  
`git reset --hard head^^`：恢复到上一个版本  
`git reset --mixed`：撤回commit，并且不会影响工作区  
`git reset head`：清除暂存区内容  
`git reflog`：日志  
`git pull`：命令用于从远程获取代码并合并本地的版本  
### Git基础设置
* 初始化用户：在GitHub会显示当前设置的用户名
>1. 设置用户名
`git config --global user.name 'iBigBai'`
>2. 设置用户邮箱
`git config --global user.email '888@qq.com'`
>3. 查看设置
`git config --list`
`git config --global user.name`
>4. 增加用户
`git config  --global --add user.name 'iBigBai'`
>5. 删除配置
`git config  --global --unset user.name`
>6. 修改配置
`git config --global user.name 'iBigBai'`
* 初始化Git：创建Git仓库
`git init`
### Git远程仓库
* Git克隆clone操作
`git clone 仓库地址`：clone项目
### 常见错误
- 错误：`The request URL returned error:403 Forbidden while accessing`
> 私有项目，没有权限，输入用户名密码，或者远程地址采用这种类型
>``` shell
vi .git/config
--将
[remote "origin"]
url=https://github.com/用户名/仓库名.git
--修改为
[remote "origin"]
url=https://用户名：密码@github.com/用户名/仓库名.git
>```
- 错误：`fatal: refusing to merge unrelated histories`
> 在两个分支合并的时候，出现了下面的这个错误。
> 解决方法：在你操作命令后面加`--allow-unrelated-histories`
>  例如：`git pull origin master --allow-unrelated-histories`
- 错误：```warning: Pulling without specifying how to reconcile divergent branches is
discouraged. You can squelch this message by running one of the following
commands sometime before your next pull:
  git config pull.rebase false  # merge (the default strategy)
  git config pull.rebase true   # rebase
  git config pull.ff only       # fast-forward only
You can replace "git config" with "git config --global" to set a default
preference for all repositories. You can also pass --rebase, --no-rebase,
or --ff-only on the command line to override the configured default per
invocation.```
## Github个人主页
### 个人主页
* 访问地址<https://用户名.github.io>
* 搭建步骤
>1. 创建站点--> 新建仓库（仓库名必须为：`用户名.github.io`）
>2. 新建`index.html`文件
### Project Page
* 访问地址<https://用户名.github.io/仓库名>
* 搭建步骤
>1. 在项目主页，点击<kbd>Settings</kbd>
>2. 在settings页面，点击<kbd>GitHub Pages</kbd>