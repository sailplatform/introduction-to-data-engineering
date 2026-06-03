When dealing with data, especially in the realm of Data Engineering, we must understand its key properties. Data varies in many ways, and understanding those variations is a critical part of being successful in data science and data engineering. The properties of data can influence how we store, process, and analyze the data. Three key properties of data, in this regard, include structure, dynamicity, and granularity.

# Structure

The structure of data refers to how it is organized and formatted. Initially, most data was structured, neatly fitting into tabular databases and spreadsheets. But today, the increasing prevalence of images, videos, text messages, wearable device data, and social media content calls for more flexible databases. Hence, now we deal with structured data (like SQL table entries and CSV files), semi-structured data (like XML and JSON files), and unstructured data (like email, image files, and log data).

**Structured data** is organized in a highly systematic manner, usually in tables with rows and columns. The data types, relationships, and constraints are all well-defined. Examples include data stored in Relational Database Management Systems (RDBMS) like Oracle Database, MS SQL Server, MySQL, etc.

**Semi-structured data** does not conform to the formal structure of data models associated with relational databases or other forms of data tables, but nonetheless contains tags or other markers to enforce hierarchies of records and fields within the data. Examples include XML, JSON, or YAML files.


**Unstructured data** is information that does not have a pre-defined data model or does not fit well into relational tables. Unstructured data is typically text-heavy but may also contain data like dates, numbers, and facts. Examples include email messages, word processing documents, videos, photos, audio files, presentations, webpages, and many other kinds of business documents.

# Dynamicity

Dynamicity or volatility refers to how data changes over time. It is important to distinguish between static data and dynamic data. Real-world data can be quite dynamic, constantly changing as new data is continuously being generated and old data becomes out of date. Continuously and rapidly changing data, introduces new challenges for storage, processing, and analysis. Regarding these, understanding the level of dynamicity also becomes crucial. As a result, this dynamic nature of data requires data engineers to manage and maintain data integrity while still providing relevant and updated insights to data-driven applications and solutions.  

**Static data** is information that doesn't change after being recorded. Examples of static data might include a bank customer's birthdate or social security number, or the recorded revenue from a company's previous fiscal year.

**Dynamic data**, on the other hand, changes regularly and continuously over time, and the existing data might be updated frequently. Examples include stock prices, sensor data, or social network data.

# Granularity

Data granularity refers to the level of detail or resolution that the data provides. For example, hourly data about temperature is more granular than daily data. While higher granularity can provide more insight, it also means more complexity in processing and analyzing the data. The ideal level of granularity often depends on the specific application and context of the data.

**Fine-grained data** presents a higher level of detail, as they break down information into smaller, more detailed increments. For instance, recording daily temperature data at an hourly interval is an example of fine-grained data.

Conversely, **coarse-grained data** is less detailed and more aggregated. If we take the daily temperature data and only record the daily average temperature or only the daily high and low, we are working with coarse-grained data.


# Conclusion

Understanding the properties of data is crucial as they impact multiple aspects such as
- the type of database to be selected for storage
- the processing power needed
- the latency with which data can be accessed 
- the kind of analytics that can be done on the data

***

activity:activity-author-data-engin-awy3fucr