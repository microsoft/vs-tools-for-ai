# 发行说明

## 0.4.0.620119 (2018-05-06)

这一版中，增加了很多重要功能，需要[最新版的Visual Studio](https://docs.microsoft.com/en-us/visualstudio/install/update-visual-studio)并[升级 CUDA / AI 框架](prepare-localmachine.md)。

因为安装深度学习和机器学习软件机器依赖不是一个容易的任务，推荐使用[一键安装工具](https://github.com/Microsoft/samples-for-ai/#using-a-one-click-installer-to-setup-deep-learning-frameworks)来自动安装。

- 用[微软认知服务](https://azure.microsoft.com/en-us/services/cognitive-services/)将AI注入应用，让它能看、听、说、理解并解释用户需要，通过自然的方式与客户交流。 
    - 在Visual Studio中通过图形界面向导来添加和管理认知服务。
    - 从预定义的模板构建认知服务应用。
    - 从生成的训练项目或门户网站来训练并管理自己的[自定义视觉](https://www.customvision.ai/)模型。
- 通过[Microsoft.ML.Scoring](https://www.nuget.org/packages/Microsoft.ML.Scoring/)库来用预先训练的模型来构建智能应用程序 
    - 训练完成后，在Visual Studio中将预训练模型加入到应用中非常容易，就像增加其它库和资源一样。
    - Visual Studio Tools for AI让创建模型推理库项目非常简单，它能自动为服务优化ONNX/TensorFlow模型，也能将优化的ONNX/TensorFlow运行时加入到项目中。
    - 此外，Visual Studio Tools for AI还能生成C#的基础代码类来简化应用程序与模型的交互。
    - 这些模型推理库项目可以进一步部署为 NuGet 包，以方便分发。
- 通过模型文件转换来实现不同AI框架间的互操作。 
    - 将Core ML, TensorFlow, scikit-learn, XGBoost and LIBSVM模型转换为[ONNX](https://onnx.ai/)格式。
    - 与WinMLTools, ONNXMLTools 和tf2onnx转换工具相集成。
- 在训练和推理项目中查看AI模型的网络架构和参数。 需要安装最新版的[Netron](https://github.com/lutzroeder/Netron/releases)。
- 在docker中运行远程计算机作业。
- 自动登录到基于密码的远程计算机（例如：Azure DSVM/DLVM）。 安装最新版的[Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)，并将putty.exe的路径加入到%Path%环境变量中。
- 添加PyTorch应用程序模板。
- [Open Platform for AI (PAI)](https://github.com/Microsoft/pai)支持实验。 
    - 将训练项目提交到PAI集群中。
    - 用图形界面管理作业和文件。
- 修复bug，提高稳定性。

## 0.3.3.0 (2018-02-10)

- 改进从存在的Visual Studio项目创建Azure ML项目的体验。
- 改进Azure Batch AI集群中创建和提交作业的界面布局和参数验证，与Azure网站门户保持一致。
- 通过[OpenSSH client](https://github.com/PowerShell/Win32-OpenSSH)连接到远程计算机。
- 修复bug，提高稳定性。

## 0.3.2.0 (2017-12-19)

- 检查扩展依赖，如Python工具等。如果VS 2017需要，则自动安装。
- 重构Azure Batch AI的作业提交体验，并支持NFS服务器。
- 修复bug，提高稳定性。

## 0.3.0.0 (2017-11-17)

- 第一版。