# Real Programmers Querty with italian punctuation

## Motivation
Inspired by ThePrimeagen's [Real Programmers Dvorak](https://github.com/ThePrimeagen/keyboards) and renerocksai [Real Programmer's QWERTY](https://git.sr.ht/~renerocksai/real-prog-qwerty).\
I in reality am a Colemak-DH user, but the key remaps are done via a programmable keyboard.\
As a Colemak-DH user I had to copy their work.\
I find it pretty comfortable, if you want a more in depth motivation just see what Harpoon (also v2 now) has to say.

## What it looks like
Will do when i have time, not bothered rn.

## Installation
I do forget how to install it so this is mostly a reminder to how dumb I am.
### Ubuntu
Used this on Ubuntu 22.04 using X11
- clone the repo
- put the layout on the right place
```
sudo ln -s /usr/share/X11/xkb/real-prog-qwerty real-prog-qwerty
```
You should be good and should now be able to activate the layout by:
```
setxkbmap -layout real-prog-qwerty
```
### Wayland
I dunno, may god have mercy on your soul.\
Probably something like 
```
ln -s ~/config/xkb/symbols/real-prog-qwerty real-prog-qwerty
```
Don't quote me on that tho
### NixOS
As I will probably run this shortly (also this is entirely taken from renerocksai)
```
sudo -i
mkdir -p /etc/nixos/xkb/symbols
cp real-prog-qwerty /etc/nixos/xkb/symbols/
```
then insert the following code into your configuration.nix file
```
services.xserver.extralayouts.real-prog-qwerty = {
    description = "real programmer's qwerty";
    languages = [ "eng" ];
    symbolsfile = /etc/nixos/xkb/symbols/real-prog-qwerty;
  };
```
and then just
```
nixos-rebuild switch
```
If this wasn't enough you probably need to restart X

## For the better us layout
Do the same thing but instead of ```real-prog-qwerty``` just put ```us-but-better``` 
and you will also become the new italian president
