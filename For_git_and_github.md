# GitHub入门

## 一、 本地git使用

### 1. 新建一个文件夹，右键打开Open Git Bash Here

### 2. 初始化仓库
输入 git init 将仓库初始化Enter后返回如下图说明初始化成功
`git init`
初始化成功后，文件夹内会自动生成 .git
(```)
周一擘@LEGION-Y7000P-ZhouYibo MINGW64 /f/Github file/Test 2025.1.26
$ git init
Initialized empty Git repository in F:/Github file/Test 2025.1.26/.git/
(```)

### 3.文件的添加\提交\删除

（1）在上面的文件目录中，新建一个文件
e.g. test_1.txt

（2）在git上输入 git add '自己新建文件的名字'，然后再输入git commit -m '提交信息'，
`git add test_1.txt`
(```)
周一擘@LEGION-Y7000P-ZhouYibo MINGW64 /f/Github file/Test 2025.1.26 (main)
$ git add test_1.html
fatal: pathspec 'test_1.html' did not match any files
(```)

`git commit -m 'First time'`

周一擘@LEGION-Y7000P-ZhouYibo MINGW64 /f/Github file/Test 2025.1.26 (main)
$ git commit -m 'First time'
[main (root-commit) 345c15b] First time
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test_1.html

（3）输入 git log 查看效果，结果如下图说明提交成功

（4）和上面步骤一样在新建一个 test.html，然后提交test.html，然后输入 git log 查看结果

（5）然后输入  git reset --hard '上图获取的id' ,然后再输入 git  reflog ,会发现我们新建的test.html被删除了。

（6）修改

（7）git 常用的命令

二、本地Git和Github的连接

1.注册GitHub账号

2.本地配置用户名和邮箱

3.生成ssh key，将生成的ssh key复制到剪贴板

4.打开GuiHub 进入个人主页 ，点击Settings，在点击 SSH and GPG keys 。