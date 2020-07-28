# Big Sur Automator (BSR) 0.1.7alpha is Released!
current version: 0.1.7alpha-r2
NOTE: I OWN NONE OF THE TOOLS AND STUFF THAT THIS AUTOMATOR USES. I DIDN'T MAKE THIS FOR PERSONAL GAINS. INFACT I MADE THIS FOR MAKE PATCHING MUCH EASIER FOR USERS. I'LL TAKE THIS REPOSITORY DOWN IF THE TOOL OWNER REQUESTS.
CREDITS: barrykn for the micropatcher used. https://www.github.com/barrykn/micropatcher

# How it works
BSR changes the whole step to make a patched Big Sur USB into simple lines of script texts. So rather than making a USB and fail, get help from the community over and over until you success, all you have to do is paste some lines of code made by an experienced guy into an app and let it happen automatically!

# Simple Guide 
1. Format your USB as the following: Map: GUID Partition Map | Format: HFS+ (macOS Extended Journal) | Name: volume | No caps in name.
2. open the text file in the repository, copy the texts in there, paste it into terminal, run it and let it happen. 
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
4. Don't run it just yes, now, remember when I told you to format the internal drive? If you selected the first name (Big Sur), type "Big\ Sur" (no quotes) and run it. If you chose the alternative name, type "BS" (no quotes) and run it.
5. reboot to the internal drive and everything "should" be fixed.

# Final Note
This is still in test.
