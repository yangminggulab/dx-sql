## 整体规划

参考 PostgreSQL 官方教程的 SQL 语言路径：先理解表、行、列，再进入查询、连接、聚合、更新删除等核心操作；本仓库更偏向力扣 SQL 练习，重点放在查询表达、连接、函数、聚合、窗口函数和子查询。

```text
SQL = 用声明式查询从关系表中取出问题答案
│
├── 这门课要解决的问题
│   ├── 数据在数据库里怎样组织？
│   │   └── 用表、行、列、键和关系表达业务对象
│   ├── 怎样从一张表里筛出想要的信息？
│   │   └── 用 SELECT、WHERE、ORDER BY、LIMIT 和表达式完成基础查询
│   └── 怎样把多张表和多行数据合成答案？
│       └── 用 JOIN、GROUP BY、子查询、UNION 和窗口函数组织复杂逻辑
│
├── 工具一  基础查询
│   ├── SELECT / WHERE    选择列并过滤行
│   ├── 计算字段          用表达式生成新结果
│   ├── 字符串和日期函数  处理文本、时间和格式
│   └── 正则与条件表达式  应对更细的匹配和分支
│
├── 工具二  多表关系
│   ├── INNER / LEFT JOIN  根据键把表连起来
│   ├── UNION / UNION ALL  合并多个查询结果
│   └── 子查询             把一个查询结果作为另一个查询的条件或来源
│
└── 工具三  汇总与窗口
    ├── 聚合函数          count、sum、avg、max、min
    ├── GROUP BY          把多行压缩成分组结果
    ├── HAVING            对分组后的结果再过滤
    └── 窗口函数          在不合并行的前提下做排名、累计和分组计算
```

<!-- Author : Dongsheng Deng & Liam Huang-->
<!-- Program Email: elegantlatex2e@gmail.com -->

[Homepage](https://elegantlatex.org/) | [Github](https://github.com/ElegantLaTeX/ElegantBook) | [CTAN](https://ctan.org/pkg/elegantbook) | [Download](https://github.com/ElegantLaTeX/ElegantBook/releases) | [Wiki](https://github.com/ElegantLaTeX/ElegantBook/wiki) | [Weibo](https://weibo.com/elegantlatex)

![License](https://img.shields.io/ctan/l/elegantbook.svg) ![CTAN Version](https://img.shields.io/ctan/v/elegantbook.svg) ![Github Version](https://img.shields.io/github/release/ElegantLaTeX/ElegantBook.svg) ![Repo Size](https://img.shields.io/github/repo-size/ElegantLaTeX/ElegantBook.svg)

---

# ElegantBook 优美的 LaTeX 书籍模板

ElegantBook 是为 LaTeX 书籍写作而设计的模板，由 [Dongsheng Deng](https://ddswhu.me/) 和 [Liam Huang](https://liam.page/) 创立，模板创立的初衷是方便我们自己做笔记 :smile:。如果你有其他问题、建议或者报告 bug，可以提交 issues 或者给我们发邮件：elegantlatex2e@gmail.com。QQ 用户交流群：692108391，欢迎加入。

## 重要提示

**重要提示**：ElegantLaTeX 项目 **不接受** 任何非预授权的提交（pull requests）！

## 致谢

特别感谢 [sikouhjw](https://github.com/sikouhjw) 和 [syvshc](https://github.com/syvshc) 长期以来对于 Github 上 issue 的快速回应，以及各个社区论坛对于 ElegantLaTeX 相关问题的回复。
特别感谢 ChinaTeX 以及 [LaTeX 工作室](http://www.latexstudio.net/)对于本系列模板的大力宣传与推广。

如果你喜欢我们的模板，你可以在 Github 上收藏我们的模板。

## 协议

本模板发布遵循 LaTeX 项目公共许可证 1.3 c 或更高版本。如果是衍生作品，请务必加入协议声明和模板信息（github、CTAN 地址）。

## 衍生作

+ [ElegantBookdown](https://github.com/XiangyunHuang/ElegantBookdown)：[XiangyunHuang](https://github.com/XiangyunHuang) 开发并维护的基于 ElegantBook 的 Bookdown 模板。
+ [bookdownplus](https://github.com/pzhaonet/bookdownplus)：应网友要求，[pzhaonet](https://github.com/pzhaonet) 在 bookdownplus 收录了 ElegantPaper 模板，并为 Mac 做了字体适配。
+ [PanBook](https://github.com/annProg/PanBook)：[annProg](https://github.com/annProg) 开发并维护的基于 Markdown 写作的工作流，收录了 ElegantBook 和 ElegantPaper 模板。
