**COMMISSION AND START THE ACCOUSTIC EVENT DETECTOR (AED) TIER**
--------------------------------

![aed1](https://user-images.githubusercontent.com/100555586/156131130-2da497da-3a59-4b60-8fb5-1875c0fb68b3.png)


1.	Proceed to the management section of Edge Apps, then click "Commission New":
 

 ![mb2](https://user-images.githubusercontent.com/100555586/156117279-59925e9e-8aff-46da-9dde-b2bdd8ebc158.jpg)


2.	Fill the edge app commissioning form following the example below. Each field brings a popup window that proposes the list of available options.

   We set the name this tier "S_2-AED", the image to select for the message bus is "SiESoCom EIP Base Application 0.1", its version is "EIP Base Application 0.1", the Edge 
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

 
After the TSA tier container has started, the system integrator is expected to set the 'Input EndPoints' for both raw data archiving and acquisition control.
•	Raw data archiving endpoints:
These endpoints define the source of the data to archive in the data base.	After clicking on the 'edit' icon of the Input Endpoint configuration, the user is presented with the list of eligible endpoints. One or many endpoints can selected by holding the "Ctrl" key of the keyboard while selecting the endpoint from the list.
 
![tsa9](https://user-images.githubusercontent.com/100555586/156125221-f1587d8a-5baf-4173-8805-0660d6479205.jpg)


•	Acquisiton control endpoints:
These endpoints are the source of the data to file.	After clicking on the 'edit' icon of the Input Endpoint configuration, the user is presented with the list of eligible endpoints. One or many endpoints can selected by holding the "Ctrl" key of the keyboard while selecting the endpoint from the list.

![tsa10](https://user-images.githubusercontent.com/100555586/156125253-ba867b62-50ad-4de7-aa28-3aa834804362.jpg)


•	Clicking on "Apply Configuration" button will then commit the request and define the time series the TSA tier will process.


2.4.6	Commission and start the AED tier



 
•	After the AED tier container has started, the system integrator is expected to input the (python) plugin file name : After clicking on the 'edit' icon of the "Plugin Package File" configuration, the user is presented with the list of eligible plugin processors.


•	Clicking on "Apply Configuration" button will then commit the request and the plugin processor will be deployed on the base application.

•	After the plugin has been deployed, the "Pipeline Deployment Configuration" config is populated and enables the "Input EndPoints" configuration to be set by the user: After clicking on the 'edit' icon of the Input Endpoint configuration, the user is presented with the list of eligible endpoints. One or many endpoints can selected by holding the "Ctrl" key of the keyboard while selecting the endpoint from the list.
 

 


•	Clicking on "Apply Configuration" button will then commit the request and define the input stream(s) that the AED tier will process.

Note : A given plugin can be further configured via the deployment of a "Plugin Configuration" file. The deployement of such a file does not require the user to re-map the endpoints, enabling a dynamic re- configuration of the AED tier, e.g. the update of a trained model.
 

 


