QUIC implementation for ns-3
================================

This repository was **forked** from the **[original](https://github.com/signetlabdei/quic)** from **[repo forked for 3.42](https://github.com/a-andre/quic)**, and **modified** to work with ns3.46.1.

## QUIC code base
This repository contains in the code for a native IETF QUIC implementation in ns-3.

The implementation is described in [this paper](https://arxiv.org/abs/1902.06121).

Please use this [issue tracker](https://github.com/signetlabdei/quic-ns-3/issues) for bugs/questions.

## Install

### Prerequisites ###

- Ubuntu 20.04
- ns3.46.1

#### Installing dependencies ####

- Download and install ns-3.46.1

```bash
wget https://www.nsnam.org/releases/ns-3.46.1.tar.bz2
tar -xf ns-3.46.1.tar.bz2
rm ns-3.46.1.tar.bz2
cd ns-3.46.1
```

- I think it works with the allinone version too.
- Reference: [ns-3.46 documentation](https://www.nsnam.org/docs/release/3.46/tutorial/html/quick-start.html)

#### Downloading #####

- Clone the quic module in the `contrib` directory

```bash
git clone https://github.com/sugawa197203/quic.git ./contrib/quic
```

## Configuration

```bash
./ns3 configure --enable-tests --enable-examples
```

- Make sure quic is listed under "Modules configured to be built:".
  - If it's not, something's wrong.

## Build

```bash
./ns3 build
```

## Test

- Testing is recommended.

```bash
./test.py
```

## It probably works in Python too

If you are not interested in using the Python bindings, use

```bash
./ns3 configure --enable-tests --enable-examples --disable-python
./ns3 build
```
