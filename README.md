<p align="center">
  <img src="https://raw.githubusercontent.com/XGenerationLab/XiYan-SQL/main/xiyanGBI.png" alt="image" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/XGenerationLab/XiYan-SQL/refs/heads/main/xiyansql.png" alt="image" width="400"/>
</p>


<div align="center">
  
[🤗 析言GBI](https://bailian.console.aliyun.com/xiyan) | 
[💻 M-Schema](https://github.com/XGenerationLab/M-Schema) | 
[📖 Arxiv](https://arxiv.org/abs/2411.08599)| 
[📄 PapersWithCode](https://paperswithcode.com/paper/xiyan-sql-a-multi-generator-ensemble)

</div>

<div align="center">

[中文版](https://github.com/XGenerationLab/XiYan-SQL/blob/main/README_zh.md) |
英文版

</div>

# XiYan-SQL: A Multi-Generator Ensemble Framework for Text-to-SQL

We are excited to announce that XiYanSQL-QwenCoder-32B can be used directly through ModelScope API. For details, see [XiYanSQL-QwenCoder-32B-2412](https://www.modelscope.cn/models/XGenerationLab/XiYanSQL-QwenCoder-32B-2412)

## News🔥
+ `Mar. 13, 2025` 🌟We release a MCP server of XiyanSQL: [XiYan-MCP-server](https://github.com/XGenerationLab/xiyan_mcp_server).

+ `Mar. 10, 2025` 🌟We have fully released our XiYanSQL-QwenCoder series models on the HuggingFace platform: [HuggingFace](https://huggingface.co/collections/XGenerationLab/xiyansql-models-67c9844307b49f87436808fc).

+ `Mar. 04, 2025` 🌟We release the method and source code of automatically generating database description for Text-to-SQL: [Database Description Generation](https://github.com/XGenerationLab/XiYan-DBDescGen).

+ `Feb. 26, 2025` 🌟We are excited to open source the [XiYanSQL-QwenCoder](https://github.com/XGenerationLab/XiYanSQL-QwenCoder) series model, dedicated to advancing the development of LLMs in the text-to-SQL domain. As of now, XiYanSQL-QwenCoder covers four mainstream model sizes: 3B, 7B, 14B, and 32B parameters, to meet the needs of different developers.

+ `Jan. 22, 2025` 🌟We release [XiYanSQL-QwenCoder-32B](https://github.com/XGenerationLab/XiYanSQL-QwenCoder) and simultaneously open source the model weights.

+ `Jan. 09, 2025` 🌟[XiYanSQL-QwenCoder-32B](https://github.com/XGenerationLab/XiYanSQL-QwenCoder): XiYanSQL-QwenCoder-32B achieves an EX score of **69.03%** on the BIRD test set, setting a new SOTA under only a single fine-tuned model.

+ `Dec. 17, 2024` 🌟[New SOTA on Bird](https://bird-bench.github.io/): XiYan-SQL reaches the **top** of Bird leaderboard with an EX score of **75.63%**, outperforming the second place by 0.84 pt. It also achieves a new SOTA with an R-VES score of **71.41%**.

+ `Dec. 13, 2024` We release the model and source code of [DateResolver](https://github.com/XGenerationLab/XiYan-DateResolver).

+ `Dec. 12, 2024` Try our model: [ModelScope](https://www.modelscope.cn/studios/XGenerationLab/XiYanSQL-QwenCoder-32B)


## Introduction in Short
XiYan-SQL is an innovative framework for LLM based Text-to-SQL. 

It contains:

1. [M-schema](https://github.com/XGenerationLab/M-Schema) a semi-structured schema representation method.

2. [XiYanSQL-QwenCoders](https://github.com/XGenerationLab/XiYanSQL-QwenCoder)  Multiple different sizes of XiYanSQL models for SQL generation.

3. [Ensemble Strategy](https://github.com/XGenerationLab/XiYan-Selection) a multi-generator ensemble strategy with selection model (to release soon).

4. [DateResolver](https://github.com/XGenerationLab/XiYan-DateResolver) a date understanding and reasoning enhanced model, major for Chinese.

5. [MoMQ](https://github.com/XGenerationLab/MoMQ) a multi-dialects Text-to-SQL MoE model based on Qwen (to release soon).

6. [Database Description Generation](https://github.com/XGenerationLab/XiYan-DBDescGen) a method and corresponding code for automatic description generation for Text-to-SQL.


## Full Intro.
To tackle the challenges of large language model performance in natural language to SQL tasks, we introduce XiYan-SQL, an innovative framework that employs a multi-generator ensemble strategy to improve candidate generation.
We introduce M-Schema, a semi-structured schema representation method designed to enhance the understanding of database structures.
To enhance the quality and diversity of generated candidate SQL queries, XiYan-SQL integrates the significant potential of in-context learning (ICL) with the precise control of supervised fine-tuning.
On one hand, we propose a series of training strategies to fine-tune models to generate high-quality candidates with diverse preferences.
On the other hand, we implement the ICL approach with an example selection method based on named entity recognition to prevent overemphasis on entities.
The refiner optimizes each candidate by correcting logical or syntactical errors.
To address the challenge of identifying the best candidate, we fine-tune a selection model to distinguish nuances of candidate SQL queries.
The experimental results on multiple dialect datasets demonstrate the robustness of XiYan-SQL in addressing challenges across different scenarios.
Overall, our proposed XiYan-SQL achieves the state-of-the-art execution accuracy of 75.63\% on Bird test, 89.65\% on the Spider test set, 69.86\% on SQL-Eval, 41.20\% on NL2GQL.
The proposed framework not only enhances the quality and diversity of SQL queries but also outperforms previous methods.


## Coming Soon🕒

1. More code and models will be released.

2. The XiYanSQL-QwenCoder series model will be released in `Feb 2025`. `Done`
   
3. The fine-tuned model for SQL generation will be released.`Jan. 2025` `Done`

4. A method and corresponding code for automatic description generation for Text-to-SQL will be provided.`Feb. 2025` `Done`

5. The code and model of [DateResolver](https://github.com/XGenerationLab/XiYan-DateResolver) will be released. `Dec. 2024` `Done`


## Timeline
The major events.

| Date     | Event                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 2024-05  | Proposing M-schema, involving ICL in SQL generation   |
|          | Achieving 86.98% on Spider test set (SOTA 86.6%)       |
| 2024-09  | Proposing DateSolver                      |
| 2024-10  | Proposing an MoE model MoMQ   |
| 2024-11  | Proposing Training Strategy and Ensemble Strategy      |
|          | Achieving 89.65% on Spider test set ([new SOTA](https://paperswithcode.com/sota/text-to-sql-on-spider)), 69.86% on SQL-Eval ([new SOTA](https://paperswithcode.com/sota/text-to-sql-on-sql-eval-1))                                                                     |
|          | Achieving 41.20% on NL2GQL, and a competitive score of 72.23% on Bird dev ([4-th](https://paperswithcode.com/sota/text-to-sql-on-bird-big-bench-for-large-scale))          |
| 2024-12  | Reaching the top of Bird leaderboard with an EX score of 75.63% and R-VES of 71.41([new SOTA](https://bird-bench.github.io/))     |
| 2025-01  | XiYanSQL-QwenCoder-32B achieves an EX score of 69.03% on BIRD test, new SOTA using only single fine-tuned model        |
|          | XiYanSQL-QwenCoder-32B has been released          |
| 2025-02  | We have released the XiYanSQL-QwenCoder series model, which includes four different sizes: 3B, 7B, 14B, and 32B parameters, to meet the needs of different developers. |

## Recruitment

We're looking for summer interns, research interns, new graduates, and internal transfers!

Please contact: Zhiling Luo, godot.lzl@alibaba-inc.com


## Application
Welcome everyone to try the intelligent data querying solution based on XiYan-SQL, which is called XiYan GBI. We welcome any product experiences and suggestions for optimization.

For product introduction, please visit: https://help.aliyun.com/zh/model-studio/user-guide/brief-introduction-of-gbi-products

To try the product, please visit: https://bailian.console.aliyun.com/xiyan

Product DingTalk Group: 94725009401


## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=XGenerationLab/XiYan-SQL&Date)](https://star-history.com/#XGenerationLab/XiYan-SQL&Date)

## Citation
If you find our work helpful, feel free to give us a cite.
```bibtex
@article{xiyansql,
      title={A Preview of XiYan-SQL: A Multi-Generator Ensemble Framework for Text-to-SQL}, 
      author={Yingqi Gao and Yifu Liu and Xiaoxia Li and Xiaorong Shi and Yin Zhu and Yiming Wang and Shiqi Li and Wei Li and Yuntao Hong and Zhiling Luo and Jinyang Gao and Liyu Mou and Yu Li},
      year={2024},
      journal={arXiv preprint arXiv:2411.08599},
      url={https://arxiv.org/abs/2411.08599},
      primaryClass={cs.AI}
}
```
