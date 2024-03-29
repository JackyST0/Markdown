# git 基础：
##### 1. 进入存放文件的文件夹并打开 git bash。

##### 2. 输入 git init ----- 初始化空的 git 版本库。

##### 3. 输入 git add (文件名) ----- 把文件上传到 git 列表上。
###### 提示：
* ###### 上传成功不显示任何命令，接着输入命令即可。

##### 4. 输入 git commit (文件名) -m "这里填入描述文件的一些信息" ----- 确认把新加入文件的列表提交到 git 服务器上。（如果是首次提交，应该会出现如下问题）
```
      *** please tell me who you are.
      Run
        git config -- global user.eamil "you@example.com"
        git config -- global user.name  "Your Name"
      to set your account's default identity.
      Omit --global to set the identity only in this repository.
      fatal: unable to auto-detect email address (got 'itcast@itcast.(none)')
```
###### 解决方法：
```
      1. 执行：git config -- global user.eamil "you@example.com"
      2. 执行：git config -- global user.name  "Your Name"
      3. 再次执行上面的提交指令即可
```
###### 提示：
* ###### -m "这里填入描述文件的一些信息" ----- 是作为以后出现代码冲突，进行回退的首要理论依据。

##### 5. 输入 git remote add origin （github 上对应仓库的 URL） ----- 指定 github 上对应的 URL 来关联了本地网络和 git 服务器的一些关系。

##### 6. 输入 git push origin master ----- 把要上传的文件真正推送到 git 服务器上。（提交后，会提示如下）
```
      Username for 'https://github.com'：               ---输入注册 github 的 username
      Password for 'https://afei-itcastedu@github.com': ---输入密码
```
###### 解决方法：
```
      按提示依次输入即可。
```       

- - -

## git 过程中的 bug ：
##### 1. ```! [rejected] master -> master (fetch first)``` ----- 在 push 远程服务器的时候发现出现此错误；原因是线上版本的內容比你电脑里这份还要新，所以 Git 不让你推上去。 
###### 解决方法：
##### 因为你电脑里的内容是比较旧的的，所以你应该先拉一份线上版本的回來更新```git pull origin master``` ，然后再重新 push 即可。
![git 图片](https://raw.githubusercontent.com/JackyST0/Markdown/master/bug%201.png)

##### 2. ```error: remote origin already exists.``` ----- 提示远程仓库已存在。
###### 解决方法：
##### 我们可以先输入 ```git remote -v``` 来查看远程仓库是否是自己的的仓库，是则可不用理会，否则我们输入 ```git remote rm origin``` 删除关联的 origin 的远程库，然后我们再重新关联上自己仓库即可。
![git 图片](https://raw.githubusercontent.com/JackyST0/Markdown/master/bug%202.png)

##### 3. ```! [rejected] master -> master (non-fast-forward)``` ----- 在 push 远程服务器的时候发现出现此错误；原因是 github 中的 README.md 文件不在本地代码目录中或和本地代码不同步。
###### 解决方法：
##### 可参考 bug1 的解决方法，若还是不行可以尝试使用 ```git push -f``` 以达到把本地修改的代码强制推上去的目的。
![git 图片](https://raw.githubusercontent.com/JackyST0/Markdown/master/bug%203%20.png)

##### 4. ```error: Your local changes to the following files would be overwritten by merge:``` ----- 原因是因为有人修改了线上的代码文件，而我们本地也修改了代码文件，这时进行pull自然就会产生冲突。
###### 解决方法：
##### 执行以下代码：
```
      git stash
      git pull origin master
      git stash pop
```
##### 如此一来，服务器上的代码更新到了本地，而且你本地修改的代码也没有被覆盖，之后使用add，commit，push 命令即可更新本地代码到服务器了。
![git 图片](https://raw.githubusercontent.com/JackyST0/Markdown/master/bug%204.png)

- - - 

## 其他命令：
-  ##### git status 
```
git status命令可用于查看当前本地仓库工作区文件的状态
```

- ##### git pull --rebase origin master
```
该命令的意思是把远程库中的更新合并到（pull=fetch+merge）本地库中，
–-rebase的作用是取消掉本地库中刚刚的commit，并把他们接到更新后的版本库之中。
```
- ##### git restore (文件名)
```
git restore指令使得在工作空间但是不在暂存区的文件撤销更改。(内容恢复到没修改之前的状态)
```
- ##### git restore --staged (文件名)
```
git restore --staged的作用是将暂存区的文件从暂存区撤出，但不会更改文件的内容。
```
- ##### git remote -v
```
此命令可以用于查看当前用户本地仓库关联的git服务器仓库地址。
``` 

- ##### git reset
```
git reset命令的作用是将暂存区的文件取消暂存
```

- ##### git reset --hard (commit标识)
```
此命令的作用是将暂存区的文件切换到指定版本
```

- ##### git log
```
git log命令的作用是查看日志
```

- ##### git clone (远程仓库的url)
```
git clone命令的作用是克隆远程仓库到本地，把Git仓库服务器上的几乎所有数据（包括日志信息、历史记录等）全部克隆到本地仓库
```

- ##### git branch
```
git branch        列出所有本地分支
git branch -r     列出所有远程分支
git branch -a     列出所有本地分支和远程分支
```

- ##### git branch (branchName)
```
此命令的作用是创建一个新的分支
```

- ##### git checkout (branchName)
```
此命令的作用是用于切换某一条分支
```

- ##### git merge (branchName)
```
此命令是用于合并某一条分支
```

- ##### git tag
```
git tag命令用于列出已有的标签
```

- ##### git tag (tagName)
```
此命令用于创建一个新标签
```

- ##### git cheackout -b (branch) (tagName)
```
此命令的作用是新建一个分支来指向某个标签从而可以查看这个标签下的内容
```