个人网站生成工厂

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