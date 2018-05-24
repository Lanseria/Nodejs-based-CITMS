# Nodejs-based-CITMS 相关毕业论文

社团工具式管理系统相关毕业论文，主要讨论：
- 小讲社团管理模式的演进
- 前端的发展史
- `JavaScript` 迈进全栈领域
- 以 `PHP` 和 `Node.js` 为例讲述微服务的流行
- 前后端分离的开发模式
- 数据库从关系型数据 `MySQL` 到非关系型数据 `Mongo` 的转变
- 毕业设计项目的设计与实现
- `docker` 的使用与一键部署

## 立即阅读

1. ⭕[摘要与关键词](./摘要与关键词.md)
1. ⭕[目录](./目录.md)
1. ⭕[绪论](./01-绪论.md)
1. ⭕[系统分析](./02-系统分析.md)
1. ⭕[系统设计](./03-系统设计.md)
1. ⭕[系统实现](./04-系统实现.md)
1. ⭕[致谢](./05-致谢.md)
1. ⭕[参考文献](./06-参考文献.md)
1. ⭕[附录](./07-附录.md)
1. ⭕[PPT](https://github.com/Lanseria/Nodejs-based-CITMS/releases/download/v0.1/show.pptx)
1. ⭕[视频](https://www.bilibili.com/video/av23434110/)

**Legend:**

- ⭕ 已完成
- ❌ 未完成
- Null 终结稿

## Build PDF USE pandoc

``` bash
# install package
sudo apt install pandoc
sudo apt install texlive-xetex
# show installed fonts
fc-list -f "%{family}\n"  :lang=zh
# build except context
pandoc -N -s --toc --smart --latex-engine=xelatex -V CJKmainfont='Noto Sans Mono CJK SC' -V mainfont='Noto Sans Mono CJK SC' -V geometry:margin=1in 0*.md  -o output.pdf
# or docx
pandoc -N -s --toc --smart --latex-engine=xelatex -V CJKmainfont='Noto Sans Mono CJK SC' -V mainfont='Noto Sans Mono CJK SC' -V geometry:margin=1in 0*.md  -o output.docx
# build except context
pandoc -N -s --toc --smart --latex-engine=xelatex -V CJKmainfont='Microsoft YaHei UI' -V mainfont='Microsoft YaHei UI' -V geometry:margin=1in 0*.md  -o output.pdf
# or docx
pandoc -N -s --toc --smart --latex-engine=xelatex -V CJKmainfont='宋体' -V mainfont='Times New Roman' -V geometry:margin=1in 0*.md  -o output.docx
# use tex
pandoc --template=template.tex --toc --latex-engine=xelatex 0*.md  -o output.docx
```

命令行有两个最关键参数
`--latex-engine=xelatex -V CJKmainfont='Noto Sans Mono CJK SC' -V`

没有这个参数，`pandoc` 显示不了中文，一个是指定 `LaTeX` 的渲染引擎，一个指定中文字体，你可以根据自己系统安装的字体来设置，其他的几个参数是锦上添花的东西，不是必须，只是我比较喜欢带书签的 `PDF` ，所以就加上了 `--toc` ，也喜欢大纲标题上带上自动分配的序列号，例如1 1.1 1.1.1……，所以也加上了-N选项。

## 内置了 latex 郑州轻工业学院论文格式

`laTeX/` 文件夹里，差不多一样，需要稍加修改

```
# 需要安装xelatex
# 最好在linux下安装
# 包文件很大,最好使用国内清华镜像
# sudo apt install texlive-xetex
$ make thesis
```

[模板论文下载](https://github.com/Lanseria/Nodejs-based-CITMS/releases/download/v0.2/main.pdf)

## 毕业论文（设计）的构成

根据我院各专业的特点，毕业论文（设计）文体结构可分为三类：

- 农理工科类毕业论文结构
- 经管文科类毕业论文结构
- 工科类毕业设计结构

### 标题

标题应简明扼要，概括论文内容。一般不超过20个汉字，必要时可以另加副标题。

### 摘要与关键词

- 摘要应说明研究目的、方法，重点是结果和结论。摘要应包含与论文（设计）同等量的主要信息，具有独立性和自含性。中文摘要一般200-300字，外文摘要不超过250个实词；
- 关键词是表示全文主题信息的单词或术语，一般3-5个；
- 摘要与关键词均须有外文翻译。

### 正文

正文是毕业论文（设计）的核心部分，占主要篇幅，可以包括：调查对象、实验和观测方法、仪器设备、材料原料、实验和观测结果、计算方法和编程原理、数据资料、经过加工整理的图表、形成的论点和导出的结论等。

> 由于学科、选题、研究方法、工作进程、结果表达方式等差异，不同学科的正文内容也不同。正文必须实事求是，客观真切，准确完备，合乎逻辑，层次分明，简练可读。

### 致谢

致谢是作者对该论文（设计）的形成作过贡献的组织或个人的书面感谢。致谢语言要诚恳、恰当，致谢内容要实在、简短。

### 参考文献

- 参考文献反映毕业论文（设计）的科学依据和所依据材料的广博程度、可靠程度，反映作者尊重他人研究成果的严肃态度，并向读者提供有关信息的出处，是毕业论文 (设计)不可缺少的组成部分；
- 参考文献列出的，一般应限于作者直接阅读过的、毕业论文 (设计)利用的、发表在正式出版物上的文献。未公开发表的资料应采用注释的方式；
- 参考文献的著录采用顺序编码制。

### 附录

毕业论文（设计）不可缺少的组成部分，或对毕业论文（设计）有重要参考价值的内容，不宜放入正文的可编入附录。

## 目录结构

论文每个部分独立成一个 Markdown 文件，文件命名以数字开头，例如 `00-摘要与关键词`、`01-目录`、`02-绪论`……

## LICENSE

[GPL](https://github.com/Lanseria/Nodejs-based-CITMS/blob/master/LICENSE)
