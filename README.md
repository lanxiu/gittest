# gittest


# 警告
使用Windows的童鞋要特别注意：

千万不要使用Windows自带的记事本编辑任何文本文件。原因是Microsoft开发记事本的团队使用了一个非常弱智的行为来保存UTF-8编码的文件，他们自作聪明地在每个文件开头添加了0xefbbbf（十六进制）的字符，你会遇到很多不可思议的问题，比如，网页第一行可能会显示一个“?”，明明正确的程序一编译就报语法错误，等等，都是由记事本的弱智行为带来的。建议你下载Visual Studio Code代替记事本，不但功能强大，而且免费！



# 错误
教程是master分支 ，而现在是main分支 

```
echo "2222" >> 2.md
git add 2.md
git commit -m "second"
git push -u origin main

```

# 版本回退

```

 git log
 git reset --hard 1094a
 git reflog
```

# 概念
>工作区 
>暂存区 （stage)   
>head:指针  
>main：最先创建的主分支


# 撤销修改

```
git checkout -- readme.txt  
回到最近一次git commit或git add时的状态
一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；

一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。
注意:都是修改，第二种情况是如下操作 git add xxx   手工修改文件   git checkout


git reset HEAD readme.txt

从暂存区回退到工作区

git checkout 

从工作区取消修改


```


# 删除文件

```

git rm aa.txt
git commit
git checkout  "还原删错的文件"

```


#  添加远程库
```

git remote add origin git@github.com:michaelliao/learngit.git
第一次 -u,建立关联，之后省略
git push -u origin master
git push origin master

删远程库
git remote -v

git remote rm origin


git clone git@github.com:michaelliao/gitskills.git

```


