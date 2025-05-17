# Administrative Dashboard

管理仪表盘负责管理所有 Omeka S 站点共享的内容以及 Omeka S 安装的核心功能。

这个 [演示视频](https://vimeo.com/455708039){target=_blank} 介绍了仪表盘的主要功能以及如何导航你的 Omeka S 安装：

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/455708039?h=438143f0d3" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>
<p><a href="https://vimeo.com/455708039">导航 Omeka S</a>，来自 <a href="https://vimeo.com/omeka">Omeka</a>，发布于 <a href="https://vimeo.com">Vimeo</a>。</p>

## Admin main page

当用户登录时，首先看到的是管理仪表盘页面。

!!! note
	根据用户角色，左侧导航栏中的选项可能不完全相同。详情请参见[下文](#left-hand-navigation)。

![管理仪表盘全览](files/admindashfullview.png)

除所有页面都存在的左侧导航栏（见下文）外，管理仪表盘还向用户展示两个模块：“**管理资源**”和“**管理站点**”。

“**管理资源**”模块显示以下资源及其总数：[条目](content/items.md)、[条目集](content/item-sets.md)、[词汇表](content/vocabularies.md)和[资源模板](content/resource-template.md)。点击资源标签将进入浏览页面；点击标签右侧的加号按钮将进入该资源类型的新增页面。

“**管理站点**”模块列出了安装中的[站点](sites/index.md)。点击站点名称将进入该站点的管理标签页；点击右侧的小箭头图标将打开该站点的公共视图（新窗口或标签页）。

## Left-hand navigation
（左侧导航栏）

以下内容显示在管理仪表盘左侧及所有管理页面的左侧。

![管理仪表盘左侧导航视图，该导航在整个管理界面均一致显示，包含下述选项](files/leftnav.png)

屏幕左上角有一个显示安装标题的链接，点击可随时返回管理仪表盘。

安装标题正下方显示“已登录为 [用户]”，其中 [用户] 是当前登录人的显示名。用户名旁有一个齿轮图标，点击可[进入用户设置页面](admin/users.md#user-settings)。

用户名附近（根据窗口宽度显示在下方或右侧）是**注销**按钮。

用户信息下方是一个搜索框，包含高级搜索选项（省略号）和搜索按钮（放大镜）。可用它搜索安装中的所有条目。

高级搜索选项（省略号）允许按资源类型细化搜索，通过点击所需资源类型旁的单选按钮，将搜索限定为**条目**、**条目集**或**媒体**。

![高级搜索选项](files/search.png)

仪表盘左侧导航按功能和用户权限划分为几个部分：

- [站点](sites/index.md)：列出并访问所有 Omeka S 安装的站点。（计算机图标）
- 资源：内容创建与元数据管理。
    - [条目](content/items.md)：管理安装中的单个资源。（盒子图标）
    - [条目集](content/item-sets.md)：管理条目集合。（多个盒子图标）
    - [词汇表](content/vocabularies.md)：管理安装的元数据标准。（闭合书本图标）
    - [资源模板](content/resource-template.md)：管理创建条目时预定义的属性集合。（方框中的铅笔图标）
- 管理：安装级别管理（部分标签可能对不同用户不可见）。
    - [用户](admin/users.md)：管理整个平台及单个站点的用户。（人物轮廓图标）
    - [模块](modules/index.md)：为站点添加功能。（方框中的加号图标）
    - [任务](admin/jobs.md)：显示当前运行的用户激活任务。注意：仅显示运行中的任务。（三条杠图标）
    - [设置](admin/settings.md)：管理所有站点、管理仪表盘和站点仪表盘的全局设置。（齿轮图标）

如安装了模块，它们会出现在左侧导航的管理部分，位于设置下方。

权限有限的用户将只能看到部分导航选项。

## System information 系统信息

在管理界面每个页面的右下角显示当前 Omeka S 版本及一些实用链接。点击“系统信息”链接可查看包含安装详细信息的完整页面。

![系统信息页面示例](files/systeminfo.png)

在此页面可核实 Omeka 使用的依赖版本，如 PHP、ImageMagick 和 MySQL。如果某模块要求服务器提供某些 PHP 功能，也可在此确认。还可以确认安装是否识别已尝试安装的模块。

注意，PHP 部分会显示“文件上传限制”，此数值反映在媒体上传和资源上传界面。同时，Omeka S 会显示可用的服务器剩余空间。

请求技术支持时，可能需要提供此页面的信息，如在 [论坛](https://forum.omeka.org/){target=_blank}发帖或在 GitHub 提交问题时。

页面底部的两个按钮可帮助验证 PHP 和 ImageMagick 是否正常工作。安装完成后立即操作，避免后续批量导入条目或执行其他 PHP 相关任务时出现问题。

![PHP CLI 版本按钮和 ImageMagick 版本按钮的示例结果](files/systeminfo_buttons.png)
