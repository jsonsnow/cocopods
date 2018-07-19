#### cocopods安装
安装教程参考了该链接（[参考地址](https://www.jianshu.com/p/f43b5964f582)），纯粹学习记录

配置ruby环境，目前Cocopods需求2.2.2版本及以上的ruby，如果版本小于该版本先进行ruby升级。

##### ruby升级步骤

1.查看当前ruby版本

```
ruby -v
```

2.安装rvm升级ruby环境

```
curl -L get.rvm.io | bash -s stable 
source ~/.bashrc
source ~/.bash_profile
```

3.查看rvm版本

```
rvm -v
```

4.列出ruby可安装版本信息

```
rvm list know
```

5.安装一个ruby版本(大于2.2.2,建议选择最新的)

```
rvm install 2.4.1
```

6.设置为默认版本

```
rvm use 2.4.2 --default
```

7.更换源（ruby-chain）

```
sudo gem update --system
gem sources --remove https://rubygems.org/
gem sources -a https://gems.ruby-china.org/
```
8.验证是否更换成功

```
gem sources -l
```

9.正式安装CocoaPods

```
sudo gem install -n /usr/local/bin cocoapods
```

10/如果安装了多个Xcode使用下面的命令选择

```
sudo xcode-select -switch /Applicaitons/Xcode.app/Contents/Developer
```

11.安装本地库

```
pod setup
```

以上为cocoapod安装步骤
第11步可以换成

```
git clone git://cocoapodscn.com/Specs.git ~/.cocoapods/repos/master
pod setup

```





