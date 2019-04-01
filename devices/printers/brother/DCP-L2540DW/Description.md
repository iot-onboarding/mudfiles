Brother Multifunction Printer
-----------------------------

https://www.brother.ca/en/p/DCPL2540DW

This printer speaks IPv4 and IPv6.
It has internal ACLs to restrict IPv4 access, but no ACLs for IPv6 access.
This really seems short-sighted as IPv6 is where it needs ACLs more.

The firmware can be upgraded by the device.

It supports HTTPS, but has no valid certificate.

NMAP scan shows the following ports open on IPv4 and IPv6:

    Starting Nmap 7.40 ( https://nmap.org ) at 2019-04-01 10:24 EDT
    Host is up (0.049s latency).
    Not shown: 994 closed ports
    PORT     STATE SERVICE
    23/tcp   open  telnet
    80/tcp   open  http
    443/tcp  open  https
    515/tcp  open  printer
    631/tcp  open  ipp
    9100/tcp open  jetdirect

The device supports google cloud printing, and so a limited amount of
outgoing access would be reasonable.  The MUD file proposed here does not
include that as yet.

In addition, it supports mDNS on port 5353 on the local LAN.

Firmware updates seem to be signaled from update.brother.co.jp,
with a POST.   I could not get it to work directly over IPv4 w/NAT,
but it did work with a HTTP proxy, it uses a POST to;

    http://update.brother.co.jp/KNE_bh7_update_nt/ifax2.asmx/fileUpdate

Firmware itself seems to be downloaded from a23-44-169-72.deploy.static.akamaitechnologies.com
over IPv6 if it is available.

Unfortunately, I missed how the name of the asset is returned.





