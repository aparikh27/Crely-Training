# Copilot instructions for this repo

Purpose: Give AI coding agents a concise, actionable onboarding for the Crely-Training workspace.

- **Big picture:** This repository is notebook-first training material for physiological signal processing (ECG). Primary artifacts are exploratory notebooks and light Python tooling. See the project overview in [README.md](README.md#L1-L20).

- **Key locations:**
  - Notebooks and working files: [01_data_exploration.ipynb](01_data_exploration.ipynb#L10-L32) (example selection shown).
  - Project README: [README.md](README.md#L1-L20)
  - NOTE: The workspace root is a Python virtual environment (`venv`) — search the workspace root and the `venv` directory for notebooks and scripts.

- **Architecture & intent:**
  - This is not a packaged Python project; it is a collection of experiments that load PhysioNet ECG datasets (MIT-BIH, PTB-XL) via WFDB and process signals using NeuroKit2/Matplotlib.
  - Data flow typically: WFDB -> NumPy/Pandas arrays -> NeuroKit2 processing -> Matplotlib figures in notebooks.

- **Common libraries / integrations to watch for:**
  - `wfdb` — reading PhysioNet record files (used in notebooks).
  - `neurokit2` — signal processing helper functions.
  - `matplotlib` — plotting outputs.
  - External data sources: PhysioNet datasets (download or WFDB remote access).

- **How to run / local dev (Windows PowerShell):**
  - Activate the workspace virtualenv (if the workspace is the `venv` folder):

    `.\Scripts\Activate.ps1`

  - Install dependencies (no `requirements.txt` detected; install the primary libs used in README):

    `pip install wfdb neurokit2 matplotlib`

  - Quick check: notebooks can be opened in VS Code/Jupyter — run cells to reproduce plots. The last recorded terminal command in this workspace was `pip install wfdb`.

- **Patterns & conventions (discoverable):**
  - Exploration happens inside notebooks — expect signal-loading and plotting routines to be inline. Extract reusable code into `src/` or `utils/` when adding modules.
  - No tests or CI detected; changes that add scripts should include a short runnable example cell in a notebook or a small `if __name__ == '__main__'` runner.

- **Agent actions that are high-value and safe to attempt:**
  - Extract signal-loading cells from notebooks into a small module (example target: `src/io.py`) and add a short notebook cell demonstrating usage.
  - Add a `requirements.txt` capturing installed libs after reproducing the environment.
  - Search notebooks for direct `wfdb` usage and standardize a helper function for record reading.

- **Where to look first:**
  - [README.md](README.md#L1-L20) for stack overview.
  - [01_data_exploration.ipynb](01_data_exploration.ipynb#L10-L32) for concrete examples of data-loading and processing.

If anything above is unclear or you want me to prioritize a specific refactor (e.g., extract I/O utilities, add `requirements.txt`, or convert a notebook to a script), tell me which and I'll proceed.
