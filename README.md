# giga-turbo's build of dwm

- Uses [Twitter Color Emoji](https://github.com/eosrei/twemoji-color-font) and [FontAwesome](https://fontawesome.com/?from=io)

## Please install `libxft-bgra`!

This build of dwm does not block color emoji in the status/info bar, so you must install [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/) from the AUR, which fixes a libxft color emoji rendering problem, otherwise dwm will crash upon trying to render one. Hopefully this fix will be in all libxft soon enough.
