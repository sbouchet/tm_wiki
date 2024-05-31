

DSDP-TM Draft API Proposal by Pierre-Alexandre 2005x11x21
=========================================================

Last conf call we said we would start on API design. I was unsure where to start as I have no internal knowledge of RSE neither access to it. So I figured I'll start by throwing a draft mostly based on the presentation I did last year at EclipseCon just as a base for discussions as many people seemed to like it a the time. I found also the notes you mentioned in the [brainstorm notes from Chicago](https://www.eclipse.org/dsdp/tm/meetingnotes/ff01_chicago/DSDPTM_Brainstorming_2005-10-14.htm) and even though that was quite short I tried to use that as best as I could. I tried to integrate in my thoughts all the things I heard on calls and on this mailing list but I haven't had enough time to really go completely through the list so I apologize if some things are missing, badly named or in contradiction with some things said in the past.

Also I tried to understand the concept of Connector by Intel but I still don't get really my head around it so I was not sure how to add that here... maybe you or somebody else could explain me with an example, or add it directly to the design.

Now on the draft, I attached 2 diagrams. I used Umbrello on linux (coming the KDE SDK). I'll try to find something nicer for next time as I couldn't find the way to draw inheritance and a few other things. Anyway, there are not that many interfaces there so it should be easy to find your way. If not, I'll be glad to help you go through.

The 2 diagrams:

([Original UML file](https://www.eclipse.org/dsdp/tm/doc/rsf/rsfmodel.zuml) is available for [Poseidon for UML Community Edition](http://gentleware.com/downloadcenter.0.html))

[Diagram 1 - TM Core](/index.php?title=Special:Upload&wpDestFile=DSDP-TM_core_class_diagram_2005x11x21.png "DSDP-TM core class diagram 2005x11x21.png")
-------------------------------------------------------------------------------------------------------------------------------------------------------

[File:DSDP-TM core class diagram 2005x11x21.png](/index.php?title=Special:Upload&wpDestFile=DSDP-TM_core_class_diagram_2005x11x21.png "File:DSDP-TM core class diagram 2005x11x21.png")

DSDP-TM class diagram

First some details on my linguistic :)

*   Remote System: it represents a Target (sorry I have been too lazy to rename it from what I did before, but feel free to scratch that name ;))
*   CommunicationInterface: it represents an underlayer to communicate with the target, examples would be TCP/IP, serial, etc...
*   Service: it represents a service to get information from the target and accomplish some action. It is based on some protocols that comes on top of the communication interfaces (ex: ssh, ftp, ...). Examples of services could be a remote file system manager, a remote shell command, a terminal, etc...
*   ServiceType represents a category of service. It defines the API for that category so that the UI can make complete abstraction of the service implementations.

I cut the diagram in 2 parts. The first part, the Model, would be static information provided by extension points. It would be description of communication interface or services, what options they provide, etc... The second part, Instances, are instances of the model, definition of a real remote system, a service, etc... These data would be stored as launch configuration (though I am not sure if we want to store those data also in projects but maybe only in the .metadata)

[Diagram 2 - Draft API for a remote file system browser/manager](/images/7/72/DSDP-TM_RemoteFS_class_diagram_2005x11x21.png "DSDP-TM RemoteFS class diagram 2005x11x21.png")
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

![](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/300px-DSDP-TM_RemoteFS_class_diagram_2005x11x21.png)

[](/File:DSDP-TM_RemoteFS_class_diagram_2005x11x21.png "Enlarge")

DSDP-TM RemoteFS diagram

This defines remote resources, and quite a few standard things (inspired in part by the workspace resources APIs).

I am not sure what you want to do next and until where you want to go (defining more services API, defining some UI APIs...?), but I hope that this humble draft will help stir the discussion and make us patient for RSE... and hopefully when RSE will be out, it will be reasonable to think that we can make it use/implement this design...


(Migrated from [https://wiki.eclipse.org/DSDP-TM_Draft_API_Proposal_by_Pierre-Alexandre_2005x11x21](https://wiki.eclipse.org/DSDP-TM_Draft_API_Proposal_by_Pierre-Alexandre_2005x11x21))