# [NOVA: AI-Enhanced Semantic Feature Norms for 786 Concepts](https://onlinelibrary.wiley.com/doi/pdf/10.1111/tops.70037)

Data from the paper on generating and verifying semantic feature norms using LLMs.

## Data

The verified concept-feature matrix (combining human and LLM judgments) is available in two formats:

- `verified_matrix_cogsci2025.parquet` — Apache Parquet format
- `verified_matrix_cogsci2025.csv` — CSV format

### Format

- **Rows (index):** 787 concepts (e.g., "accordion", "airplane", "almond")
- **Columns:** 8,202 semantic features (e.g., "CAN BE SWEET", "HAS ANTENNAE")
- **Values:** Binary (0 or 1), indicating whether a feature applies to a given concept
- **Index column name:** `stimulus`

### Loading the data

```python
import pandas as pd

# Parquet
df = pd.read_parquet("verified_matrix_cogsci2025.parquet")

# CSV
df = pd.read_csv("verified_matrix_cogsci2025.csv", index_col=0)

print(df.shape)  # (787, 8202)
```

## Contact

For any queries, reach out to [siddharth.suresh@wisc.edu](mailto:siddharth.suresh@wisc.edu) or [sidd.suresh97@gmail.com](mailto:sidd.suresh97@gmail.com).
