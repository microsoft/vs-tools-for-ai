# Frequently Asked Questions

## Install Visual Studio Tools for AI

## Prepare development environment

#### Python may not be installed on Windows Server OS

After downloading the Python installer to a local directory, right-click it and select ***Run as administrator***.
We recommend that you install Python to %LocalAppData%.

![Install Python in administrator mode](/docs/media/faq/prepare-localmachine/install_python_admin.png)

## Develop AI projects

#### Python projects or examples cannot run.

If multiple Python environments exist, Visual Studio may choose a wrong environment as default, or the project is manually set to an incorrect one.
Please refer to [Setting up the default Python environment](https://github.com/Microsoft/vs-tools-for-ai/blob/master/docs/prepare-localmachine.md#setting-up-the-default-python-environment) and change the global or per-project Python environment.

#### CNTK BrainScript Deep Learning projects or examples cannot run.

Please go to option page ***AI Tools &gt; Options &gt; Options &gt; AI Tools &gt; CNTK***, and check whether "**CNTK RuntimeSDK Directory**" is set correctly. That is, cntk.exe should be found under "${CNTK RuntimeSDK Directory}\\cntk".

Please refer to [here](https://github.com/Microsoft/vs-tools-for-ai/blob/master/docs/prepare-localmachine.md#microsoft-cognitive-toolkit-cntk) on how to install CNTK BrainScript package.

#### IntelliSense does not work for CNTK, TensorFlow, and etc. Python code.

After having installed these frameworks, it needs some time for Visual Studio to refresh the Python completion DB.
Please go to menu ***Tools &gt; Python &gt; Python Environments*** (Visual Studio 2017), or ***Tools &gt; Python Tools &gt; Python Environments*** (Visual Studio 2015). Then, click the refreshing button.

![Refresh Python completion DB](/docs/media/faq/local-development/refresh_python_db.png)

#### IntelliSense does not work for CNTK BrainScript code.

At present, Visual Studio Tools for AI does not support IntelliSense for CNTK BrainScript language.
