
                                   Abschlussprüfung Sommer 2023
Fachinformatiker für Anwendungsentwicklung
Dokumentation zur betrieblichen Projektarbeit
Entwurf und Implementierung der Mitgliederverwaltung und der
Benutzerrechtevergabe für den Relaunch des Internetauftritts des gemeinnützigen Vereins „Freundeskreis DPSG St. Liborius“ aus Dortmund-Körne.
Prüfungbewerber
Richard Monemou
Martener Straße 336
44379 Dortmund

Praktikumsbetrieb
                                        
                                             NH Computer Lerning Center LLC
                              Stockholmer Allee 30c
                                   44269 Dortmund

                                                        Ausbildungbetrieb
              Qualifizierungsakademie Rhein Ruhr GmbH & Co. KG
                                Stockholmer Allee 30c
                                    44269 Dortmund
 
  
Inhalt
1	Einführung	1
2	Projektdefinition	1
2.1	Umfeld	1
2.2	Projektbegründung	2
2.3	Projektbeschreibung	2
2.4	Projektziel	2
2.5	Schnittstellen	2
2.6	Abgrenzung	3
2.6.1	Einstieg:	3
2.6.2	Ausstieg:	3
2.6.3	Abweichung zum Antrag	3
3	Analyse	3
3.1	Vorgespräch	3
3.2	Ist-Situation	4
3.3	Lastenheft	4
3.4	Soll-Konzept	5
3.4.1	Funktionale Anforderungen	5
3.4.2	Nicht Funktionale Anforderungen	6
4	Planung	6
4.1	Arbeitspakete und Projektstrukturplan	6
4.2	Projektplanung	7
4.2.1	Zeitplanung	7
4.2.2	Gantt-Diagramm	8
4.3	Projektmanagement-Methode	11
4.4	Ressourcenplanung	12
4.5	Kostenplanung	13
4.6	Wirtschaftlichkeit	14
5	Design	14
5.1	Anwendungsfall-Diagramm	14
5.2	Datenbankmodell	15
5.2.1	ER-Modell	15
5.3	Login Formular	16
5.3.1	Nach Login	16
5.4	Mitglieder	17
5.5	Administrator	17
5.6	Kassenwart	17
5.7	Programmablaufplan Login	17
6	Durchführung	18
6.1	Entwicklungsprozess	18
6.2	Implementierung Login System	20
6.3	Absicherung gegen Ausprobieren von URLs oder Einfügen	21
6.4	Implementierung persönlicher Mitgliederbereich	21
6.5	Implementierung Kassenwartbereich	22
6.6	Implementierung Admin Bereich	23
7	Testphase	25
7.1	Whitebox Tests	25
7.2	Blackbox Tests	25
7.3	Testfälle	26
7.4	Testfälle Vorgehensweise Beschreibung	27
7.4.1	Kompatibilität und Responsivität	27
7.4.2	Anmeldung von Mitgliedern	28
7.4.3	Administrative Rechte	28
7.4.4	Einfache Mitglieder Rechte	30
7.5	Kassenwart Rechte	31
8	Abschluss	31
8.1	Übergabe und Abnahme	31
8.2	Dokumentation	31
8.3	Fazit	31
8.4	Soll-Ist-Vergleich der Ausführung	32
8.5	Soll-Ist-Vergleich Zeitplanung	32
8.6	Ausblick	33
9	Persönliche Erklärung	33
1	Tabellenverzeichnis	I
2	Abbildungsverzeichnis	I
3	Code Auszuge	II
4	Glossar	III
5	Codeauszüge	IV
5.1	Quellcode für Das Login System	IV
5.2	Quellcode für Mitglieder Anlegen	VI
5.3	Quellcode für Passwort Reset	X
6	Lastenheft Auszug	XIV
7	Pflichtenheft Auszug	XV
7.1	Behalten der Bisherige Hoster	XV
7.2	Funktionale Anforderungen	XV
7.3	Nicht Funktionale Anforderungen	XV
8	Testprotokolle	XVI
9	Kundendokumentation	XVIII

 
1	Einführung
Das folgende Projekt wird als Abschlussprojekt im Rahmen der Ausbildung zum Fachinformatiker für Anwendungsentwicklung durchgeführt. Das Projekt umfasst den Entwurf, die Umsetzung und Implementierung der Mitgliederverwaltung und die Benutzerrechtevergabe für das Gesamtprojekt „Relaunch des Internetauftritts des gemeinnützigen Vereins Freundeskreis DPSG St. Liborius“.
Neben dem Angebot für „normale“ Besucher der Seite soll für Vereinsmitglieder ein erweitertes Angebot bestehen.
Die Mitgliederverwaltung soll den unterschiedlichen Nutzergruppen folgende Möglichkeiten bieten:
Für alle Mitglieder:
•	Eigene Daten bearbeiten 
•	Daten aller Mitglieder sehen
Für den Administrator:
•	Neue Mitglieder eintragen
•	Bestehende Mitglieder bearbeiten und löschen
•	Mitglider Rechte vergeben und ändern
Für den Kassenwart:
•	Finanzdaten, wie gezahlte bzw. offene Mitgliedsbeiträge u.Ä. sehen und bearbeiten
2	Projektdefinition
2.1	Umfeld
Der Betrieb New Horizons Dortmund gehört zu New Horizons Worldwide LLC, dem seit 1997 bestehenden, welt-größten, unabhängigen Anbieter von IT-Trainings mit Niederlassungen auf 6 Kontinenten. Obwohl das Unternehmen in erster Linie ein Bildungsanbieter im IT-Bereich ist, setzt es jedoch zusätzlich gelegentlich Projekte für befreundete Unternehmen / Institutionen um.
Eine dieser Institutionen ist der gemeinnützige Verein „Freundeskreis DPSG St. Liborius“ aus Dortmund-Körne, der seine Website relaunchen will.
2.2	Projektbegründung
Der bisherige Internetauftritt des Vereins wird vom bisherigen Web-Host technisch nicht mehr unterstützt wegen veraltete PHP Version und muss daher zumindest funktional vollständig überarbeitet werden. Aufgrund des durch die erforderlichen Anpassungen resultierenden Arbeitsaufkommens bietet sich gleichzeitig eine vollständige Überarbeitung der Benutzerführung und Neugestaltung der Internetpräsenz an, auch weil zusätzliche Features in den Internet-Auftritt integriert werden sollen. 
2.3	Projektbeschreibung
Für das Gesamtprojekt – den Relaunch der Vereinswebsite – wird in diesem Teilprojekt die Rechtevergabe und Migliederverwaltung für vereinsinterne Nutzer der Website realisiert.
Der Fokus liegt hierbei auf der Implementierung der entsprechenden Backend-Funktionalität. Die zu nutzende Technologie wird hierbei vom Webhoster bestimmt:
Für die Darstellung HTML 5 und CSS 3, für die Datenbank und die Anbindung per Skriptsprache MySQL und PHP 8.x.
Da das Prokziel eine lokal lauffähige Version der Site ist, kommt für die Entwicklung das Paket „XAMPP“ mit dem Webserver „Apache“ und den oben genannten Komponenten MySQL bzw. MariaDB und PHP zum Einsatz.
2.4	Projektziel
Ziel ist es ein funktionierendes Backend für die Benutzerverwaltung der Website zu entwickeln. 
2.5	Schnittstellen
Technisch:
Weil der Auftraggeber seinen bisherigen Provider Host Europe behalten möchte, sind wie schon in 2.3 beschrieben die folgenden technischen Schnittstellen für die Umsetzung dieses Projekts von Bedeutung:  HTML5, PHP in Version 8, MySQL und Apache Webserver für die lokale Entwicklungsumgebung.
Personell:
Herr Dennis Faughn für den Auftraggeber New Horizons
Herr Daniel Christ als Vereinsvorstand des Freundeskreises.
Frau Kerstin Burslam für das Teil-Projekt "Veranstaltungs- und Finanzverwaltung" 
2.6	Abgrenzung
2.6.1	Einstieg:
Das Projekt begründet sich in der nicht mehr funktionsfähigen Webseite des Vereins und dem Wunsch, nicht den Webhoster zu wechseln.
2.6.2	Ausstieg: 
Das Projekt gilt als abgeschlossen, wenn die Anwendung auf einem Rechner mit einem lokalen Webserver funktionsfähig ist.
2.6.3	Abweichung zum Antrag
Das Teilprojekt gilt als erfolgreich abgeschlossen, wenn das Teilprojekt die benötigte Funktionalität aufweist ohne dass die beiden Teilprojekte auf einem Server zusammengeführt werden.
3	Analyse
3.1	Vorgespräch
Die Firma New Horizons GmbH möchte für ihren Kunden, der Verein „Freundeskreis DPSG St Liborius“ aus Dortmund-Körne die Webseite www.freundeskreis-libori.de relaunchen.
Teilnehmende des Gespräches waren außer den Projektdurchführenden ein Vertreter des Freundeskreises DPSG St Liboris der Auftraggeber „Denis Faughn“ und ein Angestellter der QA als technischer Berater. Dabei wurden grob die Wünsche und Anforderungen an den zukünftigen Web-Auftritt formuliert. Besonderer Wert wurde hierbei auf die folgenden Features gelegt:
•	Einrichtung einer sicheren, verschlüsselten Verbindung für die gesamte Webseite 
•	Überarbeitung/Homogenisierung der Benutzerführung
•	Diferenzierte Zugriffs-und Editionsberechtigungen für unterschiedliche Benutzergruppen
3.2	Ist-Situation
Auf Basis des Vorgesprächs, wurde folgende Ist-Situation erfasst:
Aufgrund technischer Probleme, einer veralteten PHP-Version und nicht mehr funktionsfähigen Joomla-Templates / Plug-Ins ist die Site auf dem bisherigen Webspace nicht mehr funktionsfähig bzw. aufrufbar. Zum Beispiel sind die Seiten für Internet-Explorer 8 und 9 optimiert, für die der Support bereits 2016 eingestellt wurde. 
Der bisherige Login-Bereich ist nicht verschlüsselt und die Benutzerführung ist verwirrend, da die Funktionalitäten auf verschiedene Menüs verteilt und an unterschiedlichen Stellen platziert bzw. nur zeitweise sichtbar sind. 
3.3	Lastenheft 
Nach der Feststellung der Ist-Situation folgt die Fertigstellung des Lastenheftes. Die Gesamtheit der Anforderungen des Auftraggebers an die Funktionalität und die Eigenschaften der Softwarelösung wurden anhand der essenziellen Fragen „Was wird gemacht?“ und „Wofür wird es gemacht?“ im Lastenheft festgehalten. Die Ziele des Lastenheftes wurden weitestgehend nach der MosCoW-Methode (Must, Should, Could, Won`t have) formuliert. Diese Methodik hilft zum einen bei der klaren Gestaltung der Zielsetzung und ermöglicht zudem eine Priorisierung der einzelnen Anforderungen an die Softwarelösung.
Must	„Als Kunde muss ich…“:	Anforderung muss umgesetzt werden
Should	„Als Kunde sollte ich…“:	Anforderung sollte umgesetzt werden, wenn die „Must“-Anforderung nicht beeinträchtigt, wird
Could	„Als Kunde möchte ich…“:	Anforderung kann umgesetzt werden, wenn die „Must- und Should“- Anforderung nicht beeinträchtigt werden
Won`t	„Als Kunde möchte ich nicht…“:	Anforderungen werden nicht umgesetzt
Tabelle 1-Moscow-tabelle
Ein Auszug des Lastenheftes befindet sich im Anhang 
3.4	Soll-Konzept
Folgende zu implementierende Features für die Teilbereiche der Webseite sind Rahmen des Relaunches angedacht.
Feature für die gesamte Website:
Das User-Interface und die Darstellung der Inhalt der Websites soll mit responsivem Design unter Einhaltung der W3C-Standards umgesetzt werden, damit sie sowohl auf stationären als auch auf unterschiedlichen mobilen Endgeräten korrekt bzw. einheitlich angezeigt wird. Um die Anforderungen zum Schutz personenbezogener Daten zu erfüllen, soll die Webseite zukünftig nur noch über eine gesicherte SSL-Verbindung aufgerufen werden.
Feature Mitglieder-Konto: 
•	Verschlüsselter Login
•	Änderungsmöglichkeit für die eigenen Kontaktdaten  
•	Ansicht der Kontaktliste (intern)
Feature Zugriffsverwaltung:
Für die Website sind folgende Nutzergruppen angedacht, für die ein Log-In erforderlich ist:
•	Vereinsmitglied
•	Vereins-Kassenwart
•	Vereins-Administrator
Feature Website-Administrator:
•	Anlegen/bearbeiten/löschen von Mitgliedern bzw. der entsprechenden Daten
Feature Vereins-Kassenwart:
•	Finanzendaten anlegen
•	Finanzendaten bearbeiten
3.4.1	Funktionale Anforderungen
1.	Verschlüsselter Login 
2.	Behalten des bisherigen Hosters
3.	Mitgliederverwaltung
3.4.2	Nicht Funktionale Anforderungen
1.	Dokumentation
2.	Responsive Design

4	Planung
4.1	Arbeitspakete und Projektstrukturplan
Auf Basis des Pflichtenhefts werden die Arbeitspakete festgelegt. Innerhalb des PSPs werden die identifizierten Arbeitspakete den definierten Projektphasen zugeordnet und hierarchisch strukturiert. Für die Darstellung wurde ein phasenorientierter Projektstrukturplan gewählt. 
 
Abbildung 1: Projektstrukturplan
 
4.2	Projektplanung
4.2.1	Zeitplanung

Projektphasen mit Arbeitspaketen	Dauer in Stunden
Analyse	5
Vorgespräch	2
Ist-Situation	1,5
Soll-Konzept	1,5
Planung	10
Arbeitspakete erstellen	1
Projektstrukturplan	1
Vorgangliste und Zeitplanung	2
Ressourcenplanung	3
Kostenplanung	3
Design	10
Anwendungsfall-Diagramm	3
ER-Diagramm	3
Entwürfe GUI	4
Durchführung	30
Datenbank erstellen	2
Test-Daten eintragen	2
Datenbankabfragen schreiben	3
Grafische Elemente erstellen (GUI)	8
Programmcode für die Verbindung von GUI und Datenbank	15
Testphase	5
Testfälle definieren	2
Tests durchführen	2
Testprotokoll auswerten und Fehlerbehebung	1
Abschluss	10
Projektübergabe und -abnahme	1
Fazit 	1
Kundendokumentation	2
Projektdokumentation 	6
Gesamtstunden	70
Tabelle 2 - Zeitplanung

4.2.2	Gantt-Diagramm
Im Gantt-Diagramm ist ersichtlich, dass die Bearbeitung einiger Arbeitspakete über mehrere Tage verteilt war. Der Grund dafür liegt darin, dass im Verlauf des Projekts gelegentlich parallel andere Aufgaben ausgeführt wurden.
 

 
Abbildung 2-Gant-Diagramm
	

 
4.3	Projektmanagement-Methode
Im Vorfeld der Implementierung wird das Vorgehen, anhand dessen die Realisierung des Projektes erfolgen soll, dargelegt. Ein „erweitertes Wasserfallmodell“, mit agilen Anteilen (hybrid) von Planung bis Testphase.


  
 
Abbildung 3-Vorgehensmodell


 
4.4	Ressourcenplanung
Sachmittel:
Software
Visual Studio Code 2019	Entwicklungsumgebung
PHP-Version 8.x *)	Skriptsprache mit Interpreter, serverbasiert
Draw.io UML Editor	Erstellung des UML-Diagramms
MySQL *)	Verwaltung der Datenbank und Datenbankserver
Apache *)	Webserver
MS-Office	Dokumentation und Präsentation
*) Bestandteil des Pakets „XAMPP“	
Tabelle 3-Softwareressourcen

