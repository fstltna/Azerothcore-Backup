# AzerothBackup backup script for Azertoth WoW Server (1.0.0)
Creates a backup of your Azeroth folder

---

1. Edit the settings at the top of azerocothbackup.pl if needed
2. create a cron job like this:

        1 1 * * * /home/wowowner/Azerothcore-Backup/azerocothbackup

3. This will back up your Azeroth installation at 1:01am each day, and keep the last 5 backups.

4. Edit the backup config:
 	Run a manual backup and it will ask you for the mysql config info. If you need to reconfigure it use the "-prefs" command-line option

---

To set up offsite backups:

1. Make sure ssh-keygen is installed: "apt install ssh-keygen"
2. Run "ssh-keygen" and when asked for the password just press enter twice
3. Run "ssh-copy-id -i ~/.ssh/id_rsa.pub your-destination-server" - This will ask you for your remote password. This is normal.
4. Run "azerocothbackup -prefs" and update the backup fields
5. Rerun the backup and it should try and upload the files to your remote site.

If you need more help visit https://wowhosting.gameplayer.club/
