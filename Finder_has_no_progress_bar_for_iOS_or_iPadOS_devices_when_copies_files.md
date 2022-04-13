# Finder Has No ProgressBar for iOS/iPadOS Devices when Copies files
## Issue
When connecting to a Mac, we can use Finder to copy files to iOS/iPadOS devices. However, during the copying progress, there is no progress bar. So it is hard to observe the copying state. The only indirect way to using Activity Monitor, which can shows the disk read speed from the disks that are connected to the Mac.

## Steps
1. Connected an iPad to Mac, click trust and input your password if needed.
2. Open Finder, find the iPad, choose Files.
3. Find a Video Player, for example, nPlayer.
4. Open another Finder. Find a mp4 or mkv file. The file should be bigger than 10GB. That will take more time to copy.
5. Drag the file to nPlayer. 

## Expected
A copy progress bar shows the copying progress.

## Actually Happened
There was no progress bar. The only UI changed happened when the copying was finished.