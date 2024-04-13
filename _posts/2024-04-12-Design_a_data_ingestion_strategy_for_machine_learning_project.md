# 001-Design a data ingestion strategy for ML projects



1\.  **Define the problem**:

Decide on what the model should predict<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image3.svg" width="30" height="30">
and when it\'s successful<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image5.svg" width="30" height="30">
 
<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image1.png" width="300" height="300" alt="Thinking">

___

2\.  **Get the data**:

Find data sources
<img src="media/image8.svg" width="30" height="30"><img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image10.svg" width="30" height="30"><img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image12.svg" width="30" height="30">and get access
<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image14.svg" width="30" height="30">

<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/image6.png" width="300" height="300"> 

***Three Different data formats***
|---|

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


