# End3rV2-Klipper
My Klipper setting/configs as I constantly change/upgrade my Ender 3 V2.

Printer: Ender 3 V2  
Main Board: BTT SKR Mini E3 V3.0  
Extruder: Creality Sprite PRO  
Bed: Stock bed with Creality PEI sheet
Nozzle: Hardened Steel (0.4 mm) *Will be swapping to a ruby 0.4mm  

Other upgrades:
 - CR touch
 - Dual Z-axis (Currently using the Z splitter, however I plan to used both Z-axis connections on the SKR board in the future)
 - X-axis linear rail (Doesn't do much)

TO-DO:  
 - Tuning with Ellis' tuning guide https://ellis3dp.com/Print-Tuning-Guide/
 - Figure out how to add "if" statements to END_PRINT to prevent a 10mm Z move from hitting the Z limit after a tall print
 - Add LED light controlled by GPIO pins

Timeline of changes:
2024-Apr-29 - V2, V3
2024-Dec-08 - V4

########## 2024-Apr-29 ##########
 - Created "Archive" folder  
*** Archived V1 ***
V2 - UPDATES:
 - New config  
    -  Adjusted ROTATION_DISTANCE
    -  Added macros
        - START_PRINT
        - END_PRINT  
        - home_check
        - BED_MESH
        - PID_EXTRUDER
        - PID_BED
 - Added general macros from https://github.com/minimal3dp/klipper/tree/main/ender3v2-skr-mini-e3-v3  
     - These have been commented out for the time being  

*** Archived V2 ***
V3 - UPDATES:
 - I screwed up the END_PRINT macro and it was in absolute coordinates set to moved to Z10 after print... It hurt to watch
 - I corrected this, added a homing step, and then brought the bed to the front  

########## 2024-Dec-08 ##########
*** Archived V3 ***
V4 - UPDATES:
 - V4 was a fresh start since after V3 there was a major failure in the Pi 4B.
        - Cause of failure remains unkown. The board had the EEPROM updated, and a new SD card was used after a few failed installs.
        - NOTE* If the PI board does fail take the SD card out and access the non backed up files on a Linux computer. home>"PI name">klipper_config
   
 - V4 includes moonraker.conf, because the printer power is now GPIO controlled using a simple relay. The power cable had to be stripped to achieve this.
 - Switched to Mainsail OS since I needed to start from the ground up anyways.
 - START_PRINT has been changed so slicer temp is used.
 - Printer was mostly tuned using Ellis' tuning guide before SD failure.
        - Most of the settings were reused. But decreased all of the speeds and accels on my slicer.
        - I haven't redone the input shaper tests, but still use the recommended settings from the previous config.
