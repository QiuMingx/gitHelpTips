# gitHelpTips
记录使用git使用常用命令

日常工作有些命令不常用，等遇到一些突发情况时，常常需要网上搜索，为了以后便利在这里记录一下。
(唉....，其实老了记忆力不好了，赶紧泡一杯枸杞补补)

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
