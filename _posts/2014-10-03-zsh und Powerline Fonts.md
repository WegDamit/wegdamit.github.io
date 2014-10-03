---
layout: post
category : shell
tagline: "Gnome Shell activity overview"
tags : [Gnome, GnomeShell, hack]
---
{% include JB/setup %}

# Powerline Fonts für zsh prompt installieren

Die Powerline fonts werden mit einem Trick "über" andere Fonts gelegt und verdeckt dort die Zeichen die in den Powerline Fonts vorkommen, was "private" Bereiche sind, also i.A. keine.

In welchen Fonts das passiert wird in der fontconfig Konfiguration (s.u.) angegegen.

Dazu erst mal die Fonts aus dem [Netz holen](https://github.com/Lokaltog/powerline/raw/develop/font/PowerlineSymbols.otf) und nach
_/usr/share/fonts/opentype/PowerlineSymbols/PowerlineSymbols.otf_ kopieren.

Und dann in fontconfig _/etc/fonts/conf.avail/10-powerline-symbols.conf_ den unten angegeben Inhalt einfügen und die Datei nach _/etc/fonts/conf.d/_ linken.

```xml
<?xml version="1.0"?>
<!DOCTYPE fontconfig SYSTEM "fonts.dtd">

<fontconfig>
    <alias>
        <family>monospace</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Droid Sans Mono</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Droid Sans Mono Slashed</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Droid Sans Mono Dotted</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>DejaVu Sans Mono</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>DejaVu Sans Mono</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Envy Code R</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Inconsolata</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Lucida Console</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Monaco</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Pragmata</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>PragmataPro</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Menlo</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Source Code Pro</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Consolas</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Anonymous pro</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Bitstream Vera Sans Mono</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Liberation Mono</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Ubuntu Mono</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Meslo LG L</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Meslo LG L DZ</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Meslo LG M</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Meslo LG M DZ</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Meslo LG S</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
    <alias>
        <family>Meslo LG S DZ</family>
        <prefer><family>PowerlineSymbols</family></prefer>
    </alias>
</fontconfig>

```

