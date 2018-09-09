##### 环境篇


在linux环境下安装docker

 - 先装vmware

 - 下载linux镜像，我使用的是基于ubuntu的[Linux Mint 18.3 "Sylvia" - Cinnamon (64-bit)](https://www.linuxmint.com/edition.php?id=246)， 之所以选择这个， 是因为之前装系统时，只有mint一次成功，所以对它比较有好感。当然， 最主要的原因还是在安装ubuntu和centos时， 都出现了不小的麻烦， 先规避一下， docker整起来再说。 
 
 - 安装docker过程

 ```
    sudo apt-get update

    sudo apt-get install docker

    docker --version
 ```

在windows环境下安装docker，windows必须是win10， 因为支持hyper-v, 可惜我的不支持， 但这怎能难倒我， 直接使用[docker toolbox](https://docs.docker.com/toolbox/overview/)， 安装完之后， 直接运行quickstart就可以了

#### 前端持续集成(CI)与持续交付(CD)

##### 什么是CI和CD

##### 为什么需要CI/CD

##### CI篇

##### CD篇

##### 实战操作， 完整走完流程

##### 帮助

[centos如何升级git到最新版本](gitversion.md)

[nginx根据端口号配置不同目录下资源](portsite.md)
