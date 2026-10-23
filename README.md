# Evaluating LLMs for Automated Exploratory Data Analysis and Natural Language Data Querying

**Author:** Sidharth Malik, Department of Computer Applications, Chandigarh University
**Type:** Survey / review paper with a proposed evaluation framework
**Year:** 2026

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

📄 **[Read the paper (PDF)](paper/LLM_EDA_TextToSQL_Evaluation_Malik.pdf)**

---

## Abstract

Large language models (LLMs) are increasingly used as an accessibility layer between analysts and structured data, turning natural language questions into SQL, Python, or charts. This paper compares LLM-based systems for two related but distinct tasks: **automated exploratory data analysis (EDA)** and **natural language querying (Text-to-SQL)**. It reviews benchmarks (Spider, Spider 2.0, BIRD) and systems (LIDA, PandasAI, DAIL-SQL, SENSE and others), proposes a **5-dimension comparison framework**, and examines the "performance cliff" when moving from clean academic schemas to messy enterprise databases. The paper argues that, in the near term, LLMs should be treated as **copilots for human or symbolic analysis**, not standalone analysts.

## Research questions

| # | Question | Section |
|---|----------|---------|
| RQ1 | How does query-translation accuracy change as database size and complexity grow? | VI |
| RQ2 | How capable are systems at open-ended automated EDA? | VI |
| RQ3 | What are the major benchmarks and metrics, and their limits? | IV |
| RQ4 | What are the practical limitations and risks? | VII |

## Key takeaways

- **Performance cliff:** GPT-4o scores about 86.6% on Spider 1.0 but only about 10.1% on the enterprise-scale Spider 2.0.
- **Benchmark reliability:** a 2026 re-annotation study found high annotation error rates in BIRD and Spider 2.0-Snow, enough to shuffle model rankings.
- **Smaller models compete:** distilled open models (e.g. SENSE-7B/13B) come close to prompted GPT-4 on Spider at far lower cost.
- **EDA is under-evaluated:** automated EDA systems mostly rely on LLM-as-judge scoring and lack realistic benchmarks.
- **Recommended use:** copilot with human or symbolic verification.

## The 5-dimension evaluation framework

1. **Correctness** – does it match what a human analyst would return?
2. **Robustness** – is it stable under rephrasing and messy column names?
3. **Efficiency** – tokens and latency per query.
4. **Interpretability** – can a person audit the generated code?
5. **Trustworthiness and safety** – hallucinated schema, sandboxed execution, prompt injection, data privacy.

A ready-to-use scorecard is in [`framework/evaluation-scorecard.md`](framework/evaluation-scorecard.md) for anyone who wants to compare two or three tools on their own database.

## Repository structure

```
.
├── README.md
├── CITATION.cff
├── LICENSE
├── .gitignore
├── paper/                  # the paper (PDF)
├── framework/              # 5-dimension scorecard template
└── references/             # reference list with links
```

## How to cite

```bibtex
@misc{malik2026llmeda,
  author       = {Malik, Sidharth},
  title        = {Evaluating Large Language Models for Automated Exploratory Data Analysis and Natural Language-Based Data Querying},
  year         = {2026},
  howpublished = {GitHub repository},
  url          = {https://github.com/YOUR-USERNAME/llm-eda-text-to-sql-evaluation}
}
```

GitHub also shows a **Cite this repository** button, generated from [`CITATION.cff`](CITATION.cff).

## License

The paper and documentation are released under [CC BY 4.0](LICENSE). You may share and adapt with attribution.

## Contact

Sidharth Malik · [LinkedIn](https://www.linkedin.com/in/sidharth-malik-66ba83291/) · sidharthmalik000@gmail.com
