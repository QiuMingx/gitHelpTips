# gitHelpTips
记录使用git使用常用命令

日常工作有些命令不常用，等遇到一些突发情况时，常常需要网上搜索，为了以后便利在这里记录一下。

### 1. `git config` 对作者的邮箱进行配置,工作和GitHub邮箱不一致，常常提示GitHub没有commits显示记录，因为邮箱设置不对。

```
查看提交日志
git log  

如果只想修改这一个仓库的邮箱：
git config user.email "your_email@example.com"

可以使用如下命令确认修改是否成功：
git config user.email


如果想对所有的仓库生效，避免在别的仓库继续出现这个情况，则输入：
#git config --global user.email "your_email@example.com"

同样可以查看确认一下：
git config --global user.email

```
### 2. `git fetch` 放弃本地修改，强制拉取更新
#开发过程，对于本地的项目中修改不做保存或代码改崩，可以用到Git pull的强制覆盖

```
git fetch --all

git reset --hard origin/master
```
### 3. `git checkout` 删除本地某个文件后从remote端获取最新的
```
例如删除了当前目录下的README.md文件，要恢复当前remote的版本:

git checkout README.md

```
### 4. `git commit --amend` 修改最后一次提交
```
对于你的最近一次提交，你往往想做两件事情：简单地修改提交信息， 或者通过添加、移除或修改文件来更改提交实际的内容。

$ git commit --amend

```
### 5. `git revert -n` 回退到某次提交
```

$ git revert -n 97ea0f9

```
### 6. `git reset --hard HEAD` 回退到版本
```
$  git reset --hard HEAD

```
### 6. `git pull origin` 获取远程仓库中develop分支
```
$  git pull origin develop 获取远程仓库中develop分支上的commits

```
yarn install --no-lockfile --registry https://registry.npmmirror.com/`

