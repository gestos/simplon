---
layout: post
title: fileselection with ranger
categories:
date: 2016-01-21 09:19:37 +0100
---

## files wählen und in eine Liste schreiben mit ranger

In /home/keuch/Downloads/ranger-1.7.2/ranger/core/actions.py ab Zeile 224:
Dort würde, wenn es keinen "self.fm.copy_buffer" gibt, die "else"-Bedingung MACRO_FAIL greifen.
Stattdessen habe ich jetzt dort eingetragen, daß "%f", d.h. die Datei, über der sich der Cursor befindet, gewählt wird.

        if self.fm.copy_buffer:
            macros['c'] = [fl.path for fl in self.fm.copy_buffer]
        else:
            # Versuch, aus einem leeren copybuffer die aktuelle Highlight-Selektion zu machen
            # macros['c'] = MACRO_FAIL
            macros['c'] = [self.fm.thisfile.relative_path]

Die Änderung ist zunächst in einer "standalone" Version funktionabel (siehe Pfad oben). Wo genau das in einer Debian-/Gentoo-Variante eingtragen wird, müßte man nachgucken.

Im Ranger selber kann man dann die Macros an die shell übegeben.
Hierzu habe ich in $HOME/.config/ranger/rc.conf folgenden Keyboardshortcut eingetragen:
map tl shell echo "%c" >> /home/keuch/files_list_by_ranger || sed "s,'\ ,'\n,g" >> /home/keuch/files_list_by_ranger
was dann zu einer Liste mit je einem Eintrag pro Zeile führt.

Auf meinem derzeitigen Gentoo wäre die Datei /usr/lib/python2.7/site-packages/ranger/core/actions.py
(nicht python3.4 - dort gibt es auch actions.py. Wurde anscheinend von meinem System für beide Versionen installert.

Funktioniert direkt nach editieren der Datei, weil der Python-Code interpretiert und nicht erst kompiliert wird.
