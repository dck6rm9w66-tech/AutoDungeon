Auto-Dungeon: Legacy — Musik
============================

Die sechs Stücke sind eigens für dieses Spiel komponiert und frei nutzbar.
Sie liegen doppelt vor:

    <name>.ogg   fertig gerenderte Aufnahme, die das Spiel abspielt
    <name>.mid   dieselbe Komposition als Standard-MIDI (Format 1, 5 Spuren)

Die MIDI-Dateien lassen sich in jedem Notensatz- oder Musikprogramm öffnen
(MuseScore, Reaper, LMMS, FL Studio, Logic, Online-MIDI-Editoren), neu
instrumentieren und über einen beliebigen Soundfont ausspielen.

Stücke
------
wander.ogg      Wanderers Pfad        100 BPM, Dur, hell
                Wald, Hügel, Küste, Nebelhain
village.ogg     Herdfeuer im Dorf     116 BPM, Dur, warm
                Dorf, Freie Stadt
halls.ogg       Hallen aus Stein       84 BPM, Moll, düster
                Schloss, Kerker, Verlies
ember.ogg       Emberthron            126 BPM, phrygisch, drohend
                Höllenschlund
steel.ogg       Klinge und Stahl      142 BPM, Moll, treibend
                normaler Kampf
reckoning.ogg   Abrechnung            152 BPM, harmonisch Moll, wuchtig
                Miniboss und Weltenboss

Eigene Musik verwenden
----------------------
Ersetze einfach die OGG-Datei unter gleichem Namen. Das Spiel lädt beim
Start alles aus diesem Ordner, blendet beim Wechsel weich über und
wiederholt jedes Stück nahtlos. Fehlt eine Datei oder der ganze Ordner,
schaltet das Spiel auf den eingebauten Synthesizer um; gespielt wird also
in jedem Fall etwas.

Auch andere Formate funktionieren, solange der Browser sie kennt
(.ogg, .mp3, .m4a) — dann muss die Dateiendung im Spiel angepasst werden
(Konstante MUSIC_DIR bzw. der Ladepfad in MusicEngine.preload).

Die Stücke sind auf nahtlose Schleifen gerendert: Der Nachhall des letzten
Takts ist in den Anfang zurückgefaltet. Achte bei eigenen Aufnahmen darauf,
sonst hört man den Ansatz bei jeder Wiederholung.
