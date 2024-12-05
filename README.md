<p align="center">
  <img src="https://raw.githubusercontent.com/XGenerationLab/XiYan-SQL/main/xiyanGBI.png" alt="image" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/XGenerationLab/XiYan-SQL/main/xiyansql.png" alt="image" width="500"/>
</p>


<div align="center">
  
[🤗 析言GBI](https://bailian.console.aliyun.com/xiyan) | 
[💻 M-Schema](https://github.com/XGenerationLab/M-Schema) | 
[📖 Arxiv](https://arxiv.org/abs/2411.08599)| 
[📄 PapersWithCode](https://paperswithcode.com/paper/xiyan-sql-a-multi-generator-ensemble)

</div>

# XiYan-SQL: A Multi-Generator Ensemble Framework for Text-to-SQL

## Introduction
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

## Coming Soon
<span style="background-color: blue;">Dec. 2024</span>
2. The complete code for XiYan-SQL will be released.
3. The fine-tuned model for SQLite will be released.
4. A method and corresponding code for automatic description generation for NL2SQL will be provided.

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
