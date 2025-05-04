## F 笔记  
### DocGitHub 代码托管平台文档  
GitHub文档：https://docs.github.com/zh  
#### 20250225 GitHubPages：https://docs.github.com/zh/pages/quickstart  
##### 目录  
###### 快速入门  
###### 入门  
关于GitHubPages  
创建GitHubPages站点  
使用自定义工作流  
配置发布源  
删除GitHubPages站点  
取消发布Pages站点  
创建自定义404页面  
使用HTTPS保护站点  
将子模块与Pages一起使用  
排查404错误  
###### 使用Jekyll设置站点  
GitHub Pages 和Jekyll  
使用Jekyll创建站点  
使用Jekyll本地测试站点  
将内容添加到Pages站点  
设置Markdown处理器  
将主题添加到Pages站点  
Pages的Jekyll构建错误  
排查Jekyll错误  
###### 配置自定义域  
在GitHubPages中自定义域  
管理自定义域  
验证自定义域  
排除自定义域的故障  
##### 笔记  
###### 谁可以使用此功能？  
GitHub Pages 适用于具有 GitHub Free 和组织的 GitHub Free 的公共存储库，  
以及具有 GitHub Pro、GitHub Team、GitHub Enterprise Cloud 和 GitHub Enterprise Server 的公共和专用存储库。   
有关详细信息，请参阅【GitHub 的计划】。  
GitHub Pages 现在使用 GitHub Actions 来执行 Jekyll 构建。  
使用分支作为构建源时，如果要使用内置的 Jekyll 工作流，则必须在存储库中启用 GitHub Actions。  
或者，如果 GitHub Actions 不可用或已禁用，  
则将 .nojekyll 文件添加到源分支的根目录  
将绕过 Jekyll 构建过程并直接部署内容。  
有关启用 GitHub Actions 的详细信息，请参阅“【管理存储库的 GitHub Actions 设置】”。  
###### 快速入门 简介  
GitHub Pages 是通过 托管和发布的公共网页。  
启动和运行的最快方法是使用 Jekyll 主题选择器加载预置主题。  
然后，您可以修改 GitHub Pages 的内容和样式。  
本指南将引导你在 username.github.io 创建用户站点。  
###### 快速入门 创建网站  
1 在任何页面的右上角，选择 ，然后单击“新建存储库”。  
2 输入 username.github.io 作为存储库名称。  
将 username 替换为你的 GitHub 用户名。  
例如，如果用户名为 octocat，则存储库名称应为 octocat.github.io。  
3 选择仓库可见性。 有关详细信息，请参阅“【关于仓库】”。  
4 选择“使用 README 初始化此存储库”。  
5 单击“创建存储库”。  
6 在存储库名称下，单击 “设置”。  
如果看不到“设置”选项卡，请选择“...”下拉菜单，然后单击“设置”。  
7 在边栏的“代码和自动化”部分中，单击“ Pages”。  
8 在“生成和部署”的“源”下，选择“从分支进行部署”。【【【  
9 在“生成和部署”的“分支”下，使用分支下拉菜单并选择发布源。【【【  
10 （可选）打开存储库的 README.md 文件。  
README.md 文件是你将为站点编写内容的位置。  
您可以编辑文件或暂时保留默认内容。  
11 访问 username.github.io 以查看新网站。  
请注意，对站点的更改在推送到后，最长可能需要 10 分钟才会发布。  
###### 快速入门 更改标题和说明(_config.yml)  
默认情况下，站点的标题为 username.github.io。  
可通过编辑存储库中的 _config.yml 文件来更改标题。【【【  
您还可以为您的网站添加说明。  
1 单击存储库的“代码”选项卡。  
2 在文件列表中，单击 _config.yml 以打开该文件。  
3 单击编辑文件。  
4 _config.yml 文件已包含指定站点主题的行。  
添加一个新行，其中 title: 后跟所需的标题。  
添加一个新行，其中 description: 后跟所需的描述。  
例如：  
```yml  
theme: jekyll-theme-minimal #已包含指定站点主题  
title: Octocat's homepage #所需的标题  
description: Bookmark this to keep an eye on my project updates! #所需的描述  
```  
5 编辑完文件后，单击“提交更改”。  
###### 快速入门 后续步骤  
若要详细了解如何向网站添加其他页面，请参阅“【使用 Jekyll 向 GitHub Pages 站点添加内容】”。  
若要详细了解如何使用 Jekyll 设置 GitHub Pages 站点，请参阅“【关于 GitHub 页面和 Jekyll】”。  
###### 入门 关于 GitHub Pages 关于GitHubPages  
GitHub Pages 是一项静态站点托管服务，  
它直接从上的仓库获取 HTML、CSS 和 JavaScript 文件，  
（可选）通过构建过程运行文件，然后发布网站。  
可以在【GitHub Pages 示例集合】中看到 GitHub Pages 站点的示例。  
  
