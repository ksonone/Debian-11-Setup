## Change user to sudoer

1. $ su -

2. $ visudo
Add user and give permission access as mentioned below:

  username ALL=(ALL:ALL) ALL

Save Changes

3. Logout and Login again

4. $ sudo -i
  enter user password to verify that user becomes sudoer or not.
  
  That's it.