# ATR ENDSEM — Hindi Retrieval Experiment Paper Package

## Research scope
A comparison of BM25 and `intfloat/multilingual-e5-small` on `carlfeynman/Bharat_NanoSCIDOCS_hi`. The experiment is Hindi-query-to-Hindi-document retrieval, not Hindi-to-English cross-lingual retrieval.

## Key results
| Metric | BM25 | Dense E5-small |
|---|---:|---:|
| Recall@5 | 0.1397 | 0.1667 |
| Recall@10 | 0.2007 | 0.2167 |
| MRR@10 | 0.3689 | 0.4682 |

These are observed macro-averages across 50 queries. The post-hoc paired tests and bootstrap intervals do not establish a statistically reliable difference at the 0.05 level.

## Contents of this ZIP
- `paper/main.tex`: editable LaTeX manuscript, with the humanized wording incorporated while retaining the paper's sections, equations, tables, figures and references.
- `paper/final_paper.pdf`: compiled 7-page paper.
- `paper/final_paper.docx`: editable Word version.
- `paper/references.bib`: bibliography source.
- `paper/figures/`: the three figures referenced by the manuscript.
- `docs/prompt_completion_register.md`: conservative status register for the 18 prompts.
- `SUBMISSION_CHECKLIST.md`: remaining checks before submission.

## Experiment files included
- `notebooks/ATR_ENDSEM_original_executed.ipynb`: the user-supplied executed Colab notebook, preserved unchanged. Its qualitative relevance labels may require correction; do not interpret an unlisted qrels item as verified irrelevant.
- `results/bm25_query_results.csv`: 50 BM25 query-level metric records.
- `results/dense_query_results.csv`: 50 dense query-level metric records.
- `results/retrieval_comparison.csv`: 50 paired query-level metric records.
- `results/error_analysis.csv`: 50 query-level top-1 comparison records. Five dense-document snippets are blank in the source and have not been filled.
- `requirements_recorded.txt`: recorded versions from the original experiment, for documentation only. These are not a validated clean-environment lockfile.

The original executed notebook and all four CSVs were added without modifying their contents. The notebook has not been independently rerun in a clean environment. The paper's post-hoc statistical tests are described in the manuscript; no separate statistics output file was provided in this upload.

## Before submission
1. Open `paper/final_paper.pdf` and check that the layout is accepted by your instructor.
2. Read the paper and confirm that you can explain the methods, metrics, results, statistical analysis and limitations.
3. Review the supplied executed notebook and result CSV files; verify that they match the experiment you intend to submit.
4. Complete the AI-provenance documentation if required by your course.
5. Upload the folder to the required GitHub repository and verify the uploaded files.
