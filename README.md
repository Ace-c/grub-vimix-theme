![grub-theme](https://github.com/user-attachments/assets/115946bd-191d-413e-b234-45ca950d1226)

# Manual Installation :
1. Clone the repository
```
git clone https://github.com/Ace-c/grub-vimix-theme.git && cd grub-vimix-theme
```
2. Copy theme to user grub theme dir, if `themes` dir not present create it
```
[ -d /boot/grub/themes ] || sudo mkdir -p /boot/grub/themes 
```
```
sudo cp -r Vimix  /boot/grub/themes/
```
> [!NOTE]
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

3. Edit grub config file 
```
sudo nano /etc/default/grub
```
4. Add this line, Give full path of your ``theme.txt`` file
```
GRUB_THEME="/boot/grub/themes/Vimix/theme.txt"
```
5. Update grub configuration 
```
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

  
> [!WARNING]
> Changing background may work or may not be, Theme may break, to revert just fallback to original one. Or, If you follow these guidelines, there is very high chances it'l work 
>  * As long as you use the same file name `background.jpg` and `resolution`, it'll work for all jpg pictures
>  * Still not working then, `Rotate The Image` using this cmd `convert -auto-orient background.jpg background.jpg` 

