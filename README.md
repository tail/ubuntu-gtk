This branch includes a patch from https://bugzilla.gnome.org/show_bug.cgi?id=747280 which fixes an issue where Chrome will crash when opening a file dialog when using awesome WM.

## Building

```sh
sudo apt-get build-dep libgtk2.0-0
git clone https://github.com/tail/ubuntu-gtk.git
cd ubuntu-gtk
git checkout gnome-bugzilla-747280
curl -L -O http.debian.net/debian/pool/main/g/gtk+2.0/gtk+2.0_2.24.28.orig.tar.xz
tar xv --strip-components=1 -f gtk+2.0_2.24.28.orig.tar.xz
dpkg-buildpackage -b
```
