Cross platform data governance
===================================
.. _userStory3:

User story 
----------
Data management uses solutions from different vendors, potentially even in different cloud providers or in a cloud, and some parts on premise.
The data governance solutions of the different cloud providers focus on data governance of their specific solutions.
Thus, for the organization it is very difficult to get an overview of the available data and the related data flows across the different solutions and platforms. 

This is a challenge, because there is no single source of truth for the data catalog to find the right information.
A data catalog's purpose is to provide an overview of available data in systems throughout the organization. 

By using Aurelius Atlas, data governance information from various independent systems can be collected and their data flows can be related. 
This way, Aurelius Atlas becomes the source of truth for the organization's data management.  

To illustrate the process of finding relevant information across various systems, the following scenario is described:
As an implementer of data pipeline, you want to update the schema of a particular table.
So you want to know who is using the data and where are this different data being used to make sure that they also adjust their schema and the subsequent pipelines. 

Step by step guide
------------------
In the `previous demo <userStory2>`__, you saw a lineage example where data was flowing across different platforms 

.. image:: imgs-user-story3/1.jpg


In this specific case, data is acquired from a **relational database**


.. image:: imgs-user-story3/2.jpg


``1 – Source data.``

``2 – Information about this data.``

``3 – Where it is stored.``

Then transferred into a Kafka topic to communicate the change events of the
relational database via **Change Data Capture (CDC)**

.. image:: imgs-user-story3/3.jpg


``1 – Source code.``

``2 – Information about this data.``

``3 – Where it is stored.``

``4 – Converted to a Kafka topic.``


Then the data is stored as a state in elastic search storage 

.. image:: imgs-user-story3/4.jpg


``1 – Source code.``

``2 – Information about this data.``

``3 – Where it is stored.``

``4 – Converted into an Elastic index.``


In the **lineage graph** of **NL1-HR-001** the implementor sees three different systems: a **SQL server**, a **Kafka system** and an **Elastic system**.
All data is consistently recorded across the different environments in **Aurelius Atlas**. 


.. image:: imgs-user-story3/5.jpg


Let’s click on **hr**(3), to see specific information related to this entity:

.. image:: imgs-user-story3/6.jpg


``1 – hr entity.``

``2 – Specific information about this entity.``

 

The available data is then visualized in a **Kibana dashboard**,
to access it, let’s click on the last event of the **lineage model**. 


.. image:: imgs-user-story3/7.jpg


``1 – Dashboard.`` 

``2 – Info about the entity.`` 

``3 - Kibana dashboard.`` 


**Benefits**

**1– Lineage graph shows database -> Kafka -> Elastic**

**2 – Different representations for different systems**

**3 – Type system is extendable** 