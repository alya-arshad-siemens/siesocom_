**COMMISSION AND START THE RAF TIER**
--------------------------------

![raf1](https://user-images.githubusercontent.com/100555586/156125928-b4590080-f760-4895-b97d-d3dd385cffa1.png)


1.	Proceed to the management section of Edge Apps, then click "Commission New":
 

 ![mb2](https://user-images.githubusercontent.com/100555586/156117279-59925e9e-8aff-46da-9dde-b2bdd8ebc158.jpg)


2.	Fill the edge app commissioning form following the example below. Each field brings a popup window that proposes the list of available options.

   We set the name this tier "S_2-RAF", the image to select for the message bus is "Raw Acoustic Filer (RFA)", its version is "Audio Stream Filer", the Edge 
   Core we deploy onto is "L890006" and the setup is "SiESoCom_2", per our target topology.

   **Note:** _The edge app name shall be unique and this rule is enforced by the portal._

![tsa2](https://user-images.githubusercontent.com/100555586/156124839-07f6f394-38bf-4542-9c6f-459e8b55316f.png)

 
3.	After clicking on "Commission New", the edge application is commissioned. In this example, we rely on the default configuration, so no configuration is required here.

![tsa3](https://user-images.githubusercontent.com/100555586/156124874-f8b815e8-9b60-4f69-89e9-b4385f413880.png)



4.	Proceed to "Operation" and click on "Deploy". This operation will copy the edge app image on the target edge core if not already there. It can take some time. Monitor the "State" indication until it transitions to "Created"


![tsa4](https://user-images.githubusercontent.com/100555586/156124900-49f518d0-4ff2-4a5c-a32e-35de7880e9cc.png)


![tsa5](https://user-images.githubusercontent.com/100555586/156124922-057e6979-c54f-40fc-847f-fd652137c54e.png)


5.	Click on "Start" button to actually start the S_2-Bus edge app. The edge app state will transition to 'Started'.

![tsa6](https://user-images.githubusercontent.com/100555586/156124955-60c1b4ad-8942-4d37-8528-442ad2566dfc.png)

 
6.	Verify the application reported properly to the infra by checking its Status. 'Status.State' parameter that shall be 'Ready', per the following snapshot.

![tsa7](https://user-images.githubusercontent.com/100555586/156125334-5c74d5ec-7887-4f6e-a024-4846c0e713de.png)



**Notice:** _M3 edge applications have 2 states of importance: The container state that can be {commissioned, started, stopped, exited} and the application state that can be {not started, Initializing, Ready}. For an edge application to be operational, its container state has to be 'started' and its application state has to be 'Ready'._

 
After the RAF tier container has started, the system integrator is expected to set the 'Input EndPoints': After clicking on the 'edit' icon of the Input Endpoint configuration, the user is presented with the list of eligible endpoints. One or many endpoints can selected by holding the "Ctrl" key of the keyboard while selecting the endpoint from the list.

![tsa9](https://user-images.githubusercontent.com/100555586/156125221-f1587d8a-5baf-4173-8805-0660d6479205.jpg)


•	Clicking on "Apply Configuration" button will then commit the request and define the acoustic stream the RAF tier will process.
