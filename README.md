# End3rV2-Klipper
My Klipper setting/configs as I constantly change/upgrade my Ender 3 V2.

2024-Apr-29  
  
Printer: Ender 3 V2  
Main Board: BTT SKR Mini E3 V3.0  
Extruder: Creality Sprite PRO  
Bed: Stock bed with Creality PEI sheet  
Nozzle Size: 0.4 mm  
  
Other upgrades:
- CR touch
- Dual Z-axis (Currently using the Z splitter, however I plan to used both Z-axis connections on the SKR board in the future)
- X-axis linear rail (Doesn't do much) 

2024-Apr-29  
- Created "Archive" folder  
*** Archived V1 ***  
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
- I screwed up the END_PRINT macro and it was in absolute coordinates set to moved to Z10 after print... It hurt to watch
- I corrected this, added a homing step, and then brought the bed to the front  

TO-DO:  
 - Tuning with Ellis' tuning guide https://ellis3dp.com/Print-Tuning-Guide/
 - Figure out why START_PRINT "default" temp is used and not the slicer
 - Figure out how to add "if" statements to END_PRINT to prevent a 10mm Z move from hitting the Z limit after a tall print
