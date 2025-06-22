---
创建时间: 2024年12月17日11时46分00秒
知识分类: Master-the-Best-Software
笔记作者: Methues
---
# Methues_Master-the-Best-Software_03-Obisidian_04-积基树本：Markdown 语法与链接创建指南

## Markdown 基础语法

*Mardown 语法是使用 Obsidian 最重要的工具，没有之一，它指的是通过少量符号搭配特定格式进行纯文本写作，之后兼容 Markdown 语法的软件便能根据纯文本内容自动完成排版。个人看来，它的主要优势在于：*

- **辅助学习**：*在写作时进行同步排版能促使写作者自动梳理逻辑，本身便能辅助学习*
- **方便迁移**：*排版格式蕴含在纯文本中，具有极强的通用性，在不同软件或平台中迁移也完全不会出现排版错乱*
- **便捷高效**：*由于在写作时已经划分好了信息结构，无需再花时间排版，目录可自动生成，信息定位也十分高效

*Markdown 语法的基础部分并不复杂，只需掌握分级标题，加粗，倾斜，列表，转义符以及代码块这几个基础的知识点即可开始实践，当然，进一步的学习对丰富我们的表达是极有帮助的，极力推荐学有余力的读者自行学习后续附带的完整教程！*

### 分级标题

要创建标题，请在单词或短语前面添加井号 (`#`) ，并用空格分隔。`#` 的数量代表了标题的级别。例如：

- `# 标题1`
- `## 标题2` 
- …………
- `###### 标题6`

还可以在文本下方添加任意数量的 == 号来标识一级标题，或者 -- 号来标识二级标题，例如：

```
标题1 
==
```

### 加粗&倾斜

加粗：`**要加粗的内容**`

斜体：`*要倾斜的内容*`

### 列表

**无序列表**：短横杠 `/` +空格后添加列表内容，每一行均采用此格式。

示例如下：

- 无序列表第一行
- 无序列表第二行
- 无序列表第三行
- …………

**有序列表**：数字序号+ `.` +空格后添加列表内容，每一行均采用此格式

示例如下：

1. 有序列表第一行
2. 有序列表第二行
3. 有序列表第三行
4. …………

**次级列表**：在输入内容前按制表符（TAB）即可实现内容缩进。

示例如下：

1. 一级列表第一行
	1. 二级列表第一行
	2. 二级列表第二行
2. 一级列表第二行
3. 一级列表第三行
	1. 二级列表第一行
	2. 二级列表第二行
4. …………

#### 任务列表

^30b2f1

`- [ ] `后输入文本内容，每一行均采用此格式，即可生成任务列表

示例如下：

- [ ] 第一个任务
- [ ] 第二个任务
- [ ] 第三个任务
- [ ] …………

### 转义符与代码块（避免引用 Markdown 语法）

从上面的内容中我们能了解到，在兼容 Markdown 语法的写作模式下，输入部分符号会触发相应的排版功能，那么，如果我们需要的输出的是符号本身，而不希望它作为一个排版标记被解读，该如何操作呢？答案是使用转义符或者代码块。

