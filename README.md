# Git-test
## 团队成员
- l9z9897
- l9zyr95
## 项目主要目的
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
| `git commit -m '提交描述' 文件名` | 提交到本地库 |
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

- 合并冲突

- SSH免密登录

  - 进入当前用户的家目录`C:\Users\L9ZYR`

  - `ssh-keygen -t ras -C 描述信息` 生成私钥公钥

  - 进入`.ssh`文件 `cd .ssh`

  - 查看公钥 `cat id_rsa.pub`

  - 将公钥复制到github的指定位置即可。

    ```
    settings -> SSH and GPG keys -> new SSH key -> 随便起个名字，将公钥复制上去
    ```

## IDEA中的git

- settings中定位git程序
- 初始化本地库  在`VCS`选项中
- 其他的操作就省略了......，很简单

## IDEA中设置github账号

- settings
- Version Control 
- GitHub
