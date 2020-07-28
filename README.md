# Big Sur Automator (BSR) 0.1.7alpha-r2 is Released!
current version: 0.1.7alpha-r2
NOTE: I OWN NONE OF THE TOOLS AND STUFF THAT THIS AUTOMATOR USES. I DIDN'T MAKE THIS FOR PERSONAL GAINS. INFACT I MADE THIS FOR MAKE PATCHING MUCH EASIER FOR USERS. I'LL TAKE THIS REPOSITORY DOWN IF THE TOOL OWNER REQUESTS.
CREDITS: barrykn for the micropatcher used. https://www.github.com/barrykn/micropatcher

# Before you start
This patch automator is still in test and it might have some issues in the command. So, please, PLEASE report issues in the issues tab. Keep in mind we don't provide support for broken macs using this script. 

# How it works
BSR changes the whole step to make a patched Big Sur USB into simple lines of script texts. So rather than making a USB and fail, get help from the community over and over until you success, all you have to do is paste some lines of code made by an experienced guy into an app and let it happen automatically!

# Simple Guide 
1. Format your USB as the following: Map: GUID Partition Map | Format: HFS+ (macOS Extended Journal) | Name: volume | No capitals in name.
2. open the provided text file in the repository, copy the texts in there, paste it into terminal, run it and let the script do all the magic. 
3. Reboot. If it doesn't boot into the USB, just option boot into the USB.
[this is where it gets risky. well not much... just a bit]
4. Open Disk Utility, select the entire internal disk and erase it as following: Format: APFS | Name: Big Sur | Alternative name: BS | Map: GUID Partition Map
5. Command + Q out of Disk Utility, open terminal (Menu bar > Utilities > Terminal) and type: /Volumes/Image\ Volume/set-vars.sh
6. Command + Q out of Terminal and install macOS normally on the internal disk. Come back after a few hours or so and Big Sur will be installed. Wait, this isn't the end. Maybe.
7. Set up your Mac and test if everything works well. If it doesn't, try following the optional guide.

# Kext Patch like a charm [Optional]
If some features are disabled like WiFi (most common), this extra guide will probably fix it. Big Sur drops support on some hardwares on old Macs. Well, fix it.
1. Boot into the patched recovery USB
2. Open up terminal (Menu bar > Utilities > Terminal)
3. Enter following: /Volumes/Image\ Volume/patch-kexts.sh /Volumes/
4. Don't run it just yet, now, remember when I told you to format the internal drive? If you selected the first name (Big Sur), type "Big\ Sur" (no quotes) and run it. If you chose the alternative name, type "BS" (no quotes) and run it.
5. reboot to the internal drive and everything "should" be fixed.

# Final Note
This is still in test.

# Release v0.1.7alpha-r2 changelog
Fixes lot's of command bugs.
Updated stuff (compared to 0.1.7alpha-r1-nfp)
- Fixes command typos
- Cuts the whole process of installing homebrew and WGET by replacing WGET with CURL
- Updates the link to download beta 2, the link may go down sometimes but much stable on unsupported Macs compared to beta 3.
- Fixes the issue where the PKG file downloaded won't install. It fixes the "File wasn't found" error, but requires the USB named "volume" to be plugged the entire process. Working on a alternative fix soon but this is the replacement for now.
- Now for downloading the patcher, it uses "git", not wget. This helps to cut the entire homebrew process but git command requires for Xcode command line utility to be installed, which may take some time. Working on a fix for this, but git is a alternative replacement for now.
- Jumped the release tag to release 1 (r1) to release 2 (r2), adding an extra "-alpha" to the version.
- Added the "rm" command to delete InstallAssistant.pkg and big-sur-micropatcher files to reduce space waste. Significantly reduces the downloaded size by 10 ~ 13 GBs. May have some leftovers, working on a fix for that.
- Updated README.md file over 10 times in less than an hour, changes made are too long to list.
