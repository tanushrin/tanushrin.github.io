# 01-Design a data ingestion strategy for ML projects



1\.  **Define the problem**:

Decide on what the model should predict<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image3.svg" width="30" height="30">
and when it\'s successful<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image5.svg" width="30" height="30">
 
<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image1.png" width="300" height="300" alt="Thinking">

___

2\.  **Get the data**:

Find data sources <img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image8.svg" width="30" height="30"><img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image10.svg" width="30" height="30"><img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image12.svg" width="30" height="30">and get access
<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image14.svg" width="30" height="30">

<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image6.png" width="300" height="300"> 


<table>
  <tr>
    <th><em>Three Different Data Formats</em></th>
  </tr>
</table>


1.  **Tabular** or **structured** data
    <img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image8.svg" width="30" height="30">

2.  **Semi-structured** data:
JSON: { \"deviceId\": 29482, \"location\": \"Office1\",
\"time\":\"2021-07-14T12:47:39Z\", \"temperature\": 23 }

3.  **Unstructured** data: <img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image16.svg" width="30" height="30"><img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image18.svg" width="30" height="30"><img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image20.svg" width="30" height="30"><img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image22.svg" width="30" height="30">

Once you've identified the data source, the original data format, and
the desired data format, then, you can design a data ingestion pipeline
to automatically extract and transform the data you need.

___


3\. **Prepare the data**: Explore the data. Clean <img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image24.svg" width="30" height="30">and
transform<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image26.svg" width="30" height="30"> the data based on the model\'s
requirements.

- 3.1.  Separate compute from storage
<br>

- 3.2.  Move and transform data<br>
       **Data ingestion pipeline (manual or scheduled):** sequence of
        tasks that move and transform the data
    

     ***Choices to create a pipeline:***


| Tool                         | Description                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------|
| **Azure Synapse Analytics / Azure Synapse Pipelines** | Configurable via an easy-to-use UI or JSON. Uses serverless SQL pools, dedicated SQL pools, or Spark pools. |
| **Azure Databricks**         | Code-first tool, uses SQL, Python, or R. Utilizes Spark clusters.                                                |
| **Azure Machine Learning**   | Provides compute clusters that automatically scale up and down. |
| **Azure Cognitive Services** | Offers Custom Vision to train a custom computer vision model.                                                    |
| **Scikit-learn**             | A machine learning library for Python.                                                                           |

    
NOTE ➡️ Azure Synapse Analytics and Azure Databricks offer more scalable compute options.

<br>

- 3.3.  Store data for model training workloads, using any of the below:

    **i. Azure Blob Storage**: Cheapest

<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image27.png" width="300" height="300" alt="Thinking"> 

   **ii. Azure Data Lake Storage (Gen 2)**: also implements a hierarchical
    namespace

<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image28.png" width="300" height="300" alt="Thinking"> 

   **iii. Azure SQL Database**:

<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image29.png" width="300" height="300" alt="Thinking"> 

___

4\. **Train the model**: Choose an algorithm
<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image31.svg" width="30" height="30">and hyperparameter values based on trial
and error.

___

5\. **Integrate the model**: Deploy to an endpoint to generate <img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image33.svg" width="30" height="30">predictions <img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image35.svg" width="30" height="30">

___

6\. **Monitor the model**: Track <img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image37.svg" width="30" height="30"> the model\'s performance

___

Quiz Time
=========


>**Q**: Which storage solution would you recommend to store the data?
We want our design to be future-proof and ready for scale. We want to extract the privacy-sensitive data from the patient database and store the data in an Azure data storage solution.

**Ask**: Who should get access to the data?

Data scientists will work with the data in the storage solution. Since we're working with privacy-sensitive medical data, we need a solution that allows us to give someone access only to a specific file or folder.

**Ask**: How should the data be stored?

Our data scientists prefer working with the raw data in CSV files. They have no experience with SQL tables.

<table>
  <tr>
    <th><strong>Answer:</strong></th>
    <td>An <em>Azure Data Lake</em> will allow us to store the data as CSV files, and make use of the hierarchical namespace to have more granular control over who has access to what.</td>
  </tr>
</table>


>**Q**:Which tool would you recommend we use to move the data?
We need to extract data from the patient database and load it into the Azure Data Lake.

**Ask**: Which tool will you use to train the model?

We'll train the machine learning model with either Azure Synapse Analytics, Azure Databricks, or Azure Machine Learning.

**Ask**: Which cloud services do you already use for data-related projects?

Our data engineers already work with Azure to get insights from operational data. They ingest and transform data with Azure Synapse Analytics, store it in an Azure SQL Database, and visualize the data with Power BI.

<table>
  <tr>
    <th><strong>Answer:</strong></th>
    <td><em>Azure Synapse Analytics</em> sounds like a good fit for us at the moment. It’ll allow us to set up a secure connection to the patient database and create automated pipelines to move the data from the database to the Azure Data Lake.</td>
   </tr>
</table>

>**Q**: Which tool should we use to anonymize the patient data?
When we automatically extract data from the patient database, we want the data to be anonymized. We must delete all personally identifiable information (PII).

**Ask**: Who will be responsible of configuring the transformations of the data?

Anonymizing data seems like a simple task. Ideally, this task would be performed by the data engineer. However, we would like data scientists to be able to do this even when a data engineer is not available, possibly through an easy-to-use interface?

**Ask**: How much data do you have?

Since we want to train the model on as much data as possible, the tool should be able to handle large amounts of data.

<table>
  <tr>
    <th><strong>Answer:</strong></th>
    <td>Let’s indeed stick with <em>Azure Synapse Analytics</em>. We can connect to the patient database, perform any necessary transformations, and move the data to the Azure Data Lake. Anyone will be able to configure the transformations using the easy-to-use mapping data flow in Azure Synapse </td>
   </tr>
</table>

>**Q**: Which architecture represents the proposed data ingestion solution?
It’d be good to have an overview of all the decisions we discussed.

**Ask**: Where will we store the data?

We decided to store the data in a Azure Data Lake Storage.

**Ask**: How will we ingest the data?

We decided to ingest the data with Azure Synapse Analytics.

<table>
  <tr>
    <th><strong>Answer:</strong></th>
    <td>Data inspection ---> Data ingestion through Azure Synapse Analytics ----> Data storage in Azure DLS</td>
   </tr>
</table>



---
**Acknowledgment:** This article is inspired by and includes insights derived from [Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/design-data-ingestion-strategy-for-machine-learning-projects/). Microsoft Learn is a valuable resource for in-depth knowledge on this topic and many others. I encourage readers to explore their modules for further information.


