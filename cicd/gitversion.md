### 升级git

	centos6 自带的git版本太低， 在克隆远程仓库时， 会出现错误， 这是我试过的最简单但能够成功安装的一个方法

##### 1. 卸载centos自带的git

```
yum uninstall git
```

##### 2. 安装WANDisco， 根据自己的系统版本号选择

```

yum install http://opensource.wandisco.com/centos/6/git/x86_64/wandisco-git-release-6-1.noarch.rpm

- or -

yum install http://opensource.wandisco.com/centos/7/git/x86_64/wandisco-git-release-7-1.noarch.rpm

- or -

yum install http://opensource.wandisco.com/centos/7/git/x86_64/wandisco-git-release-7-2.noarch.rpm

```

##### 3. 安装git

```
yum install git
```

##### 4. 检查git版本

```
git --version
``````
