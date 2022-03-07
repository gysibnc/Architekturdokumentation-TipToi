**Architekturdokumentation der Software *TipToi***

# Einführung
<!--
Diese Vorlage einer Architekturdokumentation ... ist eine vereinfachte und angepasste Version der Vorlage arc42[^1] sowie . 
-->
Mit TipToi soll Kindern, unter anderem solche die noch nicht fliessend lesen können, die Möglichkeit geboten werden spielerisch dinge zu lernen. Dazu wird ein «Stift» mit einem Infrarotsensor an seiner Spitze und einem Lautsprecher am anderen Ende eingesetzt. Der Stift kann mit dem Infrarotsensor von einem codierten Papier die Informationen entnehmen, welche er benötigt, um mittels Software zu wissen welche Audiodatei er über den Lautsprecher ausgeben kann. Dies geschieht anhand eines bedrucktem Punkteraster (OID), welche es in jeglicher Form gibt. Beispielsweise als Buch, Puzzle, Figuren, GLobus, etc. Für das Kind ergibt dies einen «Ziele auf das Bild und erhalte eine Erklärung» Effekt. Die Oberfläche, welche ein bedrucktes Punkteraster (OID) hat, kann vom Infrarot-Scanner des tiptoi Stift ausgelesen werden.

# Kontextabgrenzung 
## TipToi Stift
- Das System besteht aus 2 Teilen: Dem TipToi Stift und den codierten Seiten
- Der TipToi Stift kann mit einem USB Kabel an den PC angeschlossen werden. Um neue Audiodateien zu installieren.
- Die codierten Seiten werden durch den Infrarotsenor im TipToi Stift gelesen
- Je nach Code welcher auf dem TipToi Produkt gelesen wird, spielt der Stift die benötigte Audiodatei ab
- Das Kind hört sich Audiofiles an und hat die Möglichkeit, solche selbst auf zu zeichnen
- Via TipToi Manager Software werden die Audiofiles aktualisiert
- Die TipToi Manager Software aktualisiert die Firmware

![Kontext_Diagramm__TipToi_2](Kontext_Dia_TipToi_Stift_V3.png)

## TipToi Manager
- Der Manager lädt Dateien vom Ravensburger TipToi Server
  - Firmwareupdates
  - Audiofiles
- Der Manager kann durch einen Anwender Bsp. die Eltern bedient werden
- Der TipToi Manager lädt die Dateien per USB auf den Stift

![Kontext_Diagramm__TipToi](Kontext_Diagramm_TipToi_v.2.jpg)

# Anforderungen
## Funktionale Anforderungen TipToi-Stift
- Das Kind muss den Stift einschalten können
- Das Kind muss den Stift ausschalten können
- Das Kind muss das Buch Initial scannen können
- Das Kind muss die im Buch vorhanden Codes scannen können
- Die Eltern müssen die Batterien einsetzen können
- Die Eltern müssen die Audiofiles auf den Stift laden können
- Der TipToi Manager lädt die Audiofiles vom Ravensburger Server
- Der TipToi Manager aktualisiert die Firmware des TipToi Stiftes automatisch
- Der Entwickler kann die OID-Debug-Funktion TipToi Produkte nutzen

![Use_Case_TipToi](Use_Case_TipToi_V3.png)

## Funktionale Anforderungen TipToi-Manager
- Die Eltern können Produkte suchen
- Die Eltern können Audiofiles  herunterladen
- Die Eltern können Firmware des Stifts aktiv updaten
- Die Eltern richten einen Account auf dem Manager ein
- Der Ravensburger TipToi Server stellt oben genannte Punke zur Verfügung
- Der TipToi Stift kann Firmware Updates verarbeiten
- Audiofiles können auf den TipToi Stift geladen und/oder davon gelöscht werden

![Use_Case_TipToi](Use_Case_TipToi_Manager.png)

## Qualitätsanforderungen
-	Der Stift muss mittels der Software eine oder mehrere Audiodateien eindeutig einem Code zuweisen können.
-	verarbeiten können.
-	Die Software soll nicht abstürzen.
-	Der Stift muss die verschiedenen Dateien voneinander unterscheiden können. 
-	Der Stift muss von einem Kind bedient werden können. 
-	Der Stift muss der Handhabung eines Kindes standhalten. 
-	Die codierte Hardware sollte robust genug für die Handhabung eines Kindes sein. 
-	Die Codierung auf dem Papier darf nicht zu auffällig sein, jedoch auch noch vom Stift lesbar sein. 


## Randbedingungen
<!-- *Anforderungen, Vorgaben, welche das Team beim Design der Software einschränkt* -->
- Da der Stift nicht unendlich Speicherkapatzität hat, sollte die Software nicht zu gross sein
- Jede codierte Hardware muss einen eindeutigen Idenifizierungscode haben
- Es muss beachtet werden, dass die Software mehrsprachig ist


# Verteilungssicht
<!--*Verteilungsdiagramm + Beschreibung*-->
- Der Personal Computer wird per USB Schnittstelle mit dem Stift verbunden
- Der TipToi Manager holt die Audiofiles und Firmware Updates auf dem Ravensburger TipToi Server und übergibt diese dem TipToi Stift
- Der TipToi Stift list den OID Code mittels Infrarot aus dem TipToi Produkt

![Verteilungs_Diagramm__TipToi](Verteilungs_Diagramm_TipToi_v2.png)


# Glossar
OID Code = (optical identification) - Oberfläche mit einem bedrucktem Punkteraster 

<!-- Dieser Abschnitt ist auskommentiert
[^1]: www.arc42.de
-->

