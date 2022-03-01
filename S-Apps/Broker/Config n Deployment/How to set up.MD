COMMISSION AND START THE MESSAGE BUS
------------------------------------

•	Proceed to the management section of Edge Apps, then click "Commission New":
 

 


•	Fill the edge app commissioning form following the example below. Each field brings a popup window that proposes the list of available options.

We set the name this tier "S_2-Bus", the image to select for the message bus is "Message Bus for Multi-tiered Setups", its version is "Managed-MQTT-Broker 1.3", the Edge Core we deploy onto is "L890006" and the setup is "SiESoCom_2", per our target topology.

Note: the edge app name shall be unique and this rule is enforced by the portal.



 
•	After clicking on "Commission New", the edge application is commissioned. In this example, we rely on the default configuration, so no configuration is required here.


•	Proceed to "Operation" and click on "Deploy". This operation will copy the edge app image on the target edge core if not already there. It can take some time. Monitor the "State" indication until it transitions to "Created"

 

 



•	Click on "Start" button to actually start the S_2-Bus edge app. The edge app state will transition to 'Started'.


 
•	Verify the application reported properly to the infra by checking its Status. 'Status.State' parameter that shall be 'Ready', per the following snapshot.



Notice: M3 edge applications have 2 states of importance: The container state that can be {commissioned, started, stopped, exited} and the application state that can be {not started, Initializing, Ready}. For an edge application to be operational, its container state has to be 'started' and its application state has to be 'Ready'


