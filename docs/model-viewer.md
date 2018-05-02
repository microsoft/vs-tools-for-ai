# Model Viewer
You can view your deep learning framework models. Currently, we support ONNX (.onnx, .pb), Keras (.h5, .keras), CoreML (.mlmodel) and TensorFlow Lite (.tflite). Netron has experimental support for Caffe (.caffemodel), Caffe2 (predict_net.pb), MXNet (-symbol.json), TensorFlow.js (model.json, .pb) and TensorFlow (.pb, .meta).

## Prerequisites
Before viewing a model, please visit [Netron release page](https://github.com/lutzroeder/Netron/releases) to install Netron first.

## Launch Model Viewer
There two entries to launch model viewer:
- Launch Visual Studio and select **AI Tools > Model Tools > View Model...**.
- Right click a supported model file from model inference library project or deep learning application project in solution explorer, click "View Model".

![View Model](./media/model-viewer/launch.png)