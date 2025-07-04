![grub-theme](https://github.com/user-attachments/assets/115946bd-191d-413e-b234-45ca950d1226)

# Manual Installation :
1. Clone this repository
```
git clone https://github.com/Ace-c/grub-vimix-theme.git && cd grub-vimix-theme
```
2. Copy theme to grub theme folder, if `themes` dir not present create it
```
sudo cp -r Vimix  /boot/grub/themes/
```
> [!IMPORTANT]
> This installation is for 1080p, if you have diff resolution, then run this cmd

> For 2k Resolution :
```
sudo cp Configs/2k/theme.txt /boot/grub/themes/Vimix/theme.txt
```
> For 4k Resolutions :
```
sudo cp Configs/4k/theme.txt /boot/grub/themes/Vimix/theme.txt
```
&nbsp;
3. Edit grub config file -
```
sudo nano /etc/default/grub
```
4. Add this line, Give full path of your ``theme.txt`` file
```
GRUB_THEME="/boot/grub/themes/Vimix/theme.txt"
```
5. Update grub configuration, just run -
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
- If you want to change the background, two ways to do it :
  - Ok, so there are two images in the `Background` , If you want to use that just rename it to `background` & replace it with the image file in  `/boot/grub/themes/Vimix` directory
  - Second, just edit theme.txt file in /boot/themes/Vimix and change the image file name or full path of the image.
* If you want to use diff image, then I'm not sure whether it'll work or not, for max chances to work, export images through ``inkscape or GIMP`` in ``png or jpg`` format
