# Day In The Life Of:
Everyday log of my progress in Machine Learning, my project development and learnings

*****************************************************************
Apr 16 Wednesday:

Apr17 version and the team-wise driver model had only ~50% accuracy -> decided not to go ahead with this since I noticed severe bias and scores of Apr15 were slightly better
*****************************************************************
Apr 15 Tuesday:

Got good results: team-99.24, driver-87.76, track-91.81

Unfortuntely: branching code within build_model is incorrect: track model trained on driver model's architecture.
And driver model isn't performing well. Bias towards Logan Sargeant.
The team-aware driver architecture has not worked.

New code "train_17Apr2025.py" to take saved features + encoder -> to re-train driver and track model.
New team-driver mapping in place. New team-constrained driver model. 
*****************************************************************
Apr 14 Monday:

Code still running, takes 50 mins for 1 iteration. PC is laggy, not much can be done.

WASPAA paper format review.

Search ML research groups @GaTech + labs/faculty.
*****************************************************************
Apr 13 Sunday:

Got awesome performance from yesrterday's model. Really happy with the scores!

TEAM Results:
Test Accuracy: 0.9687
F1 Score: 0.9688

DRIVER Results:
Test Accuracy: 0.7463
F1 Score: 0.7444

TRACK Results:
Test Accuracy: 0.7973
F1 Score: 0.7976

Scripted a custom predictor.py code to display Pitch Contours + top 3 predictions on a random audio file. And it works soooo well!! Wow I'm impressed. After that setback with a bad model yesterday, this was a relief.

But I can't settle. Improved the model to make it more robust. Added a team-driver awareness since team was performing extremely well and driver model could be leveraged over that.

Decided there is no time to edit other race footages. Need to work with what we have. Started running train_15Apr2025.py
*****************************************************************
Apr 12 Saturday:

Tested the Apr 09 model on a few test audio and was NOT satisfied with its performance at all! I think those scores are the validation results, NOT TEST results.

Decided to revamp the code: worked on feature extraction + CNN BiLSTM model
Started running the code tonight

Decided to stop the timing and other activities since it would take too long and I'm already running late. We anyway have a lot of data to play with.

Also, started backing up data from hard drive to IDrive since the TB was getting too hot during processing and I was afraid I might loose the valuable data!
*****************************************************************
Apr 11 Friday:

New feature extraction + CNN code
Finished timing Singapore GP.

Ran on the 12 race dataset. Error: .h5 -> .keras model extension.
*****************************************************************
Apr 10 Thursday: 

Results for the mel-spectrogram model:
Team Classification:
- Number of teams: 10
- Test Accuracy: 96.06%
- Test Loss: 0.4057

Driver Classification:
- Number of drivers: 22
- Standard Test Accuracy: 89.53%
- Team-Aware Test Accuracy: 90.42%
- Test Loss: 0.5439

Track Classification:
- Number of tracks: 6
- Test Accuracy: 87.56%
- Test Loss: 1.1952

New model with ResNet50 pre-trained model

New csv for 12-race dataset

Separated pit stops to another folder.
*****************************************************************
Apr 09 Wednesday:

How to reduce loss + improve accuracy without overfitting? (Apart from increasing epochs 35->50)
Tried normalisation, less aggressive learning rate, adding dropout layers after every convolutional layer.
Finished timing British GP, continuing with Singapore GP.
*****************************************************************
Apr 08 Tuesday:

Chat with Jon Myers -> UC Santa Cruz, Swara Studio IDTAP project.

Run train.py on 6-race dataset -> got 08Apr F1 models:

Team Classification:
- Number of teams: 10
- Test Accuracy: 87.02%
- Test Loss: 0.6784

Driver Classification:
- Number of drivers: 22
- Test Accuracy: 78.42%
- Test Loss: 0.8180

Track Classification:
- Number of tracks: 6
- Test Accuracy: 20.68%
- Test Loss: 1.7262
*****************************************************************
Apr 07 Monday:

Mail Thomas Nuttall, Prof. Xavier Serra from UPF-MTG, Barcelona regarding research opportunity.
Mail GaTech admin office to initiate i20 and about financial documents.
Continue with Mexico recording race footage.
*****************************************************************
Apr 05 & 06: Indian Music Workshop @IIT Hyderabad!

