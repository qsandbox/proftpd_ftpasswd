# ProFTPD ftpasswd
At https://qSandbox.com we had a problem that ProFTPD server kept stopping from time to time.
The reason was that ftpasswd script was failing to restore the password and group file permissions.
This caused the proftpd server to stop working.
 
You can use this this script OR install Ubuntu 20 and copy /usr/sbin/ftpasswd to your older Ubuntu servers.

Blog post related to this tool.
https://qsandbox.com/830

# Installation

Login as root

Always make a backup!
cp /usr/sbin/ftpasswd /usr/sbin/ftpasswd_old_not_reverting_perms

Download the ftpasswd file from this repo OR install Ubuntu 20 and then copy /usr/sbin/ftpasswd file.

wget 'https://raw.githubusercontent.com/qsandbox/proftpd_ftpasswd/master/ftpasswd'

Set permissions
chmod 0755 ftpasswd

Move the file. DID YOU MAKE A BACKUP?
mv ftpasswd /usr/sbin/ftpasswd

# Support
We haven't created nor maintain any of the code related to the proftpd server.
Therefore if you stumble upon any bugs please submit them to: 
https://github.com/proftpd/proftpd

# Disclaimer
May contain inaccuracies, use at your own risk.


