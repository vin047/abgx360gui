# abgx360gui
### Linux/BSD source mirrored from http://abgx360.xecuter.com/

abgx360gui requires **[wxWidgets 3.0.2 or newer](http://wxwidgets.org/downloads/)** (and **[xterm](http://invisible-island.net/xterm/)** for Linux):
* OSX: `brew install wxwidgets --with-static` (--with-static is useful if you're thinking of distributing as an app bundle later, but isn't required to just compile and run)
* Linux (apt-get): `sudo apt-get install libwxgtk3.0-dev xterm`

To compile:
```bash
./configure
make
```

To run abgx360gui:
```
./abgx360gui
OR
use your favorite file manager to browse to this folder and double click on abgx360gui
```
NOTE: This is just a GUI, you need to have [abgx360](https://github.com/vin047/abgx360) installed in order to do anything useful.

**REMEMBER: As of 09/2016, you need to download the [ini file](http://abgx360.xecuter.com/abgx360.ini.zip) and place it 1 folder above your StealthFiles folder. See http://abgx360.xecuter.com/index.php for more details.**

## OSX Tips:
`abgx360gui` will only work if the `abgx360` is in your `PATH`. To use, move `abgx360` to a folder included in your system `PATH`. Alternatively, you can package both programs into an app bundle to make it work. Details on how to do this can be found [here](http://vin047.xyz/binaries-to-app-bundle/) or you can download the pre-packaged app bundle under [releases](https://github.com/vin047/abgx360gui/releases).

## Linux Tips:
If you encounter this error:
```bash
    wxWidgets must be installed on your system.

    Please check that wx-config is in path, the directory
    where wxWidgets libraries are installed (returned by
    'wx-config --libs' or 'wx-config --static --libs' command)
    is in LD_LIBRARY_PATH or equivalent variable and
    wxWidgets version is 2.7.1 or above.
```
First check that `wx-config` exists in your path (normally `/usr/local/bin`); it
might be named something else like `wxgtk2-3.0-config`, and you will need to create
a symbolic link named `wx-config` in order for the configure script to find it.

Example: `sudo ln -s /usr/local/bin/wxgtk2-3.0-config /usr/local/bin/wx-config`
