{{Page_Title|NAT}}
{{Flags
|High-level issues=Needs Topics
|Content=Incomplete, Needs Summary
|Checked_Out=No
}}
{{API_Name}}
{{Summary_Section|NAT is the system through which many computers are able to talk to outer world via only one ip address usually using ports enabling many more people to cohabit the internet's limited space. }}
{{Concept_Page
|Content=NAT:

Usually NAT service is provided through a router. In a home where someone has one Ip from there Internet Service Provider having router allows all of them to share this ip while still being distinguishable to outer world.

There are other ways than the following on how NAT may work, but most of the time it is as this:

Whenever a computer sends a request, Tcp/udp, the request contains many other small bits of information among the main information. The ones that enable NAT are Destination Port and Source Port. (see link)

Steps...
1. Server listening at port 80
2. Client/Chrome/Computer at local network sends request to www.example.com at port 80. (thus Destination Port = 80).
3. Client waits for it on whatever port, let's say port 200. (thus source port =200)
4. the request goes to router first as client is behind router.
5. The router takes the request change the Source Port to new number, let's say 400, and sends the request to www.example.com at 80. Also, remembers that any request that it receives for port 400 is for x ip/client at local network.
6. Server receives the request, since request's destination was aimed at 80, server accepts as it was listening on it. And return the request with new data at the ip address it received from, the ip address given by isp, and at the port which was defined in source port. So basically, switch the Source port with destination port. 
7. Router recieves the request, sees it is meant for port 400, which it knows mean some computer in local network so it redirects that request to that ip address of local network which may look like 192.168.1.23 and where as its public ip may been something like this 67.123.0.345.

Link: http://sanjibmukherjee.info/http://sanjibmukherjee.info/wp-content/uploads/2011/11/fig2.jpg
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}