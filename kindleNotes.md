### Kindle Notes

***

my Kindle somehow ended up being read-only.  I couldn't add or remove books
using ***Calibre*** inside Ubuntu.  Here was the fix

* find the device `mount |grep Kindle` the output was something like `/dev/sdb1 on /media/Kindle type vfat
 (rw,nosuid,nodev,uid=1000,gid=1000,shortname=mixed,dmask=0077,utf8=1,showexec,flush,uhelper=udisks`
 * correct the filesystem with `sudo fsck.fvat -r /dev/sdb1`