**Markdown 中多数转义符为原字符前多加一个右斜杠** `\` ，即直接输入原字符会被转化成相应的排版命令，在原字符前先加一个右斜杠 `\` ，输出的才是原字符。

或者，我们也可以使用代码块，代码块内的内容会被认定为代码从而不触发相应的排版功能。

- **行内代码**：代码内容前后用 \` 包围
- **围栏代码快**：代码块前后各一行输入 \`\`\`

示例如下：

这是一段行内代码 `code`

下面是一段围栏代码块

```
code
```

## Markdown 进阶

对于有志进一步掌握 Markdown 写作语法的读者，本人先前整理的几篇额外教程也可供各位参考

- [[Methues_Master-the-Best-Software_02-Markdown_01-Introduction to Markdown Syntax|Markdown 语法简介]]
- [[Methues_Master-the-Best-Software_02-Markdown_02-Basic Markdown Syntax|Markdown 基本语法]]
- [[Methues_Master-the-Best-Software_02-Markdown_03-Extended Markdown Syntax|Markdown 扩展语法]]

需要快速查询 Markdown 语法则可以参考这篇：[[Methues_Master-the-Best-Software_02-Markdown_04-Markdown Syntax Quick Reference|Markdown语法速查]]

### 其他写作规范（个人推荐）

以下所列举的内容并非强制性的，但为了让纯文本写作输出的内容看起来更舒适，本人在此额外推荐一些写作习惯，有些是 Markdown 语法中非强制性但建议使用的内容，有些则是源自 LaTeX，结合个人写作习惯总结而来。

**标题与段落间，段落与段落间额外空行**：这其实也是 Markdown 的基础语法之一，这一习惯可以有效将排版时因字符长度超出产生的自动换行和人为的用于切换段落的换行区分开来。

**中英文切换时，添加空格**：这一点是 LaTeX 中的规则，笔者接触后发现这对于排版的美观确实大有帮助，因此将其融入日常写作习惯当中。（**阿拉伯数字同样视作英文**）

**修饰性标点所属语言和修饰内容统一**：修饰性标点即引号`“”`、括号`（）`这种用于将句子中的部分内容截取出来的标点。引号应该和其所引用的内容（两个引号中间的内容）语言一致，括号应该和其所注释的内容（左括号前面的内容）语言一致，更详细的解释请见[[Methues_Master-the-Best-Software_03-Obisidian_04-Guide-to-Markdown-Syntax-and-Link-Creation#^fd8360|中英文混排中的括号使用实例]]。

**非修饰性标点所属语言和句子主体统一**：除修饰性标点以外，中文句子（即使插入有英文）用中文标点，英文句子（即使插入有中文）用英文标点，英文标点后加空格（括号例外，括号贴在修饰的文本两边），中文标点后不加空格。

**括号贴两边**：英文括号贴在其所修饰内容的两侧，即左括号左侧可以有空格，右侧应紧贴内容，右括号与正常标点一致，但如果右括号和其他标点连续使用的，右括号与其他标点之间不加空格，之后再空格。示例如下：I (you can also say 'me') love to read books (especially on weekends).

#### 中英文混排中的括号使用实例

^fd8360

1. 常见的一种是中文主句里夹了一个括号，括号里全是英文或阿拉伯数字，一般是选择中文括号是比较合适的，显得和中文主句连接更紧密，示例如下：
	-  ADCIRC 模型将通用波动连续性方程（GWCE）与动量守恒方程一起作为控制方程进行求解。
2. 英文中的中文注释，选用英文括号，示例如下：
	- The philosophy based on the texts of the Daodejing (道德經) and the Zhuangzi (莊子).
3. 中英文混排中的对英文注释说明用的括号，应该用英文，示例如下：
	- 我作为一个消费者，对于 13-inch MacBookPro (with Retina Display) 很不看好。
4. 对于段首或句首用数字来排序的情况，如果数字外要加括号，个人觉得用英文括号较为合适，如(1)、(2)、(3)、(4)。

## Emoji Toolbar 插件

Emoji（絵文字，日语发音为“えもじ”）是一种起源于日本的字符，用于在数字通信中表达情感或想法。它们通常是小型的图像或图标，可以嵌入在文本消息、社交媒体帖子、电子邮件和其他在线通信中。Emoji 的流行始于智能手机的短信功能，并且随着时间的推移，它们已经发展成为全球数字交流中不可或缺的一部分。

随着技术的发展，Emoji 已经标准化，并且被纳入 Unicode 编码系统，这使得它们能够在不同的设备和平台上保持一致的显示。现在，Emoji 已经成为全球范围内人们日常交流的一部分，并且不断有新的 Emoji 被添加到 Unicode 标准中。

在笔记中适当插入 Emoji 可以消除沉闷严肃的氛围，让我们的笔记变得活泼灵动，想要输入 Emoji，我们可以选择找一个[汇总 Emoji 的网站](https://www.emojiall.com/zh-hans/all-emojis)，从上面直接复制。

但是每次输入 Emoji 都要专门跳到浏览器中查看终归还是有些太麻烦了，如果想实现更快捷的输入，我们也可以选择 Emoji Toolbar 插件。安装相应插件后，在 Obsidian设置→快捷键→Emoji Toolbar: Open emoji picker 中，为输入 Emoji 绑定好相应的快捷键（笔者自己绑定的是 Ctrl+Alt+E），之后只需按相应快捷键+选择相应的 Emoji，就能完成 Emoji 的输入啦。

*插件在 Obsidian 的第三方插件市场就可以下载，如果暂时没有网络，也可以在本系列教程的附件中找到下载好的版本，将“obsidian-emoji-toolbar”文件夹复制到“XXX（Obsidian 仓库名称）/.obsidian/plugin”目录下即可*。

## 在 Obsidian 中创建链接

在文档中插入的 URL 图片地址，网页 URL 地址，我们称之为外部链接。如果在 Obsidian 文档中想要引用其它文档，或者其文档中的标题，部分段落，我们需要创建内部链接。在 Obsidian 中我们通常将内部链接称作双链或者双向链接，然后在 Obsidian 环境中我们使用链接（Link）指代内部链接，如果有特殊情况会单独说明。 ^f92158

在文档中创建链接的语法为 `[[文档名称]]`，当我们输入前两个中括号后，Obsidian 界面中会弹出文档选择下拉列表，然后自动插入文档名称并补全后面的两个中括号。一个文档内部可能会引用多个外部文档的链接，同时文档也会被别的文档引用为链接，这样就行成了一个双向的链接。我们将当前文档引入的链接称之为出链（Outgoing links），如果有其它文档引用了当前文档，则将其它文档称之为反向链接（Backlinks）。

在引入其它文档内容时我们可以选择指向整个文档，也可以引用文档标题，进一步还可以引用某个段落（块），此外还可以对引用的内容指定别名。下面是 4 种链接引用方式举例，其中 x 用来指代任意符合链接规范的文本，在 Obsidian 中输入 `[[` 后全是可视化操作选择，例如在选择文档后，在文档后输入 | 会加载文档内容让你选择要引用的段落。

- 链接到文档 ( `[[文档名]]`)：[[Methues_Master-the-Best-Software_03-Obisidian_04-Guide-to-Markdown-Syntax-and-Link-Creation]] 
- 链接到文档中的标题 (`[[文档名#标题名]]`)：[[Methues_Master-the-Best-Software_03-Obisidian_04-Guide-to-Markdown-Syntax-and-Link-Creation#Obsidian 双链使用]]
- 链接到文档中的段落 (`[[文档名#^段落编号]]`)：[[Methues_Master-the-Best-Software_03-Obisidian_04-Guide-to-Markdown-Syntax-and-Link-Creation#^f92158]]
- 链接到文档中的段落并使用别名 (`[[文档名#^段落编号|别名]]`)：[[Methues_Master-the-Best-Software_03-Obisidian_04-Guide-to-Markdown-Syntax-and-Link-Creation#^f92158|链接到文档]]
- 链接到外部网址/文件/文件夹（`[名称]（url）`）：[Obsidian 1.7.5 安装包](<D:\00 The Tyrant's Realm\01 Tyrant's Breath\02 Areas\Methues_Master-the-Best-Software\Methues_Master-the-Best-Software_03-Obisidian\附件\安装包>)

> 注意：当 obsidian 中 url 含有空格时，点旁边打开箭头是无法正常打开 url 的，实际上打开的 url 会在空格处被断开，并不是真正完整的 url，想解决这一问题，将 url 两侧用尖括号围起来即可（示例：`[名称]（<url>）`

## 相关文档

所属项目：[[Methues_Master-the-Best-Software_03-Obisidian|实用软件终极指南-03：Obsidian]]

上一篇笔记：[[Methues_Master-the-Best-Software_03-Obisidian_03-How-to-download-Obsidian-and-Guide-to-the-Interface|华厦开新：Obsidian 下载与初识界面]]

下一篇笔记：[[Methues_Master-the-Best-Software_03-Obisidian_05-Guide-to-GTD-Workflow-and-P.A.R.A.-Organization-Method|整纷剔蠹：GTD 工作流与 P.A.R.A. 组织法攻略]]