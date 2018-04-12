# Preparing development environment

Before training deep learning models on your local or remote computer you should make sure you have the latest applicable prerequisites installed. This includes making sure the latest drivers and libraries for your NVIDIA GPU (if you have one). You should also ensure you have installed Python and Python libraries such as NumPy, SciPy, Python support for Visual Studio / Visual Studio Code, and appropriate deep learning frameworks such as Microsoft Cognitive Toolkit (CNTK), TensorFlow, Caffe2, MXNet, Keras, Theano, PyTorch and/or Chainer.

> [!NOTE]
>
> Software introduction in the following subsectons is excerpted from their homepages.

## NVIDIA GPU driver, CUDA and cuDNN

### NVIDIA GPU driver

Deep learning frameworks take advantage of NVIDIA GPU to let machines learn at a speed, accuracy, and scale towards true artificial intelligence. If your computer has NVIDIA GPU cards, please visit [here](http://www.nvidia.com/Download/index.aspx) or try OS update to install the latest driver.

### CUDA

[CUDA](https://developer.nvidia.com/cuda-zone) is a parallel computing platform and programming model invented by NVIDIA.
It enables dramatic increases in computing performance by harnessing the power of the GPU.
Currently, CUDA Toolkit 8.0 is required by deep learning frameworks.

To install CUDA

- Visit this [site](https://developer.nvidia.com/cuda-80-ga2-download-archive), download CUDA and install it.
- Make sure to install the CUDA runtime libraries, and then add CUDA binary path to the %PATH% or $PATH environment variable.
- On Windows, this path is "C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\bin" by default.

![install CUDA on Windows](./media/prepare-local-machine/install_cuda_win.png)

### cuDNN

[cuDNN](https://developer.nvidia.com/cudnn) (CUDA Deep Neural Network library) is a GPU-accelerated library of primitives for deep neural networks by NVIDIA. cuDNN v6 is required by latest deep learning frameworks.

To install cuDNN
- Visit [here](https://developer.nvidia.com/rdp/cudnn-download) to download and install the latest package.
- Ensure to add the directory containing cuDNN binary to the %PATH% or $PATH environment variable.
- On Windows, you can copy cudnn64_6.dll to "C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\bin".

> [!NOTE]
>
> Previous deep learning frameworks such as CNTK 2.0 and TensorFlow 1.2.1 need cuDNN v5.1.
> However, you can install multiple cuDNN versions together.


## Python

Python has been the primary programming language for deep learning applications.
**64-bit** Python distribution is required, and the latest [Python 3.5](https://www.python.org/downloads/release/python-354/) is recommended for the best compatibility.

Please add Python directory to the %PATH% or $PATH environment variable.
You also need to install **pip**, which is the package management system to install and manage software packages written in Python.
Deep learning frameworks rely on pip for their own installation.

> [!NOTE]
>
> 1. On Windows, it is preferred to install the Python launcher for yourself only.
> 2. If your Python distribution is installed in the system directory (e.g. the one shipped with Visual Studio 2017), administrative permission is required to install Python packages with pip.

![install Python on Windows](./media/prepare-local-machine/install_python_win.png)

Then, we verify whether Python is installed correctly, and upgrade pip to the latest version.
Suppose Python 3.5 is installed, please execute the following commands in a terminal:

- **Windows**
    ```cmd
    C:\>python -V
    Python 3.5.4

    C:\>pip3 -V
    pip 9.0.3 from c:\users\test\appdata\local\programs\python\python35\lib\site-packages (python 3.5)

    C:\>python -m pip install -U pip
    ```

- **macOS**
    ```bash
    MyMac:~ test$ python3 -V
    Python 3.5.4

    MyMac:~ test$ pip3 -V
    pip 9.0.3 from /Library/Frameworks/Python.framework/Versions/3.5/lib/python3.5/site-packages (python 3.5)

    MyMac:~ test$ python3 -m pip install -U pip
    ```

- **Linux**
    ```bash
    test@MyLinux:~$ python3 -V
    Python 3.5.4

    test@MyLinux:~$ pip3 -V
    pip 9.0.3 from /usr/local/lib/python3.5/dist-packages (python 3.5)

    test@MyLinux:~$ sudo python3 -m pip install -U pip
    ```

## Working with Python in Visual Studio on Windows

Visual Studio provides [open-source](https://github.com/Microsoft/ptvs) support for the Python language through the Python development and Data Science workloads (Visual Studio 2017) and the free Python Tools for Visual Studio extension (Visual Studio 2015 and earlier).
Learn more about [Working with Python in Visual Studio](https://docs.microsoft.com/en-us/visualstudio/python/python-in-visual-studio) for more details.

### Visual Studio 2017

When Visual Studio 2017 installation starts, please choose **Python development** workload for Python language support.

Note that a 64-bit Python 3.6 will also be installed automatically.
If you have installed Python 3.5, please refer to the following "Setting up the default Python environment" subsection.

![Working with Python in Visual Studio 2017](./media/prepare-local-machine/install_python_tools_vs2017.png)

### Visual Studio 2015

When Visual Studio 2015 installation starts, please choose **Custom** type, and then select **Python Tools for Visual Studio**.

![Working with Python in Visual Studio 2015](./media/prepare-local-machine/install_python_tools_vs2015.png)

### Setting up the default Python environment

Users need to setup the default Python environment in Visual Studio for AI projects if there are multiple ones.
E.g. Users install Python 3.5 manually, and Visual Studio 2017 Python development workload installs a 64-bit Python 3.6 automatically.
Or users create several Anaconda virtual Python environments.

To set the default Python environment globally for Visual Studio, please go to menu ***Tools > Python > Python Environments*** (Visual Studio 2017), or ***Tools > Python Tools > Python Environments*** (Visual Studio 2015).
Then, select e.g. **Python 3.5 (64 bit)** and click ***Make this the default environment for new projects*** button.

![Setting up the default Python environment](./media/prepare-local-machine/install_python_setup_default.png)

## Working with Python in Visual Studio Code

Python is fully supported in Visual Studio Code through extensions.
Please visit [here](https://code.visualstudio.com/docs/languages/python) for more details.


## Essential packages

### NumPy and SciPy

- **NumPy** is a general-purpose array-processing package designed to efficiently manipulate large multi-dimensional arrays of arbitrary records without sacrificing too much speed for small multi-dimensional arrays.

- **SciPy** (pronounced "Sigh Pie") is open-source software for mathematics, science, and engineering, depending on NumPy.
Starting from version 1.0.0, SciPy now has official prebuilt wheel package for Windows.

To install NumPy and SciPy, run the following command in a terminal:
```bash
pip3 install -U numpy scipy
```

> [!NOTE]
>
> The above command will upgrade existing old or unofficial (e.g. third party packages from http://www.lfd.uci.edu/~gohlke/pythonlibs/ for Windows) NumPy and SciPy to the latest official ones.

### Jupyter Notebook

[Jupyter Notebook](http://jupyter.org/) is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations and narrative text.

To install Jupyter Notebook, run the following command in a terminal:
```bash
pip3 install jupyter nbconvert
```

### Pandas

[Pandas](https://pandas.pydata.org/) is an open source, BSD-licensed library providing high-performance, easy-to-use data structures and data analysis tools for the Python programming language.

To install Pandas, run the following command in a terminal:
```bash
pip3 install pandas
```

### Matplotlib

[Matplotlib](https://matplotlib.org/) is a Python 2D plotting library which produces publication quality figures in a variety of hardcopy formats and interactive environments across platforms.

To install Matplotlib, run the following command in a terminal:
```bash
pip3 install matplotlib
```


## Deep learning and machine learning frameworks

### Microsoft Cognitive Toolkit (CNTK)

The [Microsoft Cognitive Toolkit](https://cntk.ai) is a unified deep-learning toolkit that describes neural networks as a series of computational steps via a directed graph. CNTK supports both Python and BrainScript programming languages.

To install CNTK Python package, see [how to install CNTK](https://docs.microsoft.com/en-us/cognitive-toolkit/Setup-CNTK-on-your-machine) for details.

> [!NOTE]
>
> - CNTK currently does not support macOS.
> - CNTK GPU-1bit-SGD version is licensed under a specific [1bit-SGD License](https://docs.microsoft.com/en-us/cognitive-toolkit/cntk-1bit-sgd-license) which is MORE restrictive, than the major CNTK License.

Briefly, to install CNTK Python package, run the following command in a terminal:
- **Windows**
    - With GPU
        ```cmd
        pip3 install https://cntk.ai/PythonWheel/GPU/cntk-2.3.1-cp35-cp35m-win_amd64.whl
        ```
    - Without GPU
        ```cmd
        pip3 install https://cntk.ai/PythonWheel/CPU-Only/cntk-2.3.1-cp35-cp35m-win_amd64.whl
        ```
- **Linux**
    - With GPU
        ```bash
        pip3 install https://cntk.ai/PythonWheel/GPU/cntk-2.3.1-cp35-cp35m-linux_x86_64.whl
        ```
    - Without GPU
        ```bash
        pip3 install https://cntk.ai/PythonWheel/CPU-Only/cntk-2.3.1-cp35-cp35m-linux_x86_64.whl
        ```

To install CNTK BrainScript package, run the following command in a terminal:
- Visit [here](https://github.com/Microsoft/CNTK/releases/tag/v2.3.1) to download the CPU-only or GPU package.

- **Windows**
    - Decompress the zip file to "%AppData%\Roaming\Microsoft\ToolsForAI\RuntimeSDK". Please create this folder if it does not exist.
    - Add "%AppData%\Roaming\Microsoft\ToolsForAI\RuntimeSDK\cntk\cntk" to the %PATH% environment variable.
    - Install Microsoft MPI from "%AppData%\Roaming\Microsoft\ToolsForAI\RuntimeSDK\cntk\prerequisites\MSMpiSetup.exe", which is required by CNTK.
    - Install Microsoft Visual C++ 2015 Redistributable from "%AppData%\Roaming\Microsoft\ToolsForAI\RuntimeSDK\cntk\prerequisites\VS2015\vc_redist.x64.exe" if it is not installed yet.

- **Linux**
    - Decompress the zip file to your home directory "~/".
    - Add "~/cntk/cntk/bin" to the $PATH environment variable.
    - Install OpenMPI by running the following command in a terminal:
        ```bash
        sudo apt-get install libopenmpi-dev
        ```

### TensorFlow

[TensorFlow](https://www.tensorflow.org/) is an open source software library for numerical computation using data flow graphs.
Please refer to [here](https://www.tensorflow.org/install/) for detailed installation.

To install TensorFlow, run the following command in a terminal:
- With GPU
    ```bash
    pip3 install tensorflow-gpu==1.4.0
    ```
- Without GPU
    ```bash
    pip3 install tensorflow==1.4.0
    ```

### PyTorch

[PyTorch](http://pytorch.org/) is a python package that provides two high-level features:
- Tensor computation (like numpy) with strong GPU acceleration
- Deep Neural Networks built on a tape-based autograd system

To install PyTorch, please run the following command in a terminal:

- **Windows**
    - There is no official wheel package yet. You could download a third-party Anaconda PyTorch package from [here](https://anaconda.org/peterjc123/pytorch/files). Please choose an appropriate file.
    - Decompress it to, e.g. your home directory, "C:\Users\test\pytorch".
    - Add "C:\Users\test\pytorch\Lib\site-packages" to the %PYTHONPATH% environment variable.
    - Or, copy the contents in "C:\Users\test\pytorch\Lib\site-packages" to your Python distribution's "Lib\site-packages" subdirectory.

- **macOS**
    ```bash
    - Python 3.5
        pip3 install http://download.pytorch.org/whl/torch-0.3.0.post4-cp35-cp35m-macosx_10_6_x86_64.whl
    - Python 3.6
        pip3 install http://download.pytorch.org/whl/torch-0.3.0.post4-cp36-cp36m-macosx_10_7_x86_64.whl
    ```
    > [!NOTE]
	>
    > macOS binaries don't support CUDA, install from source if CUDA is needed

- **Linux**
    ```bash
    - Python 3.5
        pip3 install http://download.pytorch.org/whl/cu80/torch-0.3.0.post4-cp35-cp35m-linux_x86_64.whl
    - Python 3.6
        pip3 install http://download.pytorch.org/whl/cu80/torch-0.3.0.post4-cp36-cp36m-linux_x86_64.whl
    ```
    > [!NOTE]
	>
    > This single package supports both GPU and CPU.

Finally, install torchvision on non-Windows:
```bash
pip3 install torchvision
```

### Caffe2

[Caffe2](https://caffe2.ai/) is a lightweight, modular, and scalable deep learning framework.
Building on the original Caffe, Caffe2 is designed with expression, speed, and modularity in mind.

Currently, there's no official prebuilt Caffe2 python wheel package available.
Please visit [here](https://caffe2.ai/docs/getting-started.html) to build from source code.

> [!NOTE]
> [here](https://github.com/Microsoft/samples-for-ai/tree/master/installer) has a third-party Caffe2 0.8.1 Windows wheel package (supports both GPU and CPU).

### MXNet

[Apache MXNet (incubating)](https://mxnet.incubator.apache.org/) is a deep learning framework designed for both efficiency and flexibility.
It allows you to **mix** [symbolic and imperative programming](http://mxnet.io/architecture/index.html#deep-learning-system-design-concepts) to maximize efficiency and productivity.

To install MXNet, run the following command in a terminal:
- With GPU
    ```bash
    pip3 install mxnet-cu80==1.0.0
    ```
- Without GPU
    ```bash
    pip3 install mxnet==1.0.0
    ```

### Keras

[Keras](https://keras.io/) is a high-level neural networks API, written in Python and capable of running on top of CNTK, TensorFlow or Theano. It was developed with a focus on enabling fast experimentation. Being able to go from idea to result with the least possible delay is key to doing good research.

To install Keras, please run the following command in a terminal:
```bash
pip3 install Keras==2.1.2
```

### Theano

[Theano](http://deeplearning.net/software/theano/) is a Python library that allows you to define, optimize, and evaluate mathematical expressions involving multi-dimensional arrays efficiently.

To install Theano, please run the following command in a terminal:
```bash
pip3 install Theano==1.0.1
```

### Chainer

[Chainer](https://chainer.org/) is a Python-based deep learning framework aiming at flexibility.
It provides automatic differentiation APIs based on the **define-by-run approach** (a.k.a. dynamic computational graphs) as well as object-oriented high-level APIs to build and train neural networks.

To enable CUDA support, install [CuPy](https://github.com/cupy/cupy):
```bash
pip3 install cupy==2.2.0
```

> [!NOTE]
>
> On Windows, you need **2015** version of [Microsoft Visual Studio](https://www.visualstudio.com/)
or [Microsoft Visual C++ Build Tools](http://landinghub.visualstudio.com/visual-cpp-build-tools)
to compile CuPy with CUDA 8.0.
First, open a **VS2015 x64 Native Tools Command Prompt** or **Visual C++ 2015 x64 Native Tools Command Prompt**, and then execute the above cupy installation command.

To install Chainer, please run the following command in a terminal:
```bash
pip3 install chainer==3.2.0
```

To enable multi-node distributed deep learning, please install
[ChainerMN](https://github.com/chainer/chainermn) in a terminal:
```bash
pip3 install chainermn
```

### scikit-learn

[scikit-learn](scikit-learn.org) is a Python module for machine learning built on top of SciPy and distributed under the 3-Clause BSD license.

To install scikit-learn, please run the following command in a terminal:
```bash
pip3 install scikit-learn
```


## [Using a one-click installer to setup deep learning frameworks](https://github.com/Microsoft/samples-for-ai/#using-a-one-click-installer-to-setup-deep-learning-frameworks)
