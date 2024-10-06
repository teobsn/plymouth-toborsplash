# plymouth-toborsplash
This is a Plymouth theme featuring a smooth throbber (spinner). It is meant to be used with a patched plymouth installation

# Installation

Clone this repository.

    sudo git clone https://github.com/teobsn/plymouth-toborsplash.git /usr/share/plymouth/themes/toborsplash

### Set theme as default

Verify list of themes:

    sudo plymouth-set-default-theme --list

Set the theme as the default:

    sudo plymouth-set-default-theme toborsplash -R

The -R option rebuilds the initrd automatically which is necessary.

## On Ubuntu

Install the theme.

    sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/toborsplash/toborsplash.plymouth 100

Select the default theme.

    sudo update-alternatives --config default.plymouth

Update the initramfs image.

    sudo update-initramfs -u

Reboot.
