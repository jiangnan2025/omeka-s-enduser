# 资源模板（Resource Templates）

**资源模板**是一组预定义的属性集合，可选地包含一个类（Class），用于指导项目的创建及属性的解释。

资源模板可通过管理后台进行管理，入口在左侧导航栏的 **资源（Resources）** 区域中。

![资源模板标签页的基本视图，展示了列标题和一个模板](contentfiles/templates_browse.png)

表格左上方显示项目分页数，包含前进和后退箭头。当前页码是可编辑的字段——输入任意有效页码并按回车键即可跳转至该页。

右上角有两个下拉菜单可用于排序。你可以按以下方式排序：**标签（label）**、**类（class）**、**所有者（owner）** 或被分配到模板的 **项目数（items）**，排序可选升序或降序。

每一行的图标可以用于：**编辑**（铅笔图标）、**删除**（垃圾桶图标）、或**查看详情**（省略号图标）。点击模板对应的项目数量可跳转至该模板下的所有项目列表。

[这个演示视频](https://vimeo.com/290924872){target=_blank} 简要介绍了资源模板的创建与应用：

<div style="padding:62.5% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/290924872?h=c6359076cd" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>
<p><a href="https://vimeo.com/290924872">Omeka S 资源模板</a> 来自 <a href="https://vimeo.com/omeka">Omeka</a> 在 <a href="https://vimeo.com">Vimeo</a>.</p>

## Resource template permissions 资源模板权限

当用户创建一个资源模板时，他们成为该模板的“所有者”。大多数用户等级都有创建模板的权限，并且可以删除自己创建的模板。只有更高级别的用户可以删除他人拥有的模板。

| Category | Permission | Global Admin | Supervisor | Editor | Reviewer | Author | Researcher |
|-----|-----|---|---|---|---|---|---|
| Resource templates | Add | Yes | Yes | Yes | No | Yes | No |
| | Edit/Delete  | All | All | All | No | Their own | No |

注意：当你更改用户的角色（例如从作者改为研究员）时，他们仍然拥有原先有权限时所创建的模板。删除用户将导致其模板“孤立”，显示为“[无所有者]”，且不能重新分配给其他用户。

## View resource templates 查看资源模板

点击资源模板的标题可进入该模板的属性及选项表格视图。

![Template view for the "Postcard" template with properties for title, description, creator, transcript of, and recipient](contentfiles/templates_view.png)

每个属性显示为表格中的一行，包含以下列：

- 原始标签，附带省略号按钮以查看该属性的词汇表、术语、原始注释及当前使用该属性的项目数量
- 数据类型
- 替代标签
- 替代注释
- 是否为必填项
- 属性值是否为私有
- 是否设置默认语言（输入时可覆盖）

可使用右上角按钮导出或编辑模板。

## 基础资源模板（Base Resource）

所有 Omeka S 安装默认包含一个“基础资源”模板，对应 [美国数字公共图书馆（DPLA）](https://dp.la/){target=_blank} 所需的元数据字段。该模板在资源模板列表中显示为“Base Resource”，无所有者。

![资源模板列表中显示的基础资源模板](contentfiles/templates_base1.png)

基础资源模板包含以下 Dublin Core 字段：标题、权利、类型、创建者、日期、描述、格式、语言、空间覆盖（地点）、出版者、替代标题、贡献者、范围、标识符、关系、被替代、替代、权利持有者、主题、时间覆盖。

## Add a resource template 添加资源模板

在管理后台的 **资源模板（Resource templates）** 标签页中，点击“添加新资源模板”按钮。

新模板页面将显示标签、建议的类，以及预加载的属性 **标题**（`dcterms:title`）与 **描述**（`dcterms:description`）。

![添加资源模板页面，预加载了标题、类、Title 与 Description 属性](contentfiles/templates_add.png)

1. 在“标签”字段中输入模板的名称。该标签将在创建项目时的下拉菜单中显示，请确保清晰易懂。
2. 可选择与模板关联的类。
3. 从页面右侧的词汇表中添加属性。可使用文本框筛选，或点击词汇表名称右侧的箭头展开选择。
4. 若需要，可修改属性（见下文“属性选项”）。

在离开页面前，请务必点击“保存”按钮。

使用该模板创建项目的用户仍可添加其他属性，且只需填写你设定为“必填”的字段。

### Property options 属性选项

你可以为每个属性设置显示标签、注释、是否必填、默认数据类型等。

点击属性行中的编辑（铅笔）图标将在右侧打开属性编辑抽屉。

![Title 属性的属性选项抽屉，尚未做出任何更改](contentfiles/template_configdrawer.png)

在离开抽屉或编辑其他属性前，必须点击抽屉底部的“设置更改”按钮，否则修改将不会保存。

![靠近属性编辑抽屉底部，红色箭头指向“设置更改”按钮](contentfiles/templates_setchanges.png)

#### Label  标签

在“替代标签”字段中输入新的标签，将应用于后台项目编辑页面及公开展示页面。

#### Comment 注释

在“替代注释”字段中添加内部说明文字。用户在使用模板创建项目时，该文本显示在属性名称下方。注释不会公开展示，仅用于编辑页面，可用于提供填写指导。

#### Other options  其他选项

- 勾选“用作资源标题”可使用该属性代替默认的 `dcterms:title`，在浏览页面中显示为“标题”。
- 勾选“用作资源描述”可使用该属性代替默认的 `dcterms:description`，在浏览页面中显示为“描述”。
- 勾选“必填”则该属性在使用模板创建项目时必须填写。
- 勾选“私有”可将该属性值设置为默认私有，仅项目所有者、全局管理员、站点管理员及编辑者可见。**注意**：用户可按项目单独更改属性的公开/私有状态，该选项仅设定默认状态。

##### Data types 数据类型

Omeka S 默认支持三种数据类型：

- 文本（Text）：纯文本输入
- URI：带标签的链接
- 资源（Resource）：可链接至已有的项目、媒体或集合

还可以通过模块添加额外选项：

- [Numeric Data Types](../modules/numericdatatypes.md)：限制为四种数值类型
- [Custom Vocab](../modules/customvocab.md) 与 [Value Suggest](../modules/valuesuggest.md)：提供受控词汇建议，但用户仍可自由输入文本

![项目编辑页面，dcterms:date 属性限制为时间戳和时间区间数据类型](contentfiles/templates_datatype-date.png)

你可以为一个属性选择多个数据类型，例如允许“文本”或“资源”作为输入，但不允许“URI”。所有选项会显示在数据类型字段中，并带有“X”按钮以删除。

若选择了受控词汇建议的数据类型，则除非同时启用 URI，否则不能输入 URI。若希望使用外部词汇作为备用选项，建议添加 URI 类型。数据类型在下拉菜单中按照预设顺序显示，无法手动排序。

![项目编辑页面，dcterms:subject 属性显示已有文本输入，并可通过 Value Suggest 模块添加受控词汇](contentfiles/templates_datatype-valuesuggest.png)

如图所示，可通过 Value Suggest 模块使用受控词汇添加主题，也可使用 Omeka 中已有值。

编辑模板不会改变已有项目的数据，即使数据类型设置变更，已有值仍保留。

## 编辑资源模板

你可以点击模板列表中的编辑图标，或在模板详情页右上角点击“编辑”来修改模板。

若不希望保存更改，可点击右上角的“取消”按钮（在“删除”与“保存”之间）。

![“Person”模板编辑视图，包含 8 个属性](contentfiles/templates_edit.png)

## 共享资源模板

你可以通过导入导出功能在不同的 Omeka S 安装之间共享资源模板。

### 导出资源模板

1. 打开主导航中的“资源模板”菜单
2. 点击要导出的模板标签
3. 在模板详情页右上角点击“导出”按钮

![红色箭头指向标签为“Textual Resource”的资源模板导出按钮](contentfiles/templates_export.png)

模板将以 JSON 文件格式下载至默认下载位置，文件名为模板的标签名。

### 导入资源模板

!!! note
	如果导入的模板使用了 [Custom Vocab](../modules/customvocab.md)，必须先在目标站点中手动创建该自定义词汇表。若模板使用了 [Value Suggest](../modules/valuesuggest.md)，也应提前安装并启用。

导入步骤如下：

- 打开主导航中的 **资源模板** 标签
- 点击右上角的“导入”按钮

![红色箭头指向 Omeka S 管理站点资源模板浏览页的导入按钮](contentfiles/templates_import1.png)

- 在导入资源模板页面点击“Choose File”按钮
  - 浏览器将打开文件选择窗口，选择你要导入的 JSON 文件
- 点击“Review import”按钮
  - 审查页面允许你确认属性及其选项是否正确
  - 若模板使用了 [Value Suggest](../modules/valuesuggest.md) 或 [Custom Vocab](../modules/customvocab.md)，将在“数据类型”列中指示原始来源，并提供下拉菜单选择替代类型。若未安装相关模块，仅显示默认数据类型。

![导入模板审查页面，所有元素为绿色高亮显示](contentfiles/templates_import2.png)
