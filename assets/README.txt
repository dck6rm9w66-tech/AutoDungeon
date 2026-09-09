Auto-Dungeon: Legacy — eigene Grafiken verwenden
================================================

Jede PNG-Datei in diesem Ordner ersetzt die vom Spiel erzeugte Grafik.
Fehlt eine Datei oder lässt sie sich nicht laden, zeichnet das Spiel das
Motiv wie bisher selbst — die generierte Grafik ist nur das Fallback.
Der Ordner muss neben index.html liegen.

Maße
----
    Gegner und Klassenkörper   64 x 64 Pixel
    Charaktere (64 Stück)      64 x 64 Pixel
    Bosse                      80 x 80 Pixel
    Gegenstände und Symbole    64 x 64 Pixel

Format: PNG mit Alphakanal (echte Transparenz, kein Farbschlüssel).
Ein Pixel der Datei ist ein Pixel im Spiel; das Spiel skaliert selbst.

Regeln
------
* Figuren stehen auf der untersten belegten Zeile. Unten keinen leeren
  Rand lassen, sonst schwebt die Figur über dem Boden.
* Blickrichtung: Gegner werden gespiegelt, Helden nicht. Alles nach
  rechts blickend zeichnen.
* Waffen werden am Helden aufrecht gezeichnet, Griff unten, Spitze oben.

Die 64 Charaktere
-----------------
Für jede Kombination aus Unterrasse und Klasse gibt es eine eigene Datei:

    hero_<unterrasse>_<klasse>.png

Unterrassen
    Mensch   nordmensch, steppenvolk, kuestenvolk, bergmensch
    Elf      waldelf, hochelf, dunkelelf, sonnenelf
    Zwerg    steinbart, feuerbart, eisenbart, graubart
    Ork      gruenhaut, aschenork, blutork, sumpfork
Klassen
    warrior, mage, rogue, paladin

4 Rassen x 4 Unterrassen x 4 Klassen = 64 Dateien, zum Beispiel
hero_dunkelelf_rogue.png oder hero_feuerbart_paladin.png.

In diesen Dateien stecken die Rassenmerkmale bereits drin: Ohren, Bart,
Hauer, Hörner, Stirnband, Diadem, Narbe und Hautton. Das Spiel zeichnet
sie deshalb nicht zusätzlich und färbt die Datei auch nicht um — was du
malst, wird genau so angezeigt. Fehlt eine Datei, greift der
Klassenkörper hero_<klasse>.png plus die gezeichneten Merkmale.

Die Statur regelt das Spiel über die Skalierung: Zwerge werden kleiner
und breiter gezeichnet, Orks größer. Zeichne alle 64 Dateien gleich groß.

Farben
------
Gegner sind im Farbton 210 (Blau) gerendert. Das Spiel dreht den Farbton
je Gegnerart und Affix weiter — ein Feuer-Slime wird rot, ein Gift-Slime
grün. Wer das nicht will, zeichnet in Graustufen. Charaktere, Gegenstände
und Symbole werden nicht umgefärbt und dürfen frei koloriert werden.

Übrige Dateien
--------------
Gegner   slime, humanoid, bandit, beast, pflanze, flying, rebell, untoter,
         kultist, golem, geist, elementar, gespenst, parasit, mutant,
         tyrant, daemon, alien, astral, lich, eldritch
Bosse    boss0 ... boss6
Klassen  hero_warrior, hero_mage, hero_rogue, hero_paladin (Rückfallebene)
Reittiere mount_horse, mount_tiger, mount_lizard, mount_griffin
Fallen   trap_spikes, trap_darts, trap_bear, trap_flame, trap_frost,
         trap_curse
Objekte  object_fountain (Lebensbrunnen)
Segen    boon_might, boon_haste, boon_ward, boon_blood, boon_fortune,
         boon_edge
Waffen   weapon_sword, weapon_dagger, weapon_axe, weapon_staff,
         weapon_bow, weapon_hammer
Rüstung  armor_head, armor_chest, armor_hands, armor_legs, armor_feet,
         armor_offhand, armor_orb, armor_ring, armor_amulet
Steine   gem_ruby, gem_sapphire, gem_emerald, gem_topaz, gem_amethyst,
         gem_onyx   (die zehn Güten färbt das Spiel über den Rahmen)
Runen    rune_1 ... rune_8   (werden je Rune zufällig zugeordnet)
Sonstige misc_potion, misc_shard, misc_gold

manifest.json listet alle Dateien mit ihren Maßen.
