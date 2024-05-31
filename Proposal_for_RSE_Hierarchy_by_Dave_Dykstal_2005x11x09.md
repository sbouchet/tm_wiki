

Talk:TM/Proposal for RSE Hierarchy by Dave Dykstal 2005x11x09
=============================================================

[Moberhuber](https://wiki.eclipse.org/User:Moberhuber "User:Moberhuber") \- 12-Nov-2005 -- For me, this is perfect. Its just exactly what I had in mind. Thanks for writing it up!

User:Uwe.stieber.windriver.com \- 17-Oct-2006
----------------------------------------------------------------------------------------------------------------------------------------------------------

Well, as for the hierarchy, for our product, we have to deal more or less with three different hierarchies. 2 of them (2 and 3) are known requirements but not yet available in the product as we had to deal with other issues.

1) This is our current hierarchy we would like support still with RSE (2.0?) simply for workflow reasons to our users/customers (small adjustments might be possible, see 4)). We would like to be able to introduce user definable filters on every level.

 <Network Shared Connection Store>
 	<Connection 1>
 	<Connection 2>
 		<Core 1>
 			<Processes> (for Linux targets)
 				<Process 1>
 					<Thread 1>
 					<Thread n>
 				<Process n>
 		...
 		<Core n> (possibly multi core targets)
 	<Connection 3>
 		<Core 1>
 			<Kernel Tasks> (for vxWorks targets)
 				...
 			<Real Time Processes> (for vxWorks targets)
 				...
 			<...> (other possible types might be having there own childs>

2) This is matching to the wish of connection groups. We have this requirement since a while, but have not yet worked on it since it become clear that we should base on RSE. We would like to group more or less a free definable collection of connections or cores.

 <Network Shared Connection Store>
 	<Target Connection Group Target 1>
 		<Connection 1 to Target 1> (purpose user mode debugging)
 			<Core 1>
 				...
 		<Connection 2 to Target 1> (purpose system mode debugging or system bring up)
 			<Core 1>
 				...

or

 <Network Shared Connection Store>
 	<Connection 1>
 		<Target Core Group "Engine Control">
 			<Core 1>
 				...
 			<Core 2>
 				...
 			<Core 3>
 				...
 		<Target Core Group "Entertainment">
 			<Core 4>
 				...
 			<Core 5>
 		...

or a combination of both.

3) Is more or less a extension to 2). It's the idea of shared board labs which may export/group network shared connection stores or connections. Of course, number 2 still applies here for everything below the stores.

 <Shared Board Lab 1>
 	<Network Shared Connection Store 1>
 	<Network Shared Connection Store 2>
 		...
 	<Network Shared Connection Store n>
 <Shared Board Lab 2>
 	<Grouped by criteria (i.e. architecture>
 		<Network Shared Connection Store 1>
 		<Network Shared Connection Store 2>
 		<Connection 1>
 		<Connection 2>
 		...
 	<Grouped by other criteria (i.e. booted Target OS)
 		...

4) We do have a very rough prototype running, which is more or less contributing to what RSE 1.0 like to see as hierarchy. It looks quite promising, but as it require to introduce a synthetic level to the hierarchy, which makes it looking not fully satisfying at the end.

The hierarchy of the prototype is:

 <connection identified by a name> (== system type)
 	<WR Debugger> (== sub system)
 		<Filter (All Cores)>
 			<Core 1>
 				<Processes>
 					...
 			...

The sub system level is obsolete and hindering (to us) as it only satisfies the hierarchy (from our point of view). It would be ok to keep the hierarchy of system type and sub system if a sub system can have the attribute "hidden" and the content provider would kind of skip the node within the tree.

Uwe Stieber  
Member of Technical Staff  
Engineering - Wind River Systems - Austria  

User:David dykstal@us.ibm.com \- 18-Oct-2006
---------------------------------------------------------------------------------------------------------------------------------------------------------

Uwe -- Thanks for looking at that hierarchy. I did that quite a long time ago as a sort of conceptual look at what I thought might be useful. Since you are doing an actual implementation what you come up with will probably be more correct for you.

I'll sit down with this and see what I can do to generate requirements against RSE from it.

It might be a good idea to post this in the R2.0 discussion wiki.

Dave Dykstal  
dykstal@acm.org


(Migrated from [https://wiki.eclipse.org/Talk:TM/Proposal_for_RSE_Hierarchy_by_Dave_Dykstal_2005x11x09](https://wiki.eclipse.org/Talk:TM/Proposal_for_RSE_Hierarchy_by_Dave_Dykstal_2005x11x09))