# otus
for otus homeworks

root@u24:~# uname -r
6.8.0-90-generic
_admin@u24:~$ ls -la
total 32
drwxr-x--- 4 _admin _admin 4096 Jan 11 03:23 .
drwxr-xr-x 3 root   root   4096 Jan 11 03:08 ..
-rw-r--r-- 1 _admin _admin  220 Mar 31  2024 .bash_logout
-rw-r--r-- 1 _admin _admin 3771 Mar 31  2024 .bashrc
drwx------ 2 _admin _admin 4096 Jan 11 03:10 .cache
-rw------- 1 _admin _admin   20 Jan 11 03:23 .lesshst
-rw-r--r-- 1 _admin _admin  807 Mar 31  2024 .profile
drwx------ 2 _admin _admin 4096 Jan 11 03:08 .ssh
-rw-r--r-- 1 _admin _admin    0 Jan 11 03:23 .sudo_as_admin_successful
_admin@u24:~$ mkdir kernel && cd kernel
_admin@u24:~/kernel$ wget https://kernel.ubuntu.com/mainline/v6.18/amd64/linux-headers-6.18.0-061800-generic_6.18.0-061800.202511302339_amd64.deb
--2026-01-11 03:29:08--  https://kernel.ubuntu.com/mainline/v6.18/amd64/linux-headers-6.18.0-061800-generic_6.18.0-061800.202511302339_amd64.deb
Resolving kernel.ubuntu.com (kernel.ubuntu.com)... 185.125.189.75, 185.125.189.76, 185.125.189.74
Connecting to kernel.ubuntu.com (kernel.ubuntu.com)|185.125.189.75|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3967584 (3.8M) [application/x-debian-package]
Saving to: ‘linux-headers-6.18.0-061800-generic_6.18.0-061800.202511302339_amd64.deb’

linux-headers-6.18.0-061800-generic_6.18. 100%[=====================================================================================>]   3.78M   369KB/s    in 11s

2026-01-11 03:29:20 (359 KB/s) - ‘linux-headers-6.18.0-061800-generic_6.18.0-061800.202511302339_amd64.deb’ saved [3967584/3967584]

_admin@u24:~/kernel$ wget https://kernel.ubuntu.com/mainline/v6.18/amd64/linux-headers-6.18.0-061800_6.18.0-061800.202511302339_all.deb
--2026-01-11 03:29:25--  https://kernel.ubuntu.com/mainline/v6.18/amd64/linux-headers-6.18.0-061800_6.18.0-061800.202511302339_all.deb
Resolving kernel.ubuntu.com (kernel.ubuntu.com)... 185.125.189.75, 185.125.189.76, 185.125.189.74
Connecting to kernel.ubuntu.com (kernel.ubuntu.com)|185.125.189.75|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14537396 (14M) [application/x-debian-package]
Saving to: ‘linux-headers-6.18.0-061800_6.18.0-061800.202511302339_all.deb’

linux-headers-6.18.0-061800_6.18.0-061800 100%[=====================================================================================>]  13.86M   345KB/s    in 37s

2026-01-11 03:30:03 (382 KB/s) - ‘linux-headers-6.18.0-061800_6.18.0-061800.202511302339_all.deb’ saved [14537396/14537396]

_admin@u24:~/kernel$ wget https://kernel.ubuntu.com/mainline/v6.18/amd64/linux-image-unsigned-6.18.0-061800-generic_6.18.0-061800.202511302339_amd64.deb
--2026-01-11 03:30:06--  https://kernel.ubuntu.com/mainline/v6.18/amd64/linux-image-unsigned-6.18.0-061800-generic_6.18.0-061800.202511302339_amd64.deb
Resolving kernel.ubuntu.com (kernel.ubuntu.com)... 185.125.189.75, 185.125.189.76, 185.125.189.74
Connecting to kernel.ubuntu.com (kernel.ubuntu.com)|185.125.189.75|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17264832 (16M) [application/x-debian-package]
Saving to: ‘linux-image-unsigned-6.18.0-061800-generic_6.18.0-061800.202511302339_amd64.deb’

linux-image-unsigned-6.18.0-061800-generi 100%[=====================================================================================>]  16.46M   391KB/s    in 46s

2026-01-11 03:30:53 (368 KB/s) - ‘linux-image-unsigned-6.18.0-061800-generic_6.18.0-061800.202511302339_amd64.deb’ saved [17264832/17264832]

_admin@u24:~/kernel$ wget https://kernel.ubuntu.com/mainline/v6.18/amd64/linux-modules-6.18.0-061800-generic_6.18.0-061800.202511302339_amd64.deb
--2026-01-11 03:30:56--  https://kernel.ubuntu.com/mainline/v6.18/amd64/linux-modules-6.18.0-061800-generic_6.18.0-061800.202511302339_amd64.deb
Resolving kernel.ubuntu.com (kernel.ubuntu.com)... 185.125.189.75, 185.125.189.76, 185.125.189.74
Connecting to kernel.ubuntu.com (kernel.ubuntu.com)|185.125.189.75|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 165642432 (158M) [application/x-debian-package]
Saving to: ‘linux-modules-6.18.0-061800-generic_6.18.0-061800.202511302339_amd64.deb’

linux-modules-6.18.0-061800-generic_6.18. 100%[=====================================================================================>] 157.97M   380KB/s    in 7m 18s

2026-01-11 03:38:14 (370 KB/s) - ‘linux-modules-6.18.0-061800-generic_6.18.0-061800.202511302339_amd64.deb’ saved [165642432/165642432]

