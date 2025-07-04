![grub-theme](https://github.com/user-attachments/assets/115946bd-191d-413e-b234-45ca950d1226)

# Manual Installation :
* Clone this repository
```
git clone https://github.com/Ayu-0/grub-vimix-theme.git && cd grub-vimix-theme
```
* Copy theme to grub theme folder, if `themes` dir not present create it
```
sudo cp -r Vimix  /boot/grub/themes/
```
> [!IMPORTANT}
> Default Vimix dir is for 1080p, if you have diff resolution, then there is install script for them, still want to do manually then just go to 2k or 4k vimix folders, then run next cmd

* Edit grub config file to use this theme -
```
sudo nano /etc/default/grub
```
* Add this line, Give full path of your ``theme.txt`` file
```
GRUB_THEME="/boot/grub/themes/Vimix/theme.txt"
```
* Now, It's time to update grub configuration, just run -
```
sudo grub-mkconfig -o /boot/grub/grub.cfg
```
or If you have UEFI system

```
sudo grub-mkconfig -o /boot/efi/EFI/debian/grub.cfg
```
