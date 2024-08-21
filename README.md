# picore
a repository for my Pi5 laptop. 
This repository is just a holding place for design files at the moment.  

UPDATE 08-21-2024.

With the availablility of several Rockchip 3588 based CM4 form-factor boards, Ive decided to retool this project around a CM4-nano carrier board. Working on redesigning the chassis.  Ive also decided to use Decktility's (https://github.com/ByteWelder/Decktility/), power management which emulates a ltc294x chip for providing the system with battery/charging information using an arduino.  Very good work.  Mainly Ive been working on porting the code/drivers to work with Rockchip.  This is above my skill level but in theory it should be possible.  If you have any skill in this area and want to help, go ahead and reach out to me with an issue.

I DO NOT RECOMMEND USING IT AT THIS TIME!!! I made a lot of specific design choices that I don't care to explain right now, and the FreeCAD files are a bit of a mess. (and Im a novice for sure with freeCAD). And to add to that it's not complete. There is no top palmrest, any mounting points for the screen, nor a front bezel. Also the mounting points for the trackball interfere with installing the PI5. The PI exit ports for USB2, USB3 and ethernet do not quite line up right. All and all, you've been warned :) 

Parts:

1. Pi5 8GB, and Pi5 official cooler
2. Waveshare UPS - https://www.waveshare.com/product/ups-hat-d.htm
        Desolder pogo pins and make harness to go to GPIO for +5, G and 2xI2c.
        Desolder the USB A connector, and power switch (solder bridged to on).
        Desolder battery holders
        Mind your gauge wires. I was using dupont jumper wires soldered on one the waveshare side, and the dupont connector on the PI GPIO side and I was getting brown outs, and voltage warnings. Switched to
        slightly heavier gauge wire and now it's stable.
4. USB 2.0 Hub board - https://a.co/d/d6xFPpz
5. USB C PD Trigger Board - https://a.co/d/i6ZYw3r
6. 2x5000mAh Lipo (remove protection boards) - https://a.co/d/iKhJBcd
7. MNT Reform Trackball - https://shop.mntre.com/products/mnt-reform-optical-trackball-module
8. Vortex Core Keyboard - https://vortexgear.store/products/core
9. 10.5 1920x1280 LCD Monitor - https://a.co/d/gWEaZZS this monitor I needed to un-case to make it thinner and I broke it as it is extremely fragile. So Im using the board, and ordered just the panel which is: NV105WAM-N31 10.5” 1920X1280 - Same screen as a Surface Go 3 but without the touchscreen.  If you buy it in a case, I think you need to use a heat gun to remove the housing, as 90% is double sided tape that will torque the display, and it is so fragile you will destroy it.  
11. USB C 2.0 Solder connectors - https://www.amazon.com/dp/B091CRLJM2?ref_=cm_sw_r_cp_ud_dp_2WHZ4DZWF5TPE4Q6B9QM
12. Micro USB Solder connectors - https://a.co/d/3a1dL1D  for the keyboard
13. Random hookup wire for USB leads, power leads etc. Mind your gauge wires. I was using dupont jumper wires soldered on one the waveshare side, and the dupont connector on the PI GPIO side and I was getting brown outs, and voltage warnings. Switched to slightly heavier gauge wire and now it's stable.
14. HDMI Cables.  Still working this out, trying ribbon cables.  It remains to be seen if 1920x1280 will work on a ribbon cable (28-04-2024, still not stable - display comes up sometimes and not others. Sometimes touching the cable makes the display appear with a 300MM ribbon).  Plan B is to strip the plastic off the connectors to make them as small as possible.  Mini HDMI to Micro required for monitor and Pi5.  Maybe a better monitor could be found, but I wanted the 1920x1280 resolution and I could only find that in HDMI.  DSI seemed to max out at 1280x800 and didn't work at the ribbon cable length needed.   
15. Invisible furniture hinges - https://a.co/d/3a1dL1D
        These are not currently strong enough to hold up the screen/lid. Im working on the idea of drilling out the small rivot and            putting a 1mm bolt/nut combination so it can be tightened to a suitable tension.

Please use this information at your own risk. Personally I have "let the smoke out" of many parts working on cyberdecks and projects like this. No warranty expressed or implied.
