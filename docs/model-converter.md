# Converting models to ONNX
[ONNX](https://onnx.ai/) is an open format to represent deep learning models. With ONNX, AI developers can more easily move models between state-of-the-art tools and choose the combination that is best for them. ONNX is developed and supported by a community of partners. To learn more about ONNX see [http://onnx.ai/](https://onnx.ai/)

Converting models to ONNX makes it easy to use them in a wide variety of optimized applications. Visual Studio Tools for AI will [generate code from ONNX models and TensorFlow models](model-inference.md) to make it easy to include models in your applications. However, only ONNX models are supported by [WindowsML](https://docs.microsoft.com/en-us/windows/uwp/machine-learning/)

Visual Studio Tools for AI makes it easy to convert trained models to ONNX by leveraging existing model converters. You can learn more about the [model converter utilities here](https://github.com/onnx/onnx), or simply use the wizard in Visual Studio to create your ONNX model.

Currently, Visual Studio Tools for AI supports converting machine learning and deep learning framework models to ONNX from the following frameworks:
- Core ML
- TensorFlow
- Scikit-Learn
- XGBoost
- LIBSVM

## Prerequisites
To install prerequisites for converting XGBoost and LibSVM models 
- Install [XGBoost](https://www.lfd.uci.edu/~gohlke/pythonlibs/#xgboost) 64-bit Windows package
- Install [LIBSVM](https://www.lfd.uci.edu/~gohlke/pythonlibs/#libsvm)  64-bit Windows package

Then run the following from your command line:
```cmd
pip3 install tensorflow==1.5.0 scikit-learn onnx "git+https://github.com/apple/coremltools@v0.8" onnxmltools winmltools "git+https://github.com/onnx/tensorflow-onnx.git@r0.1"
```

## Launch Model Converter
- Launch Visual Studio and select **AI Tools > Model Tools > Convert Model...**.
- Select source model type and file.
- Select target model type(we only support ONNX currently) and file.

### Convert Core ML model
- Input graph name for ONNX model.

    ![Convert CoreML](./media/model-converter/coreml.png)

### Convert TensorFlow model
You can convert two types of TensorFlow models to ONNX:
- Frozen protobuf model (file extension is *.pb)
- Checkpoint MetaGraphDef model (file extension is *.meta )

    ![Open folder](./media/model-converter/tensorflow-checkpoint.png)

- Add input nodes and output nodes. The node name must in the graph.

![Convert TensorFlow](./media/model-converter/tensorflow.png)

### Convert Scikit-Learn/XGBoost/LIBSVM model
- Input graph name for the ONNX model.
- Add input features according to the input of the source model.

![Convert Sckikit](./media/model-converter/sklearn.png)

### Start Converting
- Click OK button, it will check dependencies first.
- If dependencies are all installed, a converter task will be added to task list explorer. 
- When converter task succeeds, it will open a file explorer with target model selected.

![Convert Tasklist](./media/model-converter/tasklist.png)
