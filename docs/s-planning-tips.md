# 规划技巧

## 基础知识

全新安装的 Omeka S 自带多种预设页面类型，随时可供分享：

- 添加新站点时，可以立即选择已安装的主题，也可以使用“默认”主题。
- 你创建的第一个 S 站点的导航栏中，会预置一个“浏览”页面，用于浏览条目。你也可以快速添加预装的“欢迎”页面，展示一些文本格式样式。
- 添加第一个条目后，你可以查看“[条目查看页面](content/items.md#public-views-for-items)”。可以通过“主题”标签下的“配置资源页面”按钮进行定制。查看附加媒体的页面布局是单独设计的。
- 开始将条目分类到条目集后，你可以为导航栏添加类似的“浏览条目集”页面，并定制相应的“条目集查看”页面。
- 根据所选主题，这些资源页面可能自带预配置的区块。大多数主题默认显示：
  - 条目页：媒体的全尺寸嵌入，按模式排序的条目元数据，包含该条目的条目集和站点页面列表，所有附加媒体的缩略图列表；
  - 媒体页：媒体的全尺寸展示，媒体元数据；
  - 条目集页：条目集元数据，条目集内容的网格或列表浏览。
- 浏览条目和条目集的页面均链接到[高级搜索表单](search.md#public-views)，顶部搜索栏也如此。

在 Omeka S 中，你通过逐页构建[站点](sites/index.md)，使用已添加的资源。建议你在大量添加资源前先规划站点，建议先尝试一些样本条目和条目集，熟悉 Omeka 的资源处理方式。

以下是一些问题和思路，帮助你规划 Omeka S 站点。

## 站点受众和目标

**这个站点的主要受众是谁？** 明确受众有助于塑造站点；“对历史建筑感兴趣的人”比“公众”更具体且有效。是否有次要受众？你希望特定受众访问站点时完成什么目标？

**你的站点目标是什么？** 你希望特定受众访问站点时完成什么？你希望访客从站点获得什么？你想重点展示哪些内容？

## 资源

**你打算如何使用本网站的条目？**  
[条目](content/items.md)是 Omeka S 的构建基石。你想创建并使用哪些[资源模板](content/resource-template.md)来完整描述条目？任何条目都会有公开展示页面，确保条目元数据能独立表达信息。

**你打算如何使用条目集？**  
你可以用[条目集](content/item-sets.md)将条目分组，包含在[站点](sites/index.md)中，帮助引导访客浏览。对某些站点来说，条目集本身也是丰富资源。

你如何分组条目？条目集将使用哪些元数据字段？条目集之间或与条目之间是否存在关联？

**你希望数据如何表现？**  
你会想在站点中统一描述哪些属性？是否想为某些属性显示不同标签，例如图书的“作者”替代“创作者”？使用[资源模板](content/resource-template.md)可更改属性标签。

在 Omeka S 中，条目和条目集可以用其他资源（条目、条目集、媒体）作为属性；例如，你可以创建“威廉·莎士比亚”的条目，并将该条目作为《哈姆雷特》的“创作者”属性。你的资源如何利用这项功能？

是否想为某些条目使用一组术语（受控词表）？你可以使用[Custom Vocab](modules/customvocab.md)。或者想使用美国国会图书馆或盖蒂的词表？可用[Value Suggest](modules/valuesuggest.md)。

## 构建站点

使用 Omeka S，你可以从零开始搭建站点，或快速使用内置页面。也可以用多个站点实现目标。

**你想包含哪些页面？** 页面内容是什么？如何排列？可以先绘制菜单草图或线框图，参考其他组织或个人的示例站点，作为建设指南。

页面由可重排的[区块](sites/site_pages.md#page-blocks)组成，区块可包含文本、图片等多种内容。你希望页面包含什么内容？访客如何访问和理解你的馆藏？

**你想如何与访客互动？** 是否想从访客处[收集](modules/collecting.md)资源？允许他们在社交媒体上[分享](modules/sharing.md)内容？

你是否允许[用户注册账户](admin/users.md)，让他们添加条目、元数据或展览？

## 推荐模块
Omeka 团队及开源社区开发了数百个模块，扩展 Omeka S 核心功能。为方便管理员针对特定工作类型安装配置，以下是一些推荐模块集：

### 发布数字馆藏

- 描述资源
  - [Extract Metadata](https://omeka.org/s/modules/ExtractMetadata/)：提取文件内嵌元数据，如照片 EXIF。
  - [Extract Text](https://omeka.org/s/modules/ExtractText/)：从文件（PDF、Word 文档、图片）提取文本，实现可搜索。
  - [Custom Vocab](https://omeka.org/s/modules/CustomVocab/)：用自定义词汇描述资源。
  - [Value Suggest](https://omeka.org/s/modules/ValueSuggest/)：使用受控词表服务的自动建议值描述资源。
  - [Numeric Data Types](https://omeka.org/s/modules/NumericDataTypes/)：添加数字和日期类型。
- 导入资源
  - [CSV Import](https://omeka.org/s/modules/CSVImport/)：从 CSV、TSV 或 ODS 文件导入更新内容（条目、条目集、媒体、用户）。
  - [File Sideload](https://omeka.org/s/modules/FileSideload/)：将服务器上的文件添加到条目。
  - 其它导入器支持 DSpace、Fedora、Dataverse、Invenio、Zenodo、Zotero 及 Omeka Classic 或 S 集合。
- 提升可发现性
  - [Mapping](https://omeka.org/s/modules/Mapping/)：将条目地理定位到一个或多个地图位置。
  - [Sharing](https://omeka.org/s/modules/Sharing/)：提供 OpenGraph 元数据，令 Omeka S 链接在社交媒体展示美观。
  - [Resource Meta](https://omeka.org/s/modules/ResourceMeta/)：使资源元数据机器可读。
  - [Persistent Identifiers](https://omeka.org/s/modules/PersistentIdentifiers/)：创建/导入/分配 DOI 或 ARK。
  - [IIIF Presentation](https://omeka.org/s/modules/IiifPresentation/)：通过 IIIF Presentation API 提供资源。
- 展示资源
  - [Faceted Browse](https://omeka.org/s/modules/FacetedBrowse/)：为馆藏添加细粒度浏览工具。
  - [Metadata Browse](https://omeka.org/s/modules/MetadataBrowse/)：浏览共享相同元数据的资源。
  - [URI Dereferencer](https://omeka.org/s/modules/UriDereferencer/)：展示外部 URI 的权威控制元数据。

此外，你可能对以下特定功能感兴趣。

### 复杂数据建模

- 描述资源
  - [Data Cleaning](https://omeka.org/s/modules/DataCleaning/)：低级别资源元数据审核与清理。
  - [Inverse Properties](https://omeka.org/s/modules/InverseProperties/)：定义属性间的互逆关系。
- 私有数据
  - [Hide Properties](https://omeka.org/s/modules/HideProperties/)：在管理端或公开端隐藏属性。
  - [Redact Values](https://omeka.org/s/modules/RedactValues/)：编辑值以屏蔽公开显示。
  - [View Private Resources](https://omeka.org/s/modules/ViewPrivateResources/)：允许低权限用户查看私有资源。
- 数据展示
  - [Data Visualization](https://omeka.org/s/modules/Datavis/)：可视化馆藏及条目信息。
  - [Mapping](https://omeka.org/s/modules/Mapping/)：地理定位条目并配合时间轴按时间展示。

### 社区协作

- 公开贡献
  - [Collecting](https://omeka.org/s/modules/Collecting/)：为站点添加采集表单。支持 Mapping、Numeric Data Types、Custom Vocab、Value Suggest。
- 转录
  - [Scripto](https://omeka.org/s/modules/Scripto/)：转录及翻译条目。
  - [DataScribe](https://omeka.org/s/modules/Datascribe/)：允许社区访客转录结构化数据。

### 地理空间与时间

- 描述资源
  - [Mapping](https://omeka.org/s/modules/Mapping/)：为条目和站点添加位置信息。
  - [Numeric Data Types](https://omeka.org/s/modules/NumericDataTypes/)：添加数字和日期类型。可配合 Mapping 创建时间轴。

### 与其他数字系统协作

- 机构存储库
  - [Data Repository Connector](https://omeka.org/s/modules/DataRepositoryConnector/)：支持 Zenodo、Dataverse、Invenio、CKAN
  - [DSpace Connector](https://omeka.org/s/modules/DspaceConnector/)
  - [Fedora Connector](https://omeka.org/s/modules/FedoraConnector/)
- 其他 Omeka 安装
  - [Omeka Classic Importer](https://omeka.org/s/modules/Omeka2Importer/)
  - [Omeka S Item Importer](https://omeka.org/s/modules/Osii/)
- Zotero
  - [Zotero Citation](https://omeka.org/s/modules/ZoteroCitations/)：使用 Zotero 生成引用和参考文献。
  - [Zotero Importer](https://omeka.org/s/modules/ZoteroImport)：从 Zotero 用户和组库导入条目和文件。
