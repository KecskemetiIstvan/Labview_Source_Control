# Labview_Source_Control
This is small tutorial of setting up verison control for Labview, with the built in LVCompare and LVMerge tools using SourceTree

##Getting Started

In this documentation I will show you, how to setup version control for Labview using Git. 
Requirements:
- Labview (version 20 was tested, but should work with any other before 21)
- SourceTree (or any other Git GUI of your choice)
- A remote repository (I have mine on GitHub)
Unlike other platforms, verison control wiht Labview is a bit different. Due to its graphical programming nature, none of the platforms are able to open and compare these files. NI has developed tools to solve this problem, namely LVCompare.exe and LVMerge.exe. In the following I will go step by step, how to connect a Git client with the Labview tools. 

##SourceTree

You can download Sourcetree from [here](https://www.sourcetreeapp.com/). After the setup is complete, the Git client should be installed also. Next you should connect your remote repository to the client, and clone it to your local disk. 


