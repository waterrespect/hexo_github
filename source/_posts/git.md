---

title: git pull push

---

# git pull

## git拉取远程代码

```bash
git clone  https://xxx.git
```

## git拉取远程指定分支下代码（-b 分支名称）

```bash
git clone -b v2.8.1 https://xxx.git
```

## pull 则是将远程主机的master分支最新内容拉下来后与当前本地分支直接合并 fetch+merge

```bash
git pull origin master
```



# 本地仓库

## 初始化一个本地仓库，在同级目录下会出现一个隐藏的.git文件

```bash
git init
```

## 查看git的配置信息

```bash
git config -l
```

姓名-邮箱

```bash
git config user.name 'waterrespect'
```

```bash
git config user.email '12345@qq.com'
```

# git push

## 本地从缓存中加到文件库（repository）中

```bash
git commit -m '版本描述'  #提交到文件库
```

## 本地一件提交到文件库中

```bash
git commit -am '版本描述'   #一步完成提交
```

## 查看当前git状态信息（查看是否有文件未提交）

```bash
git status
```

## 删除缓存区所有文件命令

```bash
git rm -r --cached .   #主要这个点一定要写
```

## 重新add到缓存区

```bash
git add .
```

## push  推送本地修改分支至远程git仓库

```bash
git push -u origin xxxxx
```



# 分支

## 查看本地添加了哪些远程分支地址

```bash
git remote
```

##  查看本地添加了哪些远程分支地址（详细）

```bash
git remote -v
```

##  删除本地指定的远程地址

```bash
git remote remove origin
```

## 添加远程地址

```bash
git remote add origin https://xxxxxxxxxxxx.git
```

## 查看本地和远程的所有分支

```bash
git branch -a     # 查看本地和远程的所有分支
```

## 查看远程所有分支

```bash
git branch -r # 查看远程所有分支
```

