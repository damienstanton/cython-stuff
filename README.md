### Experiments in Cython

#### Why?

The Python-C API is gross and requires a huge amount of hand-written C wrapper code. However, compiled C extensions are probably going to be very useful for the vehicle and robotics applications we are working on. Cython achieves this with 99% compatibility with Python syntax. For our cases, this fits much better than, say a DSL in Lua or building something in  cgo. One clear tradeoff here is size: anything that needs to be small and performant should probably just be written in Go.

#### Setup

This script is built for Python 3.6 using `venv` and `pip`

```sh
./setup
```

#### Newdir

Since distutils is required for each new module, this little script autmatically generates the right `setup.py` file for you

```sh
./newdir <dirname>
```

#### Build

Each `pyx` module from the tutorial gets its own dir.

```sh
./build <dirname>
```


#### License

Copyright (c) 2017 by Damien Stanton. Distributed under the MIT license.
