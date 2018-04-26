# 模型查看器

Visual Studio Tools for AI已集成了[Netron](https://github.com/lutzroeder/Netron)，这是一个神经网络，深度学习和机器学习模型的查看工具。 此工具支持 ONNX (.onnx, .pb), Keras (.h5, .keras), Core ML (.mlmodel) 和TensorFlow Lite (.tflite). 它对 Caffe (.caffemodel), Caffe2 (predict_net.pb), MXNet (-symbol.json), TensorFlow.js (model.json, .pb) 和 TensorFlow (.pb, .meta) 也有部分支持。

## 先决条件

确保从Netron[发布页](https://github.com/lutzroeder/Netron/releases)安装了最新版本。

## 启动模型查看工具

有两种方法启动模型查看工具

- 选择菜单栏上的 **AI Tools > Model Tools > View Model...** 。
- 从解决方案资源管理器中，右击模型推断库或深度学习应用项目中支持的模型文件，然后点击 **View Model**。

![查看模型](./media/model-viewer/launch.png)