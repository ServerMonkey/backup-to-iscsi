# backup-to-iscsi
Backup a folder to iSCSI target.

Tested on Debian 11

### Example installation
Add these lines:  
`:syslogtag, startswith, "backup-to-iscsi" /var/log/backup-custom.log`  
`& stop`  
to:  
`/etc/rsyslog.d/00-crontab.conf`  
and run:  
`systemctl restart rsyslog.service`

Then add this to crontab:  
`0 1 * * * cronic backup-to-iscsi <IQN> <PATH_SRC> <PATH_DES>`

### How to use
`backup-to-iscsi -h`
