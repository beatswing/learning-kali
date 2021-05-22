# Learning Kali

## Boot Kali 2021 on Raspberry Pi400
## Fix resolution on display settings
We needto update the configuration by

    # change to folder where config file should be updated
    cd /dev
    # create a tmp folder for mounting
    mkdir fixres
    # mount
    mount mmcblk0p1 fixresolution
    # change into folder
    cd fixres 
    # update config
    nano config.txt
    
    # uncomment overscan when you have black borders
    disable_overscan=1
    
    # uncomment to define required resolution (in my case dell26 inch lcd)
    framebuffer_width=2560
    framebuffer_height=1440
    
    # also enabled settings for pi4 (not sure if it was necessary)
    kernel=kernel8l-alt.img

    # unmount and reboot
    umount fixres
    reboot
