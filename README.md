# mctmanager-docs
Docs for MCTManager

https://braekpo1nt.github.io/mctmanager-docs/

# Contributing

## Dev Environment Setup

### Prerequisites:
- Python 3
- Knowledge of how markdown documents are made

### Python virtual environment
Create your python virtual environment with the following command (assuming your python installation is referred to by `python3` on your machine)

```
python3 -m venv venv
```

then activate the virtual environment with your respective operating system's script. For example:

**macOS:**
```
source ./venv/bin/activate
```

### Install required packages
Once inside the virtual environment, you can install the required packages with the following command:
```
pip install mkdocs-material
```

### Starting up the local site
Once inside the virtual environment with `mkdocs-material` installed, you can start up a local version of the site for editing purposes using the following command:
```
mkdocs serve
```

# Resources

I used the instructions from this video to start this up: https://www.youtube.com/watch?v=Q-YA_dA8C20
