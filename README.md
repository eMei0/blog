# Hugo静态博客

这是一个使用Hugo静态博客生成器创建的GitHub Pages项目。

## 项目结构

```
blog/
├── archetypes/        # 文章模板
├── content/           # 博客内容
│   ├── posts/         # 博客文章
│   └── about.md       # 关于页面
├── themes/            # 主题
│   └── ananke/        # 自定义主题
├── config.toml        # Hugo配置文件
├── index.html         # 临时首页
└── README.md          # 项目说明
```

## 如何使用

### 安装Hugo

在使用此博客之前，您需要先安装Hugo。

#### Windows安装方法

1. 使用Chocolatey（推荐）：
   ```
   choco install hugo -confirm
   ```

2. 或者直接下载二进制文件：
   - 访问 [Hugo Releases](https://github.com/gohugoio/hugo/releases)
   - 下载适合您系统的版本（如hugo_extended_0.92.0_Windows-64bit.zip）
   - 解压文件并将hugo.exe添加到系统PATH中

#### macOS安装方法

使用Homebrew：
```
brew install hugo
```

#### Linux安装方法

使用Snap：
```
snap install hugo
```

或使用apt（Debian/Ubuntu）：
```
sudo apt-get install hugo
```

### 运行博客

1. 在博客根目录下打开终端
2. 运行以下命令启动本地服务器：
   ```
   hugo server -D
   ```
3. 在浏览器中访问 http://localhost:1313 查看博客

### 创建新文章

使用以下命令创建新文章：
```
hugo new posts/my-new-post.md
```

然后编辑 `content/posts/my-new-post.md` 文件添加您的内容。

### 构建静态文件

要生成可部署的静态文件，运行：
```
hugo
```

生成的文件将位于 `public` 目录中。

## 部署到GitHub Pages

1. 创建一个名为 `<username>.github.io` 的GitHub仓库
2. 构建静态文件：`hugo`
3. 将 `public` 目录中的内容推送到该仓库的主分支

或者，您可以设置GitHub Actions自动部署：

1. 在仓库中创建 `.github/workflows/hugo.yml` 文件
2. 添加适当的工作流配置
3. 推送到GitHub，它将自动构建和部署您的站点

## 自定义博客

### 修改配置

编辑 `config.toml` 文件以更改站点标题、描述、菜单等。

### 修改主题

本博客使用自定义的ananke主题。您可以修改 `themes/ananke` 目录下的文件来自定义主题。

### 添加更多功能

您可以通过安装Hugo模块或修改主题来添加更多功能，如评论系统、分析工具等。

## 许可证

[MIT](LICENSE)
