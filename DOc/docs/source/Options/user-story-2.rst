Managing data pipelines with full lineage
=========================================
.. _userStory2:


.. raw:: html

      <iframe width="560" height="315" src="https://www.youtube.com/embed/gt-NzPn5KCU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

.. raw:: html
    <br/>


User story
----------

In many organizations data is ingested from various source systems and
then transformed and consumed based on different technologies. While the
technologies are specific to the organization, data processing usually
is based on multiple transformation steps. Changing the output of a
source or a transformation step is potentially impacting subsequent
transformation steps. A data scientist changing the output schema of his
analysis or a data integration expert altering the output of a
transformation step use an impact analysis to investigate whether the
planned change is affecting other transformation steps or data users.
The challenge is to identify how the data is used and if it is being
used, who is the responsible person owning this part.


Overlooking a dependent transformation step or a data usage can cause
subsequent data processing to fail with a consequence of having inconsistent or
wrong data in other systems or in dashboards used for decision making.


As part of data governance also lineage information is collected in
Aurelius Atlas. That is, capturing the data processing and the data
usage as processes, where each process may consume data and may produce
data. Looking at the lineage graph directly shows the consumers of data,
which allows to relate it to the responsible persons.


To illustrate the process of finding relevant information from a lineage
graph and who is responsible, the following scenario is
described: An implementer of data pipeline wants to extend the schema of
a particular table. To make sure that the subsequent processing will not
fail, he wants to know who is using the data such that the subsequent
processing is also adjusted.

Step by step guide
------------------

You can search for the table **NL1-HR-001** in the technical context



.. image:: imgs-user-story2/first.jpg 


You get a list of results, lets click on the called **NL1-HR-001**


.. image:: imgs-user-story2/second.jpg 


As you can see in the detail page of the dataset, you have all
these elements:


.. image:: imgs-user-story2/third.jpg 


``1. – Name and type of the dataset.``

``2. – Hierarchy: Where it is located inside the system.``

``3. – Description.``

``4. – Summary of all the elements of the page.``

``5. - If the lineage model is available or not.``

``6. - Button to navigate through each section quickly.``

To find the Lineage model:

``1. – Click on the button.``

``2 – Click on Lineage Model``


.. image:: imgs-user-story2/fourth.jpg 


Once in the Lineage model, you click on the source to see the detail
page.


.. image:: imgs-user-story2/fifth.jpg 


In this detail page you can find all the information about the data, and
how it's being used.

Here is an overview of the elements on the detail page:

``1– Name and type of data.``

``2– Data governance.``

``3– Properties of the data.``



.. image:: imgs-user-story2/six.jpg 

Let’s follow the flow of the data, if you click on the next square
called **Change-event**, you can see how this data was changed to a Kafka
topic.

.. image:: imgs-user-story2/seven.jpg 


If you click on the next one, you can see that this Kafka topic was
converted into an **Elastic index**.

.. image:: imgs-user-story2/eigth.jpg 

With the lineage graphs you’re able to see where the data is going, this
is not limited to a particular system but it is across different
applications in which we are tracking the governance information.


**Benefits**

**1 – Clear information about where the data is stored.**

**2 – See the entire data flow step by step.**

**3 – How this data is being used.**

**4 - Track sensitive information.**

**5 – Improve data compliance.**