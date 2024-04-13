![](media/image1.png){width="4.478512685914261in"
height="2.6440474628171478in"}

1.  **Define the problem**:

> Decide on what the model should predict![Head with
> gears](media/image3.svg){width="0.3472222222222222in"
> height="0.24195975503062117in"} and when it\'s
> successful![Trophy](media/image5.svg){width="0.30719160104986876in"
> height="0.18947397200349955in"}

![Create an image of an emoji at a desk, deep in thought with a visual
thought bubble above its head. The thought bubble contains icons
representing various data sources for machine learning, such as
databases, cloud storage symbols, social media icons, sensor data, and
APIs. The setting is a modern office, playful and colorful, suitable for
a tech-themed illustration. The emoji should convey a sense of curiosity
and exploration, emphasizing the search for diverse data
sources.](media/image6.png){width="4.70751968503937in"
height="2.9684208223972in"}

2.  **Get the data**:

Find data sources
![Table](media/image8.svg){width="0.31578958880139985in"
height="0.31578958880139985in"}![Cloud](media/image10.svg){width="0.31578958880139985in"
height="0.31578958880139985in"}![Document](media/image12.svg){width="0.31578958880139985in"
height="0.31578958880139985in"}and get access
![Key](media/image14.svg){width="0.32553915135608047in"
height="0.24166666666666667in"}

[Three Different data formats]{.underline}

1.  **Tabular** or **structured** data
    ![Table](media/image8.svg){width="0.3889621609798775in"
    height="0.3889621609798775in"}

2.  **Semi-structured** data:

> JSON: { \"deviceId\": 29482, \"location\": \"Office1\",
> \"time\":\"2021-07-14T12:47:39Z\", \"temperature\": 23 }

3.  **Unstructured** data: ![Music](media/image16.svg){width="0.3473687664041995in"
    height="0.3473687664041995in"}![Clapper
    board](media/image18.svg){width="0.3473687664041995in"
    height="0.3473687664041995in"}![Images](media/image20.svg){width="0.35789479440069993in"
    height="0.35789479440069993in"}![Contract
    RTL](media/image22.svg){width="0.3368416447944007in"
    height="0.3368416447944007in"}

Once you've identified the data source, the original data format, and
the desired data format, then, you can design a data ingestion pipeline
to automatically extract and transform the data you need.

3\. **Prepare the data**: Explore the data. Clean ![Mop and
bucket](media/image24.svg){width="0.3468208661417323in"
height="0.3468208661417323in"}and
transform![Transfer](media/image26.svg){width="0.2202121609798775in"
height="0.2202121609798775in"} the data based on the model\'s
requirements.

-   Separate compute from storage

```{=html}
<!-- -->
```
-   Move and transform data

```{=html}
<!-- -->
```
-   **Data ingestion pipeline (**manual or scheduled**):** sequence of
    tasks that move and transform the data

> [Choices to create a pipeline:]{.underline}

-   **Azure Synapse Analytics**/ **Azure Synapse Pipelines:**
    easy-to-use UI, or by defining the pipeline in JSON format.

> Uses different types of computes:
>
> serverless SQL pools, dedicated SQL pools, or Spark pools

-   **Azure Databricks:** If you prefer a code-first tool and to use
    SQL, Python, or R.

> Uses Spark clusters.

-   **Azure Machine Learning:** provide compute clusters, that
    automatically scale up/down.

> **NOTE:** Azure Synapse Analytics and Azure Databricks offer more
> scalable compute 

-   **Azure Cognitive services:** Azure Cognitive Services offer Custom
    Vision to train a custom computer vision model.

-   **Scikit-model**

```{=html}
<!-- -->
```
-   Store data for model training workloads, using any of the below:

    -   **Azure Blob Storage**: Cheapest

> ![Create a simplified and clear image of Azure Blob Storage,
> represented as a cloud storage space with a few large, easily
> identifiable icons such as a document, an image, and a video file. The
> design should be minimalist and user-friendly, aimed at conveying the
> concept of cloud storage for semi-structured and unstructured data to
> a layman, using a modern and approachable
> style.](media/image27.png){width="1.4421052055993in"
> height="1.4421052055993in"}

-   **Azure Data Lake Storage (Gen 2)**: also implements a hierarchical
    namespace

> ![Create an image of Azure Data Lake Storage for a layman\'s
> understanding, depicted as a simple, large blue lake with three
> distinct streams flowing into it: a document icon, a video play
> button, and a photo icon. The design should be very minimalist, using
> bold and clear elements against a calm blue background to symbolize a
> unified storage solution. This image should convey the idea of storing
> various data types in an easily accessible and centralized
> manner.](media/image28.png){width="1.3473687664041996in"
> height="1.3473687664041996in"}

-   **Azure SQL Database**:

> ![](media/image29.png){width="2.0369892825896763in"
> height="2.112432195975503in"}

4\. **Train the model**: Choose an algorithm
![Statistics](media/image31.svg){width="0.38391294838145235in"
height="0.2619149168853893in"}and hyperparameter values based on trial
and error.

5\. **Integrate the model**: Deploy to an endpoint to generate ![Bar
graph with downward
trend](media/image33.svg){width="0.23117672790901136in"
height="0.23117672790901136in"}predictions ![Bar graph with downward
trend RTL](media/image35.svg){width="0.19959755030621174in"
height="0.19959755030621174in"}

6**. Monitor the model**: Track ![Security
camera](media/image37.svg){width="0.31513123359580053in"
height="0.31513123359580053in"} the model\'s performance