Hardware	
Arbeitsplatz-PC	
Tabelle 4-Hardwareressourcen

Personal: 
Innerhalb der Personalplanung ist neben dem Praktikanten als verantwortlichen Entwickler, der Projektbetreuer des Praktikumsbetriebes als Auftraggeber aufzuführen
Person	Anlass	Zeit (h)
Richard Monemou	Projektdurchführung	70
Denis Faughn (Auftraggeber)	Vorgespräch	2
	Tests und Abnahme	4
Tabelle 5-Personalressourcen





4.5	Kostenplanung
Sachmittel
Bezeichnung	Gesamtkosten	 Anteilig  (70 h)
Arbeitsplatz-PC	1400,00 €           AfA über 3 Jahre	11,60 €
Visual Studio Code 19	0,00 € 	0,00 €
PHP	0,00 €	0,00 €
MySQL	0,00 € 	0,00 €
Apache Server	0,00 €	0,00 €
MS-Office	25,00 € mtl. 	7,50 €
Draw.io	0,00€ (Lizenzfrei)	0,00€
Gemeinkosten 
(Miete,Betriebskosten)	550,00 €mtl.       Fiktiver Wert	165,00 €
	Summe	184,10 €
Tabelle 6-Sachmittelkosten
Personalkosten - fiktive Werte
Person	Kosten / Stunde	Kosten Projekt
Richard Monemou	15,00 €	1050,00 € (70 h)
Denis Faughn
(Auftraggeber)	22,00 €	132,00 € (6 h)
	Summe	1182,00 €
Tabelle 7-Personalkosten
Gesamtkosten:
Kostenart	Betrag
Sachmittelkosten	184,10 €
Personalkosten	1182,00 €
Summe	1366,10 €
Tabelle 8-Gesamtkosten


4.6	Wirtschaftlichkeit
Das Projekt ist kein gewinnorientiertes Projekt.
Die Website dient für den öffentlichen Auftritt des Vereins und für interne Informationen für die Mitglieder wie z.B. Veranstaltungstermine, Beitragszahlungen etc. 
Für dieses Projekt ist eine Amortisationsrechnung nicht sinnvoll.
5	Design
5.1	Anwendungsfall-Diagramm
Mit Hilfe des Grafikwerkzeuges Draw.io wird ein Anwendungsfall-Diagramm erstellt. 

 
Abbildung 4-Use-Case-Diagramm





5.2	Datenbankmodell
5.2.1	ER-Modell
Die Datenbank enthält 2 Tabellen. 1.: „VereinsMitglied“ mit entsprechenden Attributen ein id_mitglieder (ID_M) als Primary Key (PK), eine Tabelle rolle mit entsprechenden Attributen ein id_rolle (ID_R) als Primary key(PK) wie es auf der unten stehende Abbildung abgebildet.  
Abbildung 5-Datenbankmodell (ER-Diagramm nach Chen)

5.3	Login Formular
Das unter stehende Mockup zeigt das vorgesehene Verhalten der Webseite je nach Endgerät (Desktop oder mobil Gerät) 
Abbildung 6-GUI Design
5.3.1	Nach Login
Das unterstehende Mockup zeigt das vorgesehene Verhalten der Webseite nach dem Login je nach Endgerät (Desktop oder mobil Gerät) 
Abbildung 7-GUI-Design Nach Login

