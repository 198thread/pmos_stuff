#### Boot Loop

_Do not follow instructions from here unless you wholly understand and accept any and all loss, damage, harm and liability as solely your responsibility._

This is the bootloop:
    _2s of_
    Device:_Your device is applying important updates, Please do not turn it off_
    Device: Screen off 
    _4s of_
    Device:_Your machine is applying important updates....._
    Device: Screen off 

1. Button sequence when stuck in bootloop of 

    Device:_Your machine is applying important updates....._
    HOLD (POWER + VOL_UP + VOL_DOWN) for 15s
    Device: Screen off
    TAP (POWER) **once**
    Device: _Nothing happens until 1-2 seconds later.._
    Device: _Please insert USB_
    TAP (VOL_UP + VOL_DOWN) **once**

    It should look like this:

    ```
    VOL_UP     ----__________________________________________________--------------------------__-----
    VOL_DOWN   ----__________________________________________________--------------------------__-----
    POWER      ----__________________________________________________------__-------------------------
                |                                       |                       |          |
                Your machine is applying...         Screen off             still off..    Please insert USB
    ```

    ##### Reboot into PMOS (Boot from internal HD)
    Device: _Dev Mode Boot Screen_
    TAP (VOL_UP) x 3 _ to choose Boot Device_
    TAP (POW) x 2 _boot from internal (or usb if you can)_

2. Check gsctool opened kernel options

    `sudo gsctool -a - I`
    should say 'CCD: Open'