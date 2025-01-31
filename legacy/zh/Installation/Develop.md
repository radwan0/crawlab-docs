## 开发模式

开发模式可以让开发者很快的预览源码的输出效果，即时更改代码就可以看到修改后的程序运行情况。开发模式是针对希望在 Crawlab 的源码基础上进行二次开发或者希望贡献 Crawlab 的开发者。相较于 [直接部署](Direct.md)，开发模式更多体现在其可调试性和灵活性，不像直接部署那么稳定。

⚠️**注意**: 强烈建议不要用开发模式在生产环境中，因为开发模式运行的程序非常不稳定，不利于在生产环境中运行。

**推荐人群**: 

- 了解 `Node`、`Golang`、`MongoDB`、`Redis` 的安装和使用方式的开发者
- 需要二次开发 Crawlab 的开发者
- 希望贡献 Crawlab 的开发者

**推荐配置**:

- Go: 1.12+
- Node: 8.x+
- MongoDB: 3.6+
- Redis: 5.x+

### 1. 拉取代码

首先是将 GitHub 上的代码拉取到本地。

```bash
git clone https://github.com/crawlab-team/crawlab
```

### 2. 安装 Node 环境

请参照 [直接部署](Direct.md) 第 2 节。

### 3. 安装前后端

请参照 [直接部署](Direct.md) 第 3 节。

### 4. MongoDB & Redis

请参照 [直接部署](Direct.md) 第 6 节。

### 5. 配置

请参照 [直接部署](Direct.md) 第 7 节。

### 6. 启动前端

在 `./frontend` 目录里，运行以下命令启动前端。

```bash
npm run build:dev
```

这时，您可以在浏览器中输入 `http://localhost:8080` 看到界面了，只是暂时还无法连上后端。

在开发模式下，任何您修改的前端代码将会直接反应到界面上，意味着您不需要重新编译启动前端。

### 7. 启动后端

在 `./backend` 目录里，运行以下命令启动后端。

```bash
go run main.go
```

⚠️**注意**: 任何后端的修改，您都需要重新启动上述命令来看到变化。

### 8. 开发 Crawlab

欢迎任何对爬虫管理平台感兴趣的开发者来贡献或开发 Crawlab。

完成上述步骤之后，相信您已经可以顺利将 Crawlab 运行起来了，而且能看到页面。为了让开发 Crawlab 更加轻松，您需要了解更多相关知识，强烈建议您先阅读 [原理章节](../Architecture/README.md) 和 [贡献章节](../Contribution/README.md)。

### 
