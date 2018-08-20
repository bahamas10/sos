SmartOS Summary
===============

SmartOS Summary - works in global and non-global zones

Example
-------

Run without any arguments to get a summary

#### Triton Headnode

![screenshot-headnode](/screenshots/headnode.png)

#### Global Zone

![screenshot-global-zone](/screenshots/global-zone.png)

#### Non-Global Zone

![screenshot-zone](/screenshots/zone.png)

Example
-------

    # sos -f -l triton

	  *--+--*--*         root@datadyne.rapture.com
	  |\ |\ |\ |\        -------------------------
	  | \| \| \| \       OS: Joyent SmartOS (SunOS) (sdc 7.0)
	  +--*--+--*--*      Kernel: 20180510T153535Z (3 months old)
	  |\ |\ |\ |\ |      Zonename: global
	  | \| \| \| \|      Uptime: 1 month (41 days)
	  *--+--+--+--+      Memory: 5.21 GB / 31.97 GB (16%)
	   \ |\ |\ |\ |      CPU: 8 x Intel(r) Xeon(r) CPU E3-1230 V2 @ 3.30GHz (3300 MHz)
	    \| \| \| \|      SMF: 92 services online
	     *--+--*--*      Packages: 109 installed (2004M) pkgin 2016Q4
	  Joyent SmartOS     VMs: 20 running (20 total)
			     Zpool Usage: goliath 22%, zones 6%

    Interfaces: 2
      - lo0      127.0.0.1, ::1
      - e1000g0  10.0.1.10

    Devices: 23
      - sd0      Kingston DataTraveler 2.09    -                 0          (0)
      - sd1      HGST  HUS724040ALS640 9    PBK6SNNX          3.64 TB    (3.64 TB)
      - sd2      HGST  HUS724040ALS640 9    PBK6DU7X          3.64 TB    (3.64 TB)
      - sd3      HGST  HUS724040ALS640 9    PBHNTKKX          3.64 TB    (3.64 TB)
      - sd4      HGST  HUS724040ALS640 9    PBHNJK6X          3.64 TB    (3.64 TB)
      - sd5      HGST  HUS724040ALS640 9    PBHNTVDX          3.64 TB    (3.64 TB)
      - sd6      HGST  HUS724040ALS640 9    PBK3YTZX          3.64 TB    (3.64 TB)
      - sd7      HGST  HUS724040ALS640 9    PBK6S6DX          3.64 TB    (3.64 TB)
      - sd8      HGST  HUS724040ALS640 9    PBK3KTRX          3.64 TB    (3.64 TB)
      - sd9      HGST  HUS724040ALS640 9    PBHN3Z6X          3.64 TB    (3.64 TB)
      - sd10     HGST  HUS724040ALS640 9    PBK32YAX          3.64 TB    (3.64 TB)
      - sd11     HGST  HUS724040ALS640 9    PBK58W4X          3.64 TB    (3.64 TB)
      - sd12     HGST  HUS724040ALS640 9    PBK3K0PX          3.64 TB    (3.64 TB)
      - sd13     ATA   Corsair Nova 2 S9    120665020000134   27.96 GB   (27.96 GB)
      - sd14     ATA   M4-CT064M4SSD2  9    000000001151032   59.63 GB   (59.63 GB)
      - sd15     HGST  HUS724040ALS640 9    PBHNZJAX          3.64 TB    (3.64 TB)
      - sd16     HGST  HUS724040ALS640 9    PBK6896X          3.64 TB    (3.64 TB)
      - sd17     HGST  HUS724040ALS640 9    PBK674VX          3.64 TB    (3.64 TB)
      - sd18     HGST  HUS724040ALS640 9    PBHNZK1X          3.64 TB    (3.64 TB)
      - sd19     HGST  HUS724040ALS640 9    PBHMRA6X          3.64 TB    (3.64 TB)
      - sd20     HGST  HUS724040ALS640 9    PBHP4V9X          3.64 TB    (3.64 TB)
      - sd21     HGST  HUS724040ALS640 9    PBK67YGX          3.64 TB    (3.64 TB)
      - sd22     HGST  HUS724040ALS640 9    PBK6DUKX          3.64 TB    (3.64 TB)

    VMs: 20 running (20 total)
      - joyent   acme              running    512 MB    10 GB    10.0.1.45   (up 1 month)
      - joyent   bart              running    512 MB    10 GB    10.0.1.30   (up 3 months)
      - joyent   cifs              running    512 MB    10 GB    10.0.1.31   (up 3 months)
      - joyent   jabber            running    512 MB    10 GB    10.0.1.38   (up 3 months)
      - joyent   mqtt              running    512 MB    10 GB    10.0.1.44   (up 1 month)
      - joyent   ns2               running    512 MB    10 GB     10.0.1.3   (up 1 month)
      - joyent   qseer             running    512 MB   200 GB    10.0.1.34   (up 3 months)
      - joyent   red               running    512 MB    10 GB    10.0.1.43   (up 1 month)
      - joyent   tftp              running    512 MB    10 GB     10.0.1.6   (up 3 months)
      - joyent   vpn               running    512 MB    10 GB     10.0.1.5   (up 3 months)
      - joyent   arbiter           running   1024 MB    50 GB    10.0.1.35   (up 23 days)
      - joyent   nagios            running   1024 MB    10 GB    10.0.1.37   (up 3 months)
      - joyent   test              running   1024 MB    10 GB    10.0.1.41   (up 1 month)
      - joyent   ops               running   2048 MB    10 GB    10.0.1.33   (up 3 months)
      - joyent   vault             running   2048 MB    10 GB    10.0.1.32   (up 3 months)
      - joyent   build             running   4096 MB   100 GB    10.0.1.29   (up 3 months)
      - lx       btsync            running   1024 MB    20 GB    10.0.1.40   (up 3 months)
      - lx       hass              running   1024 MB    20 GB    10.0.1.42   (up 1 month)
      - lx       plex              running   2048 MB    50 GB    10.0.1.36   (up 3 months)
      - lx       vulture           running   4096 MB    50 GB    10.0.1.39   (up 26 days)

    Hard Errors:
     - ok: no hard errors found

    Zpool Status:
     - ok: all pools are healthy

Usage
-----

    $ sos -h
    Usage: sos [--color=auto|yes|no] [-l <logo>] [--full] [--help]

    SOS - SmartOS Summary
      Gather and display information about a SmartOS installation

    Options
      -c, --color=auto|no|yes  enable/disable color output, defaults to auto
      -C, --main-color=blue    main color to use in output, defaults to blue
      -f, --full               additional output
      -h, --help               print this message and exit
      -l, --logo=name          logo name, defaults to automatic

License
-------

MIT License
