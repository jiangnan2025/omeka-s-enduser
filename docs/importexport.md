# 导入与导出

Omeka S 网站有多种导入和导出方法。第三方模块可能提供更多功能；这里仅记录由 Omeka 团队支持的方法。

## 连接到另一个 Omeka 站点

### 从 S 导入到 S

您可以使用 [Omeka S Item Importer 模块](modules/ositemimporter.md) 将项目和项目集从一个 Omeka S 安装导入到另一个。无法导入站点及其页面。建议在导入前将目标站点尽可能设置得与源站点相近，包括安装并激活所有相同的模块，以及安装使用的词汇表。

### 导入或导出资源模板

[您可以通过导出和导入在 Omeka S 安装之间共享资源模板。](https://omeka.org/s/docs/user-manual/content/resource-template/#share-resource-templates)

### 导入或导出自定义词汇表

[您可以通过导出和导入在 Omeka S 安装之间共享自定义词汇表。](https://omeka.org/s/docs/user-manual/modules/customvocab/#manage-custom-vocabs)

## 连接到非 Omeka 平台

Omeka S 拥有用于从以下平台导入资源的模块：

- [Zotero](modules/zoteroimport.md)
- [Zenodo](modules/datarepositoryconnector.md)
- [Fedora](modules/fedoraconnector.md)
- [DSpace](modules/dspaceconnector.md)
- [CKAN](modules/datarepositoryconnector.md)
- [Dataverse](modules/datarepositoryconnector.md)
- [Invenio](modules/datarepositoryconnector.md)。

### 从电子表格导入

Omeka S 可接受任何电子表格（表格）格式的数据，无论是 CSV、Excel 文件还是 ODS。使用 [CSV Import 模块](modules/csvimport.md) 从电子表格向 Omeka S 网站添加项目、项目集、多媒体和用户。这包括从许多不同数据库和平台导出的数据。

首先，查看是否存在针对您要导出的平台的连接器或导入模块。Omeka S 支持 Zotero、Zenodo、Fedora、DSpace、CKAN、Dataverse 和 Invenio 的模块。如果没有特定模块，请将源平台的数据导出为电子表格。导入 Omeka S 之前，可能需要对数据进行一些修改或清理。

### 导出到电子表格

可以通过使用 Python 脚本查询安装的 API 来导出 Omeka S 资源。您可以用它将 Omeka S 的材料复制到其他平台，或作为工作备份。

[Omeka-s-csv.py](https://github.com/omeka/omeka-s-csv.py){target=_blank} 是一个将 Omeka S 安装中的数据导出为 CSV 格式的 Python 脚本。

导出后的电子表格将按字母顺序有元数据术语的列标题：`dcterms:description`、`dcterms:title` 等。

还会有一部分以 `o:` 开头的列，包括内部 Omeka S ID (`o:id`)、项目附加多媒体的内部 ID (`o:media`)、隐私设置 (`o:is_public`，值为 "TRUE" 或 "FALSE")、创建和修改日期、所有者、站点及其他资源数据。最后是包含安装生成的媒体缩略图 URL 的 `thumbnail` 列。

此脚本无法导出站点或页面信息，也不会导出资源模板、词汇表或存储于模块中的其他数据（例如资源模板上的反属性设置）。

#### 需求

omeka-s-csv.py 支持 Python 2 和 3，无需额外或外部依赖。

Linux 用户通常已安装 Python，相关软件包可从发行版获得。Windows 和 Mac 用户有多种安装 Python 的选择，包括从 [Python 官网](https://www.python.org/downloads/) 下载安装程序。

#### 导出

在系统中存放 `omeka-s-csv.py` 文件的文件夹内打开终端，运行脚本：

```
python3 omeka-s-csv.py
```
（也可以根据系统使用 `./omeka-s-csv.py`、`python omeka-s-csv.py` 或 `python2 omeka-s-csv.py`。）

脚本会提示输入要导出的 Omeka S API 端点。这是指向目标 Omeka S 安装的 URL，应以 `http://` 或 `https://` 开头，以 `/api` 结尾。

接着，会提示输入 API 密钥。导出非公开数据需要密钥，但仅导出公开数据时可以留空，按回车即可。

最后，会提示输入“分隔符”，用于在单个 CSV 单元格中分隔多条数据。请确保所选字符不出现在实际数据中。默认是“竖线”字符（`|`），通常是安全选择。按回车使用默认，否则输入您希望使用的分隔符。

脚本将运行，并显示进度。导出结果文件位于与 `omeka-s-csv.py` 文件相同的文件夹内：`items.csv`、`item_sets.csv` 和 `media.csv`。

### 使用 API 访问数据

您也可以直接使用自己 S 站点的 API 按需抓取数据，而非一次性导出电子表格。注意，API 支持[请求不同格式](https://omeka.org/s/docs/developer/api/rest_api/#responses){target=_blank}，包括 `jsonld` 和 `rdfxml`。[更多 API 信息，请参阅开发者文档部分。](https://omeka.org/s/docs/developer/api/){target=_blank}
