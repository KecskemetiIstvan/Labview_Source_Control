# Labview_Source_Control
This is small tutorial of setting up verison control for Labview, with the built in LVCompare and LVMerge tools using SourceTree

## Getting Started

In this documentation I will show you, how to setup version control for Labview using Git. 
Requirements:
- Labview (version 20 was tested, but should work with any other before 21)
- SourceTree (or any other Git GUI of your choice)
- A remote repository (I have mine on GitHub)

Unlike other platforms, verison control wiht Labview is a bit different. Due to its graphical programming nature, none of the platforms are able to open and compare these files. NI has developed tools to solve this problem, namely LVCompare.exe and LVMerge.exe. In the following I will go step by step, how to connect a Git client with the Labview tools. 

## SourceTree

You can download Sourcetree from [here](https://www.sourcetreeapp.com/). After the setup is complete, the Git client should be installed also. Next you should connect your remote repository to the client, and clone it to your local disk. 

## Interfacing the two

To connect the Git client to Labview I have followed this [tutorial](https://gitlab.com/sas-blog/LVCompare-Merge-Setup/), which has everythin you need. In short, open a terminal in SourceTree and copy the following command:

`cd && git clone https://gitlab.com/sas-blog/LVCompare-Merge-Setup.git && cd LVCompare-Merge-Setup && ./setupLVTools.sh	`

This should clone the neccessary scripts to your disk, and setup LVCompare and LVMerge as the default diff and merge tools.
After that you should be ready to go!

## Usage

To compare remote and local files, you should select the "External Diff" option in the dropdown menu:

![ExternalDiff](https://github.com/KecskemetiIstvan/Labview_Source_Control/assets/135843312/f4fe3725-2e9a-480c-bdef-6920baee1818)

It should launch LVCompare.exe, where the differences are highlighted in circles:

![CompareTool](https://github.com/KecskemetiIstvan/Labview_Source_Control/assets/135843312/afdb9273-c496-488d-9a55-435346ee6e50)

If you want, you can launch these tools from command line using the:
`git difftool` and `git mergetool` command. Try `git help ...` for additional information. 

## Credits

This tutorial is just a small summary of the whole process, all credit goes to (https://gitlab.com/sas-blog), who made the needed scripts. 
