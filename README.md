SmartOS Summary
===============

SmartOS Global Zone Summary

Example
-------

Run without any arguments to get a full synopsis and report

    $ ./sos
    Hostname: datadyne
    Zonename: global
    Kernel: joyent_20150423T155306Z
    Uptime: 8 days (8 days)
    Memory: 15.747 GB
    Processors: 6
      - 6 x AMD Phenom(tm) II X6 1075T Processor (3000 MHz)

    Interfaces: 2
      - lo0      127.0.0.1, ::1
      - rge0     10.0.1.10

    Devices: 13
      - cmdk0    -     -                    120665020000134   30.017 GB  (27.955 GB)
      - cmdk1    -     -                    000000001151032   64.023 GB  (59.626 GB)
      - cmdk2    -     -                         WD-WCAYV20   250.059 GB (232.885 GB)
      - cmdk3    -     -                         WD-WCAYUN7   250.059 GB (232.885 GB)
      - sd0      -                     9    -                 0 B        (0 B)
      - sd1      ATA   SAMSUNG HD154UI 9    S1XWJ1MSC02676    1.5 TB     (1.365 TB)
      - sd2      ATA   SAMSUNG HD154UI 9    S1XWJ1LS905643    1.5 TB     (1.365 TB)
      - sd3      ATA   SAMSUNG HD154UI 9    S1XWJ1LS905632    1.5 TB     (1.365 TB)
      - sd4      ATA   SAMSUNG HD154UI 9    S1XWJ1WZ403431    1.5 TB     (1.365 TB)
      - sd5      ATA   SAMSUNG HD154UI 9    S1XWJ1LS905642    1.5 TB     (1.365 TB)
      - sd6      ATA   SAMSUNG HD154UI 9    S1XWJ1MSC02675    1.5 TB     (1.365 TB)
      - sd7      ATA   SAMSUNG HD154UI 9    S1XWJ1LS905633    1.5 TB     (1.365 TB)
      - sd8      ATA   SAMSUNG HD154UI 9    S1XWJ1WZ403369    1.5 TB     (1.365 TB)

    Zones: 10 zones running - 13 zones total
      - joyent   arbiter           running    512 MB    10 GB    10.0.1.35   (up 8 days)
      - joyent   cifs              running    512 MB    10 GB    10.0.1.31   (up 8 days)
      - joyent   ns1               running    512 MB    10 GB     10.0.1.2   (up 8 days)
      - joyent   ns2               running    512 MB    10 GB     10.0.1.3   (up 8 days)
      - joyent   skyevm            running    512 MB    10 GB    10.0.1.34   (up 50 minutes)
      - joyent   datadyne-hr       running   1024 MB    20 GB    10.0.1.11   (up 8 days)
      - joyent   nagios            running   1024 MB    10 GB    10.0.1.37   (up 4 days)
      - joyent   jetpack           running   4096 MB    10 GB    10.0.1.32   (up 8 days)
      - joyent   vulture           running   4096 MB   100 GB    10.0.1.30   (up 8 days)
      - joyent   gvoice            stopped    256 MB    20 GB    10.0.1.33
      - joyent   chef-build-32     stopped    512 MB    10 GB    10.0.1.40
      - joyent   chef-build-64     stopped    512 MB    10 GB    10.0.1.41
      - lx       plex              running   2048 MB    20 GB    10.0.1.36   (up 8 days)

    Zpool Status:       
     - ok: all pools are healthy

    Disk Space:         
     - warning: goliath 82%, zones 42%

    SMF Status:         
     - ok: all services are online

    Memory Usage:       
     - ok: 1.484 GB / 15.747 GB (9.43%)

    Kernel Age:         
     - ok: joyent_20150423T155306Z - 10 days old (10 days)

    Hard Errors:        
     - ok: no hard errors found

Usage
-----

Run with `-l` to get a list of checks that can be run

    $ ./sos -l
    summary
    zpool_status
    disk_usage
    smf_status
    memory_usage
    kernel_age
    hard_errors

You can specify one or more checks by name to run

    $ ./sos zpool_status
    ok: all pools are healthy
    $ ./sos smf_status
    ok: all services are online
    $ ./sos disk_usage
    warning: goliath 82%, zones 42%
    $ echo $?
    1

These checks are Nagios compatible

Finally, some nagios checks also allow custom thresholds

    $ ./sos --warning-disk-usage 85 disk_usage
    ok: goliath 82%, zones 42%
    $ ./sos --critical-disk-usage 50 disk_usage
    critical: goliath 82%, zones 42%

License
-------

MIT License
