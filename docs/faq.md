# Frequently Asked Questions

## Install Visual Studio Tools for AI

### **Q: Does Visual Studio Tools for AI work with Visual Studio for Mac?**
Visual Studio Tools for AI is an extension for Visual Studio 2017 / 2015.
It does not work with Visual Studio for Mac.

### **Q: Does Visual Studio Tools for AI work with Visual Studio 2013?**
Visual Studio Tools for AI supports only Visual Studio 2017 and 2015.

### **Q: I download the VSIX file from marketplace.visualstudio.com, but why cannot I install it?**
Visual Studio Tools for AI is hosted on Visual Studio Marketplace in two [VS 2017](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.vstoolsai-vs2017), and [VS 2015](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.vstoolsai-vs2015) packages.
Please download the correct package for your Visual Studio.

An easier way to install is from within Visual Studio:
- Choose **Tools > Extensions and Updates** on the menu bar, or type **Extensions** in the **Quick Launch** window.
- Search in upper right-hand corner for **Visual Studio Tools for AI**.
- Select **Microsoft Visual Studio Tools for AI** extension.
- Click **Download** button.


## Prepare development environment

### **Q: Python may not be installed on Windows Server OS.**
After having downloaded the Python installer to a local directory, right-click it and select **Run as administrator**.
We recommend that you install Python to %LocalAppData%.

![Install Python in administrator mode](media/faq/prepare-localmachine/install_python_admin.png)

## Develop AI projects

### **Q: Python projects or examples cannot run.**
If multiple Python environments exist, Visual Studio may choose a wrong environment as default, or the project is manually set to an incorrect one.
Please refer to [Setting up the default Python environment](prepare-localmachine.md#setting-up-the-default-python-environment) and change the global or per-project Python environment.

### **Q: CNTK BrainScript projects or examples cannot run.**
Please go to option page **AI Tools > Options > AI Tools > CNTK**, and check whether **CNTK directory** is set correctly.
That is, cntk.exe should be found under "${CNTK RuntimeSDK Directory}\\cntk".

Please refer to [here](prepare-localmachine.md#microsoft-cognitive-toolkit-cntk) on how to install CNTK BrainScript package.

### **Q: IntelliSense does not work for CNTK, TensorFlow, and etc. Python code.**
After having installed these frameworks, it needs some time for Visual Studio to refresh the Python completion DB.
Please first choose **Tools > Python > Python Environments** (Visual Studio 2017), or **Tools > Python Tools > Python Environments** (Visual Studio 2015) on the menu bar.
Then, click the refreshing button.

![Refresh Python completion DB](media/faq/local-development/refresh_python_db.png)

### **Q: IntelliSense does not work for CNTK BrainScript code.**
At present, Visual Studio Tools for AI does not support IntelliSense for CNTK BrainScript language.

## Microsoft Cognitive Services

### **Q: [The Computer Vision application created from template always returns "Unauthorized" error.](https://github.com/Microsoft/vs-tools-for-ai/issues/15)**
This is a known issue in the Computer Vision application template. Please open the ComputerVisionApiExtensions.cs, and add the following line of code in ComputerVisionApiExtensions class's constructor:
```csharp
this.AzureRegion = GetRegion(region);
```

### **Q: I cannot retrieve subscription keys or create applications due to `Unauthorized` status code.**
Please right-click **AI Tools > Azure Cognitive Services** node on the Server Explorer panel, and select **Refresh**.

### **Q: Resource group <XXX> fails to retrieve cognitive services due to one or more errors occurred.**  
Please right-click **AI Tools > Azure Cognitive Services** node on the Server Explorer panel, and select **Refresh**.

### **Q: Text Analytics application reports region / location error.**
The [TextAnalytics SDK](https://www.nuget.org/packages/Microsoft.Azure.CognitiveServices.Language/1.0.0-preview) only allows regions from **westus**, **westeurope**, **southeastasia**, **eastus2**, **westcentralus**.
Please relocate (move or create new) your service in these provider locations. 

### **Q: Text Analytics application fails to display Chinese characters in the Console.**
You need to change PC language to **Chinese** from **Control Panel > Clock, Language, and Region > Language**.

### **Q: Custom Vision Python application cannot run due to `No module named 'azure.cognitiveservices'`.** 
Please install the Custom Vision Python SDK by running the following command in a terminal:

```bash
python -m pip install azure-cognitiveservices-vision-customvision
```

### **Q: Custom Vision Python application returns `Bad Request` status code.**
It is probably caused by permission issues of your Custom Vision account.
Please try the following steps:

-   Make sure that you don't exceed the quota to create new Custom Vision projects (not the Visual Studio projects).
    The maximum allowed in a service / resource group differs between pricing tiers.

-   Try another subscription key, or regenerate a new one. 
