Cross data platform data governance
===================================

(What is the problem?)

(Why is this a problem?)

(How we solve it?)

(Example scenario)

**To illustrate the process of finding relevant information, the
location of the data and who is consuming this one, the following
scenario is described:** A implementer of data pipeline, you want to
update schema of a particular table, so you want to know who is using
the data and where are this different data being used to make sure that
they also adjust their schema and the subsequent pipelines.

In the `previous demo <#_DON’T_KNOW_WHERE>`__, you saw how the data was
captured across platforms, so in our specific case here we use a
relational database and then a Kafka instance to communicate the change
events and then store the state in elastic search storage.

We make the data available in the Kibana dashboard, so here we have
three different systems a server a **SQL server**, a **Kafka system**
and an **Elastic system** and we record all data consistently across the
different environments in our Aurelius Atlas tooling

.. image:: imgs-user-story3/lineage.jpg


.. imgae:: imgs-user-story3/source.jpg

Benefits

**1 – Select dataset NL1-HR-001**

**2 – Lineage graph shows database -> Kafka -> Elastic**

**3 – Different representations for different systems**

**4 – Type system is extendable**