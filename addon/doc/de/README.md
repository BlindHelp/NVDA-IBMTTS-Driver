# IBMTTS-Treiber, Erweiterung f�rNVDA #
  Diese Erweiterung erm�glicht das Einbinden der IBMTTS-Sprachausgabe in NVDA.  
  Die eigentlichen IBMTTS-Bibliotheken d�rfen nicht angeboten werden, daher handelt es sich hierbei nur um den Treiber.  
  Wenn du bei der Verbesserung des Treibers mithelfen m�chtest, z�gere nicht uns einen Pull-Request zu senden!  

# Herunterladen.
Die neueste Version kann unter [diesem Link heruntergeladen werden](https://davidacm.github.io/getlatest/gh/davidacm/NVDA-IBMTTS-Driver)

# Funktionen:
* Anpassung von Stimme, Variante, Geschwindigkeit, Tonh�he, Betonung und Lautst�rke.
* Zus�tzliche Parameter f�r Kopfgr��e, Rauigkeit und Atmung. Erstelle deine eigene Stimme!
* Verwendung von Backquote-Sprachtags erlauben. Lasse sie zum Schutz vor Schadcode und Scherzkeksen ausgeschaltet oder schalte sie ein, um jede Menge Spa� mit der Sprachausgabe zu haben. Es m�ssen allerdings auch einige Anpassungen in NVDA vorgenommen werden, damit dies korrekt funktioniert.
* Geschwindigkeit zus�tzlich erh�hen. Falls dir die Sprachausgabe zu langsam ist, schalte diese Option ein und hole das Maximum an Geschwindigkeit heraus!
* Automatischer Sprachenwechsel. Liest den Text automatisch in der richtigen Sprache vor.
* Umfangreicher Filter. Dieser Treiber enth�lt einen umfangreichen Satz aus Filtern, mit denen Abst�rze oder seltsames Verhalten der Sprachausgabe vermieden werden.
* W�rterbuch-Unterst�tzung. Dieser Treiber erlaubt  das Einbinden spezieller W�rter, Stammw�rterb�cher sowie Abk�rzungsw�rterb�cher f�r jede Sprache. Fertige W�rterb�cher sind im [Community-Dictionary-Repository](https://github.com/thunderdrop/IBMTTSDictionaries) oder im [alternativen Repository von mohamed00 (inklusive IBM-Sprachausgabenw�rterb�cher)](https://github.com/mohamed00/AltIBMTTSDictionaries) verf�gbar

# Voraussetzungen.
## NVDA.
  NVDA 2018.4 oder neuer ist erforderlich. Dieser Treiber ist mit Python 3 kompatibel, und kann auch in zuk�nftigen NVDA-Versionen genutzt werden. Sobald NVDA mit Pyton 3 ver�ffentlicht wurde, wird diese Erweiterung nicht mehr mit Python 2.7 kompatibel sein. Bitte verwende daher immer die neueste NVDA-Version. Es ist kostenlos! 

## IBMTTS-Sprachausgabenbibliotheken.
  Dies ist nur der Treiber, du musst dir die Bibliotheken selbst besorgen.  
  Dieser Treiber unterst�tzt die etwas neueren Bibliotheken, in denen ostasiatische Sprachen sowie spezifische Fehlerkorrekturen f�r bessere Textkodierung enthalten sind. �ltere Bibliotheken sollten jedoch auch funktionieren.  
  Seit Version 21.01 unterst�tzt der Treiber auch die Integration der noch etwas neueren IBM-Bin�rdateien, und nicht nur die SpeechWorks-Bin�rdateien. Ein Satz unabh�ngiger korrekturen ist f�r diesen Treiber enthalten, und die zus�tzlichen Sprachen und anderen Unterschiede werden ber�cksichtigt. Nur die Formant-Stimmen werden derzeit unterst�tzt. Danke an @mohamed00 f�r diese Arbeit.

# Installation.
  Du kannst die Erweiterung wie jede normale NVDA-Erweiterung installieren. �ffne danach die NVDA-Einstellungen und w�hle die IBMTTS-Dateien in der Kategorie IBMTTS.
  Hier kannst du auch die IBMTTS-Dateien in eine Erweiterung kopieren, um sie lokal zu verwenden.

# F�r die Weiterverbreitung paketieren.
  �ffne eine Kommandozeile im Hauptverzeichnis der Erweiterung und lasse den Befehl scons laufen. Die Erstellte Erweiterung wird, sofern keine Fehler aufgetreten sind, im Hauptverzeichnis abgelegt.

## Hinweise:

* Wenn sich die Sprachausgabe in der Erweiterung oder der "eciLibraries"-Erweiterung befindet, aktualisiert der Treiber automatisch die Pfade in den Ini-Dateien, sodass du sie in einer portablen NVDA-Kopie verwenden kannst.
* Beim Verwenden der Schaltfl�che zum Kopieren der IBMTTS-Dateien wird eine neue Erweiterung erstellt. Wenn du IBMTTS wieder deinstallieren m�chtest, m�ssen zwei Erweiterungen deinstalliert werden, n�mlich "IBMTTS-Treiber" und "Eci libraries".
* Die Scons und Gettext-Werkzeuge in diesem Projekt sind nur mit Python 3 kompatibel. Python 2.7 funktioniert nicht.
* Du kannst die ben�tigten IBMTTS-Dateien auch direkt in der Erweiterung ablegen (nur f�r pers�nliche Nutzung). Kopiere sie einfach in das Verzeichnis "addon\synthDrivers\ibmtts". Der Standard-Bibliotheksname kann falls notwendig in der Datei "settingsDB.py" angepasst werden.

# Referenzen.
Dieser Treiber basiert auf dem IBM-TTS-SDK, dessen Dokumentation unter [diesem Link](http://www.wizzardsoftware.com/docs/tts.pdf) verf�gbar ist.

Eine Kopie ist auch in [diesem Repository](https://github.com/david-acm/NVDA-IBMTTS-Driver) erh�ltlich.

Siehe die Dateien

[tts.pdf](https://cdn.jsdelivr.net/gh/davidacm/NVDA-IBMTTS-Driver/apiReference/tts.pdf)
oder [tts.txt.](https://cdn.jsdelivr.net/gh/davidacm/NVDA-IBMTTS-Driver/apiReference/tts.txt)