Got to meet Prof. Xavier Serra(UPF-MTG), Zack Zukowski (Stability AI) and many other students(UPF, QMUL) and professionals(Microsoft AI, Beatoven.ai) in the MusicTech field.
Discussed my F1 proj ideas and got valuable inputs.
*****************************************************************
Apr 02 Wednesday:

Continued Austin timing, last 2 driver povs remain. Abu Dhabi GP last 2 drivers footage remain. Aim to complete it overnight and start Las Vegas next.

Setup meetings with Uri Nieto and Philipp from FastF1.com

Completed the Amazon SDE coding test. Got a call to take up final interview rounds -> declined since I decided to go into GaTech Fall 2025.
Completed steps for my GaTech account BuzzCard and requested i20 form procedure to be initiateed.
*****************************************************************

Apr 01 Tuesday:
Continued USA Austin timing of driver povs + recording driver pov footage of Abu Dhabi GP 2024.
Had a violin concert in the evening
*****************************************************************
Mar 30 Sunday:

Finished lap times of Dutch GP. Started with US Austin GP.
Organised the issues in F1 log + noted improvisations to be made.
*****************************************************************
Mar 29 Saturday:

Finished noting lap times of Emilia-Romagna GP.
Finished 12 drivers' povs of Dutch GP
*****************************************************************
Mar 28 Friday: 

Relation btw Heisenberg's Uncertainty Principle and FT: https://www.youtube.com/watch?v=MBnnXbOM5S4 [3Blue1Brown YT vid]
*****************************************************************
Mar 27 Thursday: Understanding Fourier Transforms 

https://www.youtube.com/watch?v=spUNpyF58BY | https://youtu.be/8V6Hi-kP9EE?si=p7yIU2K08B3g-ruk 
https://www.youtube.com/watch?v=U7ii8agAhIs | https://www.youtube.com/watch?v=G74t5az6PLo 
https://www.youtube.com/watch?v=gz6AKW-R69s | https://www.youtube.com/watch?v=iOsGkk63NfE
*****************************************************************
Mar 26 Wednesday:

Mailed Prof Vinoo Alluri (IIIT Hyd), Prof Vipul Arora (IIT Kanpur), Swar-Studio UCSC, Philip Oehrly (FastF1.com) regarding research opportunities and contributing my F1 project to FastF1.com
*****************************************************************
Mar 24 Monday: Took 1 week break from life!

Started lapping F1 Emilia-Romagna Imola GP 2024 + Finalise ML resources to start learning
*****************************************************************
17 Mar Thursday:

After discussions and thinking, decided to switch my focus towards bettering myself at ML since my goals and future roles and much more aligned towards ML than generics Software Engg.
*****************************************************************
06 Mar Thursday:

"Cmd + Shift" shortcuts are detected and work well, while individual delete or backspace is not.

Discuss with my brother possible options to go ahead and tackle the issue.
*****************************************************************
05 Mar Wednesday:

Revise compiler Cherno YT
*****************************************************************
04 Mar Tuesday:

Investigating what exactly is wrong with track panel and keyboard connection.

What trackeditactionscontroller.cpp globalDelete() does: 
1. If a time selection exists, delete only the selected time range.
2. If no clips are selected, exit without doing anything.
3. If clips are selected, delete them.
*****************************************************************
03 Mar Monday:

Reverted changes in au3 files, the partial fix still works.
Created a PR with the modification in shortcuts.xml : https://github.com/audacity/audacity/pull/8362

Got a detailed good comment from a reviewer requesting changes.
*****************************************************************
01 Mar Saturday:

Trying to find the code-flow when delete key is pressed and how track-delete aciton is called. But I'm still not able to find alternatives to trackeditactionscontroller.cpp which is present in au3 dir

Tried injecting a FocusScope within trackslistclipsmodel.cpp and I was able to confirm that delete key could be recognised, but the code didn't take further action.

Analysed trackList() in au3trackeditinteractions.cpp, TracksListModel::onTrackRemoved() in trackslistmodel.cpp, TracksListClipsModel::load() in trackslistclipsmodel.cpp
*****************************************************************
28 Feb Friday:

Added functions:
* OnDeleteTrack() → FileMenus.cpp (for menu commands)
* DeleteTrack() → ProjectTrackManager.cpp (actual track deletion)
* Shortcut entry → shortcuts.xml

