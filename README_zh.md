<p align="center">
  <img src="https://raw.githubusercontent.com/XGenerationLab/XiYan-SQL/main/xiyanGBI.png" alt="image" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/XGenerationLab/XiYan-SQL/refs/heads/main/xiyansql.png" alt="image" width="400"/>
</p>


<div align="center">
  
[🤗 析言GBI](https://bailian.console.aliyun.com/xiyan) | 
[🤖 XiYanSQL Model](https://github.com/XGenerationLab/XiYanSQL-QwenCoder) | 
[💻 M-Schema](https://github.com/XGenerationLab/M-Schema) | 
[📖 Arxiv](https://arxiv.org/abs/2507.04701)| 
[📖 Preview](https://arxiv.org/abs/2411.08599)| 
[📄 PapersWithCode](https://paperswithcode.com/paper/xiyan-sql-a-multi-generator-ensemble)

</div>

<div align="center">

中文版 |
[英文版](https://github.com/XGenerationLab/XiYan-SQL/blob/main/README.md)

</div>

# XiYan-SQL：一种多生成器集成的Text-to-SQL框架

#### [这里](https://github.com/alibaba/XiYan-SQL)是新的阿里巴巴官方XiYan-SQL代码库，目前我们将会同步维护这两个地址。

## 新闻🔥

+ `2025-11-21` 🌟 [New SOTA on BIRD-CRITIC-Open](https://bird-critic.github.io/): XiYan-SQL-CRITIC 技术在极具挑战性的多方言基准测试**BIRD-CRITIC-Open**上取得了令人瞩目的 **44.37%** 成功率，以 SOTA 性能稳居榜首！

+ `2025-10-30` 🌟 我们很高兴发布了XiYan-SQL的训练框架 **[XiYan-SQLTraining](https://github.com/alibaba/XiYan-SQL)**，它主要面向SQL/通用大模型的训练，其中包括XiYan提出的SQL数据处理、模型训练、评测等功能，在未来我们会逐步进行完善。
  
+ `2025-10-20` 🌟 [New SOTA on BIRD-CRITIC-Flash](https://bird-critic.github.io/): XiYan-SQL-CRITIC 技术，实现了**44.53%** 的通过率，在BIRD-CRITIC-PG榜单上获得第一名创造了新SOTA，同时在BIRD-CRITIC-Flash榜单上实现了**48.5%** 的通过率，也是新的SOTA性能。
+ `2025-10-20` 🌟 XiYan-SQL的训练框架**XiYan-SQLTraining** 将会在XiYan-SQL的阿里巴巴官方仓库近期开源发布，敬请期待！！！
+ ...
+ `2025-05-22` 🌟 [New SOTA on BIRD-CRITIC-Flash](https://bird-critic.github.io/): XiYanSQL-CRITIC算法在BIRD-CRITIC-Flash基准测试中取得了**41%** 的通过率，创下了新的 SOTA 性能。

+ `2025-04-29` 🌟 我们很高兴更新了[XiYanSQL-QwenCoder-2504](https://github.com/XGenerationLab/XiYanSQL-QwenCoder) 系列模型。此版本在上一版本的基础上进行了多项优化，单模型性能达到了新的SOTA水平，欢迎大家试用。

+ `2025-03-21` 🌟想要高安全性的数据访问？[XiYan-MCP-server](https://github.com/XGenerationLab/xiyan_mcp_server)现已支持本地模式，可在您自己的PC/Mac上运行[XiYanSQL-QwenCoder-3B](https://www.modelscope.cn/models/XGenerationLab/XiYanSQL-QwenCoder-3B-2502) 。

+ `2025-03-20` 🌟我们很高兴地宣布，XiYanSQL-QwenCoder-32B 现已可通过ModelScope API直接使用。详情请参阅[XiYanSQL-QwenCoder-32B-2412](https://www.modelscope.cn/models/XGenerationLab/XiYanSQL-QwenCoder-32B-2412)。

+ `2025-03-12` 🌟我们发布了 XiyanSQL 的 MCP 服务器： [XiYan-MCP-server](https://github.com/XGenerationLab/xiyan_mcp_server).

+ `2025-03-10` 🌟我们在 HuggingFace 平台上全面发布了XiYanSQL-QwenCoder系列模型： [HuggingFace](https://huggingface.co/collections/XGenerationLab/xiyansql-models-67c9844307b49f87436808fc).
  
+ `2025-03-04` 🌟我们发布了用于Text-to-SQL任务的自动生成数据库描述的方法和源代码: [Database Description Generation](https://github.com/XGenerationLab/XiYan-DBDescGen).

+ `2025-01-22` 🌟我们正式发布[XiYanSQL-QwenCoder-32B](https://github.com/XGenerationLab/XiYanSQL-QwenCoder-32B)并开源模型权重

+ `2025-01-09` 🌟[XiYanSQL-QwenCoder-32B](https://github.com/XGenerationLab/XiYanSQL-QwenCoder-32B): XiYanSQL-QwenCoder-32B在BIRD测试集上取得了**69.03%** 的执行准确率，成为了该榜单上仅使用单个微调模型的SOTA。

+ `2024-12-17` 🌟[Bird榜单上新的SOTA](https://bird-bench.github.io/): XiYan-SQL以**75.63%** 的执行准确率登上**Bird榜首**，领先第二名0.84pt

+ `2024-12-13` 我们公开了[DateResolver](https://github.com/XGenerationLab/XiYan-DateResolver)的代码和模型

+ `2024-12-12` 模型体验请访问：[ModelScope](https://www.modelscope.cn/studios/XGenerationLab/XiYanSQL-QwenCoder-32B)


## 简介
XiYan-SQL是一个全新的基于LLM的Text-to-SQL框架。

XiYan-SQL包含以下内容：

1. [M-schema](https://github.com/XGenerationLab/M-Schema) 一种半结构化的schema表示方法。

2. [XiYanSQL-QwenCoders](https://github.com/XGenerationLab/XiYanSQL-QwenCoder) 专用于SQL生成的多种不同尺寸的XiYanSQL模型。

3. [集成策略](https://github.com/XGenerationLab/XiYan-Selection) 一个具有选择模型的多生成器集成策略（即将发布）。

4. [DateResolver](https://github.com/XGenerationLab/XiYan-DateResolver) 一个增强日期理解和推理的模型，主要针对中文。

5. [MoMQ](https://github.com/XGenerationLab/MoMQ) 一个基于QWen的多方言Text-to-SQL的MoE模型（即将发布）。

6. [数据库描述自动生成](https://github.com/XGenerationLab/XiYan-DBDescGen) 一个自动生成数据库描述的方法和相应代码。

🌟 欢迎大家为 XiYanSQL 项目做出贡献！！！

## 引言
为了应对大型语言模型在Text-to-SQL任务中的挑战，我们引入了XiYan-SQL，这是一个全新的框架，采用多生成器集成的策略来提高候选SQL的质量。
为此，我们提出了M-Schema，一种半结构化的数据库schema表示方法，旨在增强模型对于数据库结构的理解能力。
然后，为了提高生成的候选SQL查询的质量和多样性，XiYan-SQL结合了ICL方法的巨大潜力和SFT方法的高可控性。
一方面，我们提出了一系列训练策略，以微调模型生成高质量且具有不同偏好的候选。
另一方面，我们采用ICL的方法来提示LLM，并提出了一种基于命名实体识别的方法来选择ICL的样例，从而防止过度强调实体。
Refiner通过纠正逻辑或语法错误来进一步优化每个候选。
为了应对识别最佳候选的挑战，我们微调了一个选择模型，用来区分候选SQL查询之间的细微差别。
在多个方言的数据集上的实验结果表明，XiYan-SQL在不同场景中均具有鲁棒性。
总体而言，我们提出的XiYan-SQL在Bird测试集上达到75.63%的执行准确率，Spider测试集上达到了89.65%，在SQL-Eval上达到了69.86%。该结果是**1st on Bird test, 1st on spider，1st on SQL_EVAL**。该框架不仅提高了生成SQL查询的质量和多样性，端到端的效果也优于以前的方法。

## 即将发布，敬请期待🕒

1. 我们将发布完整的XiYan-SQL代码。`2025-02`

2. 我们将发布微调的SQLite模型[XiYanSQL-QwenCoder-32B](https://github.com/XGenerationLab/XiYanSQL-QwenCoder-32B)。`2025-01` `已发布`

3. 我们将提供一种用于NL2SQL的自动生成数据库描述的方法和对应的代码。`2025-02` `已发布`

4. 我们将发布[DateResolver](https://github.com/XGenerationLab/XiYan-DateResolver)的模型和代码。`2024-12` `已发布`

5. 我们将发布MoMQ的模型和训练代码。`2025-01` 

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
|          | 在NL2GQL上达到41.20%，Bird dev上达到72.23% ([4-th](https://paperswithcode.com/sota/text-to-sql-on-bird-big-bench-for-large-scale))  |
| 2024-12  | 以75.63%的EX和71.41的R-VES登顶Bird榜单([新的SOTA](https://bird-bench.github.io/)) |
| 2025-01  | XiYanSQL-QwenCoder-32B在BIRD上达到了69.03%的EX，是仅使用单个微调模型的SOTA  |
|          | XiYanSQL-QwenCoder-32B正式发布      |
| 2025-02  | 我们发布了 XiYanSQL-QwenCoder系列模型，包含 3B、7B、14B、32B四种不同大小的参数，以满足不同开发者的需求。 |
| 2025-04  | 我们发布了XiYanSQL-QwenCoder系列模型2504版本，该版本相比上一版本性能有所提升。它仍然包含 3B、7B、14B和32B四种不同的参数大小。我们鼓励大家使用这些模型。|

## 应用
欢迎大家体验基于XiYan-SQL打造的智能问数解决方案——析言GBI。
登录阿里云百炼-应用广场-析言GBI，任何产品体验及效果优化建议欢迎与我们交流。

产品介绍请访问：https://help.aliyun.com/zh/model-studio/user-guide/brief-introduction-of-gbi-products

体验产品请访问：https://bailian.console.aliyun.com/xiyan

产品钉群：94725009401

## 联系我们

如果您对我们的研究或产品感兴趣，请随时联系我们。

#### 联系信息:

刘义富, zhencang.lyf@alibaba-inc.com

#### 加入我们的钉钉群

<a href="https://github.com/XGenerationLab/XiYan-SQL/blob/main/xiyansql_dingding.png">Ding Group钉钉群</a> 


## 引用
如果您觉得我们的工作对您有帮助，欢迎给我们一个引用。

```bibtex
@article{XiYanSQL,
      title={XiYan-SQL: A Novel Multi-Generator Framework For Text-to-SQL}, 
      author={Yifu Liu and Yin Zhu and Yingqi Gao and Zhiling Luo and Xiaoxia Li and Xiaorong Shi and Yuntao Hong and Jinyang Gao and Yu Li and Bolin Ding and Jingren Zhou},
      year={2025},
      eprint={2507.04701},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2507.04701}, 
}
```
```bibtex
@article{xiyansql_pre,
      title={A Preview of XiYan-SQL: A Multi-Generator Ensemble Framework for Text-to-SQL}, 
      author={Yingqi Gao and Yifu Liu and Xiaoxia Li and Xiaorong Shi and Yin Zhu and Yiming Wang and Shiqi Li and Wei Li and Yuntao Hong and Zhiling Luo and Jinyang Gao and Liyu Mou and Yu Li},
      year={2024},
      journal={arXiv preprint arXiv:2411.08599},
      url={https://arxiv.org/abs/2411.08599},
      primaryClass={cs.AI}
}
