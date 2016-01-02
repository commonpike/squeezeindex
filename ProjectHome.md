Squeezeboxserver expects to find audio located in one specific folder (and subfolders). If you specify your disks root folder as the squeezebox root, it recreates the whole disk structure on your squeezebox hardware, with mostly empty folders.

If you are using linux, you have root access, and if you are used to having your audio all across your disk, you can use squeezeindex, eg daily, to index all audio and put symlinks in one specific folder. If you point your squeezeboxserver there, it will show up quite tidy on your squeezebox hardware.

Read more about squeezeboxserver here:
  * http://en.wikipedia.org/wiki/Squeezebox_Server


Structure of this package :

```
|-- etc
|   `-- cron.daily
|       `-- squeezeindex
`-- usr
    `-- share
        `-- squeezecenter
            |-- Bin
            |   `-- i386-linux
            |       `-- squeezeindex.sh
            `-- INDEX
```
If you're familiar with linux, that basically sums it up :-)
  * unzip the tarball (its under downloads)
  * Put the stuff on the right place,
  * and wait for a day.

Alternatively, you can run squeezeindex.sh by hand. it uses locate, so optionally run updatedb first.

It will create symlinks in the INDEX folder; it searches for **.wav**.mp3 **.au**.aif **.aiff**.flac, it ignores files starting with a dot or an underscore, and files in the /mnt folder. You can change all this in the shell script.