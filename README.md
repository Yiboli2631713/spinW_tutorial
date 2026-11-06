# spinW_tutorial
This is a tutorial for learning [spinW](https://github.com/SpinW/pySpinW)

The Binder environment is at [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/yanglonggroup/spinW_tutorial/HEAD)

## Run online with Binder

Click the Binder badge, wait for JupyterLab to open, and open a tutorial in `ipynb/`. Run its cells in order. The first import cell automatically starts a virtual display on headless Linux; the structure plots use `snapshot()` so the images appear inside the notebook.

`environment.yml` selects Python 3.12 and installs the Python packages, Xvfb, Qt support libraries, and Mesa software OpenGL from Conda/PyPI. It replaces the old requirements file; no separate runtime, apt, or startup files are needed.

## Installation on Linux

Install Conda or Miniforge, then run:

```bash
git clone https://github.com/yanglonggroup/spinW_tutorial.git
cd spinW_tutorial
conda env create -f environment.yml
conda activate spinw-tutorial
python -m pip check
jupyter lab
```

Open the four tutorials in `ipynb/` and use the Python kernel from this environment. Always run the first import cell before the visualization cells. On a Linux desktop with an existing display, the virtual-display setup is skipped.

The environment file contains Linux graphics packages for Binder. For a local Windows/macOS desktop, use Python 3.12 in a virtual environment and install `pyspinw==1.1.0b2`, `jupyterlab`, and `ipykernel` with pip instead; a working desktop Qt/OpenGL environment is required.

See the [pySpinW documentation](https://spinw.org/pyspinw/) for API details.
