![grub-theme](https://github.com/user-attachments/assets/115946bd-191d-413e-b234-45ca950d1226)

# Manual Installation :

* Copy theme to grub theme folder, if not `themes` dir not present create it
```
sudo cp -r path-to-theme-folder /boot/grub/themes/
```
* Edit grub config file to use this theme -
```
sudo nano /etc/default/grub
```
* Add this line, Give full path of your ``theme.txt`` file
```
GRUB_THEME="/boot/grub/themes/your-theme-name/theme.txt"
```
* Now, It's time to update grub configuration, just run -
```
sudo grub-mkconfig -o /boot/grub/grub.cfg
```
