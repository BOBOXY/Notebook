# GitHub入门

## 一、 本地Git使用

### 1. 新建一个文件夹，右键打开Open Git Bash Here

### 2. 初始化仓库
输入 git init 将仓库初始化Enter后返回如下图说明初始化成功
`git init`

```
周一擘@LEGION-Y7000P-ZhouYibo MINGW64 /f/Github file/Test 2025.1.26
$ git init
Initialized empty Git repository in F:/Github file/Test 2025.1.26/.git/
```
初始化成功后，文件夹内会自动生成 .git

### 3. 文件的添加\提交\删除

#### （1）在上面的文件目录中，新建一个文件
e.g. test_1.txt

#### （2）在git上输入 git add '自己新建文件的名字'，然后再输入git commit -m '提交信息'，
`git add test_1.txt`
```
周一擘@LEGION-Y7000P-ZhouYibo MINGW64 /f/Github file/Test 2025.1.26 (main)
$ git add test_1.html
fatal: pathspec 'test_1.html' did not match any files
```

`git commit -m 'First time'`
```
周一擘@LEGION-Y7000P-ZhouYibo MINGW64 /f/Github file/Test 2025.1.26 (main)
$ git commit -m 'First time'
[main (root-commit) 345c15b] First time
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test_1.html
```

#### （3）输入 git log 查看效果，结果如下说明提交成功
```
周一擘@LEGION-Y7000P-ZhouYibo MINGW64 /f/Github file/Test 2025.1.26 (main)
$ git log
commit 345c15b3a46614933662a9d4478f11a3299f974f (HEAD -> main)
Author: QLYB985 <932893706@qq.com>
Date:   Thu Jan 16 21:21:57 2025 +0800

    First time
```
#### （4）和上面步骤一样在新建一个 test.html，然后提交test.html，然后输入 git log 查看结果

#### （5）然后输入  git reset --hard '上图获取的id' ,然后再输入 git  reflog ,会发现我们新建的test.html被删除了。

#### （6）修改
`git status`
`git diff`

#### （7）git 常用的命令

## 二、本地Git和Github的连接

### 1. 注册GitHub账号

### 2. 本地配置用户名和邮箱
```
git config --global user.name "你的用户名"
git config --global user.email "你的邮箱"
```
```
git config --global user.name "BOBOXY"
git config --global user.email "932893706@qq.com"
```

### 3. 生成ssh key，将生成的ssh key复制到剪贴板
```
ssh-keygen -t rsa -C "932893706@qq.com"
```
本人windows PC 在此步骤报错，但先前已设置好

### 4. 打开GuiHub进入个人主页，点击Settings，在点击 SSH and GPG keys
然后把密钥粘贴到相应位置就创建成功

### 5. 回到 Git bash，输入：ssh -T git@github.com
`ssh -T git@github.com`
本人windows PC 在此步骤报错，但先前已设置好（原因未知），并且在终端中可以查看

## 三、本地Git和Github的连接

### 1. 登入自己的 Github，点击创建 Create repository

### 2. 对创建的项目工程内容进行选择性的填写

### 3. 在创建完成自己的库之后，下面就要让自己的电脑克隆一个自己所创建的库，方面自己电脑上的代码同步到 GitHub 所创建的库当中。为了实现，就需要安装一个软件 Git Bash。

### 4. 使用Git将代码提交到GitHub
该过程需要使用经常的接触的两个 Git 命令，包括：push和 pull
push：该单词直译过来就是 “推” 的意思，如果我们本地的代码有了更新，为了保持本地与远程的代码同步，我们就需要把本地的代码推到远程的仓库，代码示例：
```
git push origin master
```

pull：该单词直译过来就是 “拉” 的意思，如果我们远程仓库的代码有了更新，同样为了保持本地与远程的代码同步，我们就需要把远程的代码拉到本地，代码示例： 
```
git pull origin master
```

#### （1）克隆仓库
1 将我们的库克隆下来到本地电脑中，方便以后进行上传代码
2 点进仓库之后点击 Code，点击 ssh 会看到一串网址（http也可以），这个地址就是代码地址，git clone 命令会用的到
3 接下来我们就开始选择文件存储地方了，在本地电脑中找到存储文件的地方，然后右键选择 Git Bash Here
4 在终端输入 git clone 地址（这个地址就是刚刚库那个Code的上代码地址）
```
git clone git@github.com:BOBOXY/Notebook.git
```
#### （2）上传代码
1 `git add test_1.txt`

2 `git commit -m 'First time'`

3 `git push origin main`


Ref: https://blog.csdn.net/black_sneak/article/details/139600633