# Python4RS
A repository containing setup instructions for using Python through VSCode for remote sensing applications.

## Step 1: Install Mamba (Fast Conda Alternative)
Why Mamba?
Mamba is a drop-in replacement for conda that is much faster at solving dependencies.

It supports Conda environments, channels, and YAML files.

Install Miniforge (Recommended with Mamba)
Miniforge comes with Mamba and uses the conda-forge channel by default.

Mac/Linux:
```
curl -L -O https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-MacOSX-arm64.sh  # or x86_64 for Intel
bash Miniforge3-MacOSX-arm64.sh
```
Windows:

Download and run installer: [Miniforge Installer](https://github.com/conda-forge/miniforge)
  - Ensure you check `Add to PATH` during installation to avoid future headaches!

## Step 2: Create a Clean Remote Sensing Environment

Open terminal (or Anaconda Prompt) and run:

```
mamba create -n rsenv python=3.11
conda activate rsenv
```
Then install remote sensing packages:
```
mamba install -c conda-forge \
    rasterio \
    geopandas \
    xarray \
    rioxarray \
    scikit-image \
    matplotlib \
    numpy \
    pandas \
    ipykernel \
    jupyterlab \
    dask \
    pyproj \
    h5py \
    spectral \
    scikit-learn
```

## Step 3: Install VSCode

1. Install VS Code: [VS Code](https://code.visualstudio.com/)
2. Inside VS Code, go to the Extensions tab and install:
   - Python (by Microsoft, not a third party)
   - Jupyter (if you use `.ipynb` files
3. Link to your environment:
   - Open Command Palette (Ctrl+Shift+P)
   - Type: Python: Select Interpreter
   - Choose the one that says: `rsenv` (should look like `Miniforge3\envs\rsenv\python.exe`)

## Step 4: Use Jupyter Notebooks in VS Code

Now you can:
- Open or create `.ipynb` files in VS Code
- Or launch `jupyter lab` from your terminal

```
jupyter lab
```
It will open a browser-based notebook interface.
