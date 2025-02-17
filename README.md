# Daily_Dev_Update
Everyday log of my progress for the Audacity Open Source code contribution journey

17 Feb Monday:

Made the relevant change in colors.txt and created a Pull Request (https://github.com/audacity/audacity/pull/8238)

Working on building Au4 on local machine using the build instructions
*****************************************************************
14 Feb Friday:

Look into Audacity4, Backlog repos for new issues.
Discuss how the software developement process works, shortlist a few issues to start exploring.
*****************************************************************
13 Feb Thursday: 

Most bugs are obslete since Audacity repo is being moved from wxWidgets to Qt.
Asked more questions on which code would be retained so that I can work on that section.
*****************************************************************
12 Feb Wednesday: 

Changes in AllThemeResources.h not reflected in the debug build. So made changes in line 291 and 376 in FreqWindow.cpp file by manually coding the color codes (255, 200, 100).
Able to produce dark pink color text in frequency spectrum.
Asked question in Audacity forum regarding #7154. 
*****************************************************************
05 Feb Wednesday: 

Trying to understand the 2 errors and solve them.

Need to explore how I can contribute to Audacity through unit tests.
*****************************************************************
04 Feb Tuesday:

Conan wasn't being installed, so manually installed it using pip. 
"⁠ cmake -G "Unix Makefiles" .. " for the build.
Build and configuration done.
Used this cmd since I didn't use xcode for the build: "make -j$(sysctl -n hw.ncpu)"

Edited FreqWindow.cpp and ran the custom build. 2 fatal errors:
make[2]: *** [src/CMakeFiles/Audacity.dir/FreqWindow.cpp.o] Error 1
make[1]: *** [src/CMakeFiles/Audacity.dir/all] Error 2
make: *** [all] Error 2

But when I run via VSCode/BlackBox, the errors look different:
fatal error: too many errors emitted, stopping now [-ferror-limit=]
20 errors generated.
make[2]: *** [_deps/muse_framework-build/global/CMakeFiles/muse_global.dir/cmake_pch.hxx.pch] Error 1
make[1]: *** [_deps/muse_framework-build/global/CMakeFiles/muse_global.dir/all] Error 2
make: *** [all] Error 2
*****************************************************************
03 Feb Monday: 
With ChatGPT's help, I added FreqWindow.cpp to the list of compiling files within Build Phases tab, previoudly only 5 main files were being compiled.
Learnt that project settins and target settings are 2 different things. Project settings just has "Info, Build Settings, Phase Dependencies" tabs while Target tab has Phases and much more.

Analysing and the file (under product title bar) is successful, but on file compilation it throws "'FreqWindow.cpp' is not a member of any targets in the current scheme that build for analyzing".

Setting up a BlackBox Agent in VS Code to explain C++ code portions in detail, for me to understand the source files and attempt to circle the code pertaining to the issue/bug.

Along with my brother's guidance, I re-installed release-3.7.1 since Master was unstable. Problem with conan installation. Read error logs and config.logs, learnt git status, checkout, manual commands, -G means generate in "cmake -GXcode ../audacity". Installed "oh my zsh" on the terminal. Should figure out how to correct the error and run audacity app.

Tried the Unix cmake build command instead of xcode. 
*****************************************************************
Jan 31 Friday:

Going through YT tutorials on how to fork open source repos and implement changes.

https://www.youtube.com/watch?v=dLRA1lffWBw 
https://www.youtube.com/watch?v=o6xikISiz2w&t=57s 

Went through 1 latest merge request on Audacity repo: studied how they approach a problem, the code changes they suggest, the level of problems that are attempted.
*****************************************************************
Jan 30 Thursday: 

Not able to run Audacity app from the local machine repo. No code changes are implemented. Tried re-installing version 3.5.4
*****************************************************************
Jan 24 Friday: 
Setup Audacity repo on local machine + successfully built on XCode (Sonoma 14 Mac Target OS deployment). 

Choose issue #7154. Understood the PlotSpectrumBase.h and PlotSpectrumBase.cpp files. It led me to FreqWindow.h and FreqWindow.cpp where the dialog box color and text attributes lie. Need to understand this to make changes.
*****************************************************************
Jan 23 2025 Thursday: 

I decide to start my journey with Audacity. I read blogs appreciating the level to which an idea started by 2 CMU students can reach, all through sheer open source contributions. 

I was able to find the active projects but the guide states it would be difficult to understand a 20+ year codebase. So I decide to narrow down the scope to just rectify open P4 and P5 issues.







