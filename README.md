# Wolfi's fork of dwm

## Patches

* https://dwm.suckless.org/patches/xresources/
* https://dwm.suckless.org/patches/status2d/
* -- https://dwm.suckless.org/patches/statuscmd/ (with systray)
* https://dwm.suckless.org/patches/hide_vacant_tags/ d2f2907c93b2667594326024c3f564e050cdddc9
* https://dwm.suckless.org/patches/swallow/
* https://dwm.suckless.org/patches/vanitygaps/
* https://dwm.suckless.org/patches/stacker/
* https://dwm.suckless.org/patches/pertag/
* https://dwm.suckless.org/patches/zoomswap/
* https://dwm.suckless.org/patches/scratchpad/
* https://dwm.suckless.org/patches/nextprev/ (https://lists.suckless.org/dev/1104/7590.html)
* colorful tags
* https://dwm.suckless.org/patches/notitle/
* https://dwm.suckless.org/patches/actualfullscreen/

## Manual

### Exclude systray icons in picom

In The function `clientmessage` in `dwm.c`, right before the `XReparentWindow` line, add:
```
XClassHint ch = {"dwmsystray", "dwmsystray"};
XSetClassHint(dpy, c->win, &ch);
```

Afterwards we can exlude things in picom.conf using `"class_g = 'dwmsystray'",`

## TODO

* https://dwm.suckless.org/patches/alwayscenter/
* https://dwm.suckless.org/patches/barpadding/
* Describe patches
* https://dwm.suckless.org/patches/sticky/

## To Check

* alwayscenter
* barpadding
* colorfull tag
* movestack
* notitle
* statuspadding


