#### =============== Check config file ==========
cat ~/.config/rclone/rclone.conf

#### =============== Mount disk ===========
rclone mount remote: /gpfs/milgram/pi/yildirim/wb338/gdrive --copy-links --no-gzip-encoding --no-check-certificate --allow-non-empty --vfs-cache-mode writes --attr-timeout 0s --default-permissions --buffer-size 32M --dir-cache-time 12h --vfs-read-chunk-size 64M --vfs-read-chunk-size-limit 1G &

#### ===============  Check if mounted successfully ====
df -h
#### ===============  Unmount ============

fusermount -qzu /gpfs/milgram/pi/yildirim/wb338/gdrive
