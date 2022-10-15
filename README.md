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



<br />
Install Splunk in 5 instances running in AWS with labels:  <br/>
<img src="https://user-images.githubusercontent.com/112047285/195969636-38bc839a-4ab5-4a57-bbc6-cc5c5ecb09c1.png" height="80%" width="80%"/>
<br />
<br />
Install a license on the cluster manager as License Master: <br/>
<img src="https://user-images.githubusercontent.com/112047285/195970522-64fec077-6b2f-4585-b5aa-bef62fafcff5.png" height="80%" width="80%"/>
<br />
<br />
Install License on the indexers and search head:  <br/>
<img src="https://user-images.githubusercontent.com/112047285/195970754-52da1399-9b84-4c1a-98ec-288dadea0573.png" height="80%" width="80%"/>
<br />
<br />
Enable clustering on the Cluster  Master to become the Master node and on the indexers as peer nodes:  <br/>
<img src="https://user-images.githubusercontent.com/112047285/195971004-d9acf47b-017a-4177-aa89-6381f2ceab38.png" height="80%" width="80%"/>
                                                             
<br />
<br />
Enable distributed search on the search head:  <br/>
<img src="https://user-images.githubusercontent.com/112047285/195971158-d01a4c98-8f84-49d6-a1e0-82c0cd5f2546.png" height="80%" width="80%"/>
<br />
<br />
Verify distributed search and clustering Configurations:  <br/>
<img src="https://user-images.githubusercontent.com/112047285/195971257-ae2a6155-bf6d-4c90-b21e-945263037a2f.png" height="80%" width="80%"/>
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
