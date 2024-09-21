# 说明

本数据集属于 **根因分析与练习系统（Root Cause Analysis and Exercises for Mathematics, RCAE）** 的基础子项目之一。旨在可以高效的发现学生数学、生物学业错误的根本原因。

![示例图片](https://raw.githubusercontent.com/digitalboy/mathGPT_graph_data/main/sample.png)

![示例图片](https://raw.githubusercontent.com/digitalboy/mathGPT_graph_data/main/bio.png)

## 总项目介绍

**根因分析与练习系统（RCAE）** 是一款利用先进的图数据库技术和强大的数据分析算法，旨在革新教育的系统。通过对学生答题记录的分析，RCAE能够快速定位学生掌握不牢固的知识点，并生成个性化的练习计划，帮助学生高效提升成绩。

## 此数据集的意义

本数据集是“根因分析与练习系统（RCAE）”的一个子项目，包含由人民教育出版社和北京师范大学出版社出版的小学数学全部知识点的详尽知识图谱。通过这个数据集，可以实现对小学数学知识点的全面了解和掌握，辅助RCAE系统进行更准确的根因分析和个性化练习推荐。
还包括生物初中，高中和竞赛的知识点和边。

## 此数据集的优势
1. **充分MECE**：已经尽可能的将知识点做到不缺失，不遗漏，不重复，相互独立。
2. **关系充分**：从先决关系、包含关系、互补关系等N种关系（数学和生物不同）。基本覆盖了领域的所有关系。
3. **拓展**：比如统计某种关系的数量，判断节点的重要性和复杂性等。

## 后续发展计划
1. **更多数据**：继续拓展初中，高中各个年级；人教出版社，北美……
2. **知识点解释**：为每个知识点提供生动、传神、有趣的解释，提高可理解性并降低学生的认知负荷。
3. **题目设计**：根据布鲁姆目标分类和孩子的认知规律，为每个知识点设计题目，难度分层。
4. **根因溯源**：可以快速的找到错题的根因，谨防无效刷题（我最恨这个了）。
5. **教师界面**：老师可以随时查看各种数据透视，快速掌握群体、个体的学业水平。
6. **结合脑科学**：学习尽快不能很快乐，但是尽量不要伤害孩子的学习热情。


## 使用方法
1. **下载数据集**：从GitHub仓库下载JSON格式的知识点图数据。
2. **加载数据**：将下载的JSON数据导入图数据库（如Neo4j）。
3. **构建知识图谱**：使用图数据库工具构建知识点之间的关系图谱。
4. **使用API**：如下。

## 体验地址
https://math.beike.ai/admin/test （暂时关闭）



## 版权声明
本数据集和相关代码由[张扬]创建，采用 **[Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/deed.zh)** 许可证进行许可。

### 您可以自由地：
- **共享** — 在任何媒介以任何形式复制、分发和传播本数据集和相关代码。
- **演绎** — 修改、转换或以本数据集和相关代码为基础进行创作。

### 在以下条件下：
- **署名** — 您必须给出适当的署名，提供指向本声明的链接，并指明是否对作品进行了修改。您可以以任何合理方式进行，但不得以任何方式暗示许可人认可您或您的使用。
- **非商业性使用** — 您不得将本数据集和相关代码用于商业目的。

### 没有附加限制：
- 您不得适用法律术语或技术措施从而限制其他人做许可证允许的任何事情。

### 免责声明：
- 本数据集和相关代码按“原样”提供，不附带任何明示或暗示的担保。使用者需自行承担使用风险。作者不对因使用本数据集和相关代码而产生的任何索赔、损害或其他责任负责，无论是在合同诉讼、侵权诉讼或其他诉讼中。

有关详细信息，请参见[Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) 许可证](https://creativecommons.org/licenses/by-nc/4.0/deed.zh)。

## 目前存在的问题
尽管已经具备的相当的可用性，但是由于本人精力有限，才疏学浅，难免疏漏。

1. **数据完整性**：数据集可能存在某些知识点的缺失或描述不完整的情况，需要持续完善。
2. **关系准确性**：知识点之间的关系需要进一步验证和优化，确保其准确性和逻辑性。
3. **系统兼容性**：不同图数据库的兼容性和性能差异可能影响知识图谱的构建和查询效率。
4. **用户反馈**：需要更多的用户反馈来优化系统的算法和数据结构，提高整体效果。

## 需要的帮助
1. **编程**：如果您有编程能力，并热爱AI+教育，联系我。
2. **一线教师**：如果您能在一线实践并检测这个系统，联系我。
3. **脑科学**：如果您对教育+认知科学有兴趣，联系我。

## 联系作者

如有任何问题或建议，请通过以下方式联系作者：

- **微信**：13510546101
- **邮箱**：digitalboyzone@gmail.com
- **Twitter**：https://x.com/freethisslave

欢迎大家提供宝贵意见和建议，共同完善数学根因分析与练习系统！

## 关系(edge)表：
```
[
    {
        "type": "Prerequisite",
        "direction": "directed",
        "description": "描述一个概念是理解另一个概念的先决条件。",
        "example": {"from": "加法", "to": "乘法"}
    },
    {
        "type": "Includes",
        "direction": "directed",
        "description": "表明一个概念是另一个更广泛概念的一部分。",
        "example": {"from": "三角形", "to": "几何图形"}
    },
    {
        "type": "RelatedTo",
        "direction": "undirected",
        "description": "表示两个概念之间的相关性或关联性。",
        "example": {"from": "概率", "to": "统计"}
    },
    {
        "type": "AppliedIn",
        "direction": "directed",
        "description": "指一个概念如何在另一个领域或实例中被应用。",
        "example": {"from": "几何学", "to": "建筑设计"}
    },
    {
        "type": "AdvancesTo",
        "direction": "directed",
        "description": "表明一个概念是另一个概念的深入或拓展。",
        "example": {"from": "基础代数", "to": "高等代数"}
    },
    {
        "type": "ContrastsWith",
        "direction": "undirected",
        "description": "描述两个概念之间的对比或差异。",
        "example": {"from": "离散数学", "to": "连续数学"}
    },
    {
        "type": "SynonymousWith",
        "direction": "undirected",
        "description": "用于连接意思相近或相同的不同表述的概念。",
        "example": {"from": "减法", "to": "差运算"}
    },
    {
        "type": "HistoricallyDevelopedFrom",
        "direction": "directed",
        "description": "反映了概念的历史发展或演变。",
        "example": {"from": "古典代数", "to": "现代代数"}
    },
    {
        "type": "SubsetOf",
        "direction": "directed",
        "description": "表示一个概念是另一个概念的子集。",
        "example": {"from": "有理数", "to": "实数"}
    },
    {
        "type": "SpecialCaseOf",
        "direction": "directed",
        "description": "表示一个概念是另一个更一般概念的特殊情况。",
        "example": {"from": "正方形", "to": "矩形"}
    },
    {
        "type": "AnalogousTo",
        "direction": "undirected",
        "description": "表示两个概念在不同情境下具有类似的结构或性质。",
        "example": {"from": "平面几何", "to": "立体几何"}
    },
    {
        "type": "ComplementaryTo",
        "direction": "undirected",
        "description": "表示两个概念在一定程度上互为补充。",
        "example": {"from": "微分", "to": "积分"}
    }
]

```
