# DNN Assignment 2

**Ganga Maheshwar Reddy Yeddula | 2026aj05054**

Chosen settings: **h=48, d=96, seeds 7/21/42**, FFN width 384, four main heads, four language-model layers and context 128. Adam starts at 0.001; HAR/adding use batch 128 and 8/12 epochs; language models use batch 32 and 600 steps. The even-ID ablation compares RNN clipping 1.0 versus none at T=200.

**VS Code:** extract this ZIP and open its root folder. With the existing local Python 3.10 installation, install requirements:

```bash
python3.10 -m pip install --user -r requirements.txt
```

Enable Microsoft's Python and Jupyter extensions. Open `problem1/problem1.ipynb`, select the installed Python 3.10 kernel, restart and **Run All**, then save. Repeat with `problem2/problem2.ipynb`.

**Google Colab:** use **File > Upload notebook** to open `problem1.ipynb`. Choose a GPU runtime if wanted, then **Run all**. Setup prompts for the **complete assignment ZIP** and extracts it automatically. Colab uses its installed Torch 2.x, NumPy, pandas and Matplotlib; setup installs missing packages. Do not install the local Python 3.10 pins into Colab.

After completion, **File > Download > Download .ipynb** saves the executed notebook. Then run `export_run_files()` in a new cell and upload that downloaded notebook when prompted. The helper downloads an updated ZIP containing its saved outputs. Open `problem2.ipynb` in Colab and supply this updated ZIP, preserving Problem 1's results across separate runtimes. Repeat the save/export steps after Problem 2.

Local runs resume completed records; Colab trains afresh by default. After code edits, set `REUSE_COMPLETED_RUNS=False` in setup cell 3. Tests follow implementations. Metrics use NumPy and avoid the SciPy import error. Internet is required for initial dataset downloads.

Outputs: `results.csv`, each problem's `figures/`, and three 500-character samples in `problem2/generated_samples.txt`. Each notebook saves elapsed time and reuse status in `figures/notebook_runtime.json`; cached replay is not full training time. Local training loops total 19.6 minutes; a measured T4 total remains pending. Update `report.pdf` if rerun measurements change. Exclude datasets, checkpoints and installed packages from submission.
