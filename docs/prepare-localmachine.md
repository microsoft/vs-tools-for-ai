# Preparing development environment

Before training deep learning models on your local or remote computer you should make sure you have the latest applicable prerequisites installed. This includes making sure the latest drivers and libraries for your NVIDIA GPU (if you have one). You should also ensure you have installed Python and Python libraries such as NumPy, SciPy, Python support for Visual Studio / Visual Studio Code, and appropriate deep learning frameworks such as Microsoft Cognitive Toolkit (CNTK), TensorFlow, PyTorch, Caffe2, MXNet, Keras, Theano and/or Chainer.

> [!NOTE]
>
> Software introduction in the following subsectons is excerpted from their homepages.

## NVIDIA GPU driver, CUDA and cuDNN

### NVIDIA GPU driver

Deep learning frameworks take advantage of NVIDIA GPU to let machines learn at a speed, accuracy, and scale towards true artificial intelligence. If your computer has NVIDIA GPU cards, please visit [here](http://www.nvidia.com/Download/index.aspx) or try OS update to install the latest driver.

### CUDA

[CUDA](https://developer.nvidia.com/cuda-zone) is a parallel computing platform and programming model invented by NVIDIA.
It enables dramatic increases in computing performance by harnessing the power of the GPU.
Currently, CUDA Toolkit **9.0** is required by latest version of deep learning frameworks.

To install CUDA

- Visit this [site](https://developer.nvidia.com/cuda-90-download-archive), download CUDA and install it.
- Make sure to install the CUDA runtime libraries, and then add CUDA binary path to the %PATH% or $PATH environment variable.
- On Windows, this path is "C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0\bin" by default.

![install CUDA on Windows](./media/prepare-local-machine/install_cuda90_win.png)

### cuDNN

[cuDNN](https://developer.nvidia.com/cudnn) (CUDA Deep Neural Network library) is a GPU-accelerated library of primitives for deep neural networks by NVIDIA. cuDNN v6 is required by latest deep learning frameworks.

To install cuDNN
- Visit [here](https://developer.nvidia.com/rdp/cudnn-archive) to download and install v7.0.5 for CUDA 9.0 package.
- Ensure to add the directory containing cuDNN binary to the %PATH% or $PATH environment variable.
- On Windows, you can copy cudnn64_7.dll to "C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0\bin".


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
Suppose Python 3.5 is installed, please run the following commands in a terminal:

- **Windows**
    ```cmd
    C:\>python -V
    Python 3.5.4

    C:\>pip3 -V
    pip 10.0.1 from c:\users\test\appdata\local\programs\python\python35\lib\site-packages (python 3.5)

    C:\>python -m pip install -U pip
    ```

- **macOS**
    ```bash
    MyMac:~ test$ python3 -V
    Python 3.5.4

    MyMac:~ test$ pip3 -V
    pip 10.0.1 from /Library/Frameworks/Python.framework/Versions/3.5/lib/python3.5/site-packages (python 3.5)

    MyMac:~ test$ python3 -m pip install -U pip
    ```

- **Linux**
    ```bash
    test@MyLinux:~$ python3 -V
    Python 3.5.4

    test@MyLinux:~$ pip3 -V
    pip 10.0.1 from /usr/local/lib/python3.5/dist-packages (python 3.5)

    test@MyLinux:~$ sudo python3 -m pip install -U pip
    ```

## Working with Python in Visual Studio on Windows

[Visual Studio](https://www.visualstudio.com/vs/) is a fully-featured IDE with unparalleled productivity for any dev, any app, and any platform.

Visual Studio provides [open-source](https://github.com/Microsoft/ptvs) support for the Python language through the Python development and Data Science workloads (Visual Studio 2017) and the free Python Tools for Visual Studio extension (Visual Studio 2015 and earlier).
Learn more about [Working with Python in Visual Studio](https://docs.microsoft.com/en-us/visualstudio/python/python-in-visual-studio) for more details.

### Visual Studio 2017

If you are students, open-source or individual developers, you can download a free copy of [Visual Studio Community 2017](https://www.visualstudio.com/vs/community/).

When Visual Studio 2017 installer starts, please choose **Python development** and **.NET desktop development** workloads for Python language and .NET support.
If you want to scale out deep learning model training and/or inferencing to the Microsoft Azure such as [Azure Machine Learning](https://azure.microsoft.com/en-us/overview/machine-learning/) or [Azure Batch AI](https://azure.microsoft.com/en-us/services/batch-ai/),
please also choose **Azure development** workload.

Note that a 64-bit Python 3.6 will also be installed by default with Visual Studio 2017.
If you have installed Python 3.5, please refer to the following "Setting up the default Python environment" subsection.

![Working with Python in Visual Studio 2017](./media/prepare-local-machine/install_python_tools_vs2017.png)

### Visual Studio 2015

When Visual Studio 2015 installer starts, please choose **Custom** type, and then select **Python Tools for Visual Studio**.
If you want to scale out deep learning model training and/or inferencing to the Microsoft Azure such as [Azure Machine Learning](https://azure.microsoft.com/en-us/overview/machine-learning/) or [Azure Batch AI](https://azure.microsoft.com/en-us/services/batch-ai/),
please install [Azure SDK](https://go.microsoft.com/fwlink/?LinkId=518003&clcid=0x409).

![Working with Python in Visual Studio 2015](./media/prepare-local-machine/install_python_tools_vs2015.png)

### Setting up the default Python environment

Users need to setup the default Python environment in Visual Studio for AI projects if there are multiple ones.
E.g. Users install Python 3.5 manually, and Visual Studio 2017 Python development workload installs a 64-bit Python 3.6 automatically.
Or users create several Anaconda virtual Python environments.

To set the default Python environment globally for Visual Studio, please go to menu **Tools > Python > Python Environments** (Visual Studio 2017), or **Tools > Python Tools > Python Environments** (Visual Studio 2015).
Then, select e.g. **Python 3.5 (64 bit)** and click ***Make this the default environment for new projects*** button.

![Setting up the default Python environment](./media/prepare-local-machine/install_python_setup_default.png)

## Working with Python in Visual Studio Code

Python is fully supported in Visual Studio Code through extensions.
Please visit [here](https://code.visualstudio.com/docs/languages/python) for more details.


## One-click installer

Setting up deep learning and machine learning software as well as their dependencies is not an easy task.
We recommend that you use the [one-click installer](https://github.com/Microsoft/samples-for-ai/#using-a-one-click-installer-to-setup-deep-learning-frameworks)
) to install them automatically across Windows, macOS and Linux.


## Essential packages

### NumPy and SciPy

- **NumPy** is a general-purpose array-processing package designed to efficiently manipulate large multi-dimensional arrays of arbitrary records without sacrificing too much speed for small multi-dimensional arrays.

- **SciPy** (pronounced "Sigh Pie") is open-source software for mathematics, science, and engineering, depending on NumPy.
Starting from version 1.0.0, SciPy now has official prebuilt wheel package for Windows.

To install NumPy and SciPy, run the following command in a terminal:
```bash
pip3 install numpy==1.14.2 scipy==1.0.1
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

The [Microsoft Cognitive Toolkit](https://cntk.ai) is a unified deep learning toolkit that describes neural networks as a series of computational steps via a directed graph. CNTK supports both Python and BrainScript programming languages.

To install CNTK Python package, see [how to install CNTK](https://docs.microsoft.com/en-us/cognitive-toolkit/Setup-CNTK-on-your-machine) for details.

> [!NOTE]
>
> - CNTK currently does not support macOS.
> - CNTK GPU-1bit-SGD version is licensed under a specific [1bit-SGD License](https://docs.microsoft.com/en-us/cognitive-toolkit/cntk-1bit-sgd-license) which is MORE restrictive, than the major CNTK License.

Briefly, to install CNTK Python package, run the following command in a terminal:
- With GPU
    ```bash
    pip3 install cntk-gpu==2.5.1
    ```
- Without GPU
    ```bash
    pip3 install cntk==2.5.1
    ```

> [!NOTE]
>
> We advise that you do not have both cntk and cntk-gpu packages installed simultaneously.


To install CNTK BrainScript package, run the following command in a terminal:
- Visit [here](https://github.com/Microsoft/CNTK/releases/tag/v2.5.1) to download the CPU-only or GPU package.

- **Windows**
    - Decompress the zip file to "%AppData%\Roaming\Microsoft\ToolsForAI\RuntimeSDK". Please create this folder if it does not exist.
    - Add "%AppData%\Roaming\Microsoft\ToolsForAI\RuntimeSDK\cntk\cntk" to the %PATH% environment variable.
    - Install Microsoft MPI from "%AppData%\Roaming\Microsoft\ToolsForAI\RuntimeSDK\cntk\prerequisites\MSMpiSetup.exe", which is required by CNTK.
    - Install Microsoft Visual C++ 2015 Redistributable from "%AppData%\Roaming\Microsoft\ToolsForAI\RuntimeSDK\cntk\prerequisites\VS2015\vc_redist.x64.exe" if it is not installed yet.

- **Linux**
    - Decompress the zip file to your home directory "~/.toolsforai".
    - Add "~/.toolsforai/cntk/cntk/bin" to the $PATH environment variable.
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
    pip3 install tensorflow-gpu==1.5.0
    ```
- Without GPU
    ```bash
    pip3 install tensorflow==1.5.0
    ```

### PyTorch

[PyTorch](http://pytorch.org/) is a python package that provides two high-level features:
- Tensor computation (like numpy) with strong GPU acceleration
- Deep Neural Networks built on a tape-based autograd system

To install PyTorch, please run the following command in a terminal:

- **Windows**
    - With GPU
        ```bash
        - Python 3.5
            pip3 install http://download.pytorch.org/whl/cu90/torch-0.4.0-cp35-cp35m-win_amd64.whl
        - Python 3.6
            pip3 install http://download.pytorch.org/whl/cu90/torch-0.4.0-cp36-cp36m-win_amd64.whl
        ```
    - Without GPU
        ```bash
        - Python 3.5
            pip3 install http://download.pytorch.org/whl/cpu/torch-0.4.0-cp35-cp35m-win_amd64.whl
        - Python 3.6
            pip3 install http://download.pytorch.org/whl/cpu/torch-0.4.0-cp36-cp36m-win_amd64.whl
        ```

- **macOS**
    ```bash
    pip3 install torch==0.4.0
    ```
    > [!NOTE]
	>
    > macOS binaries don't support CUDA, install from source if CUDA is needed

- **Linux**
    - With GPU
        ```bash
        - Python 3.5
            pip3 install http://download.pytorch.org/whl/cu90/torch-0.4.0-cp35-cp35m-linux_x86_64.whl
        - Python 3.6
            pip3 install http://download.pytorch.org/whl/cu90/torch-0.4.0-cp36-cp36m-linux_x86_64.whl
        ```
    - Without GPU
        ```bash
        - Python 3.5
            pip3 install http://download.pytorch.org/whl/cpu/torch-0.4.0-cp35-cp35m-linux_x86_64.whl
        - Python 3.6
            pip3 install http://download.pytorch.org/whl/cpu/torch-0.4.0-cp36-cp36m-linux_x86_64.whl
        ```

Finally, install torchvision:
```bash
pip3 install torchvision
```

### Caffe2

[Caffe2](https://caffe2.ai/) is a lightweight, modular, and scalable deep learning framework.
Building on the original Caffe, Caffe2 is designed with expression, speed, and modularity in mind.

Currently, there's no official prebuilt Caffe2 python wheel package available.
Please visit [here](https://caffe2.ai/docs/getting-started.html) to build from source code.

> [!NOTE]
> This [site](https://github.com/linmajia/ai-package/tree/master/caffe2/0.8.1) has a third-party Caffe2 0.8.1 Windows wheel package (supports both GPU and CPU).

### MXNet

[Apache MXNet (incubating)](https://mxnet.incubator.apache.org/) is a deep learning framework designed for both efficiency and flexibility.
It allows you to mix [symbolic and imperative programming](http://mxnet.io/architecture/index.html#deep-learning-system-design-concepts) to maximize efficiency and productivity.

To install MXNet, run the following command in a terminal:
- With GPU
    ```bash
    pip3 install mxnet-cu90==1.1.0.post0
    ```
- Without GPU
    ```bash
    pip3 install mxnet==1.1.0.post0
    ```

### Keras

[Keras](https://keras.io/) is a high-level neural networks API, written in Python and capable of running on top of CNTK, TensorFlow or Theano. It was developed with a focus on enabling fast experimentation. Being able to go from idea to result with the least possible delay is key to doing good research.

To install Keras, please run the following command in a terminal:
```bash
pip3 install Keras==2.1.5
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
pip3 install cupy==4.0.0
```

> [!NOTE]
>
> On Windows, you need **2015** version of [Microsoft Visual Studio](https://www.visualstudio.com/)
or [Microsoft Visual C++ Build Tools](http://landinghub.visualstudio.com/visual-cpp-build-tools)
to compile CuPy with CUDA 8.0.
First, open a **VS2015 x64 Native Tools Command Prompt** or **Visual C++ 2015 x64 Native Tools Command Prompt**, and then execute the above cupy installation command.

To install Chainer, please run the following command in a terminal:
```bash
pip3 install chainer==4.0.0
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
pip3 install scikit-learn==0.19.1
```

### XGBoost

[XGBoost](https://github.com/dmlc/xgboost) is an optimized distributed gradient boosting library designed to be highly efficient, flexible and portable. It implements machine learning algorithms under the Gradient Boosting framework.

To install XGBoost, please run the following command in a terminal:
- **Windows**
    There is no official prebuilt wheel package for Windows yet.
    Please visit [here](https://www.lfd.uci.edu/~gohlke/pythonlibs/#xgboost) and download a suitable 64-bit package.
    ```bash
    pip3 install /download/path/xgboost*win_amd64.whl
    ```
- **Non-Windows**
    ```bash
    pip3 install xgboost
    ```

### LIBSVM

[LIBSVM](https://www.csie.ntu.edu.tw/~cjlin/libsvm/) is an integrated software for support vector classification, (C-SVC, nu-SVC), regression (epsilon-SVR, nu-SVR) and distribution estimation (one-class SVM).
It supports multi-class classification.

To install LIBSVM on Windows, please visit [here](https://www.lfd.uci.edu/~gohlke/pythonlibs/#libsvm) and download a suitable 64-bit package because there is no official prebuilt wheel package for Windows yet.
Then, please run the following command in a terminal:
```bash
pip3 install /download/path/libsvm*win_amd64.whl
```

To install LIBSVM on non-Windows, please build from the [source code](https://github.com/cjlin1/libsvm/releases).


## Model management packages

### Open Neural Network Exchange (ONNX)

[ONNX](http://onnx.ai/) is the first step toward an open ecosystem that empowers AI developers to choose the right tools as their project evolves. ONNX provides an open source format for AI models.
Caffe2, PyTorch, Microsoft Cognitive Toolkit, Apache MXNet and other tools are developing ONNX support.

> [!NOTE]
>
> On non-Windows, please make sure to install the [Protobuf](https://github.com/google/protobuf/releases) compiler and set environment variable ONNX_ML=1 for onnx-ml.

To install ONNX, please run the following command in a terminal:
```bash
pip3 install onnx
```

### Core ML Community Tools (coremltools)

[coremltools](https://github.com/apple/coremltools) contains all supporting tools for CoreML model conversion and validation. This includes Scikit Learn (0.17+), LIBSVM, Caffe, Keras (1.2.2, 2.0.4+) and XGBoost (0.7+).
These frameworks should have been installed when you are converting models.

To install coremltools, please run the following command in a terminal:
- **Windows**
    > [!NOTE]
    > There is no official prebuilt wheel package for Windows yet. The following method installs Python stuff only.
    ```bash
    pip3 install "git+https://github.com/apple/coremltools@v0.8"
    ```
- **Non-Windows**
    ```bash
    pip3 install coremltools
    ```

### ONNX ML Tool (onnxmltools)

[onnxmltools](https://github.com/onnx/onnxmltools) enables you to convert models from different machine learning toolkits into ONNX.
Currently the following toolkits (need installation) are supported:
- Apple Core ML
- scikit-learn (subset of models convertible to ONNX)

To install onnxmltools, please run the following command in a terminal:
```bash
pip3 install onnxmltools
```

### Microsoft ML Tool (winmltools)

[winmltools](https://pypi.python.org/pypi/winmltools) enables you to convert models from different machine learning toolkits into ONNX for use with Windows Machine Learning.

To install winmltools, please run the following command in a terminal:
```bash
pip3 install winmltools
```

### tf2onnx

[tf2onnx](https://github.com/onnx/tensorflow-onnx) converts a TensorFlow graph to an ONNX graph.
tf2onnx is in its early development. Mileage will vary since TensorFlow supports ~4 times the operations that the current ONNX version supports. But standard models seem to be using mostly ops that ONNX does support.

To install tf2onnx, please run the following command in a terminal:
```bash
pip3 install "git+https://github.com/onnx/tensorflow-onnx.git@r0.1"
```


### Netron

[Netron](https://github.com/lutzroeder/Netron) is a viewer for neural network, deep learning and machine learning models.

Netron supports ONNX (.onnx, .pb), Keras (.h5, .keras), CoreML (.mlmodel) and TensorFlow Lite (.tflite).
Netron has experimental support for Caffe (.caffemodel), Caffe2 (predict_net.pb), MXNet (-symbol.json), TensorFlow.js (model.json, .pb) and TensorFlow (.pb, .meta).

To install Netron, please visit its [release page](https://github.com/lutzroeder/Netron/releases) and download a suitable installer.


## Inter-operation between ML/DL frameworks via model file conversion

In recent years, machine learning and deep learning become very popular in IT industry.
There have been plenty of frameworks for users to build their own models.
However, they differ with each other greatly on the implementation details.
This will inevitably result in that models produced by one framework cannot be reused for subsequent training or inference in another framework, which brings inconvenience and increases cost to users on framework choice.

Model file conversion is a feasible trial towards such challenge.
In the above subsections, we introduce several model converters: coremltools, onnxmltools, winmltools and tf2onnx, as well as their installation method.

For Windows users, we recommend that you use the [one-click installer](https://github.com/Microsoft/samples-for-ai/#using-a-one-click-installer-to-setup-deep-learning-frameworks) to setup these converters.
If you wish to install them by yourself, first go to the third-party web site to install unofficial [XGBoost](https://www.lfd.uci.edu/~gohlke/pythonlibs/#xgboost) and [LIBSVM](https://www.lfd.uci.edu/~gohlke/pythonlibs/#libsvm) 64-bit Windows packages,
and then run the following command in a terminal:
```bash
pip3 install tensorflow==1.5.0 scikit-learn onnx "git+https://github.com/apple/coremltools@v0.8" onnxmltools winmltools "git+https://github.com/onnx/tensorflow-onnx.git@r0.1"
```
