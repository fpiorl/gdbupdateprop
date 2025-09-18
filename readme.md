gdbupdateprop
=============


Little hack that can be used to update android properties 
(yes even read-only `ro` properties) using gdb.

Requires **root**.

# installation
first of all you need `gdb`
you can install it with termux.

Install termux
```sh
    wget https://f-droid.org/repo/com.termux_1021.apk
    adb install com.termux_1021.apk
```

After installing termux install `gdb` from termux 

```sh
# inside termux: 
    pkg install gdb
```

`gdb` should be located in `/data/data/com.termux/files/usr/bin/gdb`

# push and run the script
After installing gdb just run the script inside your android machine:
```sh
    adb push gdbsetprop /data/
    # example change ro.debuggable to 0
    adb shell su -c "/data/gdbsetprop ro.debuggable 0"
```
