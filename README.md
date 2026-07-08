# Column Transformer with Scikit-Learn

A focused, practical demonstration of scikit-learn's `ColumnTransformer` — applying different preprocessing steps to different columns of the same dataset in a single, reusable pipeline, and comparing that to doing it manually column-by-column.

**Tools:** Python, Pandas, NumPy, scikit-learn

---

## Dataset

`covid_toy.csv` — a small (100-row) toy dataset with a deliberate mix of column types that need different treatment: `age` (numeric, no missing values), `fever` (numeric, has missing values), `cough` (ordinal categorical: Mild/Strong), `gender` and `city` (nominal categorical), and `has_covid` (target).

## What's in the Notebook

1. **Manual preprocessing ("Aam Zindagi")** — imputing missing `fever` values with `SimpleImputer`, ordinal-encoding `cough`, one-hot-encoding `gender`/`city`, and manually `np.concatenate`-ing all the transformed arrays back together. This is the tedious, error-prone way most beginners start with.
2. **`ColumnTransformer` version ("Mentos Zindagi")** — the same three preprocessing steps, but declared once as a `ColumnTransformer` and applied with a single `.fit_transform()` / `.transform()` call. Same result, a fraction of the code, and it generalizes cleanly to a `Pipeline`.

The side-by-side structure is the point: it's not just a ColumnTransformer example, it's a demonstration of *why* ColumnTransformer exists — the manual version is on-screen right above it for direct comparison.

## Files

- `Column Transformer.ipynb` — the notebook
- `covid_toy.csv` — the dataset (renamed from `covid Data set.csv` to match the `pd.read_csv('covid_toy.csv')` call in the notebook, so it now runs top-to-bottom without edits)
- `requirements.txt`

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook "Column Transformer.ipynb"
```

## Contact

**Muhammad Ahmed Jawaid**
[LinkedIn](https://www.linkedin.com/in/m-ahmed-jawaid-416662253/) · ahmedjawaid513@outlook.com
