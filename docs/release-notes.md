# Release Notes

## 0.4.0.620119 (2018-05-06)
We add many cool features in this release, which requires [recent version of Visual Studio](https://docs.microsoft.com/en-us/visualstudio/install/update-visual-studio) and [upgrading CUDA / AI frameworks](prepare-localmachine.md).

Since setting up deep learning and machine learning software as well as their dependencies is not an easy task,
we recommend that you use the [one-click installer](https://github.com/Microsoft/samples-for-ai/#using-a-one-click-installer-to-setup-deep-learning-frameworks) to install them automatically.


-   Infuse AI into your apps with [Microsoft Cognitive Services](https://azure.microsoft.com/en-us/services/cognitive-services/) to see, hear, speak, understand and interpret your user needs through natural methods of communication.
    -   Add Cognitive Services via GUI wizard and manage them in Visual Studio.
    -   Build Cognitive Service apps from pre-defined project templates.
    -   Train and manage your own [Custom Vision](https://www.customvision.ai/) model from the generated training project or web portal.
-   Build intelligent apps using pre-trained AI models with the [Microsoft.ML.Scoring](https://www.nuget.org/packages/Microsoft.ML.Scoring/) library 
    -   Once training is complete, building intelligent apps in Visual Studio is as easy as putting your trained model in your app just like any other library or resource.
    -   Visual Studio Tools for AI makes this easy by enabling you to create a Model Inference Library project which automatically optimizes your ONNX/TensorFlow model for serving, as well as placing on optimized ONNX/TensorFlow runtime in the project.
    -   Moreover, Visual Studio Tools for AI generates a C# stub class to simplify interaction with models in your app.
    -   These Model Inference Library projects can be further deployed as NuGet packages for convenient distribution.
-   Interoperation between different AI frameworks through model file conversion.
    -   Convert Core ML, TensorFlow, scikit-learn, XGBoost and LIBSVM models to [ONNX](https://onnx.ai/) format.
    -   Integration with WinMLTools, ONNXMLTools and tf2onnx converters.
-   View network architecture and parameters of AI models in your training and inference projects. Please install the latest version of [Netron](https://github.com/lutzroeder/Netron/releases).
-   Run remote machine jobs in Docker.
-   Log in automatically to your password-based remote machines (e.g. Azure DSVM/DLVM). Please install the latest version of [Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html), and set the directory of putty.exe to %Path% environment variable.
-   Add PyTorch application template.
-   Experimental support for [Open Platform for AI (PAI)](https://github.com/Microsoft/pai).
    -   Submit training projects to PAI clusters.
    -   Manage jobs and files with GUI tools.
-   Bug fixes and stability improvements.


## 0.3.3.0 (2018-02-10)
-   Improve the experience of creating Azure ML projects from existing Visual Studio projects.
-   Improve the UI layout and parameter validation of Azure Batch AI cluster creation and job submission to keep consistent with Azure web portal.
-   Connect to a remote machine with [OpenSSH client](https://github.com/PowerShell/Win32-OpenSSH).
-   Bug fixes and stability improvements.


## 0.3.2.0 (2017-12-19)
-   Check extension dependencies such as Python Tools, and automatically install them if necessary for VS 2017 extension.
-   Refine the job submission experiences of Azure Batch AI, and support NFS servers.
-   Bug fixes and stability improvements.


## 0.3.0.0 (2017-11-17)
-   Initial version.
