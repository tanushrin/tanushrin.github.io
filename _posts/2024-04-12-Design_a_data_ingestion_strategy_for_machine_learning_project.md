# 001-Design a data ingestion strategy for ML projects



1\.  **Define the problem**:

Decide on what the model should predict<img src="media/image3.svg" width="30" height="30">
and when it\'s successful<img src="media/image5.svg" width="30" height="30">
 
<img src="media/image1.png" width="300" height="300" alt="Thinking">

___

2\.  **Get the data**:

Find data sources
<img src="media/image8.svg" width="30" height="30"><img src="media/image10.svg" width="30" height="30"><img src="media/image12.svg" width="30" height="30">and get access
<img src="media/image14.svg" width="30" height="30">

<img src="media/image6.png" width="300" height="300"> 

***Three Different data formats***

1.  **Tabular** or **structured** data
    <img src="media/image8.svg" width="30" height="30">

2.  **Semi-structured** data:
JSON: { \"deviceId\": 29482, \"location\": \"Office1\",
\"time\":\"2021-07-14T12:47:39Z\", \"temperature\": 23 }

3.  **Unstructured** data: <img src="media/image16.svg" width="30" height="30"><img src="media/image18.svg" width="30" height="30"><img src="media/image20.svg" width="30" height="30"><img src="media/image22.svg" width="30" height="30">

Once you've identified the data source, the original data format, and
the desired data format, then, you can design a data ingestion pipeline
to automatically extract and transform the data you need.
___

3\. **Prepare the data**: Explore the data. Clean <img src="media/image24.svg" width="30" height="30">and
transform<img src="media/image26.svg" width="30" height="30"> the data based on the model\'s
requirements.

-   Separate compute from storage


-   Move and transform data


       **Data ingestion pipeline (**manual or scheduled**):** sequence of
        tasks that move and transform the data
    

     ***Choices to create a pipeline:***   
    <div style="padding-left: 20px;">
        
    <p><b>i. Azure Synapse Analytics/Azure Synapse Pipelines:</b><br>
        This tool can be configured using an easy-to-use UI, or by defining the pipeline in JSON format. It uses different types of computes such as serverless SQL pools, dedicated SQL pools, or Spark pools.</p>
    
    <p><b>ii. Azure Databricks:</b><br>
        If you prefer a code-first tool and to use SQL, Python, or R. It uses Spark clusters.</p>
    
    <p><b>iii. Azure Machine Learning:</b><br>
        Provides compute clusters that automatically scale up and down.<br>
        <strong>NOTE:</strong> Azure Synapse Analytics and Azure Databricks offer more scalable compute options.</p>
    
    <p><b>iv. Azure Cognitive Services:</b><br>
        Azure Cognitive Services offer Custom Vision to train a custom computer vision model.</p>
    
    <p><b>v. Scikit-learn:</b><br>
        A machine learning library for Python.</p>
    </div>





-   Store data for model training workloads, using any of the below:

    **i. Azure Blob Storage**: Cheapest

<img src="media/image27.png" width="300" height="300" alt="Thinking"> 

   **ii. Azure Data Lake Storage (Gen 2)**: also implements a hierarchical
    namespace

<img src="media/image28.png" width="300" height="300" alt="Thinking"> 

   **iii. Azure SQL Database**:

<img src="media/image29.png" width="300" height="300" alt="Thinking"> 

___

4\. **Train the model**: Choose an algorithm
<img src="media/image31.svg" width="30" height="30">and hyperparameter values based on trial
and error.
___

5\. **Integrate the model**: Deploy to an endpoint to generate <img src="media/image33.svg" width="30" height="30">predictions <img src="media/image35.svg" width="30" height="30">
___
6\. **Monitor the model**: Track <img src="media/image37.svg" width="30" height="30"> the model\'s performance
___
