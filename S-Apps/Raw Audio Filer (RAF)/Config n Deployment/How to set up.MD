**COMMISSION AND START THE RAF TIER**
--------------------------------

![raf1](https://user-images.githubusercontent.com/100555586/156125928-b4590080-f760-4895-b97d-d3dd385cffa1.png)


1.	Proceed to the management section of Edge Apps, then click "Commission New":
 

 ![mb2](https://user-images.githubusercontent.com/100555586/156117279-59925e9e-8aff-46da-9dde-b2bdd8ebc158.jpg)


2.	Fill the edge app commissioning form following the example below. Each field brings a popup window that proposes the list of available options.

   We set the name this tier "S_2-RAF", the image to select for the message bus is "Raw Acoustic Filer (RFA)", its version is "Audio Stream Filer v1.0", the Edge 
   Core we deploy onto is "L890006" and the setup is "SiESoCom_2", per our target topology.

   **Note:** _The edge app name shall be unique and this rule is enforced by the portal._

![raf2](https://user-images.githubusercontent.com/100555586/156127433-c16eb679-c485-4307-ab42-dc35061daf57.png)


 
3.	After clicking on "Commission New", the edge application is commissioned. In this example, we rely on the default configuration, so no configuration is required here.

![raf3](https://user-images.githubusercontent.com/100555586/156127475-8297b888-3afa-4ee0-b884-e17e46a6b982.png)

4.	Proceed to "Operation" and click on "Deploy". This operation will copy the edge app image on the target edge core if not already there. It can take some time. Monitor the "State" indication until it transitions to "Created"


![raf4](https://user-images.githubusercontent.com/100555586/156127515-1030410b-305c-4137-9eba-592232000ed4.png)


![raf5](https://user-images.githubusercontent.com/100555586/156127540-7ec6fa1b-46ec-48ed-9e1d-88b66b811b43.png)



5.	Click on "Start" button to actually start the S_2-Bus edge app. The edge app state will transition to 'Started'.

![raf6](https://user-images.githubusercontent.com/100555586/156127608-e2d21df8-bfca-473a-98b5-53ac28f873e9.png)


 
6.	Verify the application reported properly to the infra by checking its Status. 'Status.State' parameter that shall be 'Ready', per the following snapshot.

![raf7](https://user-images.githubusercontent.com/100555586/156127651-2d214ff6-bd9e-47e3-bf70-5b4e243ff8cd.png)



**Notice:** _M3 edge applications have 2 states of importance: The container state that can be {commissioned, started, stopped, exited} and the application state that can be {not started, Initializing, Ready}. For an edge application to be operational, its container state has to be 'started' and its application state has to be 'Ready'._

 
After the RAF tier container has started, the system integrator is expected to set the 'Input EndPoints': After clicking on the 'edit' icon of the Input Endpoint configuration, the user is presented with the list of eligible endpoints. One or many endpoints can selected by holding the "Ctrl" key of the keyboard while selecting the endpoint from the list.

![raf9](https://user-images.githubusercontent.com/100555586/156127722-c171e470-9067-4316-b9ea-eb5e32234986.jpg)


•	Clicking on "Apply Configuration" button will then commit the request and define the acoustic stream the RAF tier will process.
