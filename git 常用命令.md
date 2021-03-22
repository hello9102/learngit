## git 常用命令

### 一、进行版本控制需要以下步骤：

#### 初始化命令

```git
git init
```

#### 查看文件状态

```
git status
```

#### 提交到暂存区

```
git add 文件名
git add .
```

#### 个人信息配置：用户、邮箱（一次即可）

```
git config --global user.email "****@163.com"
git config --global user.name "Name"
```

#### 生成版本

```
git commit -m '描述信息'
```

#### 查看版本记录

```
git log
```

### 二、回滚

#### 回滚至之前版本

```
git log
git reset --hard 版本号
```

#### 回滚至之后版本

```
git reflog
git reset --hard 版本号
```

### 三、紧急修复bug

#### 查看分支

```
git branch
```

#### 创建分支

```
git branch 分支名称
```

#### 切换分支

```
git checkout 分支名称
```

#### 创建并切换分支

```
git checkout -b 分支名称
```

#### 分支合并（可能产生合并）

```
git merge 要合并的分支

注意：切换分支再合并
```

#### 删除分支

```
git branch -d 分支名称
```

### 四、远程仓库

#### 添加远程链接

```
git remote add origin 地址
```

#### 推送代码

```
git push origin 分支名称
```

#### 下载代码（第一次）

```
git clone 地址
```

#### 拉取代码

```
git pull origin dev
等价于
git fetch origin dev
git merge origin/dev
```

#### 保持代码提交整洁

```
git rebase 分支
```

#### 记录图形展示

```
git log --graph --pretty=format:"%h %s"
```

### 五、多人协同开发

#### Tag标签管理

```
git tag -a v1.0 -m '版本介绍'					创建本地创建Tag信息
git tag -d v1.0 									   删除tag
git push origin --tags 							 将本地tag信息推送到远程仓库
git pull origin --tags 							 更新本地tag版本信息

git checkout v.10 									 切换tag
git clone -b v0.1 地址								指定tag下载代码
```

### 六、配置

#### 项目配置文件：项目/.git/config

```
git config --local user.name 'name'
git config --local user.email '****@163.com'
```

#### 全局配置文件：～/.gitconfig

```
git config --global user.name 'name'
git config --global user.name '****@163.com'
```

#### 系统配置文件：/etc/.gitconfig

```
git config --system user.name 'name'
git config --system user.name '****@163.com'

注意：需要有root权限
```

