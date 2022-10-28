个人网站生成工厂

## 快捷启动项目

> 需要环境 `git` `npm`

``` bash
$ git clone git@github.com:WANGJUEYA/B612-Factory.git --recursive
$ cd B612-Factory
$ npm install
$ npm run server
```

+ 如果本地ssh密钥不为空会有 `Permission denied`报错, 使用 git-bash 客户端
+ 用自己的markdown文件替换 `./source/_posts` 下所有文件

## 主题没有在仓库存储, 需要手动拉取

```bash
cd .\themes\

git clone git@github.com:WANGJUEYA/hexo-theme-christmas-tree.git christmas-tree

git clone git@github.com:blinkfox/hexo-theme-matery.git

git clone git@github.com:fluid-dev/hexo-theme-fluid.git

git clone git@github.com:wujun234/hexo-theme-tree.git

cd ..
```

# 笔记没有在仓库中存储, 需要手动拉取

```bash
cd .\source\

git clone git@github.com:WANGJUEYA/magic-book.git _posts

cd ..
```

# 加入子模块

```bash
git rm -r --cached themes/christmas-tree
git submodule add git@github.com:WANGJUEYA/hexo-theme-christmas-tree.git ./themes/christmas-tree
git rm -r --cached source/_posts
git submodule add git@github.com:WANGJUEYA/magic-book.git ./source/_posts
```

# 升级计划

+ ~~分类页展示目录树~~
+ 首页标题动态拉取数据库 `subtitle`
+ markdown能替换跳转链接相对路径
+ ~~在线文章有编辑按钮, 点击跳转github仓库源对应编辑页面(有权限用户能直接编辑提交)~~
+ ~~GitHub Action自动构建(子模块同步构建)~~
+ 配置文件整理 [_config.\[theme\].yml](https://hexo.io/zh-cn/docs/configuration#%E4%BD%BF%E7%94%A8%E4%BB%A3%E6%9B%BF%E4%B8%BB%E9%A2%98%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6)