5.4	Mitglieder
Im Dropdown Button nach Login, Optionen: Egene Daten ansehen und bearbeiten, Mitgleder liste ansehen, Eigene Passwort Zurücksetzen.

5.5	Administrator
Der admin hat eigene persönlich bereich wie einfach Mitglieder plus zusätlich 
Mitglieder Daten Ändern, Löschen, Mitglieder Rechte verwalten und neue mitglieder anlegen.

5.6	Kassenwart
Der Kassenwart hat auch eigene persönlich Bereich wie einfach Mitglieder plus zusätzlich Finanzdaten hinzufügen, löschen, ändern
Da Finanzverwaltung kein Teil meines Projektes ist, deshalb werden, Finanzdaten hinzufügen, Finanzdaten löschen und Finanzdaten ändern als Button in Kassenwart Bereich vorhanden aber nicht dahinter zu implementierten Quellcode.    
5.7	Programmablaufplan Login
Der PAP des Logins ist sehr entscheidend für die weitere Umsetzung meines Projektes. Es wird schon bei dem Login je nach Mitgliedgruppe das Mitglied orientiert auf Seite, wovon es Zugriff Recht hat.
Für das Login System wurde Hash-Verfahren mit pepper-und-Salz und das Prepared Statement benutzt, für die genaue Erklärung ist in der Durchführung zu finden.
 
Abbildung 8-PAP des Login Systems
6	Durchführung
6.1	Entwicklungsprozess
Vor der Implementierung des Projektes musste ein geeigneter Entwicklungsprozess ausgewählt werden um eine definierte Vorgehensweise bei der Entwicklung festzulegen.
Da die Anforderungen eindeutig definiert und festgelegt wurden, könnte sich die Umsetzung des Projekts wie es in Abschnitt 4.3 (Projektmanagement Methode) erwähnt wurde an den Phasen des Erweitertes Wasserfallmodell mit Agilen Anteilen (hybrid) von Planung bis Tesphase orientieren. Um das Projekt zu organisieren, wurde ein Ordner namens “Freundeskreis“ erstellt. Innerhalb dieses Ordners wurden vier Unterordner erstellt: einer für die Bilder mit dem Namen “img“, einer für die statischen Seiten, einer für die PHP-Skripte und einer für die CSS-Datei sowie die Index-Datei.
In „img“ wurde das logo gelegt, in „static“ wurden die Standardseiten für die drei Mitgliedergruppen gelegt, in styles wurden die CSS-Datei für die Gestaltung der Webseiten und in Php_script zum Schluß wurden alle einzelne Anwendungsfälle des Anwendungfall-Diagramm von Abschnitt 5.1 (Anwendungsfall-Diagramm) als Feature gelegt und implementiert.
Die folgende Abbildung zeigt die Struktur des Projekts in VS Code 2019.

 







Abbildung 9-Ordnerstruktur des Projekts in VS-Code 2019

 
6.2	Implementierung Login System
Das Login-System ist ein sehr wichtiger Baustein des Projektes und für die drei Nutzergruppen des Vereins von entscheidender Bedeutung. Da das Login-System von außen zugreifbar ist, wurden bei der Implementierung drei wichtige Sicherheitsmaßnahmen getroffen:
1.	Das Salt & Pepper-Verschlüsselungsverfahren wurde verwendet, um das Login gegen unbefugten Zugriff zu sichern. Zusätzlich zum Passwort – bei der ersten Registrierung automatisch erzeugt – wird ein zufälliger „Salt“-Wert erzeugt und an das Passwort angehängt. Ebenfalls wird ein „Pepper“-Wert angehängt, der nicht in der Datenbank gespeichert ist, sondern sicher vor Zugriff im Skript abgelegt ist. Anschließend wird aus dem Ergebnis ein Hash-Wert gebildet.
sollte die Datenbank unglücklicherweise gehackt werden und der in Datenbank gespeicherte Hash-Wert ausgelesen werden, ist das Login immer noch sicher, da der Pepper-Wert im Skript gespeichert ist und unbekannt bleibt.
2.	Das Prepared Statement wurde verwendet, um die Datenbank gegen SQL-Injection-Angriffe zu schützen. Das SQL-Statement wird in der Datenbank vorbereitet, bevor es ausgeführt wird, und als Template erstellt, bei dem Platzhalter anstelle von konkreten Werten eingesetzt werden. Diese Platzhalter werden dann später durch tatsächliche Werte ersetzt, wenn das Statement ausgeführt wird. Der entsprechende Code-Ausschnitt sieht wie folgt aus:  
3.	require("db.php");
4.	    //Statement vorbereiten
5.	    $stmt = $mysql->prepare ("SELECT * FROM vereinsmitglied WHERE email= :email"); //benutzer überprüfen
6.	    // statement binden
7.	    $stmt->bindparam (":email", $_POST["email"]);
8.	    $stmt->execute ();
9.	    $count = $stmt->rowCount();

3	Die Länge des Passwortes wurde auf mindestens 8 alphanumerische Zeichen festgelegt, um es einem potenziellen Hacker zu erschweren, das Passwort zu knacken.
6.3	Absicherung gegen Ausprobieren von URLs oder Einfügen
Es wurde eine Sicherheitsmaßnahme getroffen, um das Kopieren des Links und damit das unbefugte Einloggen zu verhindern. Hierfür wurde nach dem erfolgreichen Login das Login-Flag als besetzt festgelegt und $_SESSION[‘logged_in‘] auf true gesetzt.

Wenn $_SESSION[‘logged_in‘] nicht gesetzt oder nicht gleich true ist, wird der Benutzer als nicht eingeloggt betrachtet und automatisch zur Startseite weitergeleitet. Der entsprechende Codeausschnitt sieht wie folgt aus:

// startet die Session und verhindert durch Copy&Paste die Seite zu zugreifen
session_start ();
if (! isset($_SESSION['logged_in']) || $_SESSION['logged_in'] !== true)
 {
    header ('Location: ../index.html');
    exit;
 }

Der Gesamtcode des Login-Systems ist im Anhang Code Auszuge1 vorhanden.

6.4	Implementierung persönlicher Mitgliederbereich
In dem Mitgliederbereich wurden die Anwendungsfälle aus dem Anwendungsfall-Diagramm für den Mitglieder umgesetzt. Dafür wurden drei Quellcodes implementiert:
1.	Abrufen Liste der Mitglieder und ihrer Kontaktinformationen
Um eine Liste der Mitglieder und ihrer Kontaktinformationen abzurufen, wurde eine einfache SELECT-Abfrage verwendet, welche die Mitgliederdaten aus der Datenbank liest und in einer mit CSS gestalteten Tabelle anzeigt.
2.	Anzeigen und Ändern der eigene Daten 
Um die eigenen Daten anzuzeigen, wurde eine einfache SELECT-Abfrage verwendet, die die Daten, die zur in der Session gespeicherten Mitglieds-ID gehören, aus der Datenbank abruft und in einer mit CSS gestalteten Tabelle anzeigt.
Zum Ändern der Daten wurde eine UPDATE-Abfrage verwendet, mit der die änderbaren Daten des Mitglieds geändert werden können.
3.	Ändern des eigenen Passworts 
•	Erstes Login (Passwort vom Verein erhalten – persönlich, nicht automatisch!)
•	Passwort ändern
•	ab dann: Login Passwort ändern für alle gleich!
3. (!) Die Änderung des eigenen Passworts ist einer der wichtigsten Punkte im Mitglieder Persönlicher-bereich. Hierfür wird das Mitglied aufgefordert, seine E-Mail-Adresse und sein aktuelles Passwort einzugeben, gefolgt von der Eingabe des neuen Passworts, das wiederholt werden muss.

Zunächst wird überprüft, ob die eingegebene E-Mail-Adresse in der Datenbank existiert. Danach wird das Passwort überprüft.
Genauer: Es wird nach Hinzufügen von Salt und Pepper der Hashwert gebildet und geprüft, ob dieser zu dem passt, der in der Datenbank zur eingegebenen E-Mail-Adresse gespeichert ist.

Der gesamte Vorgang ist in 6.2 (Implementierung Login System) detailliert beschrieben
Die dazu gehorigen QuelleCode ist im Anhang Code Auszuge3 Passwort ändern zu sehen

6.5	Implementierung Kassenwartbereich
Wie in 5.6 beschrieben, ist die Umsetzung der Anwendungsfälle für den Kassenwartbereich nicht Aufgabe dieses Teilprojekts. Im Kassenwartbereich wurde das wie bei den Mitgliedern implementiert. Zusätzlich wurde das entsprechende Menü vorbereitet.

6.6	Implementierung Admin Bereich
In Admin-Bereich wurde der Quellcode für die Umsetzung der im Anwendungsfall-Diagramm vorhandenen Anwendungsfälle implementiert. 
•	Neue Mitglieder anlegen:
In dieser PHP-Datei wurde ein Eingabeformular für die Mitgliederdaten erstellt. Dabei wurde auf eine korrekte Eingabekontrolle geachtet. Alle Eingabefelder wurden als “required“ gesetzt, sodass das Formular nur abgeschickt werden kann, wenn alle Felder ausgefüllt sind. Für die E-Mail-Kontrolle wurde der Input-Type auf “email“ gesetzt. Für die Postleitzahlenkontrolle wurde das Pattern =“[0-9]{5}“ verwendet, da in Deutschland die Länge der Postleizahl nur 5 Zahlen beträgt. Es werden also 5 Zahlen der Postleitzahl im Intervall von 0 bis 9 inklusive 0 und 9 gewählt. Für die Telefonnummernkontrolle wurde der Input-Type auf “tel“ gesetzt und ein 
Pattern = “0\d{6,14}“ verwendet. Die Telefonnummer soll nur mit einer “0“ beginnen und kann 6 bis 14 weitere Zahlen enthalten, wobei die minimal Länge 7 und die maximale Länge 20 beträgt.

Danach wurde eine Verbindung zur Datenbank ‘Freundeskreis‘ hergestellt und ein zufallString als Provisoriches Passwort mit der Function generateRandomString() erzeugt. 
Hier ein Codeausschnitt:
function generateRandomString ($length = 6)
  {
        $characters = ‘0123456789
                       abcdefghijklmnopqrstuvwxyz
                       ABCDEFGHIJKLMNOPQRSTUVWXYZ‘
         $charactersLength = strlen($characters);
         $randomString = ‘‘;
         for ($i = 0; $i < $length; $i++)
              {
                $randomString .= $characters[rand(0,          $charactersLength-1)];   
              }
                return $randomString;
        }  $passwort = generateRandomString(6);
Die Funktion  generateRandomString erzeugt einem zufälligen String mit einer Länge von 6 Zeichen (oder einer anderen Länge, falls ein Parameter übergeben wird). Dazu werden alle möglichen Zeichen in der Variablen $characters definiert, aus der dann ein zufälliger String erzeugt wird. In der letzten Zeile des Codes wird die Funktion aufgerufen und das Ergebnis in der Variablen $passwort gespeichert. Dadurch wird ein zufälliger String erzeugt und dieser String kann dann zum Beispiel als Passwort verwendet werden.
Danach  wurde überprüft ob der Mitglieder noch nicht registriert ist. Wenn nicht, wird    das Passwort mit dem Peppe-Wert Konkateniert zusammengehäsht und dann das  Mitglieder registriert. Wenn das Anlegen erflogreich ist, wird das generierte Passwort  im Browser angezeigt und das Mitglied aufgefordert, beim ersten Login das Passwort zu ändern.
Es wurde prepared Statement benutzt um mysql injection zuvermeiden.
Die dazugehorige QuelleCode ist Im Anhang  Code Auszug2 Mitglieder Anlegen zu sehen
Weitere umgesetzte Anwendungsfälle sind:
•	Mitgliederdaten löschen oder ändern
wie im Abschnitt 6.4.2 erklärt, wurde eine einfache DELETE-Abfrage verwendet, die gewählte ID und dazu gehörigen Daten löscht.
•	Mitgliederrechte verwalten
Auch in dieser PHP-Datei wurde auch eine Verbindung zur Datenbank ‘freundeskreis‘ hergestellt und ein SQL-Query mit einem JOIN zwischen Tabelle ‘vereinsmitglied‘ und der Tabelle ‘rolle‘ ausgeführt, um den status des mitglieds zu ermitteln.
 
7	Testphase
Es werden White- und Blackbox Tests durchgeführt.  Testfälle, die nicht zum erwarteten Ergebnis führen, werden in einem zweiten Durchlauf nach Korrektur des Programms erneut aufgerufen. Auszüge aus der Beschreibung der Testfälle und aus dem darauf basierenden Testprotokoll befinden sich im Anhang.
Zu testen sind im Wesentlichen folgende Hauptbestandteile
•	Responsivität 
•	Login für Alle Mitglieder Gruppen
•	Passwort ändern
•	Verwaltung von Mitgliedern
•	Verwaltung von Mitgliederrechten
Dabei sollen mindestens vier verschiedenen fiktive Mitglieder als Testdaten eingetragen werden
7.1	Whitebox Tests
In den Whiteboxtests wird primär geprüft, ob die verlangte Funktionalität vorhanden ist und keine Fehler im Programmablauf auftreten. Aufgrund der Kenntnis des Codes können im Fehlerfall nötige Korrekturen durch den testenden Entwickler zeitnah ausgeführt werden.
7.2	Blackbox Tests
Die Blackbox Tests eignen sich besonders, um die Benutzerbarkeit der Software, die Logik der Eingabe und die Ergonomie mit Blick auf den Workflow zu prüfen, da die Testperson noch nicht mit der Software gearbeitet hat. Getestet wird durch einen Verein Mitglied, der die Anwendung auch später Administrieren wird.
Es werden die gleichen Testfälle verwendet, die auch schon in den Whitebox Tests genutzt wurden. Es ist zu erwarten, dass bereits dort korrigierte Fehler nicht mehr auftreten, es können sich jedoch durchzuführende Änderungen an der logischen Abfolge der Eintragung, der GUI-Gestaltung und der Art der Anzeige der Werte ergeben.
7.3	Testfälle
Die untenstehenden Tabellen kennzeichnen die Testfälle.
Test-ID	Testfälle und Beschreibung 
1.		Responsivität
1.1	Webseite auf Desktop aufgerufen
1.2	Webseite auf Tablet und Handyaufgerufen
2.	Login (Anmeldung von Mitgliedern)
2.1	Als Administrator
	Werte: E-Mail, Passwort
2.2	Als Kassenwart
	Werte: E-Mail, Passwort
2.3	Als Einfach Mitglied
	Werte: E-Mail, Passwort
3.	Administrative Rechte
3.1	Mitglieder Anlegen
	Werte: Vorname, Name, Geburtsdatum, E-Mail, Straße, Hausnummer, Ort, PLZ, Telefone, Mitglied Level
3.2	Mitglieder löschen
3.3	Mitglieder Rechte ändern
	Werte: 0 oder 1 oder 2 oder 3
3.4	Passwort Reset
	Werte: E-Mail, Altes Passwort, Neues Passwort
3.3	Mitglieder Daten Bearbeiten
	Werte: Vorname, Nachname, E-Mail, Straße, Hausnummer, PLZ, Ort, Telefone,
3.4	Mitglied Löschen
Tabelle 9 Testfälle1




Die Tabelle TestProtokolle geht hier weiter
Test-ID	Testfälle und Beschreibung 
4	Einfache Mitglieder Rechte
4.1	Eigene Daten bearbeiten
	Werte: Vorname, Name, E-Mail, Straße, Hausnummer, Ort, PLZ, Telefone.
4.2	Mitglieder Liste und kontakt Daten aufrufen
5	Kassenwart Rechte
5.1	Eigene Daten bearbeiten
	Werte: Vorname, Name, E-Mail, Straße, Hausnummer, Ort, PLZ, Telefone
5.2	Mitglieder Liste und kontakt Daten aufrufen
Tabelle 10 Testfälle2









7.4	Testfälle Vorgehensweise Beschreibung
7.4.1	Kompatibilität und Responsivität
Es wurde die Kompatibilität und das Responsive Design der Webseite überprüft. Hierfür wurde die Webseite in verschiedenen Browsern wie Google, Edge, Firefox, sowie auf verschiedenen Endgeräten wie dem iPad Air, iPhone XR und dem Laptop HP aufgerufen, um sicherzustellen, dass Mitglieder unabhängig von ihrem Endgerät und Browser auf die Webseite zugreifen können. Das Ergebnis war erfolgreich.    
7.4.2	Anmeldung von Mitgliedern
Es wurde überprüft, ob sich Mitglieder erfolgreich anmelden können. Dazu wurden Anmeldedaten eingegeben und anschließend auf die Schaltfläche “Anmelden“ geklickt. Das Ergebnis war, dass sich das Mitglied erfolgreich einloggen konnte.
7.4.3	Administrative Rechte
7.4.3.1	Neue Mitglied Anlegen
 Im Admin-Bereich wurde auf die Schaltfläche “Mitglieder Anlegen“ geklickt. Dabei wurde zunächst versucht ein existierendes Mitglied erneut anzulegen, was zur Fehlermeldung “Mitglied existiert bereits“ führte.
Anschließend wurden die Daten eines neuen Mitglieds eingegeben. 
•	Ein Eingabe Feld wurde leer gelassen kam die Fehlermeldung “Fülle dieses Feld aus“.
•	Die PLZ wurde mit einer Zahlensequenz kleiner oder größer als 5 Ziffern eingegeben, was zur Fehlermeldung “Deine Eingabe muss mit dem geforderten Format überreinstimmen“ führte 
•	Die E-Mail-Adresse wurde eingegeben ohne das “@“-Zeichen, erschien die Fehlermeldung “ die E-Mail muss ein “@-Zeichen“ enthalten.
•	Die Telefone Nummer wurde ohne eine führende “0“ eingegeben, erschien ebenfalls die Fehlermeldung “Deine Eingabe muss mit dem geforderten Format überreinstimmen“.
Nachdem alle diese Eingabekontrollen erfüllt wurden, wurde auf die Schaltfläche “Senden“ geklickt. Daraufhin erschien die Erfolgsmeldung “Das Mitglied ‘Max Muster man‘ wurde mit dem Benutzernamen ‘musterman@gmail.com‘ und dem Provisorischen Passwort ‘Muster Passwort‘ registriert. 
7.4.3.2	Mitglieder Daten Ändern
Es wurde überprüft, ob ein Administrator die Daten eines Mitglieds erfolgreich bearbeiten kann. Hierfür wurde im Admin Bereich auf die Schaltfläche “Mitglieder bearbeiten“ geklickt, woraufhin eine Tabelle mit Liste aller Mitglieder angezeigt wurde. Ein Mitglied wurde ausgewählt anschließend auf die Schaltfläche “Bearbeiten“ geklickt. Es wurden neue Daten in die Eingabefelder für E-Mail, Telefonnummer und Straße eingegeben und danach auf die Schaltfläche “Speichern“ geklickt. Die Erfolgsmeldung “Die Daten des Mitglieds wurden erfolgreich aktualisiert“.
7.4.3.3	Mitglieder löschen
Es wurde überprüft, ob Administratoren Mitglied erfolgreich löschen können. Hierfür wurde in Admin Bereich auf die Schaltfläche “Mitglieder Daten bearbeiten“ geklickt, erschient eine Tabelle mit Liste aller Mitglieder. Es wurde ein Mitglied ausgewählt dann auf die Schaltfläche “Delete“ geklickt. Das Mitglied wurde erfolgreich gelöscht.
7.4.3.4	Mitgliederrechte Vergabe
 Es wurde überprüft ob Administratoren Mitgliederrechte erfolgreich zuweisen und entfernen können, um sicherzustellen, dass Benutzer nur auf die Funktionen und Daten zugreifen können, auf die sie berechtigt sind. Während der Implementierung der Datenbank wurden bestimmte Status für Mitglieder definiert, die auch als Mitgliedslevel bezeichnet werden.
