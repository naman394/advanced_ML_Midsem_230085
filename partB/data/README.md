# Dataset Information for Part B

## Dataset Used: make_classification (scikit-learn synthetic dataset)

### How to Obtain
This dataset is generated programmatically using `sklearn.datasets.make_classification`. No manual download is required. The dataset is created at runtime inside the notebooks using:

```python
from sklearn.datasets import make_classification
X, y = make_classification(n_samples=1000, n_features=20, n_informative=15, 
                            n_redundant=5, random_state=42)
y = 2 * y - 1  # Convert labels to {-1, +1} for SVM
```

### How It Is Used
- **task_1_1.ipynb, task_1_2.ipynb, task_1_3.ipynb**: Only markdown cells, no dataset needed.
- **task_2_1.ipynb**: Dataset justification and preprocessing are documented.
- **task_2_2.ipynb**: Full DCD (Dual Coordinate Descent) implementation applied to this dataset.
- **task_2_3.ipynb**: Results, comparison plots, and reproducibility checklist.
- **task_3_1.ipynb**: Ablation experiments comparing full DCD vs. ablated components.
- **task_3_2.ipynb**: Failure mode analysis using a non-linearly-separable dataset.

### Dataset Properties
- **Samples**: 1000
- **Features**: 20 (15 informative, 5 redundant)
- **Classes**: 2 (binary: -1 or +1)
- **Labels**: Converted to {-1, +1} for linear SVM compatibility
- **No manual steps required**: All data is generated in-memory.
