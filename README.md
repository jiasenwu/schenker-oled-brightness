See [system76-oled](https://github.com/pop-os/system76-oled)

# build the package
```
makepkg
```
Then run `pacman -U <path to zst file>` to install the package. The brightness adjustment shortcut should work after next login.

# debug
However it doesn't work as expected. You can diagnose with the following command.
```
RESUT_LOG=debug /usr/bin/system76-oled
```
And check the logs on the screen.
