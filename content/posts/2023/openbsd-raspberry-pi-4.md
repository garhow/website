---
draft: false
date: 2023-11-05T01:38:23-06:00
title: "My Experience Using OpenBSD 7.3 on the Raspberry Pi 4"
---

A few months ago, I decided to rebuild my email and web server using [OpenBSD](https://www.openbsd.org/) because I appreciate its focus on security, stability, and correctness, which are things that I prioritize in a server, especially one that handles something as important as email. I also really love [OpenSMTPD](https://www.opensmtpd.org/) and [httpd](https://man.openbsd.org/httpd.8), and OpenBSD bundles them with the install. I used a Raspberry Pi 4B for the server and it worked out really well!

## Installation

This was actually the most difficult part of the whole process. Most guides will say to use a serial console for the installation but I don't have the equipment for that right now, so I decided to just use the TTY and a monitor. It can't be that hard, right? Wrong. I spent hours trying to get the installer to even use the HDMI port because it would give you a split-second to input some command like "set tty" or something.. Absolute nightmare. Besides that, the installation went pretty well... except for the fact that I was underpowering the board, making the install last at least 4 hours longer than it normally would take. My fault. I don't even know how I did this. After all that, OpenBSD 7.3 was finally installed on my Raspberry Pi 4. :D

## Performance

OpenBSD 7.3 runs beautifully, at least for the software I'm running on top of it. Even while the mail and web servers are running, it only uses up around 800 MB out of the 4 GB of RAM. I haven't done any graphical stuff with it, so I don't know how well it can handle that.

## Conclusion

Running OpenBSD 7.3 on the Raspberry Pi 4 has been a great experience, besides the install process. Everything runs very smooth, and unlike my previous Raspbian installs, I never have to do any maintenance or anything.. *it just works*.
