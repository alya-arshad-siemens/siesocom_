**COMMISSION AND START THE ACCOUSTIC EVENT DETECTOR (AED) TIER**
--------------------------------

![aed1](https://user-images.githubusercontent.com/100555586/156131130-2da497da-3a59-4b60-8fb5-1875c0fb68b3.png)


1.	Proceed to the management section of Edge Apps, then click "Commission New":
 

 ![mb2](https://user-images.githubusercontent.com/100555586/156117279-59925e9e-8aff-46da-9dde-b2bdd8ebc158.jpg)


2.	Fill the edge app commissioning form following the example below. Each field brings a popup window that proposes the list of available options.

   We set the name this tier "S_2-AED", the image to select for the message bus is "SiESoCom EIP Base Application 0.1", its version is "EIP Base Application 0.1", the Edge 
   Core we deploy onto is "L890006" and the setup is "SiESoCom_2", per our target topology.

   **Note:** _The edge app name shall be unique and this rule is enforced by the portal._

![aed2](https://user-images.githubusercontent.com/100555586/156133146-2a6715ca-e78b-4bd3-853b-a9750427481f.png)


 
3.	After clicking on "Commission New", the edge application is commissioned. In this example, we rely on the default configuration, so no configuration is required here.

![aed3](https://user-images.githubusercontent.com/100555586/156133170-6ccd0b48-9993-446f-abe5-cf17c3a8c853.png)




4.	Proceed to "Operation" and click on "Deploy". This operation will copy the edge app image on the target edge core if not already there. It can take some time. Monitor the "State" indication until it transitions to "Created"


![aed4](https://user-images.githubusercontent.com/100555586/156133195-9e73e72d-4642-4ec0-9c14-42875feaf618.png)

![aed5](https://user-images.githubusercontent.com/100555586/156133234-e18a8b0b-5d56-45ad-96e5-b5531b56543a.png)



5.	Click on "Start" button to actually start the S_2-Bus edge app. The edge app state will transition to 'Started'.

![aed6](https://user-images.githubusercontent.com/100555586/156133259-8e9a74d8-bdd4-4a8d-b49c-a88d0eb32d87.png)


 
6.	Verify the application reported properly to the infra by checking its Status. 'Status.State' parameter that shall be 'Ready', per the following snapshot.

![aed7](https://user-images.githubusercontent.com/100555586/156133274-c0169ab0-60d2-40df-8afa-4e2bde399fa5.png)


**Notice:** _M3 edge applications have 2 states of importance: The container state that can be {commissioned, started, stopped, exited} and the application state that can be {not started, Initializing, Ready}. For an edge application to be operational, its container state has to be 'started' and its application state has to be 'Ready'._

 
•	After the AED tier container has started, the system integrator is expected to input the (python) plugin file name : After clicking on the 'edit' icon of the "Plugin Package File" configuration, the user is presented with the list of eligible plugin processors.

![aed9](https://user-images.githubusercontent.com/100555586/156133366-4e8b92f8-92c5-4313-90ed-1ecdc120a163.jpg)


•	Clicking on "Apply Configuration" button will then commit the request and the plugin processor will be deployed on the base application.

•	After the plugin has been deployed, the "Pipeline Deployment Configuration" config is populated and enables the "Input EndPoints" configuration to be set by the user: After clicking on the 'edit' icon of the Input Endpoint configuration, the user is presented with the list of eligible endpoints. One or many endpoints can selected by holding the "Ctrl" key of the keyboard while selecting the endpoint from the list.
 
![aed10](https://user-images.githubusercontent.com/100555586/156133393-1f0baeff-a01b-45e2-9a70-7d58bd2b9a5c.jpg)


•	Clicking on "Apply Configuration" button will then commit the request and define the input stream(s) that the AED tier will process.

**Note:** _A given plugin can be further configured via the deployment of a "Plugin Configuration" file. The deployement of such a file does not require the user to re-map the endpoints, enabling a dynamic re- configuration of the AED tier, e.g. the update of a trained model._

![aed11](https://user-images.githubusercontent.com/100555586/156133440-71c89f14-2759-4372-af6f-178b8212895d.jpg)

