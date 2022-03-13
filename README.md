# Linux-errors
Multiple errors from linux (installation, steps, etc.)

ERROR: $ snap install --devmode --beta anbox 
         error: cannot communicate with server: Post "http://localhost/v2/snaps/anbox": dial unix /run/snapd.socket: connect: no such file or directory

SOLUTION: $ systemctl enable --now snapd apparmor
            Synchronizing state of apparmor.service with SysV service script with /lib/systemd/systemd-sysv-install.
            Executing: /lib/systemd/systemd-sysv-install enable apparmor
            Created symlink /etc/systemd/system/multi-user.target.wants/snapd.service → /lib/systemd/system/snapd.service.
            Created symlink /etc/systemd/system/sysinit.target.wants/apparmor.service → /lib/systemd/system/apparmor.service.
                                                                                                                                   
─$ snap install --devmode --beta anbox  
  2022-03-13T13:44:23-04:00 INFO Waiting for automatic snapd restart...
  Warning: /snap/bin was not found in your $PATH. If you've not restarted your session since you
         installed snapd, try doing that. Please see https://forum.snapcraft.io/t/9469 for more
         details.

  anbox (beta) 4-56c25f1 from Simon Fels (morphis) installed
                                                             
