---
layout: page
title: About This Node
permalink: /about.html
---

**Node:** {{ site.node_number }}
**Callsign:** {{ site.callsign }}
**Type:** Allstar node and DVSwitch server - DMR (Brandmeister), YSF, P25, D-STAR, NXDN using the DVMEGA DVstick 30.

*DVSwitch Server itself is really three independent systemd services working together:

Analog_Bridge — converts between AMBE digital voice (via a hardware AMBE USB dongle, like a DVMEGA DVstick 30) and analog audio on a USRP-style local interface.

MMDVM_Bridge — speaks the network protocol for whichever digital mode is active (DMR, YSF, P25, D-STAR, NXDN) and hands audio off to Analog_Bridge.

YSFGateway (when running in YSF mode) — manages the actual link to a YSF reflector and exposes a UDP command port for controlling that link.

All three run independently of Asterisk and app_rpt — stopping or restarting DVSwitch Server’s services has no effect on node616925’s normal AllStar operation, and vice versa. - credit to KJ7T server setup*
