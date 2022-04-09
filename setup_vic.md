# Setup VIC

First of all, download last source tarball from https://vice-emu.sourceforge.io/ (at the moment is [vice-3.6.1.tar.gz](https://sourceforge.net/projects/vice-emu/files/releases/vice-3.6.1.tar.gz/download)).

> **Tips** you can download it directly executing from terminal `wget https://sourceforge.net/projects/vice-emu/files/releases/vice-3.6.1.tar.gz/download` command.

Then execute the following commands from terminal.

```
sudo apt-get update && sudo apt-get --yes upgrade

sudo apt install build-essential byacc flex xa65 libgtk2.0-dev libreadline-dev libasound2-dev libvte-dev dos2unix texlive-latex-base libsdl2-image-dev

cd /opt

sudo tar xzvf vice-3.6.1.tar.gz
sudo ln -sf vice-3.6.1 vice
sudo chown -R <username>:<username> vice/

cd vice

./configure --enable-fullscreen --enable-gnomeui --with-x --with-alsa --without-pulse --without-oss --without-resid

make

sudo make install

cp -R data/ ~/.vice
```

All executables will be available under `src` directory.


*References*

* https://programitalia.wordpress.com/2018/08/04/pi-vice-emu/
* https://forums.raspberrypi.com/viewtopic.php?t=264621


