# Set Startup Boot Logo

[1] Go to path and edit
  
    sudo nano /etc/default/grub
    
    Find and change
    
    GRUB_CMDLINE_LINUX_DEFAULT="quiet"
    
    to 
    
    GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"
 
 [2] Save Changes
 
 [3] Run Following Command
  
     sudo update-grub
     
 [4] Finally, reboot System...That's it!!
