# Jeffery's build of st - the simple (suckless) terminal (forked from LukeSmithxyz)


Forked from [LukeSmithxyz's build](https://github.com/LukeSmithxyz/st) which was forked from [https://github.com/shiva/st](https://github.com/shiva/st) for simplicity's sake, which is the [suckless terminal (st)](https://st.suckless.org/) with some patches added:

+ copy to clipboard
+ solarized colors (light and dark toggleable)
+ vertcenter
+ scrollback with keyboard
+ scrollback with mouse

##  additions

+ Transparency (You will also need to have a composite manager, such as compton or xcompmgr running for the transparency to appear.)
+ Default font is system "mono" at 14pt
+ Fixed transparency patch (see below for installation)
+ Toggle light/dark mode now Alt-Tab instead of the frequently conflicting F6
+ Alt-k and Alt-j scroll back/foward in history one line at a time
+ Alt-u and Alt-d scroll back/foward in history a page at a time

+ Scroll through history -- Shift+PageUp/PageDown or Shift+Mouse wheel
+ Increase/decrease font size -- Shift+Alt+PageUp/PageDown
+ Return to default dont size -- Shift+Alt+Home
+ Paste -- Shift+Insert

## Installation for newbs

```
make clean
make
sudo make install
```

### Transparency

To remove transparency, just unapply the diff patch and reinstall.

```
make clean
patch -R < patches/transparency.diff
make
sudo make install

```
If you want add transparency back in again, run the following. 
```
make clean
patch < patches/transparency.diff
make
sudo make install
```

