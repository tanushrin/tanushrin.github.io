# 02- Design a machine learning model training solution 



1\.  **Identify machine learning tasks**:

Define the problem -> Get the data -> Prepare the data -> Train the model -> Integrate the model -> Monitor the model
<img src="https://raw.githubusercontent.com/tanushrin/tanushrin.github.io/main/_posts/media/machine-learning-process.png" width="900" height="100">

Few ML models to note:

- ### Classification
**Predict a categorical value.**
<br>Example: Determining whether an email is spam or not spam.

- ### Regression
**Predict a numerical value.**
Example: Estimating the price of a house based on its features like size and location.

- ### Time-Series Forecasting
**Predict future numerical values based on time-series data.**
Example: Forecasting stock prices for the next month based on past performance data.

- ### Computer Vision
**Classify images or detect objects in images.**
Example: Identifying and tagging friends in a photo on a social media platform.

- ### Natural Language Processing (NLP)
**Extract insights from text.**
Example: Analyzing customer reviews to determine sentiment as positive, negative, or neutral.



___

2\.  **Choose a service to train a model**:

Things to consider while choosing a service:

- Type of model to train, 
- Extent of control over model training, 
- Time to invest in model training, 
- Existing services within the organisation , 
- Ease of using Programming language 

-- __Work in progress..............__


___

Quiz Time
=========


>**Q**: How should we train the model to predict diabetes?
Thank you for helping us decide on how to best train a model which can detect diabetes.
>It’s very important for us that the diabetes classification model is as accurate as possible. We want the model to be trained with our own data.

**Ask**: Who will train the model?

We have a team of data scientists. They should all be able to train a classification model. They are used to working with Python and have no experience with SQL or Spark.

**Ask**: How do you want to train the model?

We prefer not to use a UI. We want our data scientists to train the model with notebooks and scripts. When we get audited, we need to show exactly how a model is trained. We also want our data scientists to have full control over how a model is trained.


<table>
  <tr>
    <th><strong>Answer (with explanation):</strong></th>
    <td>Creating our own custom model using <em>scikit-learn</em> seems to meet our needs. It will take some extra effort and time from our data scientists, but hopefully it will be worth it.</td>
  </tr>
</table>


>**Q**: Which tool should we use to train the diabetes model?
Since developing this model may take some time and effort, we want to make sure that our data scientists can work together smoothly.

**Ask**: Which tool are the data scientists using now?

Our data scientists are currently working in Jupyter notebooks on their own devices. We want them to work in a tool that allows them to collaborate more easily.

**Ask**: Which programming language do the data scientists use to train models?

They feel most comfortable with Python. They're not experienced with PySpark and we don't want them to invest time in learning new functions and libraries at this moment. We want to focus on developing and deploying the model, so that we can test our application as soon as possible.


<table>
  <tr>
    <th><strong>Answer (with explanation):</strong></th>
    <td><em>Azure Machine Learning</em> sounds like a good fit for us at the moment.Data scientists can even use Jupyter notebooks with Azure Machine Learning compute, that’s great!</td>
  </tr>
</table>

>**Q**: Which compute would you recommend to train the model?
We want our data scientists to get started with Jupyter notebooks in the Azure Machine Learning workspace.

There seem to be quite a few options when it comes to compute in Azure Machine Learning.

**Ask**: How much data do you have to train the model?

We extracted a small anonymized dataset from the patient database. The data scientists are starting from scratch, so we want them to develop a model on the small dataset first. Later, when the model is approved, we'll re-train the model with more data.

**Ask**: How will the model be trained?

Our data scientists will begin developing the model by working in Jupyter notebooks. They'll iteratively train a model with different algorithms and hyperparameter values to find the best model.


<table>
  <tr>
    <th><strong>Answer (with explanation):</strong></th>
    <td><em>A compute instance</em> seems ideal for experimentation with Jupyter notebooks, and we don’t need those expensive GPUs yet.</td>
  </tr>
</table>


>**Q**: Which virtual machine size should we use for model development?
We’ll create an Azure Machine Learning workspace for our data science team. We’ll also create the compute instance, and give the data scientists access to the compute instance.

That way, they don’t need additional access and can’t go rogue and create more compute instances that may be unnecessary. Our data scientists can let us know when they need more compute and our administrator will create the compute for them.

We need one more detail from you to create the compute instance. There seem to be several sizes available.

**Ask**: What size is the training dataset?

The anonymized dataset that should be used by the data scientists contains 10 000 rows. It's quite small. We'll work with a larger dataset after initial model development.

**Ask**: What’re you going to use the compute instance for?

We want to create the compute so that our data scientists can work in Jupyter notebooks in Azure Machine Learning Studio. Currently, the plan is to use the compute instance only for model development.

<table>
  <tr>
    <th><strong>Answer (with explanation):</strong></th>
    <td><em>A DS11</em> is a good size to start experimenting with in a Jupyter notebook. Since it’s memory-optimized, we expect a better performance when loading and exploring data directly in the notebook. And since we’re just experimenting now, we might as well go with the cheapest option. If it turns out that we need more compute power, we can easily scale up.</td>
  </tr>
</table>

>**Q**: How should we train another model to predict skin disorders?
In the future, we want to add another feature to our application. We want people to take a picture, upload it, and a model to predict whether a patient has a skin disorder.

**Ask**: Who will train the model?

We do have the team of data scientists... But after asking around, no one seems to have extensive experience with computer vision models. Perhaps we'll hire a computer vision expert, if skin disease detection proves to be a valuable addition to the application.

**Ask**: How do you want to train the model?

The skin detection feature is an idea we want to test. We don't want to spend too much time and effort training a data scientist to develop a computer vision model. We also don't want to minimize the amount of data or computing power needed to training the model.

<table>
  <tr>
    <th><strong>Answer (with explanation):</strong></th>
    <td>To minimize cost and effort, <em>Azure Cognitive Services</em> offer Custom Vision to train a custom computer vision model. Any of our data scientists can use Custom Vision to quickly develop a prototype for the skin detection model.

If the prototype of the model proves to be successful, we can decide to invest more time and effort to take the model to the next level.

It seems we have a good plan to move forward and give our data scientists the tools they need to be productive!</td>
  </tr>
</table>


___

Knowledge Check
===============


>**Q1.**: A data scientist wants to train a machine learning model to predict the sales of supermarket items to adjust the supply to the projected demand. What type of machine learning task will the model perform? 

<table>
  <tr>
    <th><strong>Answer (with explanation):</strong></th>
    <td><em>Time-series forecasting</em> is used to predict future sales.</td>
  </tr>
</table>

>**Q2.**: The data scientist received data to train a model to predict the sales of supermarket items. The data scientist wants to quickly iterate over several featurization and algorithm options by only providing the data and editing some configurations. Which tool would best be used in this situation? 

<table>
  <tr>
    <th><strong>Answer (with explanation):</strong></th>
    <td>You'll only have to provide the data and <em>Automated Machine Learning</em> will iterate over different featurization approaches and algorithms.</td>
  </tr>
</table>









