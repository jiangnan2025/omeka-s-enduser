# Omeka S 用户手册

[Omeka S](https://omeka.org/s/) 是一个面向高校、美术馆、图书馆、档案馆和博物馆的网页发布系统。它创建了一个本地网络，由多个独立策划的展览组成，共享一个协作构建的条目池及其元数据。你可以观看我们的 [Omeka S 快速演示视频](https://vimeo.com/241702586)。

Omeka S 与 [Omeka Classic](http://www.omeka.org) 同时开发，二者同属 Omeka 网页发布平台家族。

本仓库包含 [Omeka S 用户手册](http://omeka.org/s/docs/user-manual/) 的内容。

### 格式规范

**章节标题** 应从 H2（`##`）开始，向下至 H4。请在文档结构合理的位置创建章节，它们将显示在文档的左侧导航栏中。（参见 [页面管理](http://omeka.org/s/docs/user-manual/sites/site_pages/) 示例。）使用 “句式大小写” 编写章节标题，而非 “驼峰式命名”。

**链接** 应相对于当前文件进行书写。例如，链接至某文件夹中的页面时可写为 `../modules/csvimport.md`，或链接至某页面中某段落时写为 `../admin/users.md#manage-users`。请勿忘记 `.md` 文件扩展名。

外部网站链接需使用完整 URL，并在链接语法后添加 `{target=_blank}`，例如：[创建一个新 issue](https://github.com/omeka/omeka-s-enduser/issues){target=_blank}。

**图像** 应放置于与页面对应的 `files` 文件夹中（例如，“内容”页面的图像应位于 `contentfiles` 文件夹）。图像命名应清晰，以页面标识符开头，使用下划线分隔图像用途，例如：`items_addItem.png`。

图像中不应包含文中未说明的信息（或未在图像的 alt 文本和 title 中提供）。视障用户不应因此错失内容。将图像视为一种快捷方式，而不是唯一理解操作方式的路径。

所有图像都应包含 alt 文本。如有需要，也可添加 title，当用户将鼠标悬停于图像上时会显示。插入 Markdown 图像的语法如下：


用户手册中图像的最大显示宽度约为 1300px（实际为 1296px）。整个 Omeka 界面的截图（公共或后台）应为大尺寸图像。图像可保存为更大尺寸（最多 2000px 宽），以便读者在新标签页中打开查看细节。

对于界面的一部分截图，如左侧导航栏或右侧抽屉，应以全尺寸显示，以确保可读性。目前，在 1920x1080 屏幕上，Omeka S 左侧导航栏宽度约为 320px，右侧抽屉宽度约为 450px。

**文本格式规范如下**：

按钮使用引号，如 “Save” 按钮。

界面元素（如页面标题、标签页、链接、下拉菜单和复选框）使用加粗格式 **bold**。

网址、文件路径、代码片段和元数据字段使用 `代码格式`。

图标请按其工具提示进行描述，例如 “edit（铅笔图标）”、“delete（垃圾桶图标）”、“details（三点图标）”。这样可以帮助使用屏幕阅读器的用户理解内容。

请使用 [术语表](https://omeka.org/s/docs/user-manual/glossary/) 中的术语来描述 Omeka S 界面中的元素。

Omeka S 相关术语包括：

- Left-hand navigation：左侧导航栏，包含资源、管理等选项
- Main work area：主工作区域，位于左侧导航右侧的窗口中央
- Drawer：从右侧打开的菜单
- Admin dashboard：管理员仪表盘
- Modules：模块
- Properties：属性
- Item sets：条目集
- Classes：类


## 权利声明

本手册文档使用 [CC-BY-NC](https://creativecommons.org/licenses/by-nc/4.0/) 许可证发布。