Created a PR and pushed my code which was a partial fix to #8115! (https://github.com/audacity/audacity/pull/8351)

PR closed since I did the changes in au3 legacy and au4 uses src. Investigating files in src to do the same changes
*****************************************************************
27 Feb Thursday:
Tried injecting a log stmt in shortcutsregister.cpp which didn’t work, so delete is not present and not recognised too.

Also, clip is deleted on delete keypress (via delete -> multi-clip-delete)
But when I click on left track panel and press delete -> press not even recognised in log.
Then again when I try to delete clip via keypress, that is not recognised too!! STRANGE how it changes behaviour once I click on track panel??

## 1 idea is to investigate Ctrl+S and see how that works and write delete-track in the same way:-

Ctrl+S is mapped inside FileMenus.cpp:
"Ctrl+S" triggers the OnSave function.
OnSave() calls: projectFileManager.Save();
it dispatches a save action for the current project.
*****************************************************************
25 Feb Tuesday:

Started my day with a rejection from MIT Media Lab for MS in MusicTech. Meh... feel sad but life still goes on..

Revised the diff btw function vs method vs struct vs class, different types of methods.

Analysed importShortcutsFromFile() from /Users/govindamadhavabs/audacity/_deps/muse_framework-src/framework/shortcuts/view/shortcutsmodel.cpp

Analysed shortcutsinstancemodel.cpp and started shortcutsregister.cpp
*****************************************************************
24 Feb Monday:

Analysis of UI-Based Track Deletion Logs
When you delete a track using the right-click Delete option, the logs show:
1. Audacity triggers the correct action: ActionsDispatcher::doDispatch | try call action: track-delete
2. Audacity recognizes a track deletion event: Au3TrackeditProject::onTrackListEvent | trackId: -1, type: DELETION
3. Errors related to QML (GUI) components appear, but the deletion still proceeds.

Key Difference Between UI Delete & Shortcut Delete

1. UI Deletion (Right-click → Delete) Works
    * The "track-delete" action is dispatched.
    * onTrackListEvent detects and processes the deletion.
2. Shortcut Key Deletion (Del Key) Doesn't Work
    * The "delete" action is dispatched instead of "track-delete".
    * No onTrackListEvent appears, meaning the track deletion event never happens.
Logs suggests that "delete" and "multi-clip-delete" are being dispatched when you press the Delete key.
However, when deleting a track via UI, "track-delete" is used instead.

Changes in /Users/govindamadhavabs/audacity/src/app/configs/data/shortcuts.xml and bool Au3Interaction::deleteTracks(const TrackIdList& trackIds) function in audacity/src/trackedit/internal/au3/au3interaction.cpp were unsuccessful.
*****************************************************************
21 Feb Friday:

AU4 is up and running. Need to sort the errors/bugs I'm interested in and start working.
I chose #8115 https://github.com/audacity/audacity/issues/8115

Found that keyboard shortcuts are handled through bindings. Searching through Track.cpp, trackeditactionscontroller.cpp, KeyboardCapture.cpp, KeyView.cpp to find where keyboard shortcuts are processed.
*****************************************************************
20 Feb Thursday:

Learnt how to use a VPN via YT vid
Installed Qt 6.2.4 using a VPN (vpngate and macOS build in network settings)

Took 7 hours to download the 4.61 gb Qt requirements. 
*****************************************************************
19 Feb Wednesday:

Qt installer not working. Manual installation caused missing files error (Qt_Network_Auth.pri)
LWinterberg recommended me to use a VPN since my IP could be getting blocked.

Revised how a program is executed in cpp, how a compiler works (Cherno YT)
*****************************************************************
18 Feb Tuesday:

Working on building Au4 on local machine using the build instructions.
Qt was causing problems. Manually installed it.
Converted "configure" file from Windows style to linux using "dos2unix configure" command.
ls -l <filename> searches for a file within a dir
*****************************************************************
**17 Feb Monday: MY FIRST PR!!

Made the relevant change in colors.txt and created a Pull Request (https://github.com/audacity/audacity/pull/8238)
The target release was set to release-3.7.1, changed it to release-3.7.2
Learnt cherry-pick command to pick only my commit and leave out the rest of the PRs in this release. Then pushed my PR once again.
My PR: https://github.com/audacity/audacity/pull/8239
Closed bug: https://github.com/audacity/audacity/issues/7154
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







