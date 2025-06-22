---
创建时间: 2024年12月25日08时10分37秒
知识分类: Master-the-Best-Software
笔记作者: Methues
---
# Methues_Master-the-Best-Software_03-Obisidian_08-一目了然：基于 Dataview 插件的项目可视化指南

## Dataview 插件

Dataview 插件的用途主要有三个方面。

**首先，Dataview 插件可以用于创建复杂的数据查询和筛选**。用户可以使用类似于 SQL 的语法，通过在笔记中标记和注释特定的数据字段或属性，然后利用 Dataview 插件进行搜索、过滤和排序。这样能够很方便地查找特定信息、生成特定条件下的数据集合，或者执行一些统计和计算操作。这对于处理大量信息的复杂项目、管理项目清单或进行定量分析非常有用。

**其次，Dataview 插件还可以用于创建和展示笔记内容的动态视图**。用户可以基于数据的不同维度和属性，使用 Dataview 插件生成列表，表格，日历和任务列表，以便以更直观的方式展示笔记中的内容和关系，并加强对整体知识结构的把握。

**最后，Dataview 插件还支持自定义模板和样式**，使用户能够根据自己的需要进行个性化的数据展示和排版。用户可以使用 Markdown 语法结合强大的 Dataview 指令，根据自己的喜好和需求，定义不同的模板和样式。这使得用户能够更好地控制和定制输出内容的格式和布局，使其更符合个人审美和展示要求。

总之，Obsidian 的 Dataview 插件为用户提供了更高级的数据查询、可视化和个性化功能，可以帮助用户更好地组织、分析和展示笔记内容，提升知识管理和信息处理的效率。

**个人目前对 Dataview 的功能定位：从笔记中汇总数据并进行可视化。**（因此，不会对自定义模板和样式相关的设置做深入研究）

具体来说，个人使用 Dataview 的主要目的就两个：一个是在个人主页中将同系列的文件以列表的形式汇总并显示，二是读取项目笔记中的内容形成项目管理表，这两者靠一些简单的操作即可完成。

## 隐式字段说明

文件中的一些已经自动有索引的内容，比如文件的名字，文件的创建时间、修改时间等，我们称之为文件的隐式字段。即使没有专门被设置，他们也是能够被 Dataview 检索到的。

这里我们会用到的一个重要隐式字段是 `file.tasks`，它所指向的对象是文中出现的所有[[Methues_Master-the-Best-Software_03-Obisidian_04-Guide-to-Markdown-Syntax-and-Link-Creation#任务列表|任务列表]]，因此我们只需用一篇“项目笔记”来记录自己要开展的项目，在其中将拆解出的任务目标通过任务列表的形式列出，之后便可通过 Dataview 和 `file.tasks.text` 字段（读取相应文件中所有任务列表对应的文本）做出项目进度汇总表。

## Dataview 基础语法讲解

鉴于上面提到的对 Dataview 的定位，笔者个人并不会在本教程中对 Dataview 语法做过于深入的挖掘，只讲解自己的一点粗浅理解，更详细的语法建议参照 PKMer 上的 Dataview 使用教程：[PKMer_Obsidian 插件：Dataview](https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E7%A4%BE%E5%8C%BA%E6%8F%92%E4%BB%B6/dataview/dataview/)

我们直接放一段用于项目追踪的基础 Dataview 语法，并附上讲解：

![[基于 Dataview 插件的项目可视化指南_Dataview 基础语法讲解.png]]

有项目文件的话，最终呈现出的效果如下：

![[基于 Dataview 插件的项目可视化指南_Dataview 项目追踪效果示例.png]]

## Dataview 基础实践示例

这部分是个人创建每日待办追踪页面和项目管理页面用到的代码，如果想要直接照搬，请结合[[Methues_Master-the-Best-Software_03-Obisidian_07-Workspace-Creation-Process-and-Templates-Sharing|个人工作区创建指南]]中的文件夹设置和笔记模板一同使用。（如果要和 QuickAdd 搭配使用，还要注意在创建指令时，设置好新生成笔记的默认存储位置）

### 用 Dataview 汇总特定文件夹下的文件列表

```dataview
list
from "04 Archives/01 Daily checklist"
```

### 用 Dataview 汇总项目计划并显示项目计划/当前进展

```dataview
table 开始日期, 结束日期, file.tasks.text as 项目计划
from "01 Projects/02 Study item"
```

```dataview
table 开始日期, 结束日期, file.tasks as 项目进度
from "01 Projects/03 Work item"
```

### 用 Dataview 汇总灵感笔记并显示分类

```dataview
TABLE 创建时间, 灵感分类
from "01 Projects/01 Idea box"
```


## 相关文档

所属项目：[[Methues_Master-the-Best-Software_03-Obisidian|实用软件终极指南-03：Obsidian]]

上一篇笔记：[[Methues_Master-the-Best-Software_03-Obisidian_07-Workspace-Creation-Process-and-Templates-Sharing|融会贯通：工作区创建流程与模板分享]]

下一篇笔记：[[Methues_Master-the-Best-Software_03-Obisidian_09-Guide-to-Luhmann-s-Note-Taking-Method|罗缕纪存：卢曼笔记法攻略]]