你可以在 GitHub 的 github.io 域或自己的自定义域上托管站点。  
有关详细信息，请参阅“【配置 GitHub Pages 站点的自定义域】”。  
  
你可以创建在 Internet 上公开可用的 GitHub Pages 站点。  
使用 GitHub Enterprise Cloud 的组织还可以通过管理对站点的访问控制来私下发布站点。  
有关详细信息，请参阅【更改 GitHub Pages 站点的可见性】（见 GitHub Enterprise Cloud 文档）。  
  
若要开始操作，请参阅【创建 GitHub Pages 站点】。  
  
组织所有者可以禁止从组织中的存储库发布 GitHub Pages 站点。  
有关详细信息，请参阅“【管理组织的 GitHub Pages 站点发布】”。  
###### 入门 关于 GitHub Pages GitHubPages站点的类型  
有三种类型的 GitHub Pages 站点：项目、用户和组织。  
项目站点连接到 上托管的特定项目，例如 JavaScript 库或配方集合。  
用户和组织网站已连接到 GitHub.com 上的特定帐户。  
  
若要发布用户站点，必须创建名为 <username>.github.io 的个人帐户拥有的存储库。  
若要发布组织站点，必须创建名为 <organization>.github.io 的组织帐户拥有的存储库。  
除非使用的是自定义域，否则用户和组织站点在 http(s)://<username>.github.io 或 http(s)://<organization>.github.io 中可用。  
  
有关自定义域如何影响站点的 URL 的详细信息，请参阅【关于自定义域名和 GitHub 页面】。  
  
您只能为 上的每个帐户创建一个用户或组织站点。  
项目站点（无论是组织还是个人帐户拥有）没有限制。  
###### 入门 关于 GitHub Pages GitHubPages站点的发布来源  
Warning  
GitHub Pages 站点可以在 Internet 上公开，即使该站点的存储库是专用的也是如此（如果计划或组织允许）。  
如果站点的存储库中有敏感数据，你可能想要在发布前删除数据。  
有关详细信息，请参阅“【关于仓库】”。  
  
可以在将更改推送到特定分支时发布站点，也可以编写 GitHub Actions 工作流来发布站点。  
  
如果不需要对站点的生成过程进行任何控制，则建议在将更改推送到特定分支时发布站点。  
可以指定要用作发布源的分支和文件夹。源分支可以是存储库中的任何分支，  
源文件夹可以是源分支上的存储库根目录 (/)，也可以是源分支上的 /docs 文件夹。  
将更改推送到源分支时，源文件夹中的更改将发布到 GitHub Pages 站点。  
  
如果想使用 Jekyll 以外的生成过程，或者不想使用专用分支来保存已编译的静态文件，  
则建议编写 GitHub Actions 工作流来发布站点。GitHub 为常见的发布应用场景提供工作流模板，以帮助编写工作流。  
  
有关详细信息，请参阅“【配置 GitHub Pages 站点的发布源】”。  
###### 入门 关于 GitHub Pages 静态站点生成器  
GitHub Pages 会发布您推送到仓库的任何静态文件。  
您可以创建自己的静态文件或使用静态站点生成器为您构建站点。  
您还可以在本地或其他服务器上自定义自己的构建过程。  
  
