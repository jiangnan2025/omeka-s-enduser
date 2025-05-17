# Glossary 术语表

以下术语表旨在帮助澄清 Omeka S 中一些不太熟悉的术语。

**Class（类）**：由 Vocabulary 定义的一种资源类型。通常，Vocabulary 期望特定的属性（Properties）与特定的类（Classes）配合使用。例如，`foaf:Person` 不会有 `dcterms:publisher` 属性，但可以预期有 `foaf:familyName` 属性。  
*Omeka Classic 类比*：Item Type（项目类型）。

**File（文件）**：上传到 Omeka S 并直接关联到某个 Item 的数据（参见 Media）。  
*Omeka Classic 类比*：File（文件，但类比较弱）。

**Global Admin（全局管理员）**：控制一切的管理员，通常是创建该安装实例的人。  
*Omeka Classic 类比*：Superuser（超级用户）。

**Installation（安装实例）**：Omeka S 的一个实例。通常由机构的中央 IT 部门负责安装，并可能为他人创建站点。

**Item（项目）**：用于构建 Omeka S 站点的记录。Item 可在安装实例中的任意站点共享，除非明确排除共享。  
*Omeka Classic 类比*：Item（项目）。

**Item Set（项目集合）**：Item 的聚合体。一个 Item 可以属于任意多个 Item Set。  
*Omeka Classic 类比*：Collection（集合）；带有相同标签的 Items。

**Media（媒体）**：Item 的额外表现或描述，超出词汇表中元数据的内容。通常指文件（任意类型，包括文本或 HTML 片段），也可以指外部数据源，如 YouTube 视频、Slideshare 幻灯片、Dspace 流等。  
*Omeka Classic 类比*：File（文件，但类比较弱）。

**Module（模块）**：Omeka S 安装的附加组件，用于扩展功能。模块可增加后台的数据录入选项和交互，并为站点添加新功能。  
*Omeka Classic 类比*：Plugin（插件）。

**Property（属性）**：一种定义过的元数据类型，用于描述资源。最常见的是 `dcterms:title`，表示项目的人类可读标题。属性的值（Values）可以是用于人类或其他智能体阅读的文本（“Literal”），也可以是资源（此处指 Omeka S 内部资源）或外部 URI（例如指向 DBpedia 资源页的 URI）。  
*Omeka Classic 类比*：Element（元素）。

**Resource Template（资源模板）**：一组预定义的属性，且可选一个类，用于指导 Item 的创建和属性的解释。典型用法是为如 `foaf:Person` 创建模板，使得使用该模板的 Item 显示预期或期望的 `foaf:` 属性输入，并将该 Item 的类设为 `foaf:Person`。  
*Omeka Classic 类比*：Item Type（项目类型，但类比较弱）。参见 Class。

**Site Admin（站点管理员）**：Omeka S 安装中单个站点的管理员。  
*Omeka Classic 类比*：Superuser role（超级用户角色）。

**Value（值）**：填充资源-属性-值三元组的实际数据。如果属性是 `dcterms:title`，合理的值可能是 “Heart of Darkness”。Literal 值可能还带有该值所用语言的信息。值也可以是资源或指向外部数据的 URI（优选返回 RDF 数据的 URI，但这点并不强制）。  
*Omeka Classic 类比*：Element Text（元素文本）。

**Vocabulary（词汇表）**：用于描述资源的已发布 RDF 元数据类和属性的集合。它们存在于 Omeka 外部，可以（有限制地）导入 Omeka S 以供整个安装实例使用。最常用的词汇表是 Dublin Core Terms (`dcterms:`)。  
*Omeka Classic 类比*：Element Set（元素集）。
