Data science projects can be complex in nature and require the input and efforts of many stakeholders. A data scientist will lead the process, and it is important that a well-defined workflow is followed. The workflow will ensure that all stakeholders are on the same page and requirements are defined and met.

A data scientist will produce a solution that is effective and achieves organization and analytic objectives with the end goal of meeting an organization need. Keep in mind that the data science life cycle is not linear (Figure 1). Real-world problems will introduce hurdles that require the process to be iterative in nature. The life cycle will give structure to the process and ensure that the data scientist stays on task.

![data science life cycle](https://stlpdatalayerpro.blob.core.windows.net/blobs/4da680f6-a5bb-4200-b79b-67c3d0604c34.png)
<sub style="margin-left:15px">**Figure 1.** The data science life cycle. (Ref: [Microsoft](https://learn.microsoft.com/en-us/azure/architecture/data-science-process/overview))</sub>


# Phases of Data Science Life Cycle

Perusing the Internet, you will also find that different data science solution vendors have adapted the life cycle to fit their products and the solutions supported by their tools. The data science life cycle is briefly explained below:

## Business Understanding
 
“We fail more often because we solve the wrong problem than because we get the wrong solution to the right problem.” – Professor Russell L. Ackoff.

Data scientists are tasked with providing solutions to difficult organization problems, and those solutions should be supported by factual data. Prior to solving a problem, it is important to understand the context of the organization and the problem. This must include defining organization and analytical objectives as well as identifying data sources.

## Data Acquisition

This process involves obtaining data from various sources and may also require setting up a data collection task and infrastructure.

Subsequently, you will perform data preparation to ensure the data is ready for analysis.

* **Data Preparation.** This is the process of cleaning and transforming raw data prior to processing and analysis. This needs to be done carefully as assumptions made here may influence, or even limit, the use of the data during analysis.
* **Data Exploration and Cleaning.** The quality of your dataset will determine your success in meeting your objectives. Data exploration includes identifying variables, conducting univariate and multivariate analyses, identifying outliers, anomalies, and missing values, as well as feature creation and selection.

## Modeling

You will explore modeling and learn about choosing the appropriate model based on the problem. You will study algorithms to implement analytical models and tune their hyper-parameters to achieve the desired performance. You will learn about the balance between generalizability and performance. In general, you want your model to learn and perform well but also to be robust when tested on unseen data.

* **Feature Engineering** is needed to prepare proper datasets that are compatible with the suitable algorithms and to improve the performance of models by leveraging domain knowledge to capture the signal of interest in the features.
* **Model Training** is made efficient when you have adequately prepared your data and engineered new features. Model training involves maximizing performance and finding a balance between performance and generalization. Even in cases when a data scientist has collected millions of records, data should be considered and treated as a scarce resource since it may be expensive to obtain.
    * Models are trained on dedicated training data and evaluated on dedicated test data. Models should not be tested on the data they have been trained on. The ability to match the training performance on unseen test data is referred to as the model's ability to generalize. To operationalize this during training, a validation data set is often sampled from the test data to allow an estimation of test performance during training. In the life cycle, it is important that this separation is anticipated early because it may influence what parts of the data may be surveyed for feature engineering and model design at the beginning of the project without violating the training/test split.
* **Model Evaluation** is an essential step in the life cycle. Typically, analytical solutions are meant to provide results when fitted with different datasets or when new data is introduced. Depending on the nature of the task (as stated in the analytic objective), model evaluation will follow corresponding metrics and techniques that will be explored in this course.

## Deployment

Once you have evaluated your models to ensure accuracy and performance, you will deploy the model to an environment for application consumption.

# Roles in the Data Science Life Cycle

The data science process involves multiple steps that require the expertise of team members in defined roles. The data science team is the talent that will help develop the analytical solutions that meet the business objectives of a data-related problem. Certain organizations can provide the structure and support for the different responsibilities within the process. In smaller organizations, personnel in the data science process might wear multiple hats to ensure the efficient execution of tasks and the development of solutions. Below, you will find the roles of a typical data science team. This list of roles will vary depending on the domain, industry, and the size of the organization.

* **Data Scientist.** This role involves solving tasks using machine learning model development and statistical techniques. This individual identifies trends and patterns within the data and makes predictions based on trends. The data scientist will write code to support the data analysis and model-building process.
* **Data Engineer.** The data engineer specializes in working with data in databases and other large repositories.
* **Solutions Architect.** This is a customer-facing role that ensures end-to-end customer deployment for organization-related data services. The solutions architect interacts with clients to design, coordinate, and execute solution prototypes.
* **Machine Learning (ML) Engineer.** The ML engineer performs modeling tasks that are different than the tasks the data scientist performs in that the ML engineer is further away from the domain side of the project. The ML engineer spends a considerable amount of time programming and creating ML solutions but also needs to have strong statistical skills. An ML engineer may focus on implementing machine learning solutions for production that occupies a role between a data scientist and a data engineer.
* **Data/Business Analyst.** A data analyst has data gathering, analysis, and visualization skills. Like the data scientist, data analysts provide insights from data to inform decision-making. They develop key performance indicators and utilize business intelligence and analytics tools. Compared to data scientists, however, data/business analysts are typically firmly rooted in the business domain and are not necessarily as proficient in programming and advanced machine learning.
* **Software Engineer.** The software engineer handles the alignment between the objectives and solution and is responsible for integrating the implemented data-driven system into the appropriate applications within the enterprise.
* **Domain Experts.** Also known as subject matter experts, domain experts know the most about the problem. Their role is to help define the content and scope of the data science project. They are key participants in the process. A domain expert will provide organization needs and characteristics to the data scientists and eventually judge the solution as successful or not by assessing whether the objectives have been achieved or not.

***

activity:activity-author-data-engin-n57qyzv6