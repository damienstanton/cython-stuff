### Experiments in Cython

#### Why?

The Python-C API is gross and requires a huge amount of hand-written C wrapper code. However, compiled C extensions are probably going to be very useful for the vehicle and robotics applications we are working on. Cython achieves this with 99% compatibility with Python syntax. For our cases, this fits much better than, say a DSL in Lua or cgo.

#### Setup

This script is built for Python 3.6 using `venv` and `pip`

```sh
./setup
```

#### Build

Each `pyx` module from the tutorial gets its own dir.

```sh
# from the root of the project
./build <dirname>
```


#### License

Copyright (c) 2017 by Damien Stanton. Distributed under the MIT license.
