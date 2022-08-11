# git相关概念

![image-20220615194100505](D:\技术\笔记\springbootVue后台管理系统\git相关.assets\image-20220615194100505.png)

# 本地创建git仓库

![image-20220615193800535](D:\技术\笔记\springbootVue后台管理系统\git相关.assets\image-20220615193800535.png)

# 更新git仓库|备注|展示日志

> git add 文件名
>
> git commit -m "备注"

![image-20220615200256122](D:\技术\笔记\springbootVue后台管理系统\git相关.assets\image-20220615200256122.png)

> git log //展示git日志
>
> git log --pretty=oneline 单行日志
>
> <img src="D:\技术\笔记\springbootVue后台管理系统\git相关.assets\image-20220615200503929.png" alt="image-20220615200503929" style="zoom: 50%;" />
>
> 





# 版本回退|回退到未来

## 回退

> git reset --hard HEAD^  //回退到上一个版本

用`HEAD`表示当前版本，也就是最新的提交，上一个版本就是`HEAD^`，上上一个版本就是`HEAD^^`，当然往上100个版本写100个`^`比较容易数不过来，所以写成`HEAD~100`。

## 回退未来

只要上面的命令行窗口还没有被关掉，你就可以顺着往上找啊找啊，找到那个版本的`commit id`是`3da78`，于是就可以指定回到未来的某个版本。

版本号没必要写全，前几位就可以了，Git会自动去找。当然也不能只写前一两位，因为Git可能会找到多个版本号，就无法确定是哪一个了。

### 或者

要重返未来，用`git reflog`查看命令历史，以便确定要回到未来的哪个版本。

# 推送至github

## 创建远程仓库

## remote

> git remote add
>
> git remote -v

![image-20220615203325563](D:\技术\笔记\springbootVue后台管理系统\git相关.assets\image-20220615203325563.png)

## push

![image-20220615203458247](D:\技术\笔记\springbootVue后台管理系统\git相关.assets\image-20220615203458247.png)

> git push -u origin master	//第一次最好-u origin 远程仓库名字，master 分支名字
>
> git push origin master		//之后可以直接push

### push时由于原有仓库导致文件夹打不开

> git rm -r --cached "文件夹名称"

再重新提交即可

![image-20220615204740961](D:\技术\笔记\springbootVue后台管理系统\git相关.assets\image-20220615204740961.png)
