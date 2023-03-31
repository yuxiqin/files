## Markdown

# Git

- origin: 表示远程(起源，因为首先clone到本地)；
- '--orphan': 表示空白;

至此获取最新的 .git 隐藏文件夹.

## 记住密码：
```
git config --global user.name "yuxiqin"
git config --global user.email "yuxiqin92@163.com"
git config --global credential.helper store
```

## 拉取到本地
```
git init
git clone https://gitee.com/yuxiqin92/notes.git
```

## 提交到远程
```
git add . #添加
git commit -m 'init' #提交
git push -u origin master #推送

三合一：
git add . & git commit -m 'ok' & git push -u origin master
```

## 强制覆盖本地
```
git fetch --all
git reset --hard origin/branch_name #(branch_name为对应的分支名)
git pull origin branch_name

三合一：
git fetch --all & git reset --hard origin/master & git pull origin master
```

## 强制覆盖远程
```
git add . #添加
git commit -m 'init' #提交
git push origin master --force #强制推送
```

## 清除所有提交
```
git checkout --orphan branch_name #创建空白分支 branch_name
git add . #添加
git commit -m 'init' #提交
git branch -D master #删除
git branch -m master #改名为master
git push -f origin master #强制提交
```