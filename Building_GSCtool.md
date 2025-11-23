## Building GSCtool (Late 2025)

1. Install deps
    `sudo apk add git build-base libusb libusb-dev linux-headers openssl-dev`

2. `git clone https://android.googlesource.com/platform/external/gsc-utils/`

3. `cd gsc-utils/extra/gsctool`

4. Make a **generated_version.h** in this directory with:
    ```
    #define VERSION "1.0.0"
    #define BUILDER "pmos"
    #define DATE "$(date)"
    ```

5. `sudo make`

6. Optionally install with
    `sudo install -m 755 gsctool /usr/local/bin/gsctool` 
    
    but I just go to the dir and run with 
    
    `sudo ./gsctool -a -I`