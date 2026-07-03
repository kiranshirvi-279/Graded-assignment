q5 Storage Health Assessment and Documentation

lsblk: Listed all block devices and their mount points to identify available storage hardware.

mount | head -5: Showed the top mounted filesystems, including overlay, proc, tmpfs, devpts, and sysfs.

df -h: Collected disk usage statistics for mounted filesystems in human-readable format.

df -i: Collected inode utilization metrics to check filesystem metadata availability.

The report uses these outputs to assess storage health and recommend monitoring or cleanup on the most utilized mount points.
