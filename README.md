cue-sdk-python
==============

[![PyPI license](https://img.shields.io/pypi/l/cuesdk.svg?style=for-the-badge)](https://pypi.org/project/cuesdk)
[![PyPI version info](https://img.shields.io/pypi/v/cuesdk.svg?style=for-the-badge)](https://pypi.org/project/cuesdk)
[![PyPI supported Python versions](https://img.shields.io/pypi/pyversions/cuesdk.svg?style=for-the-badge)](https://pypi.org/project/cuesdk)

# Intro

This repository is dedicated for a `cuesdk` package on [PyPI](https://pypi.org/)

`cuesdk` package is a `ctypes`-based CUE SDK binding for Python 3

# Prerequisites

- `cuesdk` works on Windows or MacOS platforms only.
- Python 3.5 or higher. Support for earlier versions of Python is not provided. Python 2.7 or lower is not supported.
- Windows:
  - Microsoft Visual C++ Redistributable for Visual Studio 2017.
    - x86 https://aka.ms/vs/15/release/VC_redist.x86.exe
    - x64 https://aka.ms/vs/15/release/VC_redist.x64.exe 
- MacOS:
  - SDK must be installed manually
    - Download latest dmg from https://github.com/CorsairOfficial/cue-sdk/releases/
    - Copy CUESDK.Framework into /Library/Frameworks/
  - example/fx.py won't work because it uses msvcrt for keypress handling. So sorry, but I don't care ;-)

# Installing

You can install the package with pip:

```sh
   $ python3 -m pip install -U git+https://github.com/thops/cue-sdk-python.git
```

# Usage

```python
from cuesdk import CueSdk

sdk = CueSdk()
sdk.connect()

print(sdk.protocol_details)

print(sdk.get_devices())

```

# Links

- API reference: https://github.com/corsairofficial/cue-sdk-python/blob/master/api_reference.md
- Code examples: https://github.com/corsairofficial/cue-sdk-python/tree/master/example
