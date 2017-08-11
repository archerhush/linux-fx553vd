# linux-fx553vd
An ArchLinux package which gains more compatibility to the newest GL, FX laptop models (GL553VD, FX553VD, and similar) with Linux by
installing the custom kernel, which is based on the latest stable 
**Linux 4.12.4** base kernel.

Successfully tested on an FX553VD laptop.

### overall patches
- <del>Parts of *Endless OS* kernel which enable support of any function 
key (except keyboard backlight control).</del>
- Keyboard backlight control support.

### setup

Before you compile everything yourself, you'll need to import `gpg` public keys of the Linux kernel mantainers in order to verify source file signatures:

    ~ $ gpg --recv-keys 79BE3E4300411886 # Linus Torvalds
    ~ $ gpg --recv-keys 38DBBDC86092693E # Greg Kroah-Hartman (Linux kernel stable release signing key)

after that, build the package:

    ~/linux-fx553vd $ makepkg -s

### installation

After the package has been built correctly, you can install it by launching:

    ~/linux-fx553vd $ pacman -U linux-fx553vd-4.12.4-1-x86_64.pkg.tar.xz

# conclusion

This project is supposed to be in a constant evolution until the stock kernel will not be completely congenial to these laptops. Please, report
new patches when you can to help to let the work grow up.
