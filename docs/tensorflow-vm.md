# Run a TensorFlow model in the cloud
In this tutorial, we will run a TensorFlow model using the [MNIST dataset](http://yann.lecun.com/exdb/mnist/) in an Azure [Deep Learning](https://docs.microsoft.com/azure/machine-learning/data-science-virtual-machine/deep-learning-dsvm-overview) virtual machine. 

The MNIST database has a training set of 60,000 examples, and a test set of 10,000 examples of handwritten digits.

## Prerequisites
Before you begin, ensure you have the following installed and configured:

### Download sample code
Download this [GitHub repository](https://github.com/Microsoft/samples-for-ai) containing samples for getting started with deep learning across TensorFlow, CNTK, Theano and more.

### Setup Azure Deep Learning Virtual Machine
Please read [instructions for setting up Deep Learning Virtual Machine](https://docs.microsoft.com/azure/machine-learning/data-science-virtual-machine/provision-deep-learning-dsvm). 

> [!NOTE] 
> Set **Location** to US West 2 (or others which have Deep Learning VM) and **OS type** as Linux.

### Edit Bash RC to support not running interactively
Login to your Deep Learning VM using a tool like Putty or similar. Execute below to modify your bashrc file to enable remote deep learning job submission (configures remote behavior to work just like if you logged into the VM).

```bash
echo -e ". /etc/profile\n$(cat ~/.bashrc)" > ~/.bashrc
``` 

## Open project

- Launch Visual Studio and select **File > Open > Project/Solution**.

- Select the **Tensorflow Examples** folder from the samples repository downloaded  

![Open project](./media/tensorflow-local/open-project.png)

- Open the **TensorflowExamples.sln** file.

![Open solution](./media/tensorflow-local/open-solution.png)

## Add Azure Remote VM

In Server Explorer, right click the **Remote Machines** node under the AI Tools node and select "Add…". Enter the Remote Machine display name, IP host, SSH port, user name and password/key file. 

![Add a new remote machine](./media/tensorflow-vm/add-remote-vm.png)

## Submit job to Azure VM
Right click on MNIST project in **Solution Explorer** and select **Submit Job**.

![Job submission to a remote machine](./media/tensorflow-vm/job-submission.png)

In the submission window:

- In the list of **Cluster to use**, select the remote machine (with "rm:" prefix) to submit the job to.

- Enter a **Job name**. 

- Click **Submit**. 

## Check status of job 
To see status and details of jobs: expand the virtual machine you submitted the job to in the **Server Explorer**. Double click on **Jobs**.

![Job browser](./media/tensorflow-vm/job-browser.png)

## Clean up resources (optional)

Stop the VM if you plan on using it in the near future. If you are finished with this tutorial, run the following command to clean up your resources:

```azure-interactive
az group delete --name myResourceGroup
```