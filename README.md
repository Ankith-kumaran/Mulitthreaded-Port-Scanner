# **Multi-threaded-Port-Scanner**

This is a mini-project for the course 18CSC302J-Computer Networks.

<br>

# Overview

A Port Scanner is an application or a method to determine which ports on a particular network are open. 
In layman terms, it is basically a person knocking on doors to check if someone is home.
There are many reasons why a port scanner is implemented; running a port scan on a network/server reveals which ports are open and available to receive(listen state), 
as well as revealing the presence of security devices such as firewalls that are present between the sender and the target. This process is called fingerprinting. 
This process is used to check for and expose vulnerabilities in a network’s security system.
It is employed in most networking systems as a countermeasure to malicious attacks.

<br>

# Project Implementation

This project is to be implemented in the following ways:

First, we will create the port scanner using python as a programming language and implement it. 

We will choose the port range from 1-1023 as they are most common to be open. As we traverse through the ports, we will be classifying them into three categories, as follows:
Open or Accepted: The host sent a reply indicating that a service is listening on the port.
Closed or Denied or Not Listening: The host sent a reply indicating that connections will be denied to the port.
Filtered, Dropped or Blocked: There was no reply from the host.


After we have received the following information, we will display only the ports that are open, as those are the ports the network/server administrators have to be wary of due to malicious attacks by anonymous users. Hence, security protocols can be reinforced in these following ports to make sure information is being handled in a safe and secure way.

The project will be implemented using Python(Py3) , making use of multithreading concepts to make sure the ports are scanned in a faster and effective manner. A queue will also be used to store all the open ports which are then displayed after all the necessary ports are scanned.

The different Application Program Interfaces(API’s) used are as follows:
-Queue
+Socket
-Threading
+Pywebio


The program will be operated mainly in three modes. The three modes are described as follows:
Mode 1:  Scan ports from 1-1024
Mode 2: ports from 1-49152
Mode 3 : standard TCP and UDP ports

When executed, the user will be able to select a mode as required and then the selected ports will be scanned using multiple threads, to reduce time. When an open port is encountered, it is appended to the queue and then displayed in the end. The user can use this information either for establishing connection using these ports, or for checking for security devices such as firewalls.

