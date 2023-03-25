# mame-unwanted

One of the goals of MAME is to software as it was released. This usually does
not excludes hacked, cracked, translation, or converted media images and you
will not find the in MAME's software lists.

These software lists have been made to the help with the identification of
media images by listing known hacked, cracked, etc images.

# Usage

This depends on also having a checkout of MAME and a MAME executable.

## 1. load the system and software hashes.
From the MAME folder run:
```
python3 scripts/minimaws/minimaws.py --database minimaws_unwanted.sqlite3 load --executable /path/to/mame --softwarepath /path/to/mame/hash --softwarepath /path/to/mame-unwanted
```

## 2. Identify media images

To scan your media images run the following command:
```
python3 scripts/minimaws/minimaws.py --database minimaws_unwanted.sqlite3 romident /path/to/folder/with/media/images/
```
This will tell you which software or system roms have been found and which are unknown.

To update the database with a new releases or updated (unwanted) software lists just re-run the command from step 1.
