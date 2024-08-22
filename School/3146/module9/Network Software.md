Network software
 - Special software needed on computer to enable networking
	 - I.e., to enable sending/recieving of data to/from computer
- Computer initiating data transfer
	- sender/source computer
- Eventual recipient of data
	- reciever/destination computer

Design goals
 - Reliability
	 - Should operate correctly
- Security
	- Should provide data protection
- Resource sharing
	- Should efficiently share available network resources
- Scability 
	- Should be able to support increase in size

Network software design
 - Layered design used to manage complexity of software 
	 - Divide responsibilities among different layers
		 - Each layer
			 - Abstracts set of services 
			 - provides well-defined interface to layer above it 
			 - Directly interacts only with layer immediately below and above it 
![](Pasted%20image%2020240313222144.png)


Layered approach 
 - Data travels from top to bottom layer on sender size 
 - Data travels from bottom to top layer on receiver side
 - Each layer uses protocol for interaction with same layer in other computers
	 - Although there is no direct interaction
	 - layer n of one computer understands information communicated by layer n on other computer 
![](Pasted%20image%2020240313222431.png)

Layering and protocol analogy 
![](Pasted%20image%2020240313222511.png)