Mitgliedslevel 0 = Mitglied blockiert.
Mitgliedslevel 1 = einfache Mitglied.
Mitgliedslevel 2 = Kassenwart.
Mitgliedslevel 3= Admin.
Im Admin-Bereich wurde auf die Schaltfläche “Mitgliederrechte ändern“ geklickt und dem Mitglied “Max Mustermann“ das Mitglied Level “0“ zugewiesen. Nachdem versucht wurde, sich als “Max Musterman“ anzumelden, erschien die Fehlermeldung “Sie wurden blockiert. Bitte kontaktieren Sie den Vereinsvorstand unter der Nummer 01xxxxxxxxxx“. 
Anschließend wurde das Mitgliedslevel von “Max Mustermann“ von “0“ auf “1“ gesetzt und versucht, sich einzuloggen. Das Login war erfolgreich und “Max Mustermann“ konnte sich als einfaches Mitglied einloggen. 
Daraufhin wurde das Mitgliedslevel von “Max Mustermann“ von “1“ auf “2“ gesetzt und erneut versucht, sich einzuloggen. Das Login war erfolgreich und “Max Mustermann“ konnte sich als Kassenwart einloggen. Schließlich wurde das Mitgliedslevel von        “Max Mustermann“ von “2“ auf “3“ gesetzt und erneut versucht, sich einzuloggen. Das Login war erfolgreich und “Max Mustermann“ könnte sich als Administrator einloggen. 

7.4.4	Einfache Mitglieder Rechte
7.4.4.1	Eigene Daten Ändern
Es wurde überprüft, ob das eingeloggte Mitglied seine eigenen Daten ändern kann. Hierfür wurde neue E-Mail-Adresse, Telefonnummer und Adresse eingegeben, und anschließend auf die Schaltfläche “Ändern“ geklickt. Das Ergebnis war, dass das Mitglied die Daten erfolgreich ändern konnte, einschließlich Vor- und Nachnamens. 
7.4.4.2	Passwort-Reset 
Es wurde den Passwort-Reset-Prozess überprüft, dafür wurde in Mitglied Personal-Bereich auf die Schaltfläche “Passwort Reset“ geklickt, um das unsichere provisorische Passwort zurücksetzen. Beim zurücksetzen, wurde die Länge des Passworts geprüft. zunächst wurde ein Passwort mit weniger als 8 Zeichen eingegeben und auf die Schaltfläche “Ändern“ geklickt. Es erschien die Fehlermeldung “ Das Passwort muss mindestens 8 Zeichen Lang sein“. Danach wurde ein Passwort mit mehr als 10 Zeichen eingegeben und auf die Schaltfläche “ Ändern“ geklickt, woraufhin die Fehlermeldung “Das Passwort darf nicht mehr als 10 Zeichen Lang sein“ erschien. Schließlich wurde ein Passwort mit 8 Buchstaben eingegeben und auf die Schaltfläche “ Ändern“ geklickt. Es erschien die Erfolgsmeldung “Das Passwort wurde erfolgreich geändert“.
7.4.4.3	Mitglieder Liste Mit Kontakt ansehen
 Im Mitglieder-Personal-Bereich wurde auf die Schaltfläche “Mitglied Liste“ geklickt. Anschließend wurden alle Mitglieder des Vereins mit ihren Kontaktdaten angezeigt.
7.5	Kassenwart Rechte
Die gleichen Testfälle die im Abschnitt 7.3.4 durchgeführt wurden.
8	Abschluss
8.1	Übergabe und Abnahme
Nach der Fertigstellung der Anwendung wurde diese mit dem Fachpersonal von der New Horizons GmbH besprochen. Durch eine gute Setzung der Ziele und Funktionen im Lasten- und Pflichtenheft sind keine Mängel aufgetreten. Durch die einfachen gestalteten Oberflächen sind die Eingewöhnungsphase kurz und es kann schnell Vertrautheit mit der Anwendung erlangt werden. Zusätzlich wurde der Code von dem Auftraggeber abgenommen, wodurch eine einheitliche und übersichtliche Programmierung sichergestellt wurde.
8.2	Dokumentation
Die Dokumentation setzt sich aus dem Benutzerhandbuch und der Projektdokumentation zusammen. Das Benutzerhandbuch dient dazu, das Mitglied in die Nutzung der Anwendung einzuführen. Ein Ausschnitt des Benutzerhandbuchs befindet sich im Anhang Abschnitt 7 (Kundendokumentation)
8.3	Fazit
Abschließend lässt sich sagen, dass das Projekt auch ohne großes wirtschaftliches 
Vorteil für das Unternehmen ein Erfolg war.
Dieses Projekt hat bestätigt, wie wichtig es ist, sich schon im Vorfeld des Projektes Gedanken über eine geeignete Struktur zu machen.  Im Zuge der Umsetzung konnten wertvolle Erfahrungen bezüglich Planung und Durchführung von Projekten gesammelt werden. Mit den Ergebnissen dieses Projektes bin ich zufrieden, da die Anwendung alle geforderten Funktionalitäten aufweist und mir wertvolle Bausteine für meine weitere berufliche Zukunft bietet. Das positive Ergebnis sehe ich nicht nur in der erfolgreich fertiggestellten Anwendung. Ich bin vielmehr mit dem Verlauf des gesamten Projektmanagements hochzufrieden. Ich ordne das Projekt als eine sehr wertvolle Lebenserfahrung, die mich sicherlich weiterbringt.
8.4	Soll-Ist-Vergleich der Ausführung
Der zu dem Beginn des Projektes erstellte Projektplan aus Abschnitt 4.1 (Arbeitspakete und Projektstrukturplan) Wurde eingehalten.
8.5	Soll-Ist-Vergleich Zeitplanung
Bei einer rückblickenden Betrachtung des IHK-Abschlussprojekts, kann festgehalten werden, dass alle zuvor festgelegten Anforderungen gemäß dem Pflichtenheft erfüllt wurden. Der zu Beginn des Projektes im Abschnitt 4.2.1 (Zeit Planung) erstellte Zeit Planung konnte eingehalten werden. In der Tabelle8-Soll-/Ist-Vergleich Zeitplanung wird die Zeit, die tatsächlich für die einzelnen Phasen benötigt wurde, der zuvor eingeplanten Zeit gegenübergestellt. Es ist zu erkennen, dass nur sehr geringfügig von der Zeitplanung abgewichen wurde bei dem Entwurfe GUI in der Design Phase wurde weniger Zeit benötigt als geplant, weil es nicht mehr nötig alle Formulare zu designen war da, von den zwei (2) im Abschnitt 5.3 (Login Formular) und Abschnitt 5.3.1 (nach Login) könnte man sich referenzieren. Die sich daraus ergebenen Differenzen konnten untereinander bei der Durchführungsphase kompensiert werden, sodass das Projekt in dem von der IHK festgelegten Zeitrahmen von 70 Stunden umgesetzt werden konnte.





Phase	Dauer Soll in Std	Dauer Ist in Std	Abweichung in Std
Analyse	5	5	0
Planung	10	10	0
Design	10	8	-2
Durchführung	30	32	+2
Testphase	5	5	0
Abschluss	10	10	0
Summe	70	70	0
Tabelle 11-Soll-Ist-Vergleich Zeitplanung

8.6	Ausblick
Obwohl alle im Lastenheft definierten Anforderungen realisiert werden konnten, können in Zukunft dennoch neue Anforderungen definiert bzw. Erweiterungsvorschläge entwickelt werden

9	Persönliche Erklärung

 

	


Anhänge

für die Dokumentation zur betrieblichen Projektarbeit
Entwurf und Implementierung der Mitgliederverwaltung und der
Benutzerrechtevergabe für den Relaunch des Internetauftritts des gemeinnützigen Vereins „Freundeskreis DPSG St. Liborius“ aus Dortmund-Körne.
 
 
1	Tabellenverzeichnis
Tabelle 1-Moscow-tabelle	4
Tabelle 2 - Zeitplanung	7
Tabelle 3-Softwareressourcen	12
Tabelle 4-Hardwareressourcen	12
Tabelle 5-Personalressourcen	12
Tabelle 6-Sachmittelkosten	13
Tabelle 7-Personalkosten	13
Tabelle 8-Gesamtkosten	14
Tabelle 9 Testfälle1	26
Tabelle 10 Testfälle2	27
Tabelle 11-Soll-Ist-Vergleich Zeitplanung	33
Tabelle 12-Glossar	III
Tabelle 13 Testprotokoll1	XVI
Tabelle 14- Testprotokoll2	XVII
2	Abbildungsverzeichnis
Abbildung 1: Projektstrukturplan	6
Abbildung 2-Gant-Diagramm	10
Abbildung 3-Vorgehensmodell	11
Abbildung 4-Use-Case-Diagramm	14
Abbildung 5-Datenbankmodell (ER-Diagramm nach Chen)	15
Abbildung 6-GUI Design	16
Abbildung 7-GUI-Design Nach Login	16
Abbildung 8-PAP des Login Systems	18
Abbildung 9-Ordnerstruktur des Projekts in VS-Code 2019	19
Abbildung 10 Lastenheft Auszug	XIV
Abbildung 11 Ansicht aus Desktop	XVIII
Abbildung 12 Ansicht aus Tablet oder Handy	XIX
Abbildung 13-login Formular	XIX
Abbildung 14-einfache Mitglieder Seite	XX
Abbildung 15 Mitglied Bereich	XXI
Abbildung 16-Kassenwart Seite	XXI
Abbildung 17-Kassenwart Bereich	XXII
Abbildung 18-Admin Bereich	XXIII
Abbildung 19 Mitglieder anlegen	XXIV
Abbildung 20-Mitglieder Liste	XXV
 Abbildung 21-Daten Aktualisierung	XXV
