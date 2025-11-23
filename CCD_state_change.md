## CCD State Change

_Do not follow instructions from here unless you wholly understand and accept any and all loss, damage, harm and liability as solely your responsibility._

1. Add in tpm

    `sudo modprobe tpm_tis_i2c_cr50`

2. Shut down tpm associated services

    `sudo rc-service trunksd stop && sudo rc-service tpm2-abrmd stop`

3. Run the tool as root

    `sudo gsctool -a -o`

4. When it says **'Press PP button NOW!'**

    TAP (POWER) _until you read_
    Device: `Another Press will be Needed!`