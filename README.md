# Assign3
## Spring 2018

The purpose of this exercise is to get comfortable creating scripts using vim on a server, while teaching you the remainder of bash scripting you'll need as a foundation for this course. The scripts themselves are not particularly exciting but they are the building blocks you'll need.  You will be asked to create 11 scripts, which all come from http://dtg.usc.edu/tgrn510/index.php/bash-scripting/.  These are to all be placed in your "bin" directory. The results of running these should be put into a forked version of this github. 

The final question is considerably more difficult and requires you to put concepts together you have learned at this point.

 Completion means the scripts work in your home directory and you have put the results in your github where you will replace the placeholder text with the results from running the script. For exampler, you should replace

*REPLACE WITH RESULTS*

with codeblock text using backticks, which show both the program being called in trgn510.pmed.io and the result.  After, it should be:

`
davidcraig@trgn510:~/bin ls | test.sh
TEST.SH
`

### 1
Please create pointless.sh, changing from printing your hostname with $HOSTNAME, to your $USER

`[sunying@trgn510 bin]$ ./pointless.sh
sunying
5
6`

### 2
Please create quotequotes.sh, please add 1 additional lines that prints the process id of the current script using a special variable in a sentence: "The process id for this script is **235**'
`[sunying@trgn510 bin]$ ./quotequotes.sh
trgn510.pmed.io
VARIABLE
I am on trgn510.pmed.io
I am on $HOSTNAME
I am on $HOSTNAME
The process id for this script is 22961`

### 3
Please create processes.sh.  Modify it such that it prints the top 5 CPU consuming processes

`[sunying@trgn510 bin]$ ./processes.sh
PID PPID CMD %MEM %CPU 1344 1174 /usr/sbin/mysqld --basedir= 2.9 0.0 541 1 /usr/bin/python -Es /usr/sb 0.6 0.0 865 1 /usr/sbin/httpd -DFOREGROUN 0.3 0.0 5586 865 /usr/sbin/httpd -DFOREGROUN 0.3 0.0 5587 865 /usr/sbin/httpd -DFOREGROUN 0.3 0.0 25847 865 /usr/sbin/httpd -DFOREGROUN 0.3 0.0 5583 865 /usr/sbin/httpd -DFOREGROUN 0.3 0.0 5584 865 /usr/sbin/httpd -DFOREGROUN 0.3 0.0 5585 865 /usr/sbin/httpd -DFOREGROUN 0.3 0.0`

### 4
Please create makeupper.sh.  Modify it to return lower case results, and change the name to makelower.sh
`[sunying@trgn510 bin]$ ps -ef | makelower.sh
uid        pid  ppid  c stime tty          time cmd
root         1     0  0 jan19 ?        00:03:11 /usr/lib/systemd/systemd --switched-root --system --deserialize 19
root         2     0  0 jan19 ?        00:00:00 [kthreadd]
root         3     2  0 jan19 ?        00:00:00 [ksoftirqd/0]
root         5     2  0 jan19 ?        00:00:00 [kworker/0:0h]
root         7     2  0 jan19 ?        00:00:01 [migration/0]
root         8     2  0 jan19 ?        00:00:00 [rcu_bh]
root         9     2  0 jan19 ?        00:00:59 [rcu_sched]
root        10     2  0 jan19 ?        00:00:05 [watchdog/0]
root        11     2  0 jan19 ?        00:00:04 [watchdog/1]
root        12     2  0 jan19 ?        00:00:02 [migration/1]
root        13     2  0 jan19 ?        00:00:02 [ksoftirqd/1]
root        15     2  0 jan19 ?        00:00:00 [kworker/1:0h]
root        17     2  0 jan19 ?        00:00:00 [kdevtmpfs]
root        18     2  0 jan19 ?        00:00:00 [netns]
root        19     2  0 jan19 ?        00:00:00 [xenwatch]
root        20     2  0 jan19 ?        00:00:00 [xenbus]
root        22     2  0 jan19 ?        00:00:00 [khungtaskd]
root        23     2  0 jan19 ?        00:00:00 [writeback]
root        24     2  0 jan19 ?        00:00:00 [kintegrityd]
root        25     2  0 jan19 ?        00:00:00 [bioset]
root        26     2  0 jan19 ?        00:00:00 [kblockd]
root        27     2  0 jan19 ?        00:00:00 [md]
root        33     2  0 jan19 ?        00:01:07 [kswapd0]
root        34     2  0 jan19 ?        00:00:00 [ksmd]
root        35     2  0 jan19 ?        00:00:03 [khugepaged]
root        36     2  0 jan19 ?        00:00:00 [crypto]
root        44     2  0 jan19 ?        00:00:00 [kthrotld]
root        46     2  0 jan19 ?        00:00:00 [kmpath_rdacd]
root        47     2  0 jan19 ?        00:00:00 [kpsmoused]
root        48     2  0 jan19 ?        00:00:00 [ipv6_addrconf]
root        67     2  0 jan19 ?        00:00:00 [deferwq]
root       160     2  0 jan19 ?        00:00:13 [kauditd]
root       223     2  0 jan19 ?        00:00:00 [ata_sff]
root       224     2  0 jan19 ?        00:00:00 [scsi_eh_0]
root       225     2  0 jan19 ?        00:00:00 [scsi_tmf_0]
root       226     2  0 jan19 ?        00:00:00 [scsi_eh_1]
root       227     2  0 jan19 ?        00:00:00 [scsi_tmf_1]
root       251     2  0 jan19 ?        00:00:00 [bioset]
root       252     2  0 jan19 ?        00:00:00 [xfsalloc]
root       253     2  0 jan19 ?        00:00:00 [xfs_mru_cache]
root       254     2  0 jan19 ?        00:00:00 [xfs-buf/xvda2]
root       255     2  0 jan19 ?        00:00:00 [xfs-data/xvda2]
root       256     2  0 jan19 ?        00:00:00 [xfs-conv/xvda2]
root       257     2  0 jan19 ?        00:00:00 [xfs-cil/xvda2]
root       258     2  0 jan19 ?        00:00:00 [xfs-reclaim/xvd]
root       259     2  0 jan19 ?        00:00:00 [xfs-log/xvda2]
root       260     2  0 jan19 ?        00:00:00 [xfs-eofblocks/x]
root       261     2  0 jan19 ?        00:04:15 [xfsaild/xvda2]
root       328     1  0 jan19 ?        00:03:53 /usr/lib/systemd/systemd-journald
root       369     1  0 jan19 ?        00:00:00 /usr/lib/systemd/systemd-udevd
root       399     1  0 jan19 ?        00:00:34 /sbin/auditd
root       400     2  0 jan19 ?        00:00:00 [ttm_swap]
root       459     2  0 jan19 ?        00:00:00 [edac-poller]
root       507     2  0 jan19 ?        00:00:00 [kworker/0:1h]
root       509     1  0 jan19 ?        00:00:14 /usr/lib/systemd/systemd-logind
root       510     1  0 jan19 ?        00:00:52 /usr/sbin/irqbalance --foreground
dbus       512     1  0 jan19 ?        00:00:30 /bin/dbus-daemon --system --address=systemd: --nofork --nopidfile --systemd-activation
chrony     514     1  0 jan19 ?        00:00:02 /usr/sbin/chronyd
polkitd    524     1  0 jan19 ?        00:00:01 /usr/lib/polkit-1/polkitd --no-debug
root       526     1  0 jan19 ?        00:02:30 /usr/sbin/rsyslogd -n
root       541     1  0 jan19 ?        00:00:01 /usr/bin/python -es /usr/sbin/firewalld --nofork --nopid
root       543     1  0 jan19 ?        00:00:20 /usr/sbin/networkmanager --no-daemon
root       666   543  0 jan19 ?        00:00:01 /sbin/dhclient -d -q -sf /usr/libexec/nm-dhcp-helper -pf /var/run/dhclient-eth0.pid -lf /var/lib/networkmanager/dhclient-5fb06bd0-0bb0-7ffb-45f1-d6edd65f3e03-eth0.lease -cf /var/lib/networkmanager/dhclient-eth0.conf eth0
root       863     1  0 jan19 ?        00:01:48 /usr/bin/python -es /usr/sbin/tuned -l -p
root       865     1  0 jan19 ?        00:00:54 /usr/sbin/httpd -dforeground
root       968     1  0 jan19 ?        00:00:40 /usr/sbin/sshd -d
root       969     1  0 jan19 ttys0    00:00:00 /sbin/agetty --keep-baud 115200 38400 9600 ttys0 vt220
root       974     1  0 jan19 ?        00:00:07 /usr/sbin/crond -n
root       977     1  0 jan19 tty1     00:00:00 /sbin/agetty --noclear tty1 linux
root       996     1  0 jan19 ?        00:00:00 /usr/sbin/dovecot -f
root      1024     1  0 jan19 ?        00:00:00 rhnsd
dovecot   1034   996  0 jan19 ?        00:00:00 dovecot/anvil
root      1035   996  0 jan19 ?        00:00:00 dovecot/log
mysql     1174     1  0 jan19 ?        00:00:00 /bin/sh /usr/bin/mysqld_safe --basedir=/usr
mysql     1344  1174  0 jan19 ?        00:07:17 /usr/sbin/mysqld --basedir=/usr --datadir=/var/lib/mysql --plugin-dir=/usr/lib64/mysql/plugin --log-error=/var/log/mysqld.log --pid-file=/var/run/mysqld/mysqld.pid --socket=/var/lib/mysql/mysql.sock
root      1414     2  0 jan19 ?        00:00:01 [kworker/1:1h]
root      1528     2  0 jan19 ?        00:00:20 [jbd2/xvdf-8]
root      1529     2  0 jan19 ?        00:00:00 [ext4-rsv-conver]
apache    5583   865  0 jan29 ?        00:00:00 /usr/sbin/httpd -dforeground
apache    5584   865  0 jan29 ?        00:00:00 /usr/sbin/httpd -dforeground
apache    5585   865  0 jan29 ?        00:00:00 /usr/sbin/httpd -dforeground
apache    5586   865  0 jan29 ?        00:00:00 /usr/sbin/httpd -dforeground
apache    5587   865  0 jan29 ?        00:00:00 /usr/sbin/httpd -dforeground
apache   11051   865  0 feb02 ?        00:00:00 /usr/sbin/httpd -dforeground
apache   11052   865  0 feb02 ?        00:00:00 /usr/sbin/httpd -dforeground
apache   13091   865  0 13:47 ?        00:00:00 /usr/sbin/httpd -dforeground
apache   13093   865  0 13:47 ?        00:00:00 /usr/sbin/httpd -dforeground
root     16224     2  0 05:45 ?        00:00:00 [kworker/u30:2]
apache   25847   865  0 jan29 ?        00:00:00 /usr/sbin/httpd -dforeground
root     26106   968  0 17:53 ?        00:00:00 sshd: varshagi [priv]
varshagi 26115 26106  0 17:53 ?        00:00:00 sshd: varshagi@pts/5
varshagi 26116 26115  0 17:53 pts/5    00:00:00 -bash
root     26533     2  0 18:01 ?        00:00:00 [kworker/0:0]
root     26976     2  0 04:14 ?        00:00:00 [kworker/u30:0]
root     27612     2  0 18:19 ?        00:00:00 [kworker/0:1]
root     28278     2  0 18:31 ?        00:00:00 [kworker/1:0]
root     28807     2  0 18:42 ?        00:00:00 [kworker/1:1]
root     28812   968  0 18:42 ?        00:00:00 sshd: sunying [priv]
sunying  28819 28812  0 18:42 ?        00:00:00 sshd: sunying@pts/0
sunying  28820 28819  0 18:42 pts/0    00:00:00 -bash
root     29171     2  0 18:48 ?        00:00:00 [kworker/1:2]
varshagi 29385 26116  0 18:52 pts/5    00:00:00 vim add.sh
sunying  29389 28820  0 18:52 pts/0    00:00:00 ps -ef
sunying  29390 28820  0 18:52 pts/0    00:00:00 /bin/bash /user/sunying/bin/makelower.sh
sunying  29391 29390  0 18:52 pts/0    00:00:00 cat /dev/stdin
sunying  29392 29390  0 18:52 pts/0    00:00:00 tr [:upper:] [:lower:]
root     32625   968  0 feb02 ?        00:00:00 sshd: davidcraig [priv]
davidcr+ 32634 32625  0 feb02 ?        00:00:00 sshd: davidcraig@pts/2
davidcr+ 32635 32634  0 feb02 pts/2    00:00:00 -bash
davidcr+ 32695 32635  0 feb02 pts/2    00:00:00 ssh varshagi@trgn510.pmed.io`

### 5
Referring to math.sh, create a script called add.sh that takes two inputs and adds them, **add.sh 5 3** would print 8
`[sunying@trgn510 bin]$ add.sh 9 9
18`

### 6
Create a program "mb_or_kb.sh", referring to bigornot.sh and useful.sh, create a script called big file that checks to see if the file exists provided as the first argument exists, and if it exists then gets the filesize, storing it as a variable. I have not provided you with a way to get filesize in exercise, and expect you to search web for a way.  The program then checks to see if the size is greater than 1,000,000.  If its less then 1,000,000, it prints the number of kilobytes (divide by 1000) followed by "kB".  If its greater than 1,000,000, then print the number of megabytes followed by "MB".

*REPLACE WITH RESULTS for mb_or_kb.sh ~/.bashrc*

### 7
Create a program "count_by_to.sh", referring to count.sh.  The file should take two arguments, and should count jumping by the first argument until the second argument is reached, starting at 0.  For example, *count.sh 2 10* would print 0 2 4 6 8 10

`[sunying@trgn510 bin]$ ./count_by_to.sh 2 10
0
2
4
6
8
10`

### 9
Please create whatgene.sh.  Please edit such that the function print_gene, prints upper case of the input.

*REPLACE WITH RESULTS*

### 10
Please create a bash shell called "genotype.sh" that takes a VCF as argument 1, and prints space delimited chromosome, position, reference, alternative, and genotype for all genotypes in VCF.

*REPLACE WITH RESULTS for genotype.sh ~/assign2/HG001_GRCh37_GIAB_highconf_CG-IllFB-IllGATKHC-Ion-10X-SOLID_CHROM1-X_v.3.3.2_highconf_PGandRTGphasetransfer.vcf | head*
