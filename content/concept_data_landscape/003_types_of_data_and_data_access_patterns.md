Data types can be seen as the 'nature' of data. They include structured, semi-structured, unstructured, and more recently due to the web — linked and graph data. Structured data includes data that conforms well to a tabular format, semi-structured data has some defined characteristics but doesn't conform completely to structured formats (like XML, JSON), unstructured data lacks a formal structure (like a plain text file, video), and linked data connects pieces of data, information or knowledge on the web.

# Types of Data Based on Their Structure

## Structured Data

When data has a pre-defined data model that contains a set of designated fields, it is called **structured data**. For instance, a person’s social security number can only be a specific number of characters, a person's birth may be limited to a 4-digit number or a person's marital status may be one of a few options. Relational database management systems are generally used to store and retrieve structured data.

Structured data may be either **quantitative** or **qualitative**.

![Diagram showing the categorization of structured data types](https://principlesofcomputing.blob.core.windows.net/ppp-data-analysis-concepts/images/1_structured-data-types.png)

### Quantitative Data

Data is **quantitative** if it can be counted or measured in numerical values, although we may also quantify uncountable entities to apply relevant data analysis techniques. Quantitative data answers questions such as, “What?”, “How many?”, and “How often?” and represents values on a continuum. Examples of quantitative data include height, weight, length, volume, temperature, age, exam scores, speed, time passed, number of items, price, and frequency of a repeated action or an observed event.

Commonly used descriptive statistics for quantitative data include:

* Mean: the average of values.
* Median: the midpoint value.
* Mode: the most common value.
* Frequency: the number of occurrences of a value on a given scale.
* Min and Max: the lowest and highest values in a given data set.
* Standard deviation: how the data is dispersed in relation to the mean.

Quantitative data can be further classified into **discrete** and **continuous** data.

* **Discrete data** only allows for specific whole number values (i.e., with no subdivisions) and is generally countable. There is always a separation between the succeeding and proceeding values, and the distance between any two consecutive values should be the same.
* **Continuous data** may have fractional values, can be infinitely divided into subdivisions, and has no specific intervals between data points. For example, continuous data variables may include an item’s height, weight, length, or volume, time passed, temperature, etc.

### Qualitative (Categorical) Data

**Qualitative data** are non-numerical, cannot be counted or measured in numerical values, and often measure described perceptions or emotions. Qualitative data describes qualities or characteristics (thus its name) and often answers questions such as “why?” or “how?”. Object colors, ethnicity, gender, professions, opinions, preferences, and attitudes are all examples of qualitative data.

Qualitative data can be further classified into **nominal** and **ordinal** data. Qualitative data may also be **binary**, which is a special category.

1. **Nominal data** refers to values that fall into unordered categories and that cannot be compared for being greater or smaller than others. For instance, ‘red’ cannot be greater than ‘blue’.

    The following is a list of some nominal data examples:

    * Spoken language (English, Spanish, Italian, French, Japanese, etc.).
    * Opinion on a topic (agree, neutral, disagree).
    * Type of bicycle (mountain, road, chopper, folding, BMX).
    * Project status (analysis, design, development, implementation, evaluation).
    * Marital status (single, widowed, married).
    * Smoking status (smoker, non-smoker).
    * Ethnicity (Native American, Afro-Caribbean, Asian, White, etc.).
    * Nationality (American, British, Indian, German, Chinese, Brazilian, etc.).
    * Gender (man, woman, non-binary, transgender, etc.).
    * Eye Color (black, brown, blue, etc.).
    * Hair color (black, brown, blonde, etc.)

2. **Ordinal data** refers to values that can be ordered and have a position relative to each other, such as competition rankings or letter grades.

    The following is a list of some ordinal data examples:

    * Degree of illness (none, mild, moderate, acute, chronic).
    * Opinion of students about classes (very unhappy, unhappy, neutral, happy, ecstatic).
    * Priority of tasks (high, medium, low).
    * Ranking in exam scores (first, second, third, etc.).
    * Level of education (primary ed., secondary ed., higher ed., graduate ed., post-doctoral).

3. **Binary (Dichotomous) data** is a specific type of qualitative data in which there are only two categories, just as is the case with Boolean values (e.g., Yes/No, True/False, On/Off). Binary data may be either nominal or ordinal.

    The following is a list of some binary data examples:

    * Smoking status (smoker, non-smoker)
    * Attendance (present, absent)
    * Pass-fail grade (pass, fail)
    * Membership status (member, non-member)
    * Priority (high, low)
    * Processing state (raw, processed)

## Unstructured Data

When data does not have a pre-defined model or a schema to be used as a base for arranging its elements, it is called **unstructured data**. Unlike structured data, unstructured data—such as text, audio, video, or images—is not fitting for traditional RDBMS. Because of its lack of predetermined schemas, unstructured data is more flexible and scalable, but it also forces us to use text queries or develop specific search algorithms in order to analyze it. Thus, in order to analyze and apply some statistical techniques to unstructured data, we should preprocess it into structured data first. From this perspective, gathering information from unstructured data resources is a general challenge and a cost factor.

Some examples of unstructured data include:

* The content of an email.
* The textual content in a file (e.g., txt files, pdf files, word processing documents, spreadsheets, presentations).
* Websites, ebooks, and online libraries.
* Mobile communication, SMS messages, phone recordings, chat, and instant messaging content.
* Digital photos, audio, and video files.

## Semi-Structured Data

**Semi-structured data** shows some of the organizational properties of structured data while also showing some of the flexible elements of unstructured data. Because of this, analyzing semi-structured data is easier than analyzing unstructured data, but also more challenging than analyzing structured data. Despite these data analysis challenges, semi-structured data may be easier to store and may be more fitting for projects involving changing requirements.

Some examples of semi-structured data include:

* XML Markup language.
* JSON-formatted documents. (Their structure consists of name-value pairs that can be arranged in a highly flexible way.)
* Email messages including their metadata. (Although the content of an email message may be unstructured, its metadata adds some structured data.)
* Log files. (Although log files may include unstructured data as content, they also typically provide a kind of structure for data processing.)



# Data Access Patterns
Data access patterns are ways in which data is accessed (read or written to) in a database or data storage system. Understanding data access patterns is important as they can impact the performance of applications, dictate the most appropriate storage solution, and cast light on optimization techniques for data retrieval.

There are various types of data access patterns, and among them, some of the most common are random access, sequential access, and transactional access. Random access allows data elements to be read or written in almost the same amount of time irrespective of their location. Sequential access is when data elements are accessed sequentially, e.g., reading lines of a file one by one. Transactional access involves complex read-write operations involving multiple items in a database.

### Random Access

Random access (also known as direct access) is a pattern where data elements can be read or written in almost the same amount of time irrespective of their physical location in a sequence of data. This is the quickest access pattern, allowing direct access to any part of the database.

### Sequential Access

In sequential access, data elements are accessed one after the other in a sequence. This pattern requires data to be accessed or retrieved in the same sequence in which it is stored.

A classic example of this access pattern is the old magnetic tape data storage, where you must go through each piece of data until you find the piece of data you're interested in. This pattern is less common today but can still be seen in certain niche applications or systems designed for high-throughput, like log-processing systems where data is almost always processed in the order it was created.

### Transactional Access

Transactional access refers to a sequence of operations (or transactions) that is performed on a database as a single logical unit of work. A transaction is bounded by certain properties commonly known by the acronym ACID, standing for Atomicity, Consistency, Isolation, and Durability [3].

Atomicity ensures the transaction is treated as a single, indivisible operation, consistency ensures that a transaction can bring the database from one valid state to another, isolation ensures concurrent execution of transactions without any conflicts, and durability ensures that once a transaction has been committed, it will remain committed even in the case of a system failure.

This pattern is common in database management systems, where, for example, debit and credit operations performed on a bank account are carried out as part of a single transaction to ensure consistent and reliable data handling.

*** 

Understanding these patterns and the nature of your data can assist in the design and selection of optimal storage schema and infrastructure.

activity:activity-author-data-engin-hpdrwuar
