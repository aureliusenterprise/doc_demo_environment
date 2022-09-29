Simple ways to get your data in
===============================
.. _simple:

**COMING SOON.....**

.. image:: imgs-access/404.jpg
..
    You can experience the user stories by yourself :ref:`clicking here<indexStory>`.  
    The demo environment is read-only, thus you will not be able to modify or create concepts yourself.  
    Aurelius Atlas provides several ways to get meta data in the application dependent on the use case of the user:

    1.	Creating Entities manually in the front end
    2.	Use an excel data dictionary that can bulk push multiple entities at once
    3.	Use the Lineage REST API that can be connected directly with a script or infrastructure

    An authorized data expert, e.g., that intends to simply change a certain definition of an existing attribute is better suited to apply this change via the front end. 
    However, a data steward that intends to load a set of data dictionaries covering a certain data base is better off providing this documentation in an excel data dictionary. 
    Furthermore, Aurelius Atlas provides a REST API (Lineage REST API) to establish a direct connection with the backend. 
    This can be used to push technical data that is automatically collected from the IT infrastructure by applying a scan or reading the files. 


    **1.Creating Entities manually in the front end.**
    --------------------------------------------------

    .. image:: imgs-simple/1.jpg


    ``1 – Click on the plus button``


    Then a side bar appears, to create an entity

    .. image:: imgs-simple/2.jpg


    Let’s have a close look on how to create an entity




    .. image:: imgs-simple/9.jpg


    ``1 – Entity type: this case is a Data domain.``

    ``2 – Name.``

    ``3 – Definition.``

    ``4 – Domain lead.``


    Once the fields are filled in, save and create your entity.

    .. image:: imgs-simple/3.1.jpg


    **2.Use an excel data dictionary that can bulk push multiple entities at once.**
    --------------------------------------------------------------------------------



    .. image:: imgs-simple/5.jpg


    ``1 – You can fill the name, description and data ownership rule.``

    ``2 – Use to create business data in bulk.``

    An excel data dictionary is a structured excel file, consisting of several sheets, matching the layers of the data governance model: each sheet corresponds to a specific model layer. 
    It is suppose to fill in the empty positions in the table of each layer. A subset of the tables columns in the excel file are inferred automatically, making sure that the input data is compliant with the data governance model. 
    Furthermore, the user is advised to follow the hierarchy of the of data governance model, starting with filling in the sheets that subsequentially correspond to their position in the data governance model layers. 
    The resulting excel data dictionary is required to be compliant with the predefined structure of the Aurelius data governance model. A script checks whether compliance is met and fills in the governance model application, based on the provided information of the excel data dictionary.


    **3.Use the Lineage REST API that can be connected directly with a  script or infrastructure.**
    --------------------------------------------------------------------------------------------------


    The Lineage REST API provides various endpoints to get and create (post) entities of different entity types. 
    To see the full list of the endpoints available and the required request fields, take a look at the **Lineage REST API swagger**. 
    (link to swagger)  
    A business can collect the metadata during creation or retrospectively during scanning from their technology, 
    and this can connect the API, to push the data to the solution.
    A script can scan the existing system or systems in place and make POST requests, to generate the entity on Aurelius Atlas capturing the technical systems, 
    collections, datasets, fields, and processes. Similarly, when deploying infrastructure as code, 
    requests can be made to the Lineage REST API to represent the components being deployed capturing the technical information. 

    In this image, you can see the swagger documentation of the Lineage REST API. 


    .. image:: imgs-simple/6.jpg


    Extending an option, you can see the expected payload or body that can be sent to the Lineage REST API to create the Generic Process Entity.


    .. image:: imgs-simple/7.jpg



        
