# 5-Dimension Evaluation Scorecard

A template based on the framework in the paper (Section V). Use it to compare two or three tools on the **same database and the same question set**, for example:

- A direct prompt to a general-purpose LLM
- A specialized tool such as PandasAI or LIDA
- A fine-tuned smaller LLM

## Setup

| Item | Your entry |
|------|-----------|
| Database / dataset | |
| Number of questions | |
| Tools compared | |
| Date run | |

## Scoring (1 = poor, 5 = excellent)

| Dimension | What to check | Tool A | Tool B | Tool C |
|-----------|---------------|:------:|:------:|:------:|
| **Correctness** | Execution result matches the gold answer from a human analyst | | | |
| **Robustness** | Still correct after rephrasing the question or renaming columns | | | |
| **Efficiency** | Tokens used and run time per question | | | |
| **Interpretability** | A non-expert can read the generated SQL/Python and follow it | | | |
| **Trust and safety** | No invented columns or tables, sandboxed execution, resistant to prompt injection, data privacy handled | | | |
| **Total** | | | | |

## Per-question log

| # | Question | Tool | Correct? (Y/N) | Tokens | Seconds | Notes (hallucinated column, error, etc.) |
|---|----------|------|:--------------:|-------:|--------:|------------------------------------------|
| 1 | | | | | | |

## Tips

- Prefer **execution accuracy** (compare results) over string matching of queries.
- Rephrase each question at least once to test robustness.
- Never run generated SQL against production data; use a read-only copy.
