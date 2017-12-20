DHCP Anonymity Profiles and implementations
=============================================

![image](images/dhcpcanon.svg)

34C3, Leipzig, 12/12/17

----  ----

Contents
========

- DHCP Anonymity Profiles
- `dhcpcanon`
- `systemd` DHCP client
- MirageOS DHCP client
- You can help
- Questions

----  ----

DHCP
=====

![image](images/serveimage.png)

----

Anonymity Profiles
-------------------

- RFC 7844 (2016)
- MAC randomization
- Windows 10 implementation for Wifi interfaces

![image](images/Windows_darkblue_2012_svg.svg)<!-- .element:  style="width: 50%;height: 50%;" -->

----

Summary RFC 7844
-----------------

- Do not send ``Hostname``
- Do not send ``Hardware vendor``
- ``Client identifier`` is the MAC
- ``Parameter Request List`` (minimized, randomized)
 - In implementations: same options and same order

----

Windows 10 capture
-------------------

![image](images/dhcp_win_req_renew_mac_annotated.svg)

----

ISC DHCP client (``dhclient)`` capture
----------------------------------------

![image](images/dhcp_dhclient_req_renew_mac_annotated.svg)

----  ----

`dhcpcanon`
==============

(thanks ![image](images/prototypefund_square.jpg)<!-- .element:  style="width: 5%;height: 5%" --> @prototypefund)

- GPL -> MIT
- implemented in Python
- packaged for Debian
- in Gnome Network Manager still "experimental" (not compiled by default with ``dhcpcanon``)

![image](images/Python_logo_and_wordmark.svg)<!-- .element:  style="width: 30%; height: 30%;" -->
![image](images/openlogo-nd.svg)
![image](images/Gnomelogo.svg)<!-- .element:  style="width: 10%;height: 10%" -->

----

Ways to run dhcpcanon
-----------------------

- standalone (requires root)
- as a daemon with `systemd` (no root)
- with a [wrapper](https://github.com/infinity0/ambient-rs) (no root)
- with resolvoconf, [resolvconf-admin](https://github.com/dkg/resolvconf-admin) or `systemd-resolved`
- with Gonme Network Manager (requires root)

----  ----

`systemd` DHCP client
======================

- patched (in upstream v235)
- already in Debian sid

![image](images/Freedesktop-logo.svg)<!-- .element:  style="width: 50%;height: 50%" -->

----  ----

MirageOS DHCP client
========================

- ``charrua-core`` DHCP library implemented in Ocaml
- patched in upstream
- TODO:
  - client running in Unix
  - unikernel that could be run in Qubes OS
  - ...

![image](images/mirage-logo-small.png)

----  ----

You can help
================

- Run and report bugs
 - `dhcpcanon` implementation
 - `systemd` DHCP client
 - Gnome Network Manager integration

![image](images/cibo00-Debugging.svg)<!-- .element:  style="width: 20%;height: 20%" -->

----

Include in Debian derivatives
-------------------------------

 - Tails
 - Subgraph OS

![image](images/Tails-logo-flat-inverted.svg)<!-- .element:  style="width: 20%;height: 20%;" -->
![image](images/Subgraph_OS_Logo.png)

----

Package for other Linux OS
---------------------------

- package for your favorite OS
 - Archlinux
 - Fedora, Qubes
 - FreeBSD
 - ...

![image](images/archlinux-logo-dark-scalable.518881f04ca9.svg)<!-- .element: style="width: 300px;" -->
![image](images/fedora_infinity_140x140.png)<!-- .element: style="width: 150px;" -->
![image](images/Qubes_OS_Logo.svg)<!-- .element: style="width: 150px;" -->
![image](images/Freebsd_logo.svg)<!-- .element: style="width: 300px;" -->

----

Implementation in other OS
---------------------------

- Android
 - MAC randomization
 - patches for DHCP client
- Apple stuff
  - Mac OS
  - iOS

![image](images/Android_robot_2014.svg)<!-- .element:  style="width: 150px;" -->
 ![image](images/Apple_logo_black.svg)

----  ----

Questions
===========

Thanks!

juga at riseup dot net

2DA8 1D01 455C 3A00 3219  8850 F305 447A F806 D46B

https://github.com/dhcpap

![image](images/juga_vcard_qr.svg)<!-- .element: style="width: 20%; height: 20%;" -->
![image](images/dhcpap.svg)<!-- .element: style="width: 20%; height: 20%;" -->