_admin@u24:~/kernel$ sudo dpkg -i *.deb
[sudo] password for _admin:
Selecting previously unselected package linux-headers-6.18.0-061800.
(Reading database ... 87424 files and directories currently installed.)
Preparing to unpack linux-headers-6.18.0-061800_6.18.0-061800.202511302339_all.deb ...
Unpacking linux-headers-6.18.0-061800 (6.18.0-061800.202511302339) ...
Selecting previously unselected package linux-headers-6.18.0-061800-generic.
Preparing to unpack linux-headers-6.18.0-061800-generic_6.18.0-061800.202511302339_amd64.deb ...
Unpacking linux-headers-6.18.0-061800-generic (6.18.0-061800.202511302339) ...
Selecting previously unselected package linux-image-unsigned-6.18.0-061800-generic.
Preparing to unpack linux-image-unsigned-6.18.0-061800-generic_6.18.0-061800.202511302339_amd64.deb ...
Unpacking linux-image-unsigned-6.18.0-061800-generic (6.18.0-061800.202511302339) ...
Selecting previously unselected package linux-modules-6.18.0-061800-generic.
Preparing to unpack linux-modules-6.18.0-061800-generic_6.18.0-061800.202511302339_amd64.deb ...
Unpacking linux-modules-6.18.0-061800-generic (6.18.0-061800.202511302339) ...
Setting up linux-headers-6.18.0-061800 (6.18.0-061800.202511302339) ...
Setting up linux-headers-6.18.0-061800-generic (6.18.0-061800.202511302339) ...
Setting up linux-modules-6.18.0-061800-generic (6.18.0-061800.202511302339) ...
Setting up linux-image-unsigned-6.18.0-061800-generic (6.18.0-061800.202511302339) ...
I: /boot/vmlinuz is now a symlink to vmlinuz-6.18.0-061800-generic
I: /boot/initrd.img is now a symlink to initrd.img-6.18.0-061800-generic
Processing triggers for linux-image-unsigned-6.18.0-061800-generic (6.18.0-061800.202511302339) ...
/etc/kernel/postinst.d/initramfs-tools:
update-initramfs: Generating /boot/initrd.img-6.18.0-061800-generic
/etc/kernel/postinst.d/zz-update-grub:
Sourcing file `/etc/default/grub'
Generating grub configuration file ...
Found linux image: /boot/vmlinuz-6.18.0-061800-generic
Found initrd image: /boot/initrd.img-6.18.0-061800-generic
Found linux image: /boot/vmlinuz-6.8.0-90-generic
Found initrd image: /boot/initrd.img-6.8.0-90-generic
Warning: os-prober will not be executed to detect other bootable partitions.
Systems on them will not be added to the GRUB boot configuration.
Check GRUB_DISABLE_OS_PROBER documentation entry.
Adding boot menu entry for UEFI Firmware Settings ...
done
_admin@u24:~/kernel$
_admin@u24:~/kernel$
_admin@u24:~/kernel$ ls -la /boot
total 197088
drwxr-xr-x  4 root root     4096 Jan 11 03:41 .
drwxr-xr-x 23 root root     4096 Jan 11 02:51 ..
-rw-r--r--  1 root root   303679 Nov 30 23:39 config-6.18.0-061800-generic
-rw-r--r--  1 root root   287416 Nov 18 11:26 config-6.8.0-90-generic
drwxr-xr-x  5 root root     4096 Jan 11 03:41 grub
lrwxrwxrwx  1 root root       32 Jan 11 03:41 initrd.img -> initrd.img-6.18.0-061800-generic
-rw-r--r--  1 root root 75970904 Jan 11 03:41 initrd.img-6.18.0-061800-generic
-rw-r--r--  1 root root 72412056 Jan 11 02:51 initrd.img-6.8.0-90-generic
lrwxrwxrwx  1 root root       27 Jan 11 02:50 initrd.img.old -> initrd.img-6.8.0-90-generic
drwx------  2 root root    16384 Jan 11 02:18 lost+found
-rw-------  1 root root 11442110 Nov 30 23:39 System.map-6.18.0-061800-generic
-rw-------  1 root root  9114947 Nov 18 11:26 System.map-6.8.0-90-generic
lrwxrwxrwx  1 root root       29 Jan 11 03:41 vmlinuz -> vmlinuz-6.18.0-061800-generic
-rw-------  1 root root 17232064 Nov 30 23:39 vmlinuz-6.18.0-061800-generic
-rw-------  1 root root 15006088 Nov 18 11:46 vmlinuz-6.8.0-90-generic
lrwxrwxrwx  1 root root       24 Jan 11 02:50 vmlinuz.old -> vmlinuz-6.8.0-90-generic
_admin@u24:~/kernel$ uname -r
6.8.0-90-generic
_admin@u24:~/kernel$ sudo update-grub
Sourcing file `/etc/default/grub'
Generating grub configuration file ...
Found linux image: /boot/vmlinuz-6.18.0-061800-generic
Found initrd image: /boot/initrd.img-6.18.0-061800-generic
Found linux image: /boot/vmlinuz-6.8.0-90-generic
Found initrd image: /boot/initrd.img-6.8.0-90-generic
Warning: os-prober will not be executed to detect other bootable partitions.
Systems on them will not be added to the GRUB boot configuration.
Check GRUB_DISABLE_OS_PROBER documentation entry.
Adding boot menu entry for UEFI Firmware Settings ...
done
_admin@u24:~/kernel$ sudo grub-set-default 0
_admin@u24:~/kernel$ sudo reboot

Broadcast message from root@u24 on pts/2 (Sun 2026-01-11 03:56:01 UTC):

The system will reboot now!

*********
Output omitted
*********

login as: _admin
_admin@192.168.3.134's password:
Welcome to Ubuntu 24.04.3 LTS (GNU/Linux 6.18.0-061800-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Sun Jan 11 03:58:30 AM UTC 2026

  System load:  0.6                Processes:              251
  Usage of /:   21.5% of 23.45GB   Users logged in:        0
  Memory usage: 13%                IPv4 address for ens33: 192.168.3.134
  Swap usage:   0%


Expanded Security Maintenance for Applications is not enabled.

55 updates can be applied immediately.
To see these additional updates run: apt list --upgradable

Enable ESM Apps to receive additional future security updates.
See https://ubuntu.com/esm or run: sudo pro status


Last login: Sun Jan 11 03:10:39 2026 from 192.168.3.1
_admin@u24:~$ 
_admin@u24:~$ uname -r
6.18.0-061800-generic
_admin@u24:~$

