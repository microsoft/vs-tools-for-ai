# Infuse AI into your apps with Cognitive Services
Cognitive Services let you build intelligent apps with powerful algorithms using just a few lines of code. Visual Studio Tools for AI now easily enables you to discover, create and customize your Cognitive Services from within Visual Studio.

## Discover and Create Cognitive Services
Once you've [installed Visual Studio Tools for AI](installation.md), it will create an **AI Tools** node in the **Server Explorer** of Visual Studio. By expanding the **AI Tools** node and selecting the **Azure Cognitive Services**, you could 
- Discover (list) all your subscribed cognitive services. Refreshing (Double clicking or right-clicking and selecting refreshing) will list all the cognitive services subscribed in your account. 
[*Note: If there are so many subscriptions (or resource groups) in your account that the refreshing goes too slow, please filter the subscriptions (and resource groups) by right clicking **Azure Cognitive Services** and selecting **Select Subscription**.*]
- Create new service. By right-clicking **Azure Cognitive Services**, selecting **Create New Cognitive Service...** and filling the dialog accordingly, one can create new cognitive service. Below is the illustration of how to create new cognitive service.

	![Create New Cognitive Service](./media/cognitive-services/create_service.gif)

## Build intelligent apps with Cognitive Services 
There is more than one way to infuse AI to your applications.

**Tools for AI** provides project templates to create new intelligent .Net or python applications based on cognitive services.

## Retrain Custom Vision Cognitive Service
Customize your model in an automatable, repeatable manner by generating code which will use your own images to retrain and download your model. Choose to call the Custom Vision Cognitive Service in Azure or use the CoreML or TensorFlow version of your model inside your app on the edge.