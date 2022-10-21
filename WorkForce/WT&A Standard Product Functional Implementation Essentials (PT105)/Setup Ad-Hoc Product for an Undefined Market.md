These instructions will lead you through the process of creating a new configuration for a non-defined Market using the Ad-Hoc Product. Any examples offered here are for illustration purposes only, and the same methods can be applied to any specified Market. To recap, an [[Undefined Market]] differs from a [[Defined Market]] in that the buyer must first shop the models to choose the ones that best suit their company needs before beginning a construction. 

This approach takes longer than [[Setup Non-US Market Instance|setting up a Non-US Market Instance]] but it delivers specialized [[Market]] capabilities rather than broad capability. 

All mentioned documentation may be located in the Document Directory or Knowledge Base.

### Step 1: Environments Created

*WorkForce Cloud Services creates DEV, TEST, PROD, and any other appropriate environments upon execution of a SaaS agreement. To check on the status of this initial stage, project teams can file a ticket. 

Log in to the [Partner Community](https://workforcesoftware.force.com/customers) to file a ticket. 

The construction begins with the most recent [[Global Base Dataset]]. Even yet, if there is a delay between environment formation and configuration start, you will reload this in a subsequent stage. 

*Consultants should discuss which environment to work in with their Project Manager or Configuration Lead.*

### Step 2: Gather Documentation

Ensure you have the following documentation available and ready:

1. **Ad-Hoc Selection of Models for WT&A**
2. **Standard Product Assembly Instructions for Ad-Hoc Product**
3. **Model-Template Mapping**
4. **GLOBAL_BASE Template Instructions** 
5. **GEN_CONTAINER Template Instructions**
6. **Model-Template Mapping**

The [[WorkForce/WT&A Standard Product Functional Implementation Essentials (PT105)/Ad-Hoc Product]], unlike the [[Defined Market|Defined Markets]], does not have a standard questionnaire. Customers shop the models by making the selections specified in the Ad-Hoc Selection of [[Model|Models]] for WT&A document. It is critical that you have a complete list of shopped models for the consumer. 

You must also use the Options sections of the MFDs that the client has chosen, which is a variable list for each implementation. Based on their model decisions, they would have to aggregate the alternatives to specify.

### Step 3: Review the Product Assembly Instructions

Before beginning the setup, go over the [[Standard Product]] Assembly Instructions for [[WorkForce/WT&A Standard Product Functional Implementation Essentials (PT105)/Ad-Hoc Product]], which walks you through each step of adding a sequence of templates to an environment. These instructions are similar to Template Instructions in that they include context as well as technical specifics for each build step. 

The procedures in this course cover essential processes in the Product Assembly Instructions as well as delivery guidelines for a specific [[market]].

### Step 4: Reload the [[Global Base Dataset]]

The [[Global Base Dataset]] serves as the starting point for all configurations. When WorkForce Cloud Services creates an environment, it comes pre-loaded with this foundation dataset. Nonetheless, as your initial configuration step, you will reload this. This is in case there is a delay between the establishment of the environment and the start of the setup. 

Submit a ticket with the request in the [Partner Community](https://workforcesoftware.force.com/customers) to acquire access to the customer's environments.

For more information on reloading the Global Base Dataset, visit the [WorkForce Knowledge Base](https://workforcesoftware.force.com/customers/s/article/How-to-Load-the-Latest-Global-Base-Dataset-in-Tenant-Manager ).

### Step 5: Load the [[Global Base Template]]

You're ready to start configuring now that you're comfortable with the general procedure. Load the following layer, the [[Global Base Template]], with the basic [[Global Base dataset]] required to generate the *DEV* instance. To finish this step, go to the **GLOBAL_BASE Template Instructions** manual. 

The [[Global Base Template]] provides the rules necessary for all models in the [[Standard Product]] and must be imported into every [[Standard Product]] implementation. 

*Consultants should discuss which environment to work in with their Project Manager or Configuration Lead.*

### Step 6: Load the [[Generic Container]]

After you've loaded the [[Global Base]], you may put the [[Generic Market]] layer on top of it. While selecting the choices specified by the client in the Ad-Hoc Selection of Models for WT&A document, follow the directions in the GEN CONTAINER Template Instructions. 

The [[Generic Container]] template has additional functional regulations associated with the given attributes and may be used to any geographic location, country, market, and so on. To allow nation or market-specific functionality, additional country or market-specific [[Standard Product|Standard Products]] may be imported on top of the [[Generic Container]].

A Time & Attendance environment can be made up of many [[Generic Container|Generic Containers]], each with its own set of features. As a result, one environment may support the usage of many nations, marketplaces, and so on.

### Step 7: Integrate Remaining Functionality

The [[Generic Container]] does not have all of the functional rules required to set up a specified [[Market]]. To finish the functional regions, continue with the Steps to Integrate portion of the [[Standard Product]] Assembly Instructions for [[WorkForce/WT&A Standard Product Functional Implementation Essentials (PT105)/Ad-Hoc Product]]. 

These instructions link to particular templates to utilize and specify market-specific remarks. Review the Model-Template Comparison document to match the MFD with the template you are integrating into the selected [[Market]] for further functional details on the models represented by the [[template|templates]].

### Step 8: Handling Demo Data

The demo data in the **WT&A US Base Product Creating Environment with Data** paper is not tailored to other markets. It may be used to generate demo data as a starting point, or the customer can contribute their own sample data.

### Step 9: Validate the Setup

Check that the configuration is operating as asked in the *MARKET* - **Customer Product Setup Questionnaire** using the **WT&A Base Product Demonstration Guide**.

### Step 10: Deploy Setup to the Customer

After validation, transmit the setup and demo data (if applicable) to the customer's staging, training, or testing environment. This might be the instanced *TEST. 

In [[Tenant Manager]], do a full dump and load into the destination environment. 

Visit the [WorkForce Knowledge Base](https://workforcesoftware.force.com/customers/s/article/Dump-and-Load-Data-in-Tenant-Manager) for additional information on dumping and loading data in Tenant Manager

*Consultants should discuss which environment to work in with their Project Manager or Configuration Lead.*

### Step 11: Clear the Demo Data

When the customer is ready to load their own sample data into their environment, you must clear the demo data that has already been imported. 

In the permitted environments, use the Truncate Script to delete the demo data while retaining all setup. 

Visit the [WorkForce Knowledge Base](https://workforcesoftware.force.com/customers/s/article/Data-Clean-Up-via-Truncate-Script-for-Partners) for additional details on utilizing the Truncate Script.
