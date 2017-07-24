## teo-simox-models: Installation from Source Code

First install the dependencies:
- [Install CMake](https://github.com/roboticslab-uc3m/installation-guides/blob/develop/install-cmake.md)
- [Install OpenRAVE](https://github.com/roboticslab-uc3m/installation-guides/blob/develop/install-openrave.md)

Additionally, this project depends on YCM to download and build external packages. Although this process is intended to run automatically during the CMake configuration phase, you may still want to install YCM and said packages by yourself. In that respect, refer to [Install YCM](https://github.com/roboticslab-uc3m/installation-guides/blob/develop/install-ycm.md).

### Install the Models

Our software integrates the previous dependencies. Note that you will be prompted for your password upon using '''sudo''' a couple of times:

```bash
cd  # go home
mkdir -p repos; cd repos  # make $HOME/repos if it does not exist; then, enter it
git clone https://github.com/roboticslab-uc3m/teo-simox-models.git  # download teo-simox-models software from the repository
cd teo-simox-models; mkdir build; cd build
cmake ..
make -j3; sudo make install; cd  # go home
```

For CMake `find_package(TEO_SIMOX_MODELS REQUIRED)`, you may also be interested in adding the following to your `~/.bashrc` or `~/.profile`:
```bash
export TEO_SIMOX_MODELS_DIR=/path/to/teo-simox-models/build
```

For additional `teo-simox-models` options use ccmake instead of cmake.

