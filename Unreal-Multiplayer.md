# Unreal VR Multiplayer Setup

This readme outlines step by step process to setup VR Multiplayer in Unreal Engine. 
<div style="margin: auto; width: 60%; padding: 10pt;">
<table>
<tr style="background-color:#FFEEEE;">
	<td style="border:0px;"><b>Meta Platform SDK</b></td>
	<td style="border:0px;">Platform SDK for login, group presence and Invitation</td>
</tr>
<tr style="background-color:#EEFFEE;">
	<td style="border:0px;"><b>EOS</b></td>
	<td style="border:0px;">Transport layer for Creation, Joining and Finding sessions</td>
</tr>
<tr style="background-color:#EEEEFF;">
	<td style="border:0px;"><b>UE4</b></td>
	<td style="border:0px;">Replication between <i>room members</i> with <i>the master client</i> as host.</td>
</tr>
</table>
</div>

SharedSpaces networking is divided into three layers.  The Meta Platform layer provides presence information needed to find and connect with friends.  
The EOS layer provides creation, finding, and Joining sessions.  And the UE4 layer handles the replication of game objects.

In this overview, we will explore each of these layers and show how we connected them together to make a
simple multiplayer application that allows people to connect and play together, without the need for a
dedicated server.

## EOS Setup [Reference](https://www.youtube.com/watch?v=KvyXSJ5vG3U&t=2294s)

First Sign in to [Epic Dev](https://dev.epicgames.com/en-US) and get to Dev Portal from top right button. 

![image](https://github.com/user-attachments/assets/e97bd6c9-0448-4852-9d7c-32b7a61279a6)

Create an Organization if not already present and create a new Product

![image](https://github.com/user-attachments/assets/6c923072-c516-4bf6-8254-6402332a9ac4)

After the product created, click it to configure it further.
You will first prompted to accept some agreements, scroll down and accept all to get started.

Now go to Product settings and there you would see your Product ID, and other Sandbox and Deployment ID, but not Client and Application ID, for that we first need to create a client configure it with permission that client has

![image](https://github.com/user-attachments/assets/fdf59501-3f8a-4a7b-b9dc-d0f8883c43fc)

Let's First create a new client, Click the Create Client button and give a name to your client

![image](https://github.com/user-attachments/assets/a8717532-8f1a-42b3-98b8-bbce41819647)

We would also need to create a Client Policy so lets create that first. Give a name and select PeerToPeer bcz we are creating a Peer to Peer connection here.

![image](https://github.com/user-attachments/assets/7954416a-1f87-41b4-9d29-4eefada8de39)

Now Scroll down and Select all the settings that you want to enable and Create the Client Policy.
After you are done, Click Add New Client and get back to Product Settings page.

Now lets create Application ID, So click New Application

![image](https://github.com/user-attachments/assets/6dfdeef9-3b70-416b-abc7-b5568014b75e)

There you see three things, Click Linked Clients to configure our client with the Application else authorization wont work, select your client and Save the Changes.

![image](https://github.com/user-attachments/assets/9e363c7a-0b61-48a9-a7e4-2bf3c22ec97a)

Now go to Permissions and Enable Online Presence, Friends and Save the changes.

![image](https://github.com/user-attachments/assets/9d84863e-aa47-434f-a2d0-6edcbbe241b5)

We dont need to configure Brand Settings now, when we are publishing then we need to configure it, thats it now go back to Product Settings
Scroll and you will see all the Ids created.


