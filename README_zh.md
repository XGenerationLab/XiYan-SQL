<p align="center">
  <img src="https://raw.githubusercontent.com/XGenerationLab/XiYan-SQL/main/xiyanGBI.png" alt="image" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/XGenerationLab/XiYan-SQL/main/xiyansql.png" alt="image" width="400"/>
</p>


<div align="center">
  
[🤗 析言GBI](https://bailian.console.aliyun.com/xiyan) | 
[💻 M-Schema](https://github.com/XGenerationLab/M-Schema) | 
[📖 Arxiv](https://arxiv.org/abs/2411.08599)| 
[📄 PapersWithCode](https://paperswithcode.com/paper/xiyan-sql-a-multi-generator-ensemble)

</div>

<div align="center">

中文版 |
[英文版](https://github.com/XGenerationLab/XiYan-SQL/blob/main/README.md)

</div>

# XiYan-SQL：一种多生成器集成的Text-to-SQL框架

## 简介
XiYan-SQL是一个全新的基于LLM的Text-to-SQL框架。

XiYan-SQL包含以下内容：

1. [M-schema](https://github.com/XGenerationLab/M-Schema) 一种半结构化的schema表示方法。

2. [训练策略](https://github.com/XGenerationLab/XiYan-SQLite) 针对SQLite的LLM训练策略和微调模型（即将发布）。

3. [即成策略](https://github.com/XGenerationLab/XiYan-Selection) 一个具有选择模型的多生成器集成策略（即将发布）。

4. [DateResolver](https://github.com/XGenerationLab/XiYan-DateResolver) 一个增强日期理解和推理的模型，主要针对中文（即将发布）。

5. [MoMQ](https://github.com/XGenerationLab/MoMQ) 一个基于QWen的多方言Text-to-SQL的MoE模型（即将发布）。

6. [数据库描述生成](https://github.com/XGenerationLab/XiYan-DBDescGen) 一个自动数据库描述的方法和相应代码（即将发布）。

## 引言
为了应对大型语言模型在Text-to-SQL任务中的挑战，我们引入了XiYan-SQL，这是一个全新的框架，采用多生成器集成的策略来提高候选SQL的质量。
为此，我们提出了M-Schema，一种半结构化的数据库schema表示方法，旨在增强模型对于数据库结构的理解能力。
然后，为了提高生成的候选SQL查询的质量和多样性，XiYan-SQL结合了ICL方法的巨大潜力和SFT方法的高可控性。
一方面，我们提出了一系列训练策略，以微调模型生成高质量且具有不同偏好的候选。
另一方面，我们采用ICL的方法来提示LLM，并提出了一种基于命名实体识别的方法来选择ICL的样例，从而防止过度强调实体。
Refiner通过纠正逻辑或语法错误来进一步优化每个候选。
为了应对识别最佳候选的挑战，我们微调了一个选择模型，用来区分候选SQL查询之间的细微差别。
在多个方言的数据集上的实验结果表明，XiYan-SQL在不同场景中均具有鲁棒性。
总体而言，我们提出的XiYan-SQL在Spider测试集上达到了89.65%的执行准确率，在SQL-Eval上达到了69.86%，在NL2GQL上达到了41.20%，在Bird development基准上达到了72.23%的分数。该结果是1st on spider，1st on SQL_EVAL，3rd on bird dev。该框架不仅提高了生成SQL查询的质量和多样性，端到端的效果也优于以前的方法。

## 即将发布，敬请期待🕒
<p>1. 我们将发布完整的XiYan-SQL代码。<code><strong>2024-12</strong></code></p>

<p>2. 我们将发布微调的SQLite模型。<code><strong>2024-12</strong></code></p>

<p>3. 我们将提供一种用于NL2SQL的自动生成数据库描述的方法和对应的代码。<code><strong>2024-12</strong></code></p>

<p>4. 我们将发布DateSolver的模型和代码。<code><strong>2024-12</strong></code></p>

<p>5. 我们将发布MoMQ的模型和训练代码<code><strong>2025-01</strong></code></p>

## 时间线
主要事件：

| 日期    | 事件   |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 2024-05  | 提出M-schema，在SQL生成中引入ICL   |
|          | 在Spider test上达到86.98% (SOTA 86.6%) |
| 2024-09  | 提出DateSolver                      |
| 2024-10  | 提出一个MoE模型MoMQ   |
| 2024-11  | 提出了新的训练和集成方法 |
|          | 在Spider test上达到89.65%([新的SOTA](https://paperswithcode.com/sota/text-to-sql-on-spider))，在SQL-Eval上达到69.86% ([新的SOTA](https://paperswithcode.com/sota/text-to-sql-on-sql-eval-1))                                                                     |
|          | 在NL2GQL上达到41.20%，Bird dev上达到72.23% ([4-th](https://paperswithcode.com/sota/text-to-sql-on-bird-big-bench-for-large-scale))         |

## 应用
欢迎大家体验基于XiYan-SQL打造的智能问数解决方案——析言GBI。
登录阿里云百炼-应用广场-析言GBI，任何产品体验及效果优化建议欢迎与我们交流。

产品介绍请访问：https://help.aliyun.com/zh/model-studio/user-guide/brief-introduction-of-gbi-products

体验产品请访问：https://bailian.console.aliyun.com/xiyan

产品钉群：94725009401

## 引用
如果您觉得我们的工作对您有帮助，欢迎引用。
```bibtex
@article{xiyansql,
      title={XiYan-SQL: A Multi-Generator Ensemble Framework for Text-to-SQL}, 
      author={Yingqi Gao and Yifu Liu and Xiaoxia Li and Xiaorong Shi and Yin Zhu and Yiming Wang and Shiqi Li and Wei Li and Yuntao Hong and Zhiling Luo and Jinyang Gao and Liyu Mou and Yu Li},
      year={2024},
      journal={arXiv preprint arXiv:2411.08599},
      url={https://arxiv.org/abs/2411.08599},
      primaryClass={cs.AI}
}
```
