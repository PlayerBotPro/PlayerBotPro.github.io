---
layout: post
title: "创建基于Jekyll的Github pages"
date: 2025-01-16 11:45:14 +0800
categories: tutorial temp
---

# 1. Ruby安装

https://jekyllrb.com/docs/installation/windows/


## 1.1 Ruby的下载与安装

https://rubyinstaller.org/downloads/

选择带有`Ruby+Devkit`的选项, 比如`=> Ruby+Devkit 3.3.6-2 (x64)`

安装过程中保持默认设置, 在最后一步勾选`ridk install`, 打开新的控制台进行下一步操作


## 1.2 `ridk install`

控制台打开后, 输入3来安装`MSYS2 and MINGW development toolchain`
![My helpful screenshot](/assets/Ruby_Install_1.png)

然后静待安装完成, 如果途中出现报错或卡住, 则需要调整代理设置, 比如开启`Tun模式`

安装完成后可以直接关闭这个控制台窗口, 然后进行下一步Jekyll的安装
![My helpful screenshot](/assets/Ruby_Install_2.png)


# 2. Jekyll安装

https://jekyllrb.com/docs/installation/windows/


## 2.1 233
在完成Ruby的安装后, 打开一个新的cmd窗口来执行`gem install jekyll bundler`, 然后静待安装完成
![My helpful screenshot](/assets/Jekyll_Install_1.png)

安装完成后, 可以使用jekyll -v来验证安装效果: 
![My helpful screenshot](/assets/Jekyll_Install_2.png)


# 3. 创建Jekyll site

https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll


## 3.1 创建github pages repo

https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll#creating-a-repository-for-your-site


## 3.2 将Jekyll site创建到repo中

在cmd中输入以下内容: 
```batch
d:
cd D:\Code\PlayerBotPro.github.io
jekyll new --skip-bundle . --force
```


## 3.3 修改`Gemfile`

### 1. 给gem "jekyll"行添加注释

将以`gem "jekyll"`开头的第十行由

`gem "jekyll", "~> 4.3.4"`

改为

`# gem "jekyll", "~> 4.3.4"`


### 2. 补充`github-pages`版本

将以`# gem "github-pages"`开头的第15行由

`# gem "github-pages", group: :jekyll_plugins`

改为

`gem "github-pages", "~> 232", group: :jekyll_plugins`

其中`232`为[Dependency versions](https://pages.github.com/versions/)中对应的`github-pages` Version


## 3.4 `bundle install`

因为之前使用了`jekyll new --skip-bundle`, 所以现在需要`bundle install`?


## 3.5 修改`.gitignore`文件

将`Gemfile.lock`加入到`.gitignore`中


## 3.6 提交repo到github, 等待自动构建完成后可以查看
![My helpful screenshot](/assets/Jekyll_Install_3.png)


# 4. 向GitHub Pages中添加内容