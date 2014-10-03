---
layout: post
category : test
tagline: "Gnome Shell activity overview"
tags : [Gnome, GnomeShell, hack]
---
{% include JB/setup %}


## Activity Overview mit dem Windows Key alleine aktivieren

Ist zwar Standard Verhalten, aber in der Sytemeinstellug -> Tastatur ist immer noch _Super-S_ ud man kann dort nicht _Supper_ ohne "echte" Taste setzen.

Aber so sollte es gehen:

in der dconf setting then key  _org.gnome.mutter.overlay-key_ auf den Wert _Super_L_ setzen.

Ist aber noch nicht getestet...
