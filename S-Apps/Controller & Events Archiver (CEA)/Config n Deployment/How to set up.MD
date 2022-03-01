**COMMISSION AND START THE CEA**
------------------------------------


![cea1](https://user-images.githubusercontent.com/100555586/156120433-991589ce-98f9-4300-896b-9f38412b6781.png)



1.	Proceed to the management section of Edge Apps, then click "Commission New":
 

 ![cea2](https://user-images.githubusercontent.com/100555586/156120467-af176bca-16ba-42a2-8d4c-15c6f0447ad9.png)




2.	Fill the edge app commissioning form following the example below. Each field brings a popup window that proposes the list of available options.

   We set the name this tier "S_2-CEA", the image to select for the message bus is "Controller and Event Aggregator (CEA)", its version is "SiSoCom Controller", the Edge Core 
   we deploy onto is "L890006" and the setup is "SiESoCom_2", per our target topology.

   **Note:** _The edge app name shall be unique and this rule is enforced by the portal._

![cea3](https://user-images.githubusercontent.com/100555586/156120481-c146dde7-081d-4dfd-a135-8fab1a00a2aa.png)



 
3.	After clicking on "Commission New", the edge application is commissioned. In this example, we rely on the default configuration, so no configuration is required here.

![cea4](https://user-images.githubusercontent.com/100555586/156120508-93568f07-cdc0-4552-a5b3-028fec32804b.png)



4.	Proceed to "Operation" and click on "Deploy". This operation will copy the edge app image on the target edge core if not already there. It can take some time. Monitor the "State" indication until it transitions to "Created"


![cea5](https://user-images.githubusercontent.com/100555586/156120543-b7428bb4-56c3-48b4-8e70-55976ca39357.png)


![cea6](https://user-images.githubusercontent.com/100555586/156120570-49ece137-f6d8-4bd7-af45-fec5ae6859e1.png)



5.	Click on "Start" button to actually start the S_2-Bus edge app. The edge app state will transition to 'Started'.

![cea7](https://user-images.githubusercontent.com/100555586/156120583-5faa1ec0-d72c-4c15-a3fa-2d471af2c74b.png)


 
6.	Verify the application reported properly to the infra by checking its Status. 'Status.State' parameter that shall be 'Ready', per the following snapshot.

![mb8](https://user-images.githubusercontent.com/100555586/156117481-fbb31402-d060-407c-8565-3915adabaecd.png)


**Notice:** _M3 edge applications have 2 states of importance: The container state that can be {commissioned, started, stopped, exited} and the application state that can be {not started, Initializing, Ready}. For an edge application to be operational, its container state has to be 'started' and its application state has to be 'Ready'._
