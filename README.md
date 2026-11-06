# spinW_tutorial
This is a tutorial for learning [spinW](https://github.com/SpinW/pySpinW)

The Binder environment is at [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/yanglonggroup/spinW_tutorial/HEAD)

## Installation

Use Python 3.12 for these tutorials. pySpinW 1.1.0b2 requires Python 3.11 or newer, below 3.15. The instructions below install pySpinW and JupyterLab in a separate environment.

### 1. Download the tutorials and create an environment

```bash
git clone https://github.com/yanglonggroup/spinW_tutorial.git
cd spinW_tutorial
python -m venv .venv
```

On macOS/Linux, use `python3 -m venv .venv` if the `python` command is unavailable. Make sure the selected interpreter is Python 3.12.

Activate the environment in Windows Command Prompt:

```bat
.venv\Scripts\activate.bat
```

Or in macOS/Linux:

```bash
source .venv/bin/activate
```

### 2. Install pySpinW and notebook dependencies

Run these commands from the repository directory after activating the environment:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m pip check
```

The `requirements.txt` file includes pySpinW, its scientific Python and Qt/OpenGL dependencies, and the Jupyter tools used to run the notebooks.

### 3. Check the installation and open the notebooks

```bash
python -c "from pyspinw import *; print('pySpinW import successful')"
jupyter lab
```

In JupyterLab, open the `ipynb/` folder and choose Tutorial 1, 2, 3, or 4. Use the Python kernel from the activated environment and run the cells in order.

The interactive `view()` calls require a desktop display with Qt/OpenGL support. On Linux, install the system libraries listed in the [Qt xcb requirements](https://doc.qt.io/qt-6/linux-requirements.html) if they are missing. For remote or headless use, pySpinW also provides `snapshot()`; Qt/OpenGL and a suitable display backend are still required.

See the [pySpinW documentation](https://spinw.org/pyspinw/) for API details.
