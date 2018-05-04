# Infuse AI into your apps with Cognitive Services
Cognitive Services let you build intelligent apps with powerful algorithms using just a few lines of code. Visual Studio Tools for AI now easily enables you to discover, create and customize your Cognitive Services from within Visual Studio.

## Discover and Create Cognitive Services
Once you've [installed Visual Studio Tools for AI](installation.md), it will create an **AI Tools** node in the **Server Explorer** of Visual Studio. By expanding the **AI Tools** node and selecting the **Azure Cognitive Services**, you could 

- Create new service. By right-clicking **Azure Cognitive Services**, selecting **Create New Cognitive Service...** and filling the dialog accordingly, one can create new cognitive service. Below is the illustration of how to create new cognitive service.

	![Create New Cognitive Service](./media/cognitive-services/create_service.gif)

- <a id="list-services">Discover (list) all your subscribed cognitive services</a>. Refreshing (Double clicking or right-clicking and selecting refreshing) will list all the cognitive services subscribed in your account. 

	*Note: If there are so many subscriptions (or resource groups) in your account that the refreshing goes too slow, please filter the subscriptions (and resource groups) by right clicking **Azure Cognitive Services** and selecting **Select Subscription**.*

- <a id="service-properties">Query the basic information of cognitive service</a>. After listing the subscribed cognitive service, you could get further information of the service of interest. Right the the cognitive service and select **Documentation**, **Properties** or **Subscription Keys** to retrieve the information you want to query. The subscription keys and **Endpoint Location** (**Properties**) are necessary to authenticate your applications. 

## Build intelligent apps with Cognitive Services 
**Tools for AI** provides more than one way to infuse AI to your applications. You could have a try directly with an example application, or add the service's SDK to an existing .NET Frameworks project.

- Create new application project based on templates. 
	1. Launch Visual Studio and select **File > New > Project**.
	2. In the **New Project** dialog, select "**AI Tools > Cognitive Services**", the supported application templates will be shown. 
	3. After the application project created, view the source code and replace the strings such as `$Your_Subscription_Key$` and `$Your_Resource_Region$` to the service information queried.(Refer to [querying the service information](#service-properties))

	![New Project From Template](./media/cognitive-services/create_project.gif)

- Create new application based on subscribed cognitive services.

	After [listing the cognitive services in **Tools for AI**](#list-services), right click the service to use and select **Create New Application...**

- Add SDK reference to an existing .NET Framework project. 

## Retrain Custom Vision Cognitive Service
Customize your model in an automatable, repeatable manner by generating code which will use your own images to retrain and download your model. 

Choose to call the Custom Vision Cognitive Service in Azure or use the CoreML or TensorFlow version of your model inside your app on the edge.

![Customized your model](./media/cognitive-services/custom_vision.gif)