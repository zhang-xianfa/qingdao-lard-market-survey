# 分析脚本

按分析模块命名，编号即建议的执行顺序。

| 脚本 | 职责 | 依赖 |
|---|---|---|
| `01_reliability.py` | 信度分析：各潜变量的 Cronbach's α，删题后 α 变化 | pandas, pyreadstat |
| `02_factor_analysis.py` | 效度分析：KMO 与 Bartlett 检验、探索性因子分析 | pandas, factor_analyzer |
| `03_descriptive.py` | 描述性统计：样本构成、各题均值与分布 | pandas |
| `04_random_forest.py` | 随机森林特征重要性（基尼指数），分群体对比 | scikit-learn |
| `05_clustering.py` | 按消费频率对消费者聚类分群 | scikit-learn, scipy |
| `06_text_mining.py` | 网络评论 TF-IDF、词云、情感占比、共现网络 | jieba, wordcloud, networkx |
| `common.py` | 数据读取与清洗的公共函数 | — |

## 约定

- 输入统一从 `../data/raw/` 读，输出图表写 `../figures/`，表格写 `../results/`。
- 图表中文字体设置写在 `common.py`，避免每个脚本重复。

## 说明

结构方程模型（SEM）由 AMOS 图形界面完成，没有对应的 Python 脚本；
模型设定与假设见 [`../docs/研究设计.md`](../docs/研究设计.md)。
如后续希望用 Python 复现，可用 `semopy` 包。