如果使用自定义生成过程或 Jekyll 以外的静态站点生成器，可以编写 GitHub Actions 来生成和发布站点。  
为多个静态站点生成器提供工作流模板。  
有关详细信息，请参阅“【配置 GitHub Pages 站点的发布源】”。  
  
如果从源分支发布站点，GitHub Pages 将默认使用 Jekyll 生成站点。  
如果想使用 Jekyll 以外的静态站点生成器，则建议编写 GitHub Actions 来生成和发布站点。  
否则，通过在发布源的根目录中创建一个名为 .nojekyll 的空文件来禁用 Jekyll 生成过程，  
然后按照静态站点生成器的说明在本地生成站点。  
  
GitHub Pages 不支持服务器端语言，例如 PHP、Ruby 或 Python。  
###### 入门 关于 GitHub Pages GitHubPages使用限制  
2016 年 6 月 15 日后创建并使用 github.io 域的 GitHub Pages 站点通过 HTTPS 提供服务。  
如果您在 2016 年 6 月 15 日之前创建站点，您可以为站点的流量启用 HTTPS 支持。  
有关详细信息，请参阅“【使用 HTTPS 保护 GitHub Pages 站点】”。  
禁止使用  
GitHub Pages 并非旨在用于或允许用作免费的 Web 托管服务  
来运行你的在线业务、电子商务站点或主要针对促进商业交易或提供商业软件即服务 (SaaS) 的任何其他网站。  
GitHub Pages 站点不应该用于敏感事务，例如发送密码或信用卡号码。  
学习练习  
允许使用 GitHub Pages 创建现有网站的副本以进行学习练习。  
但除需要遵守 GitHub 服务条款外，必须自行编写代码，  
网站不得收集任何用户数据，并且网站必须提供明确的免责声明，  
表明项目与原始项目无关，且仅用于学习目的。  
使用限制  
GitHub Pages 站点受到以下使用限制的约束：  
GitHub Pages 源仓库的建议限制为 1 GB。有关详细信息，请参阅“【关于 GitHub 上的大文件】”。  
发布的 GitHub Pages 站点不得超过 1 GB。  
如果花费的时间超过 10 分钟，GitHub Pages 部署将超时。  
GitHub Pages 站点的软带宽限制为每月 100 GB。  
GitHub Pages 站点的_软_限制为每小时 10 次生成。如果使用自定义 GitHub Actions 工作流生成和发布站点，则此限制不适用。  
为了为所有 GitHub Pages 站点提供一致的服务质量，可能会实施速率限制。这些速率限制无意干扰 GitHub Pages 的合法使用。  
如果你的请求触发了速率限制，你将收到相应响应，其中包含 HTTP 状态代码 429 以及信息性 HTML 正文。  
  
如果你的站点超出这些使用配额，我们可能无法为你的站点提供服务；  
或者你可能收到来自 GitHub 支持 的礼貌电子邮件，建议降低站点对服务器影响的策略，  
包括将第三方内容分发网络 (CDN) 置于你的站点前，利用其他 GitHub 功能（如发行版）或转用可能更符合需求的其他托管服务。  
###### 入门 关于 GitHub Pages GitHubPages上的MIME类型  
MIME 类型是服务器发送到浏览器的标头，提供有关浏览器所请求文件性质和格式的信息。  
GitHub Pages 支持数千种文件扩展名中 750 多种 MIME 类型。 支持的 MIME 类型列表是从 mime-db 项目生成的。  
  
虽然无法基于每个文件或每个仓库指定自定义 MIME 类型，但您可以添加或修改 MIME 类型以在 GitHub Pages 上使用。 有关详细信息，请参阅 mime-db 贡献指南。  
###### 入门 关于 GitHub Pages 数据收集  
###### 入门 关于 GitHub Pages 延伸阅读  
##### 笔记  
###### 快速入门 更改标题和说明(_config.yml)  



