**COMMISSION AND START THE AFE TIER**
--------------------------------

![afe1](https://user-images.githubusercontent.com/100555586/156128153-baadf221-87b5-4fcc-9d45-cb463c5ce791.png)


1.	Proceed to the management section of Edge Apps, then click "Commission New":
 

 ![mb2](https://user-images.githubusercontent.com/100555586/156117279-59925e9e-8aff-46da-9dde-b2bdd8ebc158.jpg)


2.	Fill the edge app commissioning form following the example below. Each field brings a popup window that proposes the list of available options.

   We set the name this tier "S_2-AFE", the image to select for the message bus is "SiESoCom EIP Base Application 0.1", its version is "EIP Base Application 0.1", the Edge 
   Core we deploy onto is "L890006" and the setup is "SiESoCom_2", per our target topology.

   **Note:** _The edge app name shall be unique and this rule is enforced by the portal._

![afe2](https://user-images.githubusercontent.com/100555586/156130535-91106f61-2489-4a10-8ed7-b9bc28ecf875.png)


 
3.	After clicking on "Commission New", the edge application is commissioned. In this example, we rely on the default configuration, so no configuration is required here.

![afe3](https://user-images.githubusercontent.com/100555586/156130555-4e274daf-295e-4501-97d7-c6e4a682e703.png)




4.	Proceed to "Operation" and click on "Deploy". This operation will copy the edge app image on the target edge core if not already there. It can take some time. Monitor the "State" indication until it transitions to "Created"


![afe4](https://user-images.githubusercontent.com/100555586/156130596-60df4b6c-c6ca-4f94-ba8a-20f668b0d6c1.png)


5.	Click on "Start" button to actually start the S_2-Bus edge app. The edge app state will transition to 'Started'.

![afe5](https://user-images.githubusercontent.com/100555586/156130657-76650995-b68d-47b3-ba34-5dbe640eed72.png)


 
6.	Verify the application reported properly to the infra by checking its Status. 'Status.State' parameter that shall be 'Ready', per the following snapshot.

![afe6](https://user-images.githubusercontent.com/100555586/156130675-722db91c-a38c-451a-a935-c37ac1e7f4cc.png)


**Notice:** _M3 edge applications have 2 states of importance: The container state that can be {commissioned, started, stopped, exited} and the application state that can be {not started, Initializing, Ready}. For an edge application to be operational, its container state has to be 'started' and its application state has to be 'Ready'._

 
•	After the AFE tier container has started, the system integrator is expected to input the (python) plugin file name : After clicking on the 'edit' icon of the "Plugin Package File" configuration, the user is presented with the list of eligible plugin processors.
 
![afe9](https://user-images.githubusercontent.com/100555586/156130772-287aff51-45f1-4bda-89fe-892c579a82cb.jpg)
 

•	Clicking on "Apply Configuration" button will then commit the request and the plugin processor will be deployed on the base application.

•	After the plugin has been deployed, the "Pipeline Deployment Configuration" config is populated and enables the "Input EndPoints" configuration to be set by the user:	After clicking on the 'edit' icon of the Input Endpoint configuration, the user is presented with the list of eligible endpoints. One or many endpoints can selected by holding the "Ctrl" key of the keyboard while selecting the endpoint from the list.

![afe10](https://user-images.githubusercontent.com/100555586/156130795-0cf71edd-f8da-4d2b-96b4-4984fa49d482.jpg)


•	Clicking on "Apply Configuration" button will then commit the request and define the input stream(s) that the AFE tier will process.
 
**Note:** _A given plugin can be further configured via the deployment of a "Plugin Configuration" file. The deployement of such a file does not require the user to re-map the endpoints, enabling a dynamic re- configuration of the AFE tier:_

![afe11](https://user-images.githubusercontent.com/100555586/156130839-8f8ac129-dcad-43c4-9a04-57b1155ef1ac.jpg)
