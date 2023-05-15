# Git-test
## 团队成员
- l9z9897
- l9zyr95
## 主要目的
- 练习git的使用
- 练习idea中git的使用
- 练习git提交本地库
- 练习git push 远程库      推送
- 练习git pull 远程库        拉取
- 练习git clone 远程库     克隆
## git 常用命令
| 命令 | 含义 |
| :--- | :--- |
| `git config --global user.name 用户名` | 设置用户签名（用一次） |
| `git config --global user.email 邮箱` | 设置用户邮箱（用一次） |
| `git init` | 初始化本地库 |
| `git status` | 查看本地库状态 |
| `git add 文件名` | 添加暂存区 |
| `git add -A` | 将全部修改的文件提交暂存区 |
| `git commit -m '提交描述' 文件名` | 提交到本地库 |
| `git commit -m '提交描述'` | 提交所有暂存区的文件到本地库 |
| `git reflog` | 查看历史记录 |
| `git log` | 查看版本详细信息 |
| `git reset --hard 版本号` | 版本穿梭 |

## git 分支操作

| 命令                  | 含义                         |
| --------------------- | ---------------------------- |
| `git branch 分支名`   | 创建分支                     |
| `git branch -v`       | 查看分支                     |
| `git checkout 分支名` | 切换分支                     |
| `git merge 分支名`    | 把指定的分支合并到当前分支上 |

## gitHub 操作

- 基本的操作

| 命令                                 | 含义                                           |
| ------------------------------------ | ---------------------------------------------- |
| `git remote -v`                      | 查看当前所有远程地址及别名                     |
| `git remote add 远程库别名 远程地址` | 给远程地址起别名                               |
| `git push 远程库别名 分支`           | 推送本地分支到远程库                           |
| `git pull 远程库别名 分支`           | 拉去远程库的相关分支<br>与当前本地分支直接合并 |
| `git clone 远程地址`                 | 将远程仓库的内容克隆到本地                     |

> 我们在向一个远程仓库`push`内容时，首先要把远程库的克隆下来，保持`master`分支是一致的，才能进行`push`操作。
>
> - `git clone 远程地址` ： 将远程仓库的内容克隆到本地库
> - 将我们要push的内容，复制到clone下来的文件夹内
> - 最后，添加暂存区，提交本地库，push远程库

- 合并冲突（比较重要，具体情况具体分析）

- <span style="color:blue; font-weight:bold">SSH免密登录 </span>    - （这个很好用，可以加速push和pull的操作）

  - 进入当前用户的家目录  `C:\Users\{user}`

    - `ssh-keygen -t rsa -C 描述信息`      (生成私钥公钥)

    ```shell
    # 一般用邮箱充当描述信息
    ssh-keygen -t rsa -C l9z9897@163.com
    ```
  
    - `cd .ssh`      (进入`.ssh`文件)
  
    - `cat id_rsa.pub`       (查看公钥)
  
  - 将公钥复制到github的指定位置即可
  
    > - 登录GitHub 点击头像选择 Settings
    >
    > - 选择 SSH and GPG keys
    >
    > - new SSH key
    >
    > - 随便起个名字，将公钥复制上去
    >
    > - 这样就可以了！可以使用SSH地址访问远程库了。
    

## IDEA中的git

- 进入IDEA

- 在Settings中，选择Version Control，选择Git，定位git程序

  > 定位到自己电脑安装的 `git.exe`文件

- 在`VCS`选项中，初始化本地库

- 然后就是添加暂存区，提交本地库，push远程库

- 其他的操作IDEA中都有相应的按钮选项

> <span style="color:blue; font-weight:bold">在配置IDEA环境前，我们也可以设置一下要忽略的文件：</span>
>
> - 在用户家目录下，创建忽略规则文件，`xxx.ignore` (建议：git.ignore)
>
> ```shell
> # Compiled class file
> *.class
> 
> # Log file
> *.log
> 
> # BlueJ files
> *.ctxt
> 
> # Mobile Tools for Java (J2ME)
> .mtj.tmp/
> 
> # Package Files #
> *.jar
> *.war
> *.nar
> *.ear
> *.zip
> *.tar.gz
> *.rar
> 
> # virtual machine crash logs, see http://www.java.com/en/download/help/error_hotspot.xml
> hs_err_pid*
> 
> .classpath
> .project
> .settings
> target
> .idea
> *.iml
> ```
>
> - (这里要说明的是：文件名可以随便取，只要保证扩展名是`ignore`；文件也可以随便放，一般建议放在用户家目录下)
> - 在`.gitconfig`文件中引用`git.ignore`文件
>
> ```shell
> [user]
> 	name = l9zyr
> 	email = l9zyr95@163.com
> [core]
> 	excludesfile = C:/Users/L9ZYR/git.ignore
> ```
>
> - 这样就好了，接下来就根据上面的步骤在IDEA中定位`git.exe`程序吧

## IDEA中设置github账号

- 进入IDEA

- 找到Settings

- 选择Version Control 

- 选择GitHub

- 绑定GitHub账号

  > 如果绑定不成功，还可以使用口令（Token）绑定：
  >
  > - 登录GitHub 点击头像选择 Settings
  > - 选择 Developer settings
  > - 创建一个Tokens(classic)      -  （创建好后要及时复制保存，因为网页一刷新就不见了）
  > - 回到IDEA，选择用Tokens绑定
  > - 将复制的Tokens粘贴到对应位置，完成即可
