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
> [!IMPORTANT]
> This installation is for 1080p, if you have diff resolution, then run this cmd
- For 2k Resolution :
```
sudo cp Configs/2k/theme.txt /boot/grub/themes/Vimix/theme.txt
```
- For 4k Resolutions :
```
sudo cp Configs/4k/theme.txt /boot/grub/themes/Vimix/theme.txt
```

* Edit grub config file -
```
sudo nano /etc/default/grub
```
* Add this line, Give full path of your ``theme.txt`` file
```
GRUB_THEME="/boot/grub/themes/Vimix/theme.txt"
```
* Update grub configuration, just run -
```
sudo grub-mkconfig -o /boot/grub/grub.cfg
```
or If you have UEFI system

```
sudo grub-mkconfig -o /boot/efi/EFI/debian/grub.cfg
```
> [!IMPORTANT]
> Before running grub UEFI cmd, Change `debian` to whatever distro you're on, if you're not on debian. Better check the location


## Changing Background :
* If you want to change the background, there is two ways to do it :
* Two images in `Background` dir, just copy and rename it to `background` in  `/boot/grub/themes/Vimix` dir
* Second, just edit theme.txt file in /boot/themes/Vimix and replace whatever image file name.
* If you want to use diff image, then I'm not sure wheater it'll work or not, for max chances to work, export images through ``inkscape or GIMP`` in ``png or jpg`` format
