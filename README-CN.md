## 整体规划

这个仓库更偏向力扣 SQL 练习，刷题时核心是先想清楚“这道题该用哪个 SQL 工具”；下面这棵树按操作类型（筛选行 / 改列值 / 拼行 / 列内跨行运算）组织本仓库的知识点。

```text
SQL 取数 = 对表中的“行”做去留、对“列”做计算，再把结果拼起来
│
├── 0  基础对象层（不是目的，是后面四种能力的对象）
│   │
│   ├── 表 / 行 / 列
│   │   └── 要点：先想清楚“最后这张表长什么样”，再倒着拆步骤
│   │
│   └── 执行顺序：FROM/JOIN → WHERE → GROUP BY → HAVING → 窗口函数 → SELECT → DISTINCT → ORDER BY
│       └── 要点：窗口函数在 HAVING 之后才算 → 不能直接在 WHERE/HAVING 里用它的结果，要再套一层子查询
│
├── 能力一  简单筛选：要不要这一行  →  WHERE
│   │
│   ├── WHERE   条件不满足就整行丢弃；只能用原始列，不能用聚合/窗口函数
│   ├── HAVING  对 GROUP BY 之后的结果再筛一次；可以用聚合函数
│   └── 子查询当筛选条件  WHERE col IN (SELECT ...) ≈ 集合的交/差
│
├── 能力二  复杂筛选但不删行：给这一行打标签/变形  →  SELECT
│   │
│   ├── 计算字段        用已有列的表达式算出新列
│   ├── CASE WHEN      条件分支但不丢行：把“判断”变成新列的取值
│   │   └── 配合聚合：SUM(CASE WHEN ... THEN x ELSE 0 END) 按条件统计
│   └── 字符串/日期函数  CONCAT/SUBSTRING/DATE_FORMAT/DATE_ADD 等单值变换
│
├── 能力三  行与行之间的数据运算：横着拼成一行  →  JOIN
│   │
│   ├── INNER/LEFT/RIGHT JOIN  按 key 把两张表的列拼到同一行（增加列）
│   ├── 自连接 self join        同一张表的不同行互相对照
│   └── UNION / UNION ALL       多个查询结果纵向叠在一起（增加行，不是JOIN）
│
└── 能力四  一列数据内部、跨行的运算：不拼表也能看别的行  →  窗口函数
    │
    ├── 聚合函数 + GROUP BY  把同列多行压成一个值（会减少行数）
    └── 窗口函数 函数() OVER (PARTITION BY ... ORDER BY ...)
        ├── 排名: ROW_NUMBER / RANK / DENSE_RANK / NTILE（分桶排名）
        ├── 累计: SUM/AVG/COUNT OVER（配合 ROWS/RANGE 帧子句）
        └── 偏移: LAG / LEAD 取上下行同列的值（自连接的替代品）
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
