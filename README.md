# Daily_Dev_Update
Everyday log of my progress for the Audacity Open Source code contribution journey

Jan 23 2025 Thursday: I decide to start my journey with Audacity. I read blogs appreciating the level to which an idea started by 2 CMU students can reach, all through sheer open source contributions. I was able to find the active projects but the guide states it would be difficult to understand a 20+ year codebase. So I decide to narrow down the scope to just rectify open P4 and P5 issues.

Jan 24 Friday: 
Setup Audacity repo on local machine + successfully built on XCode (Sonoma 14 Mac Target OS deployment). 

Choose issue #7154. Understood the PlotSpectrumBase.h and PlotSpectrumBase.cpp files. It led me to FreqWindow.h and FreqWindow.cpp where the dialog box color and text attributes lie. Need to understand this to make changes.

Jan 30 Thursday: 

Not able to run Audacity app from the local machine repo. No code changes are implemented. Tried re-installing version 3.5.4

Jan 31 Friday:

Going through YT tutorials on how to fork open source repos and implement changes.

https://www.youtube.com/watch?v=dLRA1lffWBw 
https://www.youtube.com/watch?v=o6xikISiz2w&t=57s 

Went through 1 latest merge request on Audacity repo: studied how they approach a problem, the code changes they suggest, the level of problems that are attempted.

03 Feb: 
With ChatGPT's help, I added FreqWindow.cpp to the list of compiling files within Build Phases tab, previoudly only 5 main files were being compiled.
Learnt that project settins and target settings are 2 different things. Project settings just has "Info, Build Settings, Phase Dependencies" tabs while Target tab has Phases and much more.

Analysing and the file (under product title bar) is successful, but on file compilation it throws "'FreqWindow.cpp' is not a member of any targets in the current scheme that build for analyzing".

Setting up a custom GPT to explain C++ code portions in detail, for me to understand the source files and attempt to circle the code pertaining to the issue/bug.


