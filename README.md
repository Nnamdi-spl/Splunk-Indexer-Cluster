<h1>Creating an Indexer Cluster in Splunk</h1>


<h2>Description</h2>
This project is a walk-through for creating a splunk indexer cluster in SplunkWeb.The indexer cluster implements a cluster manager as both License Master and Master node for the cluster.A Cluster Master manages an indexer cluster.It coordinates the replicating activities of the peer nodes to ensure high availability and automatic failover and tells the search head where to find data. It also helps to manage the configuration of peer nodes and orchestrate remedial activities if a peer in the cluster goes down.The topology consists of a cluster master,three peer nodes and a search head.

<br />


<h2>Lab Environment Setup</h2>

- <b>5 t2micro EC2 Intances running in AWS</b> 
- <b>Windows 10 work station (21H2)</b>
- <b>MobaXterm SSH Client</b>
<h2>Intances Set-up </h2>

- <b>Indexer1 - idx1</b> 
- <b>Indexer2 - idx2</b>
- <b>Indexer3 - idx3</b>
- <b>Cluster Master - cm</b>
- <b>Search Head - sh1</b>
<h2>Program walk-through:</h2>


![Install Splunk in 5 instances running in AWS with proper labels:] 
(https://user-images.githubusercontent.com/112047285/195969636-38bc839a-4ab5-4a57-bbc6-cc5c5ecb09c1.png)
<br />
<br />
Select the disk:  <br/>
<img src="https://imgur.com/tcTyMUE.PNG" height="80%" width="80%"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://imgur.com/a/V5byISk.PNG" height="80%" width="80%"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://imgur.com/ihxH4IO" height="80%" width="80%"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
