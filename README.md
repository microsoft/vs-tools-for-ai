 # Visual Studio Tools for AI
Visual Studio Tools for AI is an extension to build, test, and deploy Deep Learning / AI solutions. It seamlessly integrates with Azure Machine Learning for robust experimentation capabilities, including but not limited to submitting data preparation and model training jobs transparently to different compute targets. Additionally, it provides support for custom metrics and run history tracking, enabling data science reproducibility and auditing. Enterprise ready collaboration, allow to securely work on project with other people.

Get started with deep learning using [Microsoft Cognitive Toolkit (CNTK)](http://www.microsoft.com/en-us/cognitive-toolkit), [Google TensorFlow](https://www.tensorflow.org), or other deep-learning frameworks today.  

## Quick Links
**Getting Started**

- [Installation](/docs/installation.md)
- [Prepare development environment](/docs/prepare-localmachine.md)
- [Deep learning sample recipes](https://github.com/Microsoft/samples-for-ai)
- [Frequently Asked Questions](/docs/faq.md)

**Quickstarts**

- [Tensorflow + Python](/docs/tensorflow-local.md)
- [Create AI project from samples gallery](/docs/quickstart-00-project-from-azuremachinelearning-gallery.md)
- [Create AI project from existing code](/docs/quickstart-01-project-from-existing.md)
- [Create AI project from template](/docs/quickstart-02-project-from-template.md)
- [Create AI project from samples repository](/docs/quickstart-03-project-from-repository.md)
- [Train MNIST using TensorFlow in Azure Batch AI](/docs/quickstart-04-train-azure-batchai.md)

**Tutorials**

- [Monitor & Visualize with TensorBoard](/docs/monitor-tensorboard.md)
- [Monitor Job History](/docs/job-history.md)
- [Manage Storage](/docs/manage-storage.md)
- [Monitor GPU Utilization](/docs/gpu-utilization.md)
- [TensorFlow + Azure Deep Learning VM](/docs/tensorflow-vm.md)
- [Infuse Apps, Websites and Bots with Microsoft Cognitive Services](/docs/cognitive-services.md)
- [Build Intelligent Apps with Pre-trained AI Models](/docs/model-inference.md)
- [Convert AI Models Between Frameworks](/docs/model-converter.md)
- [View Network Architecture and Parameters of AI Models](/docs/model-viewer.md)

# Supported Operating Systems
Currently this extension supports 64-bit Windows operating systems.
Windows 10 is recommended for the best compatibility.

> [!NOTE]
>
> 32-bit Windows are not supported.

# Supported Visual Studio versions
Visual Studio Tools for AI works with both Visual Studio 2017 and 2015 on Windows.
[Community](https://www.visualstudio.com/downloads/), Professional and Enterprise editions are supported.

This extension is hosted on Visual Studio MarketPlace in two
[VS 2017](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.vstoolsai-vs2017),
and [VS 2015](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.vstoolsai-vs2015) packages.
**When downloading, the package file name may incorrectly end with ".zip".
Please save it as ".vsix" and then install locally.**

For the Visual Studio Code version please see [Visual Studio Code Tools for AI](http://aka.ms/vscodetoolsforai)

## Develop, debug and deploy deep learning models and AI solutions  
Use the productivity features of Visual Studio to accelerate AI innovation today. Use built-in code editor features like syntax highlighting, IntelliSense and text auto formatting. You can interactively test your deep learning application in your local environment using step-through debugging on local variables and models. 

[Learn more about creating deep learning projects in Visual Studio](/docs/quickstart-02-project-from-template.md)

![deep learning ide](/docs/media/ide.png)

## Get started quickly with the Azure Machine Learning Sample Gallery  
Visual Studio Tools for AI is integrated with Azure Machine Learning to make it easy to browse through a gallery of sample experiments using CNTK, TensorFlow, MMLSpark and more. 

[Learn more about creating projects from the sample gallery](/docs/quickstart-00-project-from-azuremachinelearning-gallery.md) 
 
![sample explorer](/docs/media/gallery.png)

## Scale out deep learning model training and/or inferencing to the cloud
This extension makes it easy to train models on your local computer or you can submit jobs to the cloud by using our integration with Azure Machine Learning. You can submit jobs to different compute targets like Spark clusters, Azure GPU virtual machines and more  

[Learn more about training models in the cloud](/docs/tensorflow-vm.md) 
 
![submit job](/docs/media/submitjobs.png)

# Support
Support for this extension is provided on our [GitHub Issue Tracker](http://github.com/Microsoft/vs-tools-for-ai/issues). You can submit a bug report, a feature suggestion or participate in discussions.

## Code of Conduct
This project has adopted the [Microsoft Open Source Code of Conduct]. For more information see the [Code of Conduct FAQ] or contact [opencode@microsoft.com] with any additional questions or comments.

## Privacy Statement
The [Microsoft Enterprise and Developer Privacy Statement] describes the privacy statement of this software.

## License
This extension is subject to the terms of the [End User License Agreement](https://www.visualstudio.com/license-terms/mlt552233/)

[Microsoft Enterprise and Developer Privacy Statement]:https://go.microsoft.com/fwlink/?LinkId=786907&lang=en7
[licensed under the MIT License]: /LICENSE
[Microsoft Open Source Code of Conduct]:https://opensource.microsoft.com/codeofconduct/
[Code of Conduct FAQ]:https://opensource.microsoft.com/codeofconduct/faq/
[opencode@microsoft.com]:mailto:opencode@microsoft.com
