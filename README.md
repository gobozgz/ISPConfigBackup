# ISPConfigBackup
A simple python script for backup all sites and databases for ISPConfig

# Requirements
Python 2

# How to use
Just edit the config in the main file, the `BACKUP_DIR` MUST be an absolute path, no final `/`.

```
#######--CONFIG--#######
DB_USER = 'root'
DB_PASSWORD = 'root'
BACKUP_DIR = '/root/backups_ispconfig' #the folder where the backup will be stored (don't put any other file in this folder if the rotation is "True")
BACKUP_ROTATION = False #if you want enable the backup rotation (True or False)
BACKUP_ROTATION_N = 5 #the number of backups that you want to keep (only if BACKUP_ROTATION is True)
########################
```

And finally launch it from console:

```shell
python ISPConfigBackup.py
```
For daily backup you can setup a cron task and setup in the config the backup rotation

# Warning
I am not responsible for any damage to your servers/websites. If you point the finger at me for messing up your server, I will laugh at you.
