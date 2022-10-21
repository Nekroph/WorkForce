This procedure is identical to the guidelines for the [[WorkForce/WT&A Standard Product Functional Implementation Essentials (PT105)/Setup US Market Instance|US Market]] instructions, except you will not need the US Wage, Hour, and Holiday [[template]]. You may also use this procedure to create a simple US Market]] without the rules. 

The Document Directory contains links to all of the documentation mentioned.

### Step 1: Environments Created

*WorkForce Cloud Services creates DEV, TEST, PROD, and any other appropriate environments upon execution of a SaaS agreement. To check on the status of this initial stage, project teams can file a ticket. 

Log in to the [Partner Community](https://workforcesoftware.force.com/customers) to file a ticket. 

The construction begins with the most recent [[Global Base Dataset]]. Even yet, if there is a delay between environment formation and configuration start, you will reload this in a subsequent stage. 
*Consultants should discuss which environment to work in with their Project Manager or Configuration Lead.*

### Step 2: Gather Documentation

Make sure you have the following documentation available before starting configuration: 


1. **Customer Standard Product Setup Questionnaire**
2. **GLOBAL_BASE Template Instructions** 
3. **STANDARD_PRODUCT Template Instructions**
4. **WT&A US Base Product Creating Environment with Data**
5. **WT&A Base Product Demonstration Guide**

The client answering the setup questionnaire is one of the initial steps in the implementation process. This might happen as early as the sales cycle. 

The [[Standard Product]] cannot be created without the questionnaire.

### Step 3: Reload the [[Global Base Dataset]]

The [[Global Base Dataset]] serves as the starting point for all configurations. When WorkForce Cloud Services creates an environment, it comes pre-loaded with this foundation dataset. Nonetheless, as your initial configuration step, you will reload this. This is in case there is a delay between the establishment of the environment and the start of the setup. 

Submit a ticket with the request in the [Partner Community](https://workforcesoftware.force.com/customers) to acquire access to the customer's environments.

For more information on reloading the Global Base Dataset, visit the [WorkForce Knowledge Base](https://workforcesoftware.force.com/customers/s/article/How-to-Load-the-Latest-Global-Base-Dataset-in-Tenant-Manager ).

### Step 4: Load the [[Global Base Template]]

This step is only done once per customer. Load the following layer, the [[Global Base Template]], with the basic [[Global Base Dataset]] required to generate the *DEV instance. To finish this step, go to the **GLOBAL BASE Template Instructions** manual. 

The [[Global Base Template]] provides the rules necessary for all models in the [[Standard Product]] and must be imported into every [[Standard Product]] implementation. 

*Consultants should discuss which environment to work in with their Project Manager or Configuration Lead.

### Step 5: Load the Standard Base

After you've loaded the [[Global Base]], you may put the [[Standard Base Product]] Market layer on top of it. Follow the steps in the **STANDARD_PRODUCT Template Instructions** while picking the choices from the Customer **Standard Product Setup Questionnaire**. 

Much of the functional policies associated with the described features are included in the [[Standard Product]] template. It is made up of three templates, each with its own import window. Only the first template, STANDARD_PRODUCT, must be explicitly imported; all subsequent templates will import automatically after the first.

### Step 6: Add Demo Data

You may build up demonstration data for the customer to interact with the environment once the [[Policy Profiles]] have been established using the **Customer US Product Setup Questionnaire** choices. 

To finish this stage, refer to the **WT&A US Base Product Creating Environment with Data** document. The sample data files are connected to the PDF page. It should be noted that some PDF readers may struggle to view these files. 

Customer sample data may also be imported as an alternative.

### Step 7: Validate the Setup

Check that the setup is performing as requested in the **Customer Standard Product Setup Questionnaire** using [testing best practices](https://workforcesoftware.force.com/customers/s/article/Configuration-Testing-Best-Practices). 

Customers will follow the **WT&A Base Product Demonstration Guide** to use the sample data if it is loaded. MFDs and customer choices are otherwise used to refer to capabilities for evaluation.

### Step 8: Deploy Setup to the Customer

After validation, transmit the setup and demo data (if applicable) to the customer's staging, training, or testing environment. This might be the instanced *TEST. 

In Tenant Manager, do a full dump and load into the destination environment.

Visit the [WorkForce Knowledge Base](https://workforcesoftware.force.com/customers/s/article/Dump-and-Load-Data-in-Tenant-Manager) for additional information on dumping and loading data in Tenant Manager. 

*Consultants should discuss which environment to work in with their Project Manager or Configuration Lead.

### Step 9: Clear the Demo Data

When the customer is ready to load their own sample data into their environment, you must clear the demo data that has already been imported. If you utilized customer-specific data that the client wants to keep or if you did not load the demo data, skip this step. 

In the permitted environments, use the Truncate script to remove the demo data while retaining all setup. 

Visit the [WorkForce Knowledge Base](https://workforcesoftware.force.com/customers/s/article/Data-Clean-Up-via-Truncate-Script-for-Partners) for additional details on utilizing the Truncate Script.