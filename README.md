# BetterScroll 官网

## 如何参与编辑

#### 1、fork 本项目

#### 2、clone 代码到本地、安装依赖

```bash
git clone [your bscroll.io repo]

cd bscroll.io

git clone git://github.com/neurotoxinvx/huno.git themes/huno

npm install

hexo server

如果提示说 hexo server 命令不存在，请执行
npm install hexo-server --save

如果报错提示 ./build 下的一个文件缺失，请执行
npm install hexo-cli -g
```

#### 3、编辑文档

bscroll.io -> source -> _posts 中的 markdown 文档

#### 4、提交 Pull Request

## hexo 常用命令

```bash

创建 hexo 项目
hexo init

hexo 实时预览
hexo s

hexo 编译
hexo g

hexo 发布到 github
hexo d

清除本地 hexo 文件空间
hexo clean

```
