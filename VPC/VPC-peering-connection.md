Here is your content written as it is from all the images 👇


** VPC Peering Connection Steps
```
Prerequisites:

 1.You must have two VPC’s with non-        overlapping CIDR
 2.You must have same account here
 3.VPC-A with CIDR range of 10.0.0.0/16
 4.VPC-B with CIDR range of 172.168.0.0/16
5.CIDR range should be different
6.Create 2 Linux instances in each VPC





Step 1 :

In the navigation pane choose peering connection and create peering connection


---

Step 2 :

Configure the following information and choose creating peering connection when you are done.

Peering connection Name tag: You can give the name to your VPC peering connection

1. VPC (requestor): Select the VPC in your account with which you want to create the VPC peering connection


2. Under Select another VPC to peer with ensure My account is selected


3. Select another of your VPCs


4. The CIDR for VPC-B is automatically populated when selected in the VPC (Acceptor) field


5. You may add an optional tag but you need to click on Create Peering connection




---

Step 3 :

In the confirmation dialogue box click OK


---

Step 4 :

1. Select the VPC peering connection that you created


2. Click on Actions dropdown menu


3. Select accept request




---

Step 5 :

1. In the confirmation dialogue choose Yes, Accept


2. A second confirmation dialogue displays choose to modify my route tables now to go directly to the route tables page or choose close to do this later




---

Step 6 :

Modify the routing tables of VPC-A & VPC-B to permit routing between the VPCs via the peering connection

1. Select the routing table for VPC-A


2. Click on the routes tab


3. Click on edit routes


4. Click on add route


5. Input CIDR for VPC-B


6. Select the peering connection ID as a target for the route


7. Click on save routes




---

Step 7 :

Modify the routing tables of VPC-A and VPC-B to permit routing between the VPCs via peering connection

1. Select the routing table for VPC-B


2. Click on the route table


3. Click on the edit route


4. Click on the add route


5. Input CIDR for VPC-A


6. Select the peering connection ID as a target for the route


7. Click on save routes




---

Final Verification :
 On VPC-A’s routing table you can see a ocal route for its CIDR range as well  as route for VPC-B’s CIDR of           172.168.0.0/16 with the peering    connection as the target

On VPC-B’s routing table you can see local route for its CIDR as well as route for VPC-A’s CIDR of 10.0.0.0/16 with the same peering connection as the target

We can see all the information regarding the VPC peering connection and associated peers




Step 8 (Testing) :

Login to your Linux instance and just access the second instance using its private IP address with curl command

Example:

curl <second instance private IP>


```

