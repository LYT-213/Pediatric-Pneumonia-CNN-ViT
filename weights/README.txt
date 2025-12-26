This directory is intended to store the trained model weights (.pth files).

Due to GitHub's file size limits (100MB max), the pre-trained model weights (which range from 100MB to 400MB) are NOT included in this repository.

To reproduce the results:
1. Run the '01_train_model.ipynb' notebook.
2. The script is configured to automatically save the best-performing model weights into this directory.
3. Once trained, these weights can be used by the evaluation notebooks (02_evaluate_benchmark.ipynb, etc.).