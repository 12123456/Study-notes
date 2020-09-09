## 一、下载项目

#### 1、初始化文件夹

​		首先新建一个空文件夹，把文件夹进行git初始化操作,在文件夹的根目录下，右键选择git bash here，在弹出的窗体中输入命令：

```
git init
```



#### 2、下载项目

​		接下来就是clone操作了，继续输入命令：git clone xx(此处为你的项目的git地址），一般这个命令clone下来的是master分支的项目，你也可以clone指定分支的工程，命令：

```
git clone -b 分支名 git地址
```



## 二、更新代码

#### 1、更新代码到本地  

```
git pull 
```



## 三、上传代码

#### 1、初始化文件夹

​		如果该工程没有git初始化，那么在工程根目录下使用git init进行初始化

```
git init
```

#### 2、添加文件

​		将项目的文件添加到仓库中使用git add，（git add . ）表示将所有文件都添加，（git add xx(指定文件)）表示将指定文件添加进去

```
git add
```

#### 3、查看本地文件信息

```
git statu
```

#### 4、提交仓库

​		将add的文件commit到仓库，命令：

```
git commit -m "注释"
```

#### 5、提交代码到当前分支

```
git push
```



## 四、其他命令



#### 1、关联项目地址

​		将本地的仓库关联到github上，命令如下：git remote add origin xxx（此处为你的git地址）

```
git remote add origin 项目地址
```

#### 2、pull

​		在进行push之前，先进行pull操作，更新代码到本地  ，命令如下：

```
git pull origin xxx(此处为你的分支名，master或者其他分支名)
```

#### 3、push

​		上传代码到github远程仓库，命令如下：

```
git push -u origin xxx（此处为你的分支名）
```

在这个步骤中可能会有弹窗要你输入你的用户名和密码，按照指示操作即可

#### 4、查看当前分支

```
git branch  
```

