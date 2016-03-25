# NAND How-To #

### Prerequisites ###
  1. Make sure you have a charged battery (at least 70% in WinMo)!!!
  1. Must already have ADB working (Make sure you have all the drivers installed).
  1. Must have Fastboot working (related to ADB...)
  1. Be able to accurately report issues!!!
  1. Must have some knowledge on how to flash images!!! (using recovery)

### Things needed to download ###
(All Files found on the Downloads section of this project)
  1. Download this RHODIMG.NBH - LK bootloader for the rhodium
  1. Download this Recovery.img - Basic Recovery image
  1. Supported rom (OMGB or CM7 rc1)

### Clean Install Method ###
(Follow Carefully and be patient )
  * If you already have are running NAND perform a Task29!!
  1. Place the all zip files on your SDCARD
  1. Place the recovery.img in your Fastboot folder
  1. Flash the new NBH, LK will load (USB must be plugged in prior to starting)
  1. Open a CMD window and cd to your Fastboot folder
  1. Erase everything to start out fresh... (Not necessary if you performed a Task29)
    * In your CMD window type these commands:
      * "Fastboot erase recovery"
      * "Fastboot erase boot"
      * "Fastboot erase misc"
      * "Fastboot erase system"
      * "Fastboot erase data"
      * "Fastboot erase cache"
  1. Load the recovery.img with fastboot:
    * In your CMD window type this command:
      * "Fastboot flash recovery recovery.img"
  1. Reboot: (Or hit the reset button)
    * In your CMD window type this command:
      * "Fastboot reboot"
  1. Once LK is starting to load (Blue screen) press and hold the "POWER BUTTON" until you feel it vibrate(Top button). LK will let you know when it detected a press.
  1. Your recovery should load
  1. To Navigate in Recovery you can use the Vol UP/DOWN(Move UP/DOWN), END Call Key(Enter/Select) or the keyboard arrows with the enter key.
  1. Select "apply update from sdcard".
  1. Select "<your rom>.zip" and wait for it to finish installing.
  1. Select "reboot system now"
  1. Your device should now be installed and should load.

### Updating LK Bootloader ###
(After Feb 2012, LK can be updated from LK itself.)
  1. Boot into the boot loader from Android, or by booting with USB plugged in after a cold boot (Batt was pulled out and back in prior to boot)
  1. Download the LK update image ruu\_lk.img (Save this image where fastboot is located)
    * In your CMD window type these commands:
      * "Fastboot flash POOPLOADER ruu\_lk.img"
      * "Fastboot reboot"
  1. Once the phone restarts, notice the DATE and TIME on LK (should be the latest version)

## Revision History ##
  * May 23 2011: (Lmiller1708)
    * Initial Release
  * May 31 2011: (arrrghhh)
    * Added battery pull method to get into recovery. (Step 7)
  * Nov 10 2011: (acl)
    * removed obsolete instructions
  * Dec 05 2011: (acl)
    * Remove kernel update portion from main install
  * Jan 11 2011: (acl)
    * Remove the (cdma only part since gsm is now supported)
  * Feb 20 2011: (acl)
    * Add instructions to update LK.

