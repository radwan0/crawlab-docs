## Git 配置

Git 是一个版本管理系统（VCS），对于需要代码回溯、分支管理、代码回滚等功能的企业来说，是个非常有用的工具。市面上的 Git 代码托管服务有很多，例如 GitHub、GitLab、Gitee 等等，当然您也可以自己搭建 Git 服务。

如 [CI/CD 章节](README.md) 中所示（如下图），Crawlab 支持 Git 仓库同步到各个在线节点，您需要做的只是启动爬虫的 Git 设置，并配置好 Git 设置。

![](http://static-docs.crawlab.cn/crawlab-ci-cd.png)

#### 开启 Git 设置

开启 Git 设置很简单，您只需要在**创建爬虫**或**爬虫详情**的地方，将下图中所示的 “是否为 Git” 开关开启。

![](http://static-docs.crawlab.cn/is-git.png)

#### 配置 Git

开启 Git 之后，您可以在爬虫详情中看到 “Git 设置” 标签，点开的界面如下图。

![](http://static-docs.crawlab.cn/git-settings.png)

Crawlab 的 Git 同步是同时支持 HTTP 和 SSH 的。

如果您是 **HTTP**，您可以这样操作：

1. 将仓库地址填写在 `Git URL` 输入框；
2. 然后点开 `需要验证`，并填写验证信息；
3. 选择 `Git 分支` ；
4. 点击 `保存` 按钮。

如果您是 **SSH**，您可以这样操作：

1. 点击 `复制` 按钮，将 `SSH 公钥` 加入到 Git 服务（您可以网上搜索一下如何在 Git 服务中添加 SSH 公钥）；
2. 将仓库地址填写在 `Git URL` 输入框；
3. 选择 `Git 分支` ；
4. 点击 `保存` 按钮。

#### 自动同步

如果您需要自动同步，您可以打开 “自动同步” 开关，然后选择同步频率。这样，Git 上的爬虫代码一旦有更新，Crawlab 就会按照同步频率自动将其同步回来。

#### 手动同步

点击红色的 “同步” 按钮并确认，即可手动同步 Git 仓库的爬虫代码。

#### 重置

有时候您需要重置代码，也就是清除该仓库的所有代码，只需要点击 “重置” 按钮并确认。

#### 查看版本

在 Log 标签中，您可以看到所有的 Commits，以及其对应的分支（Branches）和版本（Tags），以及谁提交的代码，如下图所示。

![](http://static-docs.crawlab.cn/git-log.png)

#### 切换版本

同样是在 Log 标签，您可以看到每一个提交（Commit）右下方有一个红色的 Checkout 按钮，点击它即可将爬虫代码切换到该版本。
