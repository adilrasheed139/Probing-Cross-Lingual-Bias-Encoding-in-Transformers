# Probing Cross-Lingual Bias Encoding in Transformer Models

This repository provides a reproducible research framework for quantifying and analyzing **gender-science bias** in transformer-based language models using the *Word Embedding Association Test (WEAT)*. The work systematically compares multiple transformer architectures, evaluates cross-lingual bias in English and Urdu, and explores how bias evolves across hidden layers of neural models.

---

## 📌 Motivation

Pretrained transformer models such as BERT, RoBERTa, and XLM-RoBERTa have significantly advanced natural language processing, but also inherit and amplify societal biases present in training data. Measuring these biases is crucial to ensuring fairness and ethical deployment of language technologies. The WEAT metric, inspired by social science association tests, has become a foundational method for detecting bias in word embeddings by comparing target and attribute word group associations. :contentReference[oaicite:1]{index=1}

---

## 🎯 Project Goals

This repository aims to:

1. Implement a rigorous and reproducible pipeline for computing WEAT effect sizes from contextualized transformer hidden representations.
2. Compare gender-science bias across multiple transformer models (BERT, RoBERTa, DistilBERT, XLM-RoBERTa).
3. Extend bias evaluation to multilingual scenarios by incorporating Urdu text corpora.
4. Conduct layer-wise bias analysis to reveal how associations progress through neural representations.
5. Provide publication-ready visualizations and benchmarks for cross-lingual fairness research.

---

## 🛠 Setup & Installation

Clone the repository and set up the environment:

```bash
git clone https://github.com/adilrasheed139/Probing-Cross-Lingual-Bias-Encoding-in-Transformers
````
## 🧠 Methodology

This project uses the Word Embedding Association Test (WEAT) to quantify bias by comparing the cosine similarities between groups of target words (e.g., *math* vs. *arts*) and groups of attribute words (e.g., *male* vs. *female*). The effect size is a normalized score indicating the relative association strength. For robust evaluation, permutation testing is used to estimate statistical significance. Effect sizes and distributions are calculated for both model-level embeddings and intermediate hidden states.

---

## 📈 Key Results

The repository includes visualizations referenced in the research manuscript:

| Figure Name                                              | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- |
| **Bias Metric (WEAT) Effect Size In English**            | WEAT effect size for English transformer models.         |
| **Bias Metric (WEAT) Effect Size in Urdu**               | WEAT effect size for Urdu analysis.                      |
| **Cross-Lingual Comparison of Gender-Science Bias**      | Overlay of bias progression across languages.            |
| **Cross-Lingual Divergence in Bias Encoding**            | Comparative plot showing divergence in bias dynamics.    |
| **English (BERT) Layer 2 Word Associations Heatmap**     | Cosine similarity heatmap at peak bias layer (English).  |
| **Urdu (XLM-R) Layer 11 Word Associations Heatmap**      | Heatmap for peak bias layer in Urdu.                     |
| **Linguistic Bias Evolution through Transformer Layers** | Layer-wise effect size plot.                             |
| **WEAT Effect Size Comparison Across Models In English** | Comparative bar chart of bias scores for English models. |
| **WEAT Effect Size Comparison Across Models In Urdu**    | Comparative bar chart for Urdu models.                   |
| **WEAT Permutation Test - Gender-Science Bias**          | Permutation distribution and observed score.             |
| **Word-Level Bias Profile English (BERT) Layer 2**       | Radar plot of individual English word biases.            |
| **Word-Level Bias Profile Urdu (XLM-R) Layer 11**        | Radar plot for individual Urdu word biases.              |

All figure files are located in the `PDF` document and are suitable for academic presentations and publications.

---

## 🧪 Reproducibility & Best Practices

This README conforms to established guidelines for scientific documentation by providing clear project description, installation instructions, methodology, and usage examples. Including detailed metadata improves reproducibility and helps external users understand the structure and purpose of the project. ([UC Davis Data Lab][2])

---

## ✍️ Authorship

**Probing Cross-Lingual Bias Encoding in Transformer Models**
**Author:** *Adil Rasheed*
**Affiliation:** *Government College University Faisalabad*
**Email:** *[adilrasheed139@gmail.com](mailto:adilrasheed139@gmail.com)*
**Status:** Under process ( manuscript and code development )

---

## 🎓 Citation

Please cite this work if you use it:

```bibtex
@article{your2025crosslingualbias,
  title={Probing Cross-Lingual Bias Encoding in Transformer Models},
  author={Adil Rasheed},
  year={2025},
  note={Under process / manuscript in preparation}
}
```

---

## 📄 License

This project is released under the **MIT License** – see `LICENSE` for details.

---

## 🧠 Acknowledgements

This research builds upon foundational work in bias detection in word embeddings and contextualized models. Core inspiration and methods derive from the original WEAT methodology used to evaluate societal bias in embeddings. ([Ijeret][3])

```

---

If you’d like, I can also generate **GitHub badges (e.g., Python version, citation count, build status)** for the top of your README. Just ask!
::contentReference[oaicite:4]{index=4}
```

[1]: https://github.com/jehna/readme-best-practices?utm_source=chatgpt.com "GitHub - jehna/readme-best-practices: Best practices for writing a README for your open source project"
[2]: https://ucdavisdatalab.github.io/workshop_how-to-data-documentation/?utm_source=chatgpt.com "README,Write Me! Digital Project Organization and Documentation"
[3]: https://ijeret.org/index.php/ijeret/article/view/200?utm_source=chatgpt.com "Bias Detection in AI Models Using Word Embedding Association Tests (WEAT) | International Journal of Emerging Research in Engineering and Technology"
