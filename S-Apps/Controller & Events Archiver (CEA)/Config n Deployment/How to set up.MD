**COMMISSION AND START THE CEA**
------------------------------------


![mb1](https://user-images.githubusercontent.com/100555586/156117260-68a63ac5-e872-4377-a6a0-1ef987594849.png)


1.	Proceed to the management section of Edge Apps, then click "Commission New":
 

 ![mb2](https://user-images.githubusercontent.com/100555586/156117279-59925e9e-8aff-46da-9dde-b2bdd8ebc158.jpg)



2.	Fill the edge app commissioning form following the example below. Each field brings a popup window that proposes the list of available options.

   We set the name this tier "S_2-CEA", the image to select for the message bus is "Controller and Event Aggregator (CEA)", its version is "SiSoCom Controller", the Edge Core 
   we deploy onto is "L890006" and the setup is "SiESoCom_2", per our target topology.

   **Note:** _The edge app name shall be unique and this rule is enforced by the portal._

![mb3](https://user-images.githubusercontent.com/100555586/156117329-90c85834-357e-46e6-ace4-8e3e32eb2f56.png)


 
3.	After clicking on "Commission New", the edge application is commissioned. In this example, we rely on the default configuration, so no configuration is required here.

![mb4](https://user-images.githubusercontent.com/100555586/156117363-be83617f-3faf-4856-830a-914a856d1302.jpg)


4.	Proceed to "Operation" and click on "Deploy". This operation will copy the edge app image on the target edge core if not already there. It can take some time. Monitor the "State" indication until it transitions to "Created"


![mb5](https://user-images.githubusercontent.com/100555586/156117395-e2d855d9-5d45-4e3f-853c-13b1ed878dbb.png)

![mb6](https://user-images.githubusercontent.com/100555586/156117429-dddc7af5-2b9a-4ba9-b29c-3618af0315f4.png)


5.	Click on "Start" button to actually start the S_2-Bus edge app. The edge app state will transition to 'Started'.

![mb7](https://user-images.githubusercontent.com/100555586/156117465-8478707d-f231-4257-89ea-a30430176d3a.png)

 
6.	Verify the application reported properly to the infra by checking its Status. 'Status.State' parameter that shall be 'Ready', per the following snapshot.

![mb8](https://user-images.githubusercontent.com/100555586/156117481-fbb31402-d060-407c-8565-3915adabaecd.png)


**Notice:** _M3 edge applications have 2 states of importance: The container state that can be {commissioned, started, stopped, exited} and the application state that can be {not started, Initializing, Ready}. For an edge application to be operational, its container state has to be 'started' and its application state has to be 'Ready'._
