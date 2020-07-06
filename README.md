# ProFTPD ftpasswd
At https://qSandbox.com we had a problem that ProFTPD server kept stopping from time to time.
The reason was that ftpasswd script was failing to restore the password and group file permissions.
This caused the proftpd server to stop working.

Here's a ticket from proftpd repo: ftpasswd fails to restore password file permissions in some cases #898
https://github.com/proftpd/proftpd/issues/898
 
You can use this script OR install Ubuntu 20, then install proftpd and copy /usr/sbin/ftpasswd to your older Ubuntu servers.

Blog post related to this tool.
https://qsandbox.com/830

# Installation

Login as root

Always make a backup!
cp /usr/sbin/ftpasswd /usr/sbin/ftpasswd_old_not_reverting_perms

Download the ftpasswd file from this repo OR install Ubuntu 20 and then copy /usr/sbin/ftpasswd file.

wget 'https://raw.githubusercontent.com/qsandbox/proftpd_ftpasswd/master/ftpasswd'

inspect the file (Perl script). You should always do that when downloading stuff from the Internet.

Set permissions

chmod 0755 ftpasswd

Move the file. DID YOU MAKE A BACKUP?

mv ftpasswd /usr/sbin/ftpasswd

# Support
We haven't created nor maintain any of the code related to the proftpd server.
Therefore if you stumble upon any bugs please submit them to: 
https://github.com/proftpd/proftpd

# Software Disclaimer
There are inherent dangers in the use of any software available for download on the Internet, and we caution you to make sure that you completely understand the potential risks before downloading any of the software.

The Software and code samples available on this website are provided "as is" without warranty of any kind, either express or implied. Use at your own risk.

The use of the software and scripts downloaded on this site is done at your own discretion and risk and with agreement that you will be solely responsible for any damage to your computer system or loss of data that results from such activities. You are solely responsible for adequate protection and backup of the data and equipment used in connection with any of the software, and we will not be liable for any damages that you may suffer in connection with using, modifying or distributing any of this software. No advice or information, whether oral or written, obtained by you from us or from this website shall create any warranty for the software.

We make makes no warranty that

the software will meet your requirements
the software will be uninterrupted, timely, secure or error-free
the results that may be obtained from the use of the software will be effective, accurate or reliable
the quality of the software will meet your expectations
any errors in the software obtained from us will be corrected.
The software, code sample and their documentation made available on this website:

could include technical or other mistakes, inaccuracies or typographical errors. We may make changes to the software or documentation made available on its web site at any time without prior-notice.
may be out of date, and we make no commitment to update such materials.
We assume no responsibility for errors or omissions in the software or documentation available from its web site.

In no event shall we be liable to you or any third parties for any special, punitive, incidental, indirect or consequential damages of any kind, or any damages whatsoever, including, without limitation, those resulting from loss of use, data or profits, and on any theory of liability, arising out of or in connection with the use of this software.

