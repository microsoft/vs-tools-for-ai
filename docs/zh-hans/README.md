# Visual Studio Tools for AI

[English](/README.md)

Visual Studio Tools for AI是用来生成、测试、部署深度学习/人工智能解决方案的扩展。 它与Azure Machine Learning无缝集成，提供了一系列丰富的试验能力，如将数据和训练任务透明的提交到不同的计算目标上。 除此之外，还有训练历史跟踪，自定义指标等功能，能提供数据科学中的跟踪和重现的能力。 它的企业级的协作能力，为多人在同一个项目上的合作提供了足够的安全保障。

使用[微软认知工具包 (CNTK)](http://www.microsoft.com/en-us/cognitive-toolkit)，[Google TensorFlow](https://www.tensorflow.org)或其它深度学习框架开始入门。

## 快速链接

**准备工作**

- [安装](docs/installation.md)
- [准备开发环境](docs/prepare-localmachine.md)
- [深度学习示例](https://github.com/Microsoft/samples-for-ai)

**快速入门**

- [Tensorflow + Python](docs/tensorflow-local.md)
- [从Azure示例集中创建AI项目](docs/quickstart-00-project-from-azuremachinelearning-gallery.md)
- [从已有的代码创建AI项目](docs/quickstart-01-project-from-existing.md)
- [从模板创建AI项目](docs/quickstart-02-project-from-template.md)
- [从示例代码仓库创建AI项目](docs/quickstart-03-project-from-repository.md)
- [在Azure Batch AI上用TensorFlow来训练MINST数据集](docs/quickstart-04-train-azure-batchai.md)

**教程**

- [用TensorBoard来监控& 可视化](docs/monitor-tensorboard.md)
- [监控任务历史](docs/job-history.md)
- [管理存储](docs/manage-storage.md)
- [监控GPU使用情况](docs/gpu-utilization.md)
- [TensorFlow + Azure深度学习虚拟机](docs/tensorflow-vm.md)

# 支持的操作系统

本扩展程序当前支持64位Windows操作系统。 推荐使用Windows 10来获得最佳的兼容性。

> [!注意]
> 
> 不支持32位操作系统。

# 支持的Visual Studio版本

Visual Studio Tools for AI可用于Windows上的Visual Studio 2017/2015。 支持[社区版](https://www.visualstudio.com/downloads/)，专业版以及企业版。

可在Visual Studio MarketPlace上找到这两个 [VS 2017](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.vstoolsai-vs2017), 和[VS 2015](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.vstoolsai-vs2015)扩展包。 **开始下载时，文件包名有可能是".zip"。 请在下载后改为".vsix"，然后再安装。**

要下载Visual Studio Code版本，请查看[Visual Studio Code Tools for AI](http://aka.ms/vscodetoolsforai)

## 开发、调试，并部署深度学习模型和AI解决方案

现在就用Visual Studio产品级的功能来加速AI创新。 使用内置的代码编辑器来获得语法高亮、智能提醒和自动格式化等功能。 你能在本地环境中，用单步调试来查看本地变量和模型，测试深度学习应用。

[进一步学习如何在Visual Studio中创建深度学习项目](docs/quickstart-02-project-from-template.md)

![深度学习集成开发环境](docs/media/ide.png)

## 使用Azure Machine Learning样例集快速入门

Visual Studio Tools for AI与Azure Machine Learning集成在一起，能够很容易的浏览CNTK、TensorFlow、MMLSpark及其它组件创建的样例库。

[进一步学习如何从样例集创建项目](docs/quickstart-00-project-from-azuremachinelearning-gallery.md)

![示例浏览](docs/media/gallery.png)

## 将深度学习模型和/或推理扩展到云端

此扩展能够轻松的在本机上训练模型，或通过集成的Azure Machine Learning将任务提交到云端。 你可以将任务提交到不同的计算平台，如Spark集群，Azure GPU虚拟机等等。

[进一步了解如何在云端训练模型](docs/tensorflow-vm.md)

![提交任务](docs/media/submitjobs.png)

# 支持

我们在[GitHub Issue Tracker](http://github.com/Microsoft/vs-tools-for-ai/issues)上提供此扩展的支持。 你可以报告bug，建议功能或参与讨论。

## 行为准则

该项目采用了 [ Microsoft 开源行为准则 ](https://opensource.microsoft.com/codeofconduct/)。 有关详细信息,请参阅 [ 行为守则常见问题解答 ](https://opensource.microsoft.com/codeofconduct/faq/) 或联系<opencode@microsoft.com>咨询问题或评论。

## 隐私声明

[Microsoft Enterprise and Developer Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=786907&lang=en7)描述了此软件的隐私声明。

## 许可证

此扩展受[最终用户许可协议](https://www.visualstudio.com/license-terms/mlt552233/)条款的限制。