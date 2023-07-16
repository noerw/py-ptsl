[![Lint and Test](https://github.com/iluvcapra/py-ptsl/actions/workflows/lint_and_pytest.yml/badge.svg)](https://github.com/iluvcapra/py-ptsl/actions/workflows/lint_and_pytest.yml)
[![codecov](https://codecov.io/gh/iluvcapra/py-ptsl/branch/master/graph/badge.svg?token=PR6SUQJISZ)](https://codecov.io/gh/iluvcapra/py-ptsl)
[![Documentation Status](https://readthedocs.org/projects/py-ptsl/badge/?version=latest)](https://py-ptsl.readthedocs.io/en/latest/?badge=latest)
![GitHub last commit](https://img.shields.io/github/last-commit/iluvcapra/py-ptsl)
[![Pro Tools Version - 2023.6](https://img.shields.io/static/v1?label=Pro+Tools+Version&message=2023.6&color=22228f)](https://github.com/iluvcapra/py-ptsl/blob/master/doc/source/ptsl_versions.rst)

# py-ptsl

Native Python PTSL (Pro Tools Scripting Library) RPC interface

## Important Notice! 

This software is developed by enthusiasts and is not a work of or supported by 
Avid. Developers who wish to contribute to this project should obtain the PTSL 
SDK [from Avid's Developer site](https://developer.avid.com) for the most 
current documentation and protobuf source files.

## Example

See the [examples directory](examples) for scripts demonstrating how to use the
client.

- [session_info.py](examples/session_info.py) - This example 
  prints a list of gettable properties from the currently-open
      session.
- [print_tracks.py](examples/print_tracks.py) - This example prints
  a list of every track in the currently-open session, including state
  information like selection, mute and solo state, track color and 
  track ID.


### Sending Commands To Pro Tools with the `Engine` class

The `Engine` class exposes `ptsl` commands with a method call interface.

```python
from ptsl import open_engine

with open_engine(company_name="MY_COMPANY", application_name="MY_TOOL") as engine:
    session_name = engine.session_name()

```