Abbildung 22 Mitgliederrechte	XXVI
Abbildung 23 Recht aktualisieren	XXVII


3	Code Auszuge













4	Glossar
Bezeichnung	Erklärung
PHP	Hypertext Preprocessor 
Entwicklung Sprache
Visual Studio code 2019	Programm Editor
Microsoft Office	Schreib, Tabellen und Präsentationsproramm
HTML	Hypertext Markup Language
CSS	Cascading Style Sheets Gestaltungs- und Formatierungssprache
SQL	Structured Query Language
 Datenbank Verwaltungssytem
MosCoW	Methode 
Must, Should, Could, Won`t have
Npw	New Password
apw	Altes Password
GUI	Graphische User Interface
PAP	Programm-Ablauf-Plan
ID_M	Mitglied Identifikation Nummer
ID_R	Mitglied Rolle Identifikation Nummer 
Admin	Administrator
AGB	Allgemein Geschäft Bedingungen 
Tabelle 12-Glossar

5	Codeauszüge
5.1	 Quellcode für Das Login System
<!DOCTYPE html>
<html lang="de" dir ="ltr">
    <head>
        <meta charset= "utf-8">
        <title> Sich anmelden</title>
</head>
        <body>
        <?php
     // Pepper Wert als Konstant definieren
        $pepper= '1234';

if(isset($_POST["submit"])){
    // Datenbank Verbindung inkludieren
    require("db.php");
    //Statement vorbereiten
    $stmt = $mysql->prepare ("SELECT * FROM vereinsmitglied WHERE email = :email"); //benutzer überprüfen
    // statement binden
    $stmt->bindparam (":email", $_POST["email"]);
    $stmt->execute ();
    $count = $stmt->rowCount ();
    if($count == 1){
       $row = $stmt->fetch ();
        // Password und Pepper wert Konkatenieren und verifizieren 
       if(password_verify($_POST["pw"].$pepper, $row["password"])){

        // eine Session starten
        session_start();
        // Session Variable definieren
        $_SESSION['logged_in'] = true;
        $_SESSION["email"] = $row["email"];
        $_SESSION["id"]    = $row["ID_M"];
        $_SESSION["Vorname"] = $row["vorname"];

        
    // Abrufen des Benutzerstatus aus der Datenbank
    $userID = $_SESSION["id"];
    $sql = "SELECT r.Status FROM vereinsmitglied v JOIN rolle r ON v.ID_M = r.ID_M WHERE v.ID_M = :ID_M";
    $stmt = $mysql->prepare($sql);
    $stmt->bindParam(":ID_M", $userID);
    $stmt->execute();
    $result = $stmt->fetch(PDO::FETCH_ASSOC);

    // Den Statuswert aus der Abfrage extrahieren
    $status = $result['Status'];

    switch ($status) {
   // wenn Status gleich 0 wird das Mitglied blockiert
        case 0:
            header ("Location: blockiert.php");
           
            break;
   // wenn Status gleich 1 wird das Mitglied zu einfache Mitglieder Seite weitergeleitet
        case 1:
            header("Location: ../static/mitglied.php"); 
            break;
   //wenn Status gleich 2 wird das Mitglied zu Kassenwart Seite weitergeleitet
        case 2:
            header("Location: ../static/kassenwart.php");
            break;
    //wenn Status gleich 3 wird das Mitglied zu Administratoren Seite weitergeleitet
        case 3:
            header ("Location: ../static/admin.php");
            break;
        default:
            die("Unknown user status");
    }
        
       } else{
        $passwort = $_POST["pw"];
        echo "login ist fehlgeschlagen";
       
       }
    } else{
        echo "der Benutzer ist bereit vergeben";
    }
}

        ?>
                     <! -- Das Login Formular -->
        <h1> Login </h1>
        <!-- die Methode ist Post das Formular wird an loginvrais.php gesendet wenn einloggen gedruckt wird. -->
        <form action ="loginvrais.php" method= "post"> 
            <! -- Input Feld für email mit dem Platzhalter "username" required bedeutet das Feld darf nicht leer sein -->
            <input type= "text" name = "email" placeholder="email" required><br>
            <input type= "password" name= "pw" placeholder="passwort" required><br>
            <button type= "submit"  name= "submit">Einloggen</button>
</form> 
<br>
</body>
</html>
Code Auszug 1 Login System

5.2	Quellcode für Mitglieder Anlegen

<?php
// startet den Session und verhindert durch Kopie Paste die Seite zu zugreifen
session_start();
if (!isset($_SESSION['logged_in']) || $_SESSION['logged_in'] !== true) {
    header('Location: ../index.html');
    exit;
}
?>
<!DOCTYPE html>
<html>
    <head>
        <!-- dies Zeile gibt das Zeichenkodierungsformat für 
            das Dokument an, in diesem Fall UTF-8. -->
    <meta charset="UTF-8">  
    <!-- Diese Zeile legt das Viewport-Meta-Tag fest, das dem Browser mitteilt,
        wie er das Layout der Seite auf verschiedenen Geräten anpassen soll. 
        In diesem Fall wird angegeben, der Viewport auf die Breite des Geräts 
        eingestellt werden soll und dass die Anfangs-Zoomstufe bei 1,0 liegen soll. -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
        <!-- Diese Zeile verknüpft eine externe Stylesheet-Datei, 
            die eine Font-Icon-Bibliothek namens Remixicon bereitstellt. -->
    <link href="https://cdn.jsdelivr.net/npm/remixicon@2.5.0/fonts/remixicon.css" rel="stylesheet"> 
    <!-- Diese Zeile verknüpft eine weitere externe Stylesheet-Datei namens "pagestyle.css",
            die CSS-Regeln zur Gestaltung von Layout und Design der Webseiten enthält. -->
    <link  rel="stylesheet" typ="css" href="../styles/pagestyle.css"> 
    <!-- Diese Zeile verknüpft noch eine weitere externe Stylesheet-Datei namens "tbstyle.css", 
        die CSS-Regeln zur Gestaltung von Tabellen auf den Webseiten enthält. -->
    <link  rel="stylesheet" typ="css" href="../styles/tbstyle.css"> 
                        <title>Freundeskreis</title> 
    </head> 
<body>
<header>
   <!-- das logo -->
   <img src="../img/logo_freundeskreis.png" alt="Logo" class="logo">
  <!-- Navbar -->
  <div class="navbar" id="mynavbar">
    <a href="#">Fördermittel</a>
    <a href="#">Termine</a>
    <a href="#">Kontakt</a>
    <a href="#">Über uns</a>
    <a href="#">Startseite</a>
  </div>
  <div class="content">
    das Logout 
    <a href="../php_script/logout.php" class="user"><i class="ri-user-fill"></i>logout</a> 
   </div>
   <div class="bx bx-menu" id= "menu-icon"> <i class="ri-menu-line"></i>
   </div>
</header>
 
<div class="aside">
  </div>

  <div class="main">
<?php   
    if (!isset($_POST["vorname"]))
    {
?>
<!-- das Formular zum Mitglieder Daten eintragen -->
    <form   action= "mitgliedanlegenstatus_pepassword.php" method= "post">
                 <input type ="text" name="vorname"  placeholder="Vorname" required><br>
                 <input type="text" name="Name"  placeholder="Name" required><br>
                 <input type="date" name="geburtsdatum"  placeholder="Geburtsdatum" required> G.Datum<br>
                 <input type= "email" name = "email" placeholder="email" required><br>
                 <input type="text" name = "Strasse"  placeholder="Strasse" required><br>
                 <input type= "text" name= "Hausnummer"  placeholder="Hausnummer" required><br>
                 <input type= "text" name = "Ort" placeholder="Ort" required><br>
                 <!-- die PLZ soll zwischen chiffer zwischen 0 und 9 gewählt werden und ein Länge von 5 chiffern sein -->
                 <input type="text" id="PLZ" name="PLZ" placeholder="PLZ" pattern="[0-9]{5}" required><br>
               <!-- die Telefone Nummer soll mit ein "0" anfangen eine minlenght von 7 chiffern und ein maxlength von 20 chiffer
                                          die zwischen 6 und 14 weiteren chiffer sein kann -->
                <input type="tel" id="telefonnummer" name="Telefone" placeholder="Telefone" pattern="0\d{6,14}" minlength="7" maxlength="20" required><br>
                 <input type = "number" name = "Status"  placeholder="Mitglied Level" required><br>
                 <input type="submit" name= "einfugen"><br>
    </form> 
<?php 
    }
    else
    {
    // Pepper konstant definieren
        $pepper ='1234';
        //Db Connection
        $servername = "localhost";
        $username   = "root";
        $password  =  "";
        $db        =  "freundeskreis";
        $conn = new mysqli($servername, $username, $password, $db);

        // ein zufallisches String aus Zahlen und Buchstaben erzeugen als Provisorisches Password
        function generateRandomString($length = 6) 
        {
            $characters = '0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ';
            $charactersLength = strlen($characters);
            $randomString = '';
            for ($i = 0; $i < $length; $i++) 
            {
                $randomString .= $characters[rand(0, $charactersLength - 1)];
            }
            return $randomString;
        } $passwort = generateRandomString(6);
        
        if($conn -> connect_error)
        { 
            die("zu spät".$conn-> connect_error);
        }
       
            $email = $_POST["email"];

            // check if email already exists
            $stm_select = $conn->prepare("SELECT email FROM vereinsmitglied WHERE email = ?");
            $stm_select->bind_param("s", $email);
            $stm_select->execute();
            $result = $stm_select->get_result();
    
            if ($result->num_rows > 0) {
                // email already exists
                echo "Diese E-Mail-Adresse ist bereits registriert.";
            } else {
            

                // Die Formular Daten definieren 
                $Vorname      =$_POST["vorname"];
                $Nachname     =$_POST["Name"];
                $geburtsdatum =$_POST["geburtsdatum"];
                $email        =$_POST ["email"];
                $Strasse      =$_POST["Strasse"];
                $Hausnummer   =$_POST["Hausnummer"];
                $Ort          =$_POST["Ort"];
                $PLZ          =$_POST["PLZ"];
                $telefon      =$_POST["Telefone"];
                $status       = $_POST["Status"];

            // das Provisorische Passwort mit dem Pepper Wert zusammen hashen
                $hash = password_hash($passwort.$pepper, PASSWORD_DEFAULT);

                // Mitglied Daten in der Tabelle vereinsmitglied einfügen
                $stmt = $conn->prepare("INSERT INTO vereinsmitglied(ID_M, vorname, Name, geburtsdatum, email, Strasse, Hausnummer, Ort, PLZ, Telefone, password)
                VALUES (NULL, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?)");
                $stmt->bind_param("ssssssssss", $Vorname, $Nachname, $geburtsdatum, $email, $Strasse, $Hausnummer, $Ort, $PLZ, $telefon, $hash);
                $stmt->execute();
                // Zuletzt eingefügte ID abrufen
                $id_m = $conn->insert_id;
                
                // Daten in die Tabelle rolle ein, wobei ID_M als Fremdschlüssel verwendet wird
                $stmt = $conn->prepare("INSERT INTO rolle (ID_M,Status) VALUES (?, ?)");
                $stmt->execute(array ($id_m, $status));

                echo " Der Mitglieder:"." $Vorname "." $Nachname "." wurde mit der Benutzername:".$email."und 
                    dem Provisorischem passwort :" ." $passwort " . "und status:".$status." registriert " ;
                }  
            
                $conn->close();
           
   }

   
?>

 <h1>Mitglied Level:</h1>
 <h> Einfach Mitglieder = 1 </h> <br>
 <h> Kassenwart = 2</h> <br>
 <h> Administrator = 3 </h> <br>
 <h> Mitglieder Banieren = 0 </h> <br>
</div>
    <!-- footer -->
 </div>
  <div class="footer">
    <a href="#">Impressum</a>
    <a href="#">DGB</a>
    <a href="#">Haftungsauschluss</a>
    <a href="#">Satzung</a>
    <p>&copy;2023</p>
 </div>

 
<script>
  let menu = document.querySelector('#menu-icon'); // Hier wird eine Variable "menu" erstellt und das HTML-Element mit der ID "menu-icon" ausgewählt.
  let navbar= document.querySelector('.navbar'); // Hier wird eine Variable "navbar" erstellt und das HTML-Element mit der Klasse "navbar" ausgewählt.
  menu.onclick=()=>{ // Wenn das "menu"-Element angeklickt wird, wird die folgende Funktion ausgeführt:
      menu.classList.toggle('bx-x'); // Hier wird die CSS-Klasse "bx-x" zum "menu"-Element hinzugefügt oder entfernt.
      navbar.classList.toggle('open'); // Hier wird die CSS-Klasse "open" zum "navbar"-Element hinzugefügt oder entfernt.
  } 
</body>
</html>
Code Auszug 2 Mitglieder Anlegen

5.3	Quellcode für Passwort Reset

<?php
// Das Pepper Kontant definieren
$pepper ='1234';
// startet den Session und verhindert durch Kopie Paste die Seite zu zugreifen
session_start();
if (!isset($_SESSION['logged_in']) || $_SESSION['logged_in'] !== true)
 {
    header('Location: ../index.html');
    exit;
 }
?>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://cdn.jsdelivr.net/npm/remixicon@2.5.0/fonts/remixicon.css" rel="stylesheet">
  <link  rel="stylesheet" typ="css" href="../styles/pagestyle.css">
  <title>Meine responsive Website</title>
</head>
<body>
<header>
   <!-- das logo -->
   <img src="../img/logo_freundeskreis.png" alt="Logo" class="logo">
  <!-- Navbar -->
  <div class="navbar" id="mynavbar">
    <a href="#">Fördermittel</a>
    <a href="#">Termine</a>
    <a href="#">Kontakt</a>
    <a href="#">Über uns</a>
    <a href="#">Startseite</a>
  </div>
     <!-- das Logout Logo in den Content -->
  <div class="content">
    <a href="../php_script/logout.php" class="user"><i class="ri-user-fill"></i>logout</a> 
    </div>
      <!-- das Menu Icon in eigene class -->
   <div class="bx bx-menu" id= "menu-icon"> <i class="ri-menu-line"></i>
   </div>
</header>
  <!-- aside -->
  <div class="aside">
  </div>
  <!-- in den main kommt den php_datei Inhalt -->
  <div class="main">
    <?php
    // Datenbank Verbindung inkludieren
    require("db.php");

    if(isset($_POST["submit"])) // wenn auf submit gedrückt wird
    {
      // Die  post variablen definieren
        $Apw =$_POST["apw"];
        $npw =$_POST["npw"];
        $w_pw =$_POST["w_pw"];
        //benutzer überprüfen
        //statement vorbereiten
        $stmt = $mysql->prepare("SELECT * FROM vereinsmitglied WHERE email = :email"); 
        // statement binden
        $stmt->bindparam(":email", $_POST["email"]);
        $stmt->execute();
        $count = $stmt->rowCount();
        //wenn ein email (mitglieder) gefunden wird
        if($count == 1)
        {
          // wird die fetch() Methode des PDO-Statement abgerufen um die Nächte Zeile aus dem Resultset zurück zugeben
          $row = $stmt->fetch();
          if(password_verify($_POST["apw"].$pepper, $row["password"]))
          {
            // Überprüfen ob das neue passwort und passwort wiederholen Überreinstimmen
                if($w_pw == "")
                {
                    echo "bitte passwort wiederholen";
                    exit;
                }
                if($npw != $w_pw)
                {
                    echo "die Passwörter stimmen nicht überein";
                    exit;
                }
                // das Neue Passwort lange soll nicht 8 unterschreiten
                if(strlen($npw)< 8)
                {
                    echo "das Passwort muss mindestens 8 buchstaben sein";
                    exit;
                }
                  // wenn das Neue Passwort und Passwort widerholen Überreinstimmen 
                  // dann das Passwort an den Pepperwert anhängen hashen und das Hash Wert in der Tabelle vereinsmitglied speichern
                  // ist zu notieren, dass das Salz Wert wird mit der Hash Funktion Password_hash () mit der Option PASSWORD_DEFAULT automatisch
                  // generiert. Diese Methode verhindert, dass zwei Mitglieder das gleiche Passwort haben, niemals gleiche Hashwert bekommen. 
                elseif($npw == $w_pw)
                {
                $hash = password_hash($npw.$pepper, PASSWORD_DEFAULT);
                $stmt = $mysql->prepare("UPDATE vereinsmitglied SET password = :passwort WHERE email = :email");
                $stmt->bindparam(":email", $_POST["email"]);
                $stmt ->bindparam(":passwort", $hash);
                $stmt -> execute();

                echo "passwort erfolgreich geändert";
                }
            }
            else
            {
            echo "falsches Passwort";
            }
        }
        else 
        {
        echo "email existiert nicht";
        }
    }
    $db = null;
   ?>
 </div>
<!-- footer -->
  <div class="footer">
    <a href="#">Impressum</a>
    <a href="#">DGB</a>
    <a href="#">Haftungsauschluss</a>
    <a href="#">Satzung</a>
    <p>&copy;2023</p>
  </div>

  
  <script>
    let menu = document.querySelector('#menu-icon'); // Hier wird eine Variable "menu" erstellt und das HTML-Element mit der ID "menu-icon" ausgewählt.
    let navbar= document.querySelector('.navbar'); // Hier wird eine Variable "navbar" erstellt und das HTML-Element mit der Klasse "navbar" ausgewählt.
    menu.onclick=()=>{ // Wenn das "menu"-Element angeklickt wird, wird die folgende Funktion ausgeführt:
        menu.classList.toggle('bx-x'); // Hier wird die CSS-Klasse "bx-x" zum "menu"-Element hinzugefügt oder entfernt.
        navbar.classList.toggle('open'); // Hier wird die CSS-Klasse "open" zum "navbar"-Element hinzugefügt oder entfernt.
    } 

  <!-- Eingabe Formular für das Passwort Ändern -->
  <form action ="passwortändernpepper.php" method= "post">
      <input type= "email" name = "email" id = "email" placeholder="dein email" required><br>
      <input type= "password" name= "apw" placeholder="dein Passwort" required><br>
      <input type= "password" name= "npw" placeholder="neues Passwort" required><br>
      <input type= "password" name= "w_pw" placeholder="Passwort wiederholen" required><br>
      <button type= "submit"  name= "submit"> Ändern</button>
  </form>

  </body>
 </html>
Code Auszug 3 Passwort Reset

6	Lastenheft Auszug
 		
Abbildung 10 Lastenheft Auszug


¬¬¬

7	Pflichtenheft Auszug
7.1	 Behalten der Bisherige Hoster
1.	Script Sprache: PHP
7.2	Funktionale Anforderungen
1.	Verschlüsselter Login 
2.	Mitglieder Verwaltung:
für die Webseite sind folgende Nutzergruppen angedacht, für die ein Log-In erforderlich ist:
a.	Vereinsmitglied
	Verschlüsselter Login
	Änderungsmöglichkeit für die eigene Daten
	Ansicht auf Alle Mitglieder
	Passwort Selber ändern
b.	Vereins-Kassenwart
	Änderungsmöglichkeit für die eigene Daten
	Ansicht auf Alle Mitglieder
	Passwort Selber ändern
	Finanzdaten Anlegen
	Finanzdaten Bearbeiten
c.	Vereins-Administrator
	Änderungsmöglichkeit für die eigene Daten
	Ansicht auf Alle Mitglieder
	Passwort Selber ändern
	Neuer Mitglieder Anlegen
	Mitglieder Daten Bearbeiten
	Mitglieder löschen
	Mitglieder Rechte verteilen
7.3	 Nicht Funktionale Anforderungen
1.	Wartebarkeit 
a.	Kommentare im Quellcode
2.	Benutzbarkeit
a.	Kunden Dokumentation
b.	
3.	Responsiv Design
a.	Smartphone
b.	Tablette
c.	Desktop
8	Testprotokolle
Die Anwendung wurde getestet und Testprotokoll wurde erstellt.
Auszug aus dem Testprotokoll:
A Beschreibung der Testfälle
Test-ID	Beschreibung 	   Erwartet
2.		Responsivität	
1.1	Webseite auf Desktop aufgerufen	   Aufruf erfolgreich  
1.2	Webseite auf Tablet und Handyaufgerufen	Aufruf erfolgreich  
Webseite könnte sich an das Große des Endgeräte anpassen
2.	Login (Anmeldung von Mitgliedern)	
2.1	Als Administrator	Login erfolgreich
Der Mitglied könnte den Admin Bereich zugreifen
	Werte: E-Mail, Passwort	
2.2	Als Kassenwart	Login erfolgreich
Der Mitglied könnte den Kassenwart Bereich zugreifen
	Werte: E-Mail, Passwort	
2.3	Als Einfach Mitglied	Login erfolgreich
Der Mitglied könnte den Mitglieder Bereich zugreifen
	Werte: E-Mail, Passwort	
3.	Administrative Rechte	
3.1	Mitglieder Anlegen	Registration erfolgreich
Mitglied könnte angelegt werden
	Werte: Vorname, Name, Geburtsdatum, E-Mail, Straße, Hausnummer, Ort, PLZ, Telefone, Mitglied Level	
3.2	Mitglieder löschen	Löschen erfolgreich
Mitglied könnte gelöscht werden
3.3	Mitglieder Rechte ändern	Rechte ändern erfolgreich
MitgliedLevel könnte geändert werde
	Werte: 0 oder 1 oder 2 oder 3	
3.4	Passwort Reset	Passwort ändern erfolgreich
Administrator könnte sein Passwort ändern
	Werte: E-Mail, Altes Passwort, Neues Passwort	
3.3	Mitglieder Daten Bearbeiten	Daten Bearbeitung erfolgreich
Mitgliederdaten könnten bearbeitet werden
	Werte: Vorname, Nachname, E-Mail, Straße, Hausnummer, PLZ, Ort, Telefone,	
3.4	Mitglied Löschen	Löschen erfolgreich
Mitglied könnte erfolgreich gelöscht werden
Tabelle 13 Testprotokoll1



Die Tabelle Testprotokolle geht hier weiter
Test-ID	Beschreibung 	   Erwartet
4	Einfache Mitglieder Rechte	
4.1	Eigene Daten bearbeiten	Daten bearbeiten erfolgreich
Das Mitglied könnte seine Daten bearbeiten
	Werte: Vorname, Name, E-Mail, Straße, Hausnummer, Ort, PLZ, Telefone.	
4.2	Mitglieder Liste und kontakt Daten aufrufen	Aufruf war erfolgreich
das Mitglied könnte sich die Liste und die Kontaktdaten ansehen  
5	Kassenwart Rechte	
5.1	Eigene Daten bearbeiten	Daten bearbeiten erfolgreich
Der Kassenwart könnte seine Daten bearbeiten
	Werte: Vorname, Name, E-Mail, Straße, Hausnummer, Ort, PLZ, Telefone	
5.2	Mitglieder Liste und kontakt Daten aufrufen	Aufruf war erfolgreich
das Mitglied könnte sich die Liste und die Kontaktdaten ansehen  
Tabelle 14- Testprotokoll2










9	Kundendokumentation
Willkommen bei Ihrer Kundendokumentation für die Mitglieder Verwaltung des Vereins Freundeskreis Liborius. Mit dieser Kundendokumentation erhalten Sie eine Einführung in die Bedienung der Anwendung. Die Webseite ermöglicht Ihnen als Mitglied sich einzuloggen ihre Wünsche je nach mitgliedgruppe zu erfüllen. Ich wünsche Ihnen viel Spaß mit der Anwendung.
Systemvoraussetzungen:
 Um ein Login zu verwirklichen sind die folgenden Systemanforderungen zu erfüllen:
•	Handelsüblicher Desktop PCs 
•	Handelsüblicher Laptop 
•	Handelsübliches Handy oder Tablet
•	Eine Internet-Verbindung
Übersicht:
Nach dem Aufruf der Webseite öffnet sich die Startseite mit einer Menüleiste, wodurch man zwischen den Buttons Fördermittel, Termine, Kontakt, über Uns, Startseite, Login, Impressum, AGB, Haftungsausschluss, Satzung Navigieren kann. 
Ansicht aus Desktop Abbildung 9 und Ansicht aus Tablet oder Handy Abbildung10
 
Abbildung 11 Ansicht aus Desktop 

 
Abbildung 12 Ansicht aus Tablet oder Handy

Bei Klick auf den „Login“ Button wird die Mitglied Login Benutzeroberfläche angezeigt. 
Die folgende Abbildung kennzeichnet die entsprechende Schaltfläche
 	 
      Abbildung 13-login Formular

Nach erfolgreichem Login als einfache Mitglieder
	
 
Abbildung 14-einfache Mitglieder Seite
Mitglieder Bereich
Cursor auf den Grünen Button “Mitglieder Bereich“ klappt folgenden Menu aus.
•	Mitgliedliste
•	Meine Daten                                                   
•	Passwort Reset.
                     
Abbildung 15 Mitglied Bereich	
Nach Erfolgreichem Login als Kassenwart

 
Abbildung 16-Kassenwart Seite

Kassenwart Bereich
Cursor auf den Grünen Button “Mitglieder Bereich“ klappt folgenden Menu aus.
•	Mitgliedliste
•	Meine Daten 
•	Finanzdaten Bearbeiten
•	Finanzdaten hinzufügen
•	Finanzdaten ändern                                                  
•	Passwort Reset
•	Beitragskonto
Die folgende Abbildung kennzeichnet die entsprechende Schaltfläche
 
Abbildung 17-Kassenwart Bereich

Nach erfolgreichem Login als Administrator 
Admin Bereich
Cursor auf den Grünen Button “Admin Bereich“ klappt folgenden Menu aus.
•	Meine Daten 
•	Mitglieder Anlegen
•	Mitglieder Bearbeiten
•	Mitgliederrecht ändern                                                  
•	Passwort Reset
Die folgende Abbildung kennzeichnet die entsprechende Schaltfläche


     	
Abbildung 18-Admin Bereich

Mitglieder Anlegen
Um neues Mitglied anzulegen, klicken Sie auf “Mitglieder anlegen“ scheint eine Benutzer Oberfläche wie in Abbildung 16- Mitglied anlegen abgebildet.
 	
Abbildung 19 Mitglieder anlegen

Mitglieder Bearbeiten oder löschen
Um Mitgliederdaten zu bearbeiten, klicken Sie auf “Mitglieder Bearbeiten“. Es wird eine Tabelle mit der Liste aller Mitglieder angezeigt. Wählen Sie das Mitglied, das Sie bearbeiten möchten, und klicken Sie auf die Schaltfläche “Bearbeiten“. Daraufhin werden die entsprechenden Daten angezeigt, die Sie bearbeiten möchten, oder klicken Sie auf die Schaltfläche “Delete“, um das Mitglied zu löschen.
 wie in Abbildung17 “Mitglieder Liste“ und Abbildung 18 “Daten Aktualisierung“ dargestellt.
In der Tabelle handelt es sich um Testdaten. 


 
Abbildung 20-Mitglieder Liste


Abbildung 21-Daten Aktualisierung

Mitgliederrechte ändern
Um Mitgliederrechte zu ändern, klicken Sie auf “Mitgliederrechte ändern“. Es wird eine Tabelle mit der Liste aller Mitglieder mit deren Rechte angezeigt. Wählen Sie das Mitglied, das Sie das Recht bearbeiten möchten, und klicken Sie auf die Schaltfläche “Bearbeiten“. Daraufhin werden die entsprechenden Daten angezeigt, die Sie bearbeiten möchten.
wie in Abbildung19 “Mitgliederrechte“ und Abbildung 20 “Recht aktualisieren“ dargestellt.

 
Abbildung 22 Mitgliederrechte



 
Abbildung 23 Recht aktualisieren

