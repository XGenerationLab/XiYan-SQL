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

[中文版](https://github.com/XGenerationLab/XiYan-SQL/blob/main/README_zh.md) |
英文版

</div>

# XiYan-SQL: A Multi-Generator Ensemble Framework for Text-to-SQL

## Introduction in Short
XiYan-SQL is an innovative framework for LLM based Text-to-SQL. 

It contains:

1. [M-schema](https://github.com/XGenerationLab/M-Schema) a semi-structured schema representation method.

2. [Training Stragegy](https://github.com/XGenerationLab/XiYan-SQLite) a LLM training strategy with tuned generation model for SQLite (to release soon).

3. [Ensemble Strategy](https://github.com/XGenerationLab/XiYan-Selection) a multi-generator ensemble strategy with selection model (to release soon).

4. [DateResolver](https://github.com/XGenerationLab/XiYan-DateResolver) a date understanding and reasoning enhanced model, major for Chinese (to release soon).

5. [MOMQ](https://github.com/XGenerationLab/MoMQ) a multi-dialects Text-to-SQL MoE model based on Qwen (to release soon).

6. [Database Description Generation](https://github.com/XGenerationLab/XiYan-DBDescGen) a method and corresponding code for automatic description generation for Text-to-SQL (to release soon).

## Full Intro.
To tackle the challenges of large language model performance in natural language to SQL tasks, we introduce XiYan-SQL, an innovative framework that employs a multi-generator ensemble strategy to improve candidate generation.
We introduce M-Schema, a semi-structured schema representation method designed to enhance the understanding of database structures.
To enhance the quality and diversity of generated candidate SQL queries, XiYan-SQL integrates the significant potential of in-context learning (ICL) with the precise control of supervised fine-tuning.
On one hand, we propose a series of training strategies to fine-tune models to generate high-quality candidates with diverse preferences.
On the other hand, we implement the ICL approach with an example selection method based on named entity recognition to prevent overemphasis on entities.
The refiner optimizes each candidate by correcting logical or syntactical errors.
To address the challenge of identifying the best candidate, we fine-tune a selection model to distinguish nuances of candidate SQL queries.
The experimental results on multiple dialect datasets demonstrate the robustness of XiYan-SQL in addressing challenges across different scenarios.
Overall, our proposed XiYan-SQL achieves the state-of-the-art execution accuracy of 89.65\% on the Spider test set, 69.86\% on SQL-Eval, 41.20\% on NL2GQL, and a competitive score of 72.23\% on the Bird development benchmark.
The proposed framework not only enhances the quality and diversity of SQL queries but also outperforms previous methods.


## Coming Soon🕒
<p>1. The complete code for XiYan-SQL will be released.<code><strong>Dec. 2024</strong></code></p>

<p>2. The fine-tuned model for SQLite will be released.<code><strong>Dec. 2024</strong></code></p>

<p>3. A method and corresponding code for automatic description generation for Text-to-SQL will be provided.<code><strong>Dec. 2024</strong></code></p>

<p>4. The code and model of DateSolver will be released.<code><strong>Dec. 2024</strong></code></p>

<p>5. The MOMQ model and training code will be released.<code><strong>Jan. 2025</strong></code></p>

## Timeline
The major events.

| Date     | Event                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 2024-05  | Proposing M-schema, involving ICL in SQL generation, achieving 86.98% on Spider test set (SOTA 86.6%)                                                             |
| 2024-09  | Proposing DateSolver                                                                                                                                              |
| 2024-10  | Proposing a MoE model MoMQ                                                                                                                                       |
| 2024-11  | Proposing Training Strategy and Ensemble Strategy      |
|          | Achieving 89.65% on Spider test set ([new SOTA](https://paperswithcode.com/sota/text-to-sql-on-spider)), 69.86% on SQL-Eval ([new SOTA](https://paperswithcode.com/sota/text-to-sql-on-sql-eval-1)),                                                                        |
|          | Achieving 41.20% on NL2GQL, and a competitive score of 72.23% on Bird dev ([4-th](https://paperswithcode.com/sota/text-to-sql-on-bird-big-bench-for-large-scale))          |



## Citation
If you find our work helpful, feel free to give us a cite.
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
