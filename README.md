# RL4System

## Environment
My operation system is Ubuntu 22.04LTS
```shell
sudo apt install swig
sudo apt install gcc
sudo apt install g++
```

Python environment,  python version == 3.10
```shell
pip install gym[all]
```
  
  Apart from that, when I try to run some foundamental code using gym, some bugs occured. The error log is below:
  ```shell
  libGL error: MESA-LOADER: failed to open iris: /usr/lib/dri/iris_dri.so: cannot open shared object file: No such file or directory (search paths /usr/lib/x86_64-linux-gnu/dri:\$${ORIGIN}/dri:/usr/lib/dri, suffix _dri)
libGL error: failed to load driver: iris
libGL error: MESA-LOADER: failed to open swrast: /usr/lib/dri/swrast_dri.so: cannot open shared object file: No such file or directory (search paths /usr/lib/x86_64-linux-gnu/dri:\$${ORIGIN}/dri:/usr/lib/dri, suffix _dri)
libGL error: failed to load driver: swrast
X Error of failed request:  BadValue (integer parameter out of range for operation)
  Major opcode of failed request:  149 (GLX)
  Minor opcode of failed request:  3 (X_GLXCreateContext)
  Value in failed request:  0x0
  Serial number of failed request:  105
  Current serial number in output stream:  106
  ```
  Fortunately, I use the code below to solve this problem.
  ```shell
  conda install -c conda-forge libstdcxx-ng
  ```
  Then it works.