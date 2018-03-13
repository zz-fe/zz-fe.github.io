## 配置git，告诉git谁在使用
```javascript
git config --global user.name ''
git config --global user.email ''
```![20170317164305_9111]
## 查看全局下的所有配置
```javascript
git config --list
```
## 创建文件夹
```javascript
mkdir zfpxgit
```
## cd change directory
```javascript
cd zfpxgit

```
## 初始化git仓库，初始化后会增加.git文件
```javascript
git init
```
## 查看目录
```javascript
ls -al
```
## 创建文件并写入内容
- 如果文件不存在则会创建文件
```javascript
echo "输入的内容"
 > index.html
```
> 单个> 会输出文件中，但是覆盖 >> 表示追加

## 查看文件内容
```javascript
cat index.html
```
## 增加到暂存区中
```javascript
git add index.html
```
## 增加到版本库中
```javascript
git commit -m 'ok'
```
##  查看版本
```javascript
git log --oneline
```
## 比较差异
- 比较的是暂存区和工作区的差异
```javascript
git diff 
```
- 比较的是暂存区和历史区的差异
```javascript 
git diff --cached
```
- 比较的是历史区和工作区的差异
```javascript
git diff master
```
## 撤回内容
- 用暂存区中的内容或者版本库中的内容覆盖掉工作区
```javascript
git checkout index.html
```
## 取消增加到暂存区的内容
```javascript
git reset HEAD index.html
```

## 删除暂存区
- 保证当前工作区中没有index.html
```
git rm index.html --cached
```

> 使用--cached 表示只删除缓存区中的内容

## 回滚版本
- 回滚最近的一个版本 git log
```
git reset --hard HEAD/commit_id
```

## 回滚到未来
```
git reflog
```
## 创建分支
```
git branch dev
```
## 切换分支
```
git checkout dev
```
## 创建分支并切换分支
```
git checkout -b dev
```
## 删除分支
```
git branch -d dev
``` 
## 在分支上提交新的版本
```
git commit -a -m 'dev1'
```

## 合并分支
```
git merge dev
```
## 分支的合并后显示log
```
git log --oneline --graph --decorate
``` 

## 在分支开发的过程中遇到其他问题需要切换其他分支
- 保留写好的内容在切换到主干
- 保留内容
```
git stash 
```

## 在次切换分之后需要应用一下保留的内容
```
git stash apply
```

## 丢掉保存的内容
```
git stash drop
```
## 使用并丢掉
```
git stash pop
```
## 有的时候开发需要合并指定的内容，而不是合并所有的提交，所以我们需要挑选最好的，自己生产版本


## 合并分支把树杈掰到主干上
```
git rebase
```


## push -u
-u参数 upstream
```
git push origin master -u
git push
```

## 创建忽略文件
```
touch .gitignore
```

## 连接远程仓库
```
git remote add origin 仓库的地址
```
## 查看远程仓库
```
git remote -v
```
## 删除远程仓库
```
git remote rm origin
```

##   组长  组员

## 组长提交项目
- 要先将组长的仓库fork到自己的仓库下
fork 是将组长代码复制一份放到自己的仓库下
- 组长将代码拉去到本地进行提交

## 克隆地址
```
git clone '地址' '文件夹的名字'
```

## 组员克隆下了代码，提交到组长自己仓库中


## 组员提交项目
- 用的是组长的仓库
- 需要组长给组员权限 settings 添加贡献者

## 组员和组长共用一个仓库，所以组员要将组长的项目拉到本地
## 组员要拉取最新的代码，防止推送时，将别人写的代码覆盖掉
```
git pull origin master
```
## 组员再次提交项目
- 拉取自己仓库的最新代码
```
git pull origin master
```

```
git remote add teacher https://.....
```![20170317170039_22798](http://ishare.58corp.com/uploads/image/201703/20170317170039_22798.png)