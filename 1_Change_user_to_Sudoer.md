## Change user to sudoer

[1] Run superuser command

    su -

[2] After become a superuser run following command:

    visudo

[3] Add user and give permission access as mentioned below [Do not forget to replace username with your actual user]:

    username ALL=(ALL:ALL) ALL

[4] Save Changes, Logout and Login again

[5] Open terminal and run following command :
    
    sudo -i

[6] Verify the user become superuser or not
  
[7] That's it.
