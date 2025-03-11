# Setting Up Microsoft Fabric Capacity with an Azure Trial
Microsoft Fabric is a cloud-based platform that offers various services and experiences for different analytical scenarios, such as data engineering, data science, real-time analytics, and business intelligence. Microsoft Fabric is built on a foundation of Software as a Service (SaaS), which means that users do not have to worry about the underlying infrastructure or management of the services. Instead, they can focus on creating and consuming insights from their data.

Microsoft Fabric brings together the best of Microsoft’s existing analytics products, such as Power BI, Azure Data Factory, and Azure Synapse, into a single unified environment. Users can easily access and reuse all the data and assets across these products and enjoy familiar, easy-to-learn shared experiences. Microsoft Fabric also provides centralized administration and governance for all the services, ensuring data security, privacy, and compliance.

For more information about Microsoft Fabric, visit the website [Learn more about Fabric](https://www.microsoft.com/en-us/microsoft-fabric/?WT.mc_id=academic-105654-visrid) or this article [What is Microsoft Fabric?](https://learn.microsoft.com/en-us/fabric/get-started/microsoft-fabric-overview?WT.mc_id=academic-105654-visrid).

This guide will walk you through the steps to set up Microsoft Fabric Capacity with an Azure trial. By following these steps, you will be able to create a Fabric Capacity in Azure, which is essential for using Fabric's data processing features. Additionally, you will need a Microsoft 365 or Office 365 trial account to access Microsoft Fabric. The guide will also provide instructions on how to avoid unexpected charges by pausing or deleting the Fabric Capacity and canceling the Azure and Office 365 trials.

>**Note:** This guide may seem long and involving many steps, but this is because we are setting a Microsoft 365 tenant, and an Azure Subscription before creating the Fabric Capacity. In an ideal scenario your IT team would have already set up the Microsoft 365 tenant and Azure subscription for you and the  signup to Microsoft Fabric would only take less than 5 minutes. 

>If you alreday have a Fabric Caaacity ypu can skip the entire signup process and go straight to creating a new workspace in Microsoft Fabric. If you have a Microsoft 365 or Office 365 account, you can skip the first part of this guide and go directly to signing up for Microsoft Fabric and creating a Fabric Capacity in Azure.

## **Part 1: Sign Up for an Office 365 Trial**  
Before using **Microsoft Fabric**, you need an **Office 365 trial account** because Fabric requires a **Microsoft 365 tenant** to work.  If you already have a Microsoft 365 or Office 365 account, you can skip this step.

1. Open this link: **[Microsoft 365 Enterprise Plans](https://www.microsoft.com/en-us/microsoft-365/enterprise/office365-plans-and-pricing)**.  
1. Choose **"Office 365 E1"** (or **E3/E5**) and click **"Try for free"**.  
1. Follow the setup prompts:  
   - Use a **personal email (not a work or school email)** to register.  
   - Click **Next**, then select **"Set up account"** to create your **Microsoft 365 tenant**.  

    >**Note:** This process will require providing a payment method and will enable recurring billing after 30 days (which can be disabled with additional steps).  This will be mentioned during the registration process: 

1. Once the account is created, Microsoft will generate a new username with a **.onmicrosoft.com** domain.  
   - Example: `yourname@yourcompany.onmicrosoft.com`  
1. After setup, click **"Start using Office 365 E1 (No Teams) - Trial"** to access the **Microsoft 365 Admin Center**.  


>**Note:**  This trial lasts **one month**, so cancel before it expires to **avoid charges**.  

![Office 365 Trial](/Images/paymentmethod-1024x709.png)

Upon activation, you can disable the recurring billing manually by logging into [https://admin.microsoft.com](https://admin.microsoft.com/ ) with the newly created organizational account, then navigate to Billing => Your Products and select the 3 dots next to the newly created Office 365 subscription.  From there you can turn off recurring billing as shown:

![Disable Recurring Billing](/Images/disablerecurring-1024x604.png)

## **Part 2: Sign up for Microsoft Fabric**  
Now that you have a Microsoft 365 tenant, you need to sign up for **Microsoft Fabric**. 

1. Navigate to **[http://app.fabric.microsoft.com](http://app.fabric.microsoft.com/)** in a new tab.  
1. Sign in using the **.onmicrosoft.com** email address from Part 1.  
1. Follow the prompts to complete account creation.  
1. Once the setup is done, the **Microsoft Fabric home page** will open in a new tab.  

## **Part 3: Sign Up for a Free Azure Account**  
One of the ways you can purchase Microsoft Fabric Capacities is by buying an Azure SKU. Azure SKUs are billed per second with no commitments. Learm more about Azure SKUs [here](https://learn.microsoft.com/en-us/fabric/enterprise/buy-subscription).

For this guide, we will use a **free Azure trial** to set up a **Fabric Capacity**. 

1. Open **[http://aka.ms/freeazure](http://aka.ms/freeazure)** in a new tab.  
1. Click **"Try Azure for free"** to start the trial.  
1. Sign in using your **.onmicrosoft.com** username.  
1. Follow the setup steps:  
   - **Verify your identity** using your **phone number**.  
   - **Enter credit card details** (only for identity verification; no charges unless you upgrade).  
   - **Important:** Use a **credit card that hasn’t been used for an Azure free trial** before.  
1. Once your Azure account is set up, confirm that your **free Azure subscription** is active by navigating to **[portal.azure.com](https://portal.azure.com/)** to access the Azure portal.  
1. On the **Home page**, click **"Subscriptions"**.  
1. You should see your **Free Azure Subscription** listed.  

## **Part 4: Create a Microsoft Fabric Capacity in Azure**  
1. Sign in to the **[Azure Portal](https://portal.azure.com/)** using your **.onmicrosoft.com** username.
2. In Azure, select the Microsoft Fabric service. You can search for Microsoft Fabric using the search menu.
3. Select **"Create Fabric Capacity"** to start the setup process.
1. In the **Create Fabric Capacity** wizard fill in the following details:
   - Under **Resource Group**, click **"Create new"**, and enter a name for your **resource group**.  *This is a logical container for your resources in Azure*.
   - Provide a **Capacity Name**.  
   - Choose a **Region**.  
   - Under **Capacity Size**, select **F2** (**cheapest option**).  *Capacities come in different stock keeping units (SKUs) and we measure them by capacity units (CUs). You can view a detailed list of Microsoft Fabric capacities in [Capacities and SKUs](https://learn.microsoft.com/en-us/fabric/enterprise/licenses#capacity).*
1. Select **"Review + Create"**.  
1. Select **"Create"**.  
1. Once the resource is created, click **"Go to resource"**.  

>**Note:** **Cost-Saving Tip:**  You can **pause and resume your capacity** anytime to **save costs**.  

## Create a new Workspace in Microsoft Fabric
1. From the [Fabric Home Page](http://app.fabric.microsoft.com/), select Workspaces > + New Workspace and teh create workspace pane opens. 

    ![Create Workspace](/Images/fabric-new-workspaces.png)

1. Fillout the following details:
    - **Name** - provide a unique name for the workspace *(mandatory)*
    - **Description** - provide a description for the workspace *(optional)*

1. Expand **Advanced** to find some of the advanced settings options. Under **License Mode** select **Fabric Capacity**. 
1. Select the capacity you created  in the Azure portal under **Capacity**

    ![License Mode](/Images/fabric-license-mode.png)

>**Note:** Your capacity need to be running in order to be able to select it. If you have paused your capacity, you will need to resume it before you can select it.

1. Finally select **Apply** to create the workspace.

## **Cleanup: Avoid Unexpected Charges** 💰  
>**NOte:** The **F2 Fabric Capacity** in **East US** costs **~$262/month**, but the **Azure free trial provides only $200** in free credits.

### **1. Pause Fabric Capacity (To Save Credits)**  
1. Go to **[portal.azure.com](https://portal.azure.com/)**.  
2. Open your **Fabric Capacity resource**.  
3. Click **"Pause"**.  

    ![Pause Fabric Capacity](/Images/pause-fabric-capacity.png)


### **2. Delete Fabric Capacity (To Stop Charges)**  
1. In **Azure Portal**, go to **"Resource Groups"**.  
2. Find the **Resource Group** containing your **Fabric Capacity**.  
3. Click **"Delete Resource Group"**.  

### **3. Cancel Azure Subscription**
Before the one-month trial ends, you should **cancel your Azure subscription** to avoid unexpected charges.
1. In **Azure Portal**, go to **"Subscriptions"**.  
2. Select your **Free Trial Subscription**.  
3. Click **"Cancel Subscription"**.  

### **4. Cancel Office 365 Trial**  
Before the one-month trial ends, you should **cancel your Office 365 trial** to avoid unexpected charges.
1. Go to **[admin.microsoft.com](https://admin.microsoft.com/)**.  
2. Click **Billing > Your Products**.  
3. Find **Office 365 E1 Trial** and click **Manage Subscription**.  
4. Click **"Cancel Subscription"**.  



