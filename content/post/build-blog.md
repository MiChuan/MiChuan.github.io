---
title: "Build Blog"
date: 2022-06-01T04:20:49+08:00
draft: false
---

>  Hugo + Github 搭建个人博客

## 个人博客

[CodePoetry](https://michuan.github.io/)

## QuickStart

### 安装 Hugo

[Releases · gohugoio/hugo (github.com)](https://github.com/gohugoio/hugo/releases)

### 配置hugo环境变量

### 创建一个新的网站

```bash
// 命令行中进入工作目录
cd workspace
这样就在 /quickstart 目录里生成了初始站点
hugo new site quickstart
```

### 安装皮肤

[皮肤列表](https://www.gohugo.org/theme/)

```bash
cd themes
git clone https://github.com/spf13/hyde.git
```

###  添加主题说明

在根目录下的 config.toml 文件中添加主题说明

```bash
echo 'theme = "hyde"' >> config.toml
```

### 运行Hugo

执行 `Hugo` 命令进行调试

```bash
hugo server --theme=hyde --buildDrafts
```

浏览器里打开： `http://localhost:1313`

### 部署

#### GitHub Pages

- **在 Github Repository 的 Setting 页面，修改 Source 的选项为 master branch /docs folder**

- **修改配置文件 config.toml**：Github Repository 的 Setting 页面找到我们的 Github Pages 的域名地址，回到 config.toml 文件，找到 baseUrl，填入上述地址

  ```bash
  baseURL = "https://yourusername.github.io/"
  ```

- **打包网站到 /docs 文件夹**
- **上传代码至 master**

## 常用命令

### 添加一个文章

```bash
hugo new posts/my-first-post.md
```

### 设置文章draft: false

### 启动 Hugo 服务器进行本地渲染

```bash
hugo server -D
```

### 打包网站到 /docs 文件夹

```bash
hugo -d docs
```

### 上传代码至 master

```bash
git add .
git commit -m "updates $(date)"
git push origin master
```

## 参考资料

[使用 Hugo + Github 搭建个人博客 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/105021100)

[Hugo中文文档 (gohugo.org)](https://www.gohugo.org/)

[syui/hugo-theme-air: cname : syui.cf (github.com)](https://github.com/syui/hugo-theme-air)
