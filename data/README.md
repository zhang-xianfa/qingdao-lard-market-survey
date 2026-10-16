# 数据目录

## `raw/` —— 原始数据

计划收录（由作者后续放入）：

| 文件 | 说明 | 来源 |
|---|---|---|
| `student.sav` | 高校学生群体问卷原始数据 | SPSS |
| `student_scale.sav` | 学生群体量表数据 | SPSS |
| `resident.sav` | 城市居民群体问卷原始数据 | SPSS |
| `resident_scale.sav` | 居民群体量表数据 | SPSS |
| `*.amw` / `*.amp` | AMOS 结构方程模型工程文件 | AMOS |
| `*.AmosOutput` | AMOS 模型输出结果 | AMOS |

> `.sav` 为 SPSS 专有二进制格式，Python 侧可用 `pyreadstat` 读取：
> ```python
> import pyreadstat
> df, meta = pyreadstat.read_sav("raw/student.sav")
> ```
> AMOS 工程文件需 AMOS 软件打开，仅作分析过程留档。

## `processed/` —— 清洗后数据

分析脚本产出的中间数据（长表、标准化后的量表得分等）。

## 隐私约定

- 问卷数据已剔除受访者姓名、电话等个人身份字段。
- **请投放前自查**：确认 `.sav` 中不含开放题的手机号、微信号等自由文本中的联系方式。
