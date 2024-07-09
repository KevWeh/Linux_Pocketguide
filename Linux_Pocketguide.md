# Linux_Pocketguide
### Autor: Kevin Wehrli


## Inhalt:

1. [Einleitung](#einleitung)
2. [Open Source](#kapitel-0-open-source)
3. [Einführung in Linux](#kapitel-1-einführung-in-linux)
4. [Installation und Konfiguration](#kapitel-2-installation-und-konfiguration)
5. [Grundlegende Befehle und Navigation](#kapitel-3-grundlegende-befehle-und-navigation)
6. [Benutzer- und Rechteverwaltung](#kapitel-4-benutzer--und-rechteverwaltung)
7. [Softwareverwaltung](#kapitel-5-softwareverwaltung)
8. [Systemüberwachung und -protokollierung](#kapitel-6-systemüberwachung-und--protokollierung)
9. [Netzwerkkonfiguration](#kapitel-7-netzwerkkonfiguration)
10. [Automatisierung und Skripting](#kapitel-8-automatisierung-und-skripting)
11. [Datensicherung und Wiederherstellung](#kapitel-9-datensicherung-und-wiederherstellung)
12. [Systemwartung und Troubleshooting](#kapitel-10-systemwartung-und-troubleshooting)
13. [Glossar](#glossar)
14. [Anhang (Quellen, weiterführende Links etc.)](#anhang)

## Einleitung
Besten Dank für dein Interesse an diesem Cheatbook. Mein Name ist Kevin und der Einfachheit halber verwende ich die Du-Form. Als grosser Fan von Linux, Open-Source-Projekten und Werken, die das nötige Wissen kurz und bündig vermitteln, ist es mir ein Anliegen, selbst ein solches Handbuch zu verfassen und auf GitHub zur Verfügung zu stellen.
Ich selbst erhebe nicht den Anspruch darauf ein Linux-Profi zu sein (hoffe es aber im Laufe des Schreibens zu werden), also verzeiht mir den einen oder anderen Fehler, der mir unterlaufen wird.
Viel Spass beim Lesen, Nachmachen und Lernen.

## Kapitel 0: Open Source
***Offenheit - Transparenz - gemeinschaftliche Zusammenarbeit*** oder in den Worten des Linux-Kernel-Entwicklers:
> **"Software is like sex: it's better when it's free."**
> 
> *- Linus Torvalds*

Da in vielen Linux-Lehrbüchern das Thema Open Source meiner Meinung nach zu wenig thematisiert wird, möchte ich es an dieser Stelle besser machen und der doch sehr relevanten Angelegenheit das Kapitel 0 widmen.

### Was bedeutet Open Source?
Wenn man den Begriff Open Source hört, kommen einem häufig die Begriffe freie und kostenlose Software und Linux in den Sinn. Dies ist insofern korrekt, da Open-Source-Software in der Regel kostenlos und Linux ein Open-Source-Projekt ist. Der eigentliche Gedanke hinter Open Source geht jedoch viel tiefer. Er bezieht sich darauf, dass der Quellcode der entsprechenden Software frei zugänglich ist. Dieser kann von der Öffentlichkeit eingesehen und je nach Art der [Lizenzierung](#lizenzen) modifiziert und weiterverbreitet werden.

Dies bringt einige Vorteile mit sich, die bei Closed Source Software (das Gegenteil von Open Source – der Quellcode ist nicht öffentlich zugänglich) nicht existieren:
- **Transparenz:** Da der Code öffentlich zugänglich ist und überprüft werden kann, lässt sich sicherstellen, dass keine versteckten Funktionen und Tracking-Mechanismen vorhanden sind. Potenzielle Fehler oder Schwachstellen können schneller entdeckt werden, was wiederum zur allgemeinen Qualitätssicherung beiträgt.
- **Sicherheit:** Dadurch, dass der Code von der breiten Masse eingesehen werden kann, können bei einer aktiven Community Sicherheitslücken schneller entdeckt und durch gemeinschaftliche Zusammenarbeit beseitigt werden.
- **Kostenersparnis:** Open-Source-Software ist in der Regel kostenlos, wodurch teils hohe Lizenzkosten vermieden werden. Dies ist auch einer der Gründe, weshalb Linux so verbreitet ist und weltweit auf so vielen Servern zum Einsatz kommt. Je nach Anwendung oder Betriebssystem muss jedoch berücksichtigt werden, dass trotzdem Kosten für Implementierung, Anpassungen, Schulungen und Support anfallen können.
- **Flexibilität:** Die Benutzer können, entsprechende technische Fähigkeiten und Ressourcen vorausgesetzt, die Software auf ihre eigenen Anwendungsfälle anpassen, optimieren und weiterentwickeln.

Nicht alles ist Gold, was glänzt. So hat natürlich auch Open-Source-Software ihre Nachteile:
- **Abhängigkeit der Community:** Open-Source-Projekte werden oft von freiwilligen Entwicklern ohne Unterstützung grosser Firmen betreut. Ausnahmen wie das Linux-Kernel-Projekt oder die Linux-Distributionen Ubuntu und RHEL zeigen, dass es auch anders geht. Kleinere Projekte können jedoch aufgrund fehlender Entwickler zu Sicherheitsrisiken werden, da der offene Quellcode Angreifern Schwachstellen aufzeigt. Dokumentationen sind oft weniger vollständig als bei Closed-Source-Software, und man ist stärker auf die Community angewiesen.
- **Kompatibilität und Integration:** Teilweise kann es bei Open-Source-Software kann es teilweise zu Kompatibilitätsproblemen im Zusammenhang mit anderen Softwarelösungen oder Systemen kommen.
- **Verantwortung und Haftung:** Auf Grund einer fehlenden zentralen Instanz bei Open-Source Projekten, welche Verantwortung übernimmt oder Garantie bietet bei Ausfällen, kann es insbesondere bei kritischen Anwendungsfällen ratsam sein auf eine Closed-Source-Anwendung oder -System zurückzugreifen, bei welcher die Verantwortlichkeiten klarer geregelt sind.
- **Langfristige Wartung und Weiterentwicklung:** Aufgrund der Abhängigkeit von der Community und den freiwilligen Entwicklern kann es zu Verzögerungen in der Weiterentwicklung oder zum Abbruch des Projekts kommen, wenn wichtige Teilnehmer das Projekt verlassen.

Open Source beschränkt sich dabei nicht ausschliesslich auf Software. In den folgenden Bereichen findet der Ansatz ebenfalls seine Anwendung:
| Bezeichnung          | Erklärung                                                         | Beispiele                                           |
|----------------------|-------------------------------------------------------------------|-----------------------------------------------------|
| Open Content         | Inhalte zur kostenlosen Nutzung und Weiterverbreitung.            | Wikipedia, Internet Archive, OpenStreetMap          |
| Open-Source-Hardware | Öffentlich einsehbare Baupläne für Hardwareprojekte.              | Arduino, RISC-V, Tinkerforge                        |
| Open Access          | Öffentlicher Zugang zu wissenschaftlicher Literatur im Internet.  | arXiv, PubMed Central, Directory of Open Access Journals (DOAJ) |

Die Open Source Bewegung hat ihre Urpsrünge in der Do-it-yourself-Bewegung, die nach dem Ersten Weltkrieg ihren Aufschwung erlebte, ebenfalls dazu beigetragen hat die Hacker-Bewegungen der 1960er/1970er Jahre und die Freie-Software-Bewegung der 1980er Jahre, aus welcher das [GNU-Projekt](#gnu-projekt) entstanden ist.

### Beispiele zu Open Source Anwendungen und Betriebssystemen
Für viele Anwendungen und Betriebssystem (OS) mit teils hohen Lizenzkosten gibt es heutzutage eine Open Source Alternative. Manchmal müssen kleine Abstriche im Design, der Benutzeroberfläche oder den Funktionen gemacht werden, aber genau dies macht für mich persönlich den Charme von Open-Source-Software aus. Bezüglich des Supports muss man sich in der Regel keine grossen Sorgen machen, wenn eine genügend grosse Community vorhanden ist, wird man mit etwas Geduld und den passenden Keywords bei Google fündig.

Anbei ein kleiner Vergleich von Closed Source Anwendungen und Betriebssystemen mit ähnlichen oder vergleichbaren Open Source Alternativen:
| Anwendungs-/OS-Art      | Closed Source                  | Open Source    |
|-------------------------|--------------------------------|----------------|
| Bildbearbeitung:        | Adobe Photoshop                | GIMP           |
| Illustration:           | Adobe Illustrator              | Inkscape       |
| Betriebssystem (Client):| Microsoft Windows, Apple MacOS | Linux (Ubuntu, Fedora etc.), FreeBSD |
| Betriebssystem (Server):| Microsoft Windows Server       | Linux (Debian, CentOS etc.)         |
| Betriebssystem (mobile):| Apple iOS                      | Android (grösstenteils Open Source)|
| Office Suiten:          | Microsoft Office               | LibreOffice   |

Weitere bekannte Beispiele für Open-Source-Anwendungen sind der Webbrowser Mozilla Firefox, das E-Mailprogramm Mozilla Thunderbird und der Webbserver Apache.

### Zusammenfassung
Das Open Source Konzept zeigt auf, dass mit Hilfe einer engagierten Community grosses geleistet werden kann. Fehler und Schwachstellen können schneller und effizienter entdeckt und behoben werden. Es besteht ausserdem kein grosser Anreiz für Entwickler versteckte Funktionen und Tracking-Mechanismen zu implementieren.  
Open Source bezieht sich dabei nicht alleine nur auf das Thema Software und findet noch in anderen Gebieten ihre Anwendung. Sollte man einmal nicht zwingend auf eine properitäre Software angewiesen sein, lohnt es sich nach einer Open Source Alternative Ausschau zu halten. 



## Kapitel 1: Einführung in Linux
Für viele ist Linux ein weiteres Betriebssystem, welches neben Windows und MacOS auch noch existiert. Dass hinter Linux jedoch nicht nur ein weiteres Betriebssystem steckt, was es mit dem Linux-Kernel-Projekt und dessen Entwickler Linus Torvalds auf sich hat, möchte ich gerne in diesem Kapitel genauer erläutern.

### Geschichte
Um die Entstehungsgeschichte des Linux-Kernel-Projekts besser zu verstehen, müssen wir einige Jahrzente zurückgehen.   

#### Die Anfänge: Unix und Minix
In den 1960er Jahren begannen Ken Thompson, Dennis Ritchie, Douglas McIlroy und Joseph Ossanna bei den Bell Labs die Entwicklung des Multiuser-Betriebssystem Unix. Für die damalige Zeit war es ein revolutionäres System und legte den Grundstein für viele zukünftige Betriebssysteme. Es war portabel und liess sich auf verschiedenen Computersystemen implementieren. Dadurch war es bei Universitäten und Entwicklern sehr beliebt. Der Muttergesellschaft der Bell Labs, AT&T, war es zum Zeitpunkt der Entwicklung von Unix verboten neue Märkte wie den Computermarkt zu erschliessen, auf Grund dessen wurden verschiedenen Universitäten das Betriebssystem zu den Kosten des Datenträgers zur Verfügung gestellt. 

In den 1980er Jahren entwickelte Professor Andrew S. Tannenbaum das Unix-ähnliche Betriebssystem Minix. Es wurde mit dem Gedanken entwickelt die Grundlagen eines Betriebssystems aufzuzeigen. Das OS selbst gewann nicht die verdiente Aufmerksamkeit, diente jedoch dem Linux-Kernel-Entwickler Linus Torvalds als Inspiration für die Entwicklung seines eigenen Betriebssystems Linux.

#### 1991: Der Beginn von Linux

## Kapitel 2: Installation und Konfiguration
Bei der Installation von Linux muss man sich nicht nur für eine der zahlreichen Distributionen entscheiden, teilweise wird einem auch noch auferlegt die Entscheidung zwischen einer Distribution mit oder ohne grafischer Oberfläche (GUI) auszuwählen. Wird auf ein Betriebssystem ohne GUI gesetzt, erfolgt die Ausgabe am Bildschirm in der sogenannten Kommandozeile (CLI). Dabei wird, mit Ausnahme von  Anzeigen von ASCII-Art, auf grafische Darstellungen verzichtet. Im ersten Moment kann dies abschreckend wirken (wie soll man das komplette Betriebssystem nur mit der Kommandozeile bedienen, könnte einem in den Sinn kommen). Stellt man sich jedoch vor, für Aussenstehende wie ein Hacker auszusehen, wirkt dies relativ motivierend und man macht schnell Fortschritte. Der Verzicht der grafischen Darstellungen bringt einige Vorteile mit sich. Die vorhandenen Ressourcen können so rechenintensiven Aufgaben zur Verfügung gestellt werden und müssen nicht für die Anzeige des GUIs zur Verfügung stehen. Ausserdem kann man einiges schneller im Betriebssystem navigieren. Nichts desto trotz ist bei den allermeisten Linux Distributionen mit grafischer Oberfläche selbstverständlich auch ein Terminal installiert, so hat man das Beste erlebnis aus beiden Welten, wenn auch nicht ganz den ressourcensparenden Effekt wie bei einer Version, welche nur über eine CLI verfügt. Ein wichtiger Hinweis noch vorab, das CLI bietet dem Benutzer die Möglichkeit mit dem System über Befehle zu interagieren. Das Programm welche die Befehle verarbeitet ist die sogenannte Shell. Hiervon gibt es unterschiedliche Versionen, welche jeweils eigene Vor- und Nachteile haben. Die am Häufigsten eingesetzte Shell ist dabei die sogenannte Bash (Bourne Again Shell).

In der nachfolgenden Tabelle möchte ich etwas genauer auf die bekanntesten Distributionen und deren Eigenheiten eingehen.

| Name                           | Eigenschaften und Eigenheiten                                                                                                 | Einsatzbereich   | Für Anfänger geeignet | Paketmanagement | Installationsbefehl | Oberfläche (GUI, CLI etc.)       |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------|-----------------------|-----------------|---------------------|----------------------------------|
| Ubuntu                         | Eine der bekanntesten und am weitverbreitetsten Distributionen. Grosse Community und online gute Dokumentationen vorhanden.   | Desktop + Server | Ja                    | dpkg / apt      | sudo apt install    | Desktop: GUI + CLI / Server: CLI |
| Debian                         | Stabilität und Zuverlässigkeit, Grundlage für viele andere Distributionen (inkl. Ubuntu). Konservative Paketaktualisierungen. | Desktop + Server | Bedingt               | dpkg / apt      | sudo apt install    | Desktop: GUI + CLI / Server: CLI |
| CentOS                         | Community-getriebene, kostenlose Version von RHEL. Bekannt für Stabilität und Langzeitunterstützung.                          | Server           | Nein                  | rpm / yum       | sudo yum install    | CLI                              |
| RedHat Enterprise Linux (RHEL) | Kommerzielle Distribution mit professionellem Support und Zertifizierungen. Fokus auf Unternehmen und deren Anforderungen.    | Server           | Nein                  | rpm / yum       | sudo yum install    | CLI                              |
| Kali Linux                     | Speziell für Penetrationstests und Sicherheitsanalysen entwickelt. Enthält zahlreiche vorinstallierte Sicherheitstools.       | Desktop + Server | Nein                  | dpkg / apt      | sudo apt install    | Desktop: GUI + CLI / Server: CLI |
| Arch Linux                     | Rolling-Release-Modell, sehr anpassbar und schlank. Benutzer müssen viel manuell konfigurieren, daher Lernkurve höher.        | Desktop          | Nein                  | pacman          | sudo pacman -S      | Desktop: GUI + CLI               |
| Linux Mint                     | Basierend auf Ubuntu, bietet eine benutzerfreundliche Erfahrung mit Multimedia-Support out-of-the-box.                        | Desktop          | Ja                    | dpkg / apt      | sudo apt install    | Desktop: GUI + CLI               |



Gerne möchte ich nachfolgend einige Möglichkeiten vorstellen, wie man Linux erleben und erlernen kann. Dabei gehe ich von der einfachsten zur schwierigsten Möglichkeit vor. Da ich mich persönlich mit Ubuntu am Besten auskenne, zeige ich die jeweiligen Installationstypen an Hand von Ubuntu auf. Jeder Distribution hat ihre Eigenheiten, im Grossen und Ganzen ist der Installationsablauf jedoch ähnlich.

### Express/Einfach:
Wer jetzt nicht länger warten möchte, dem Empfehle ich die Cloudvariante Linode von Akamai. Neben den vielen Cloudanbietern, welche heutzutage existieren, hat sich Linode auf das Deployment von Linux spezialisiert. Wer nun denkt, dass diese Variante mit hohen Kosten verbunden ist, den kann ich beruhigen. Man erhält ein Startguthaben in der Höhe von $100. Wenn dies aufgebraucht oder abgelaufen ist, belaufen sich die Kosten auf ca. $5 - $15 pro Monat, sofern man sich für eine ressourcensparende Variante entscheidet. Der einzige "Nachteil", wenn man ihn denn so nennen darf, ist dass lediglich Linux Distributionen mit CLI zur Verfügung stehen.
Zu Beginn muss man sich ein Konto einrichten (evtl. Kreditkarte???)
Die Verbindung mit der in der Cloud bereitgestellten Linux VM erfolgt folgendermassen:

### Einfach:
#### Windows:
Im Jahr 2016 unter Windows 10 hat Microsoft das sogenannte Windows-Subsystem für Linux (WSL) ins Leben gerufen.

##### MacOS:
Da der Apple Kernel? auf dem Unix System basiert, ist bei den Geräten mit MacOS bereits ein Terminal installiert. Als Shell kommt die so genannte Z shell (zsh) zum Einsatz diese ist jedoch (grösstenteils?) Kompatibel zu der am häufigsten eingesetzten Bash Shell, welche auf den meisten Linux Distributionen als Standard-Shell vorhanden ist. Unter MacOS kann man auf Grund dessen im Betriebssystem gleich navigieren wie unter einer reinen Linux Installation.

### Mittel:
Mit etwas mehr Aufwand ist die Installation einer Virtuellen Maschine (VM), worauf dann eine Distribution der Wahl installiert werden kann. Bei einer VM kommt ein so genannter Hypervisor zum Einsatz. Dieser gaukelt dem zu installierenden System vor, ein eigener Computer mit eigener Hardware zu sein. Als VM-Software kann ich, nicht nur auf Grund der Open Source Natur der Anwendung, Oracle VM VirtualBox empfehlen. In erster Linie werden wir uns die Installation der VirtualBox anschauen. Im Anschluss erfolgt die Installation von Ubuntu auf der VirtualBox selbst.

### Schwierig:
Als letztes erfolgt eine Bare Metal ("blankes Metall"). Hierbei erfolgt die Installation des Linux Betriebssystem direkt auf der Hardware. Der Grundsätzliche Installationsprozess unterscheidet sich dabei nicht gross von der Installation auf einer VM. Dennoch gibt es die eine oder andere Eigenheit, welche es zu beachten gilt.

## Kapitel 3: Grundlegende Befehle und Navigation
Im nächsten Kapitel behandeln wir die Arbeit in der Kommandozeile. Als Shell kommt dabei Bash zum Einsatz. Eines vorweg, in der Linux CLI gibt es nicht den einen richtigen Weg um eine Aufgabe zu erledigen. Man kann jede Aufgabe auf gefühlt 1'000 unterschiedliche Arten erledigen und kommt dabei zu einem ähnlichen, wenn nicht gar identischen Ergebniss. Daher wird bei den nachfolgenden Befehlen jeweils versucht auch den einen oder anderen Alternativweg aufzuzeigen.

### Wichtiger Hinweis:
Das Betriebssystem Linux mit seinen sämtlichen Befehlen, ist was die Kommandozeile anbelangt Case Sensitive. Dies bedeutet, dass zwischen Gross- und Kleinschreibung unterschieden wird. Anders als unter Windows und MacOS eventuell angewöhnt, kann es gerade z.B. bei der Suche nach einer Datei auf einem Linux-System dazuführen, dass man die Datei findet oder eben nicht. Daher meine Empfehlung, man sollte sich daran gewöhnen, dass alles klein geschrieben wird, ausser es sei z.B. in einem Skript notwendig die Ausgabe in Gross- und Kleinschreibung anzeigen zu lassen. Der Hinweis bezüglich der Case Sensitivity kommt an dieser Stelle, weil es bei den Befehlen (welche im Übrigen immer klein geschrieben werden), Optionen gibt, welche zu einem komplett anderen Ergebniss führen können, wenn man den jeweiligen Buchstaben klein oder gross schreibt.

### Befehlsaufbau:
Linuxbefehle sind wie folgt aufgebaut (eine genauere Erklärung der jeweiligen Befehlen und Optionen erfolgt im nächsten Abschnitt):
|kompletter Befehl     | Befehlsteil | Optionen | Parameter  | besonderes | Erläuterung |
|----------------------|-------------|----------|------------|------------|-------------|
| `ls -ahlS /etc/usr/` | `ls`        | `-ahlS`  | `/etc/usr/`| -          | `ls` listet den Inhalt auf / als Optionen kommen `-ahlS` zum Einsatz / der Pfad `/etc/usr/` gibt dem Befehl `ls`vor mit welchem Verzeichnis gearbeitet wird | 

Da häufig mit wiederkehrenden Befehelen gearbeitet wird, kann man jeweils mit der Pfeiltaste nach oben ( ↑ ) die letzten Eingaben erneut aufgerufen werden.

### Befehle
#### sudo
Den Meisten, welche sich etwas mehr als mit der Kenntniss, dass es sich bei Linux um ein Betriebssystem handelt, beschäftigt haben, sollte der Befehlsteil `sudo` (sprich: [`su:du:]) ein Begriff sein. Es stellt die Abkürzung für die Aussage "Super User Do" dar.

Der Befehlspräfix ermöglicht den auf `sudo`nachfolgenden Befehl mit Administratorenrechten auszuführen. Dies ist notwendig, sobald mit Files gearbeitet wird bei welchem man nicht der entsprechende Besitzer oder der entsprechenden Gruppe zugehörig ist. Hierbei spielt jedoch auch die eingestellte Berechtigungsstufe des jeweiligen Files eines Rolle (mehr dazu beim nachfolgenden Befehl `ls`).

Um `sudo`verwenden zu können muss man der Benutzergruppe sudo angehören. Der jeweils erste Benutzer eines Systemes, respektive der Account, welches bei der Installation des Systemes als erstes angelegt wird, ist automatisch der Gruppe sudo zugewiesen. Alle weiteren Konten welche danach angelegt werden, müssen jeweils manuell der sudo Gruppe zugewiesen werden.

Bei der Arbeit im System, wird man jeweils schnell mit der Mitteilung "Permission denied" darauf hingewiesen, sollte man den Befehlsprefix `sudo` vergessen haben anzugeben. Hier noch mein Tipp: Damit man den jeweils letzten Befehl nicht nochnmals komplett eintippen muss, kann man in den meisten Fällen `sudo !!` unterhalb der Meldung "Permission denied" ausführen. Die `!!`-Zeichen weisen das System darauf hin den letzten Befehl nochmals abzurufen.

Nach der Eingabe eines Befehles mit `sudo`wird man jeweils dazu aufgefordert das Passwort seines Accountes anzugeben. Je nach eingestelltem Zeitintervall, müssen bei den nächsten Ausführungen von Befehlen mit zusätzlichen Administratorenrechten kein Passwort mehr übermittelt werden.

#### Die wichtigsten Befehle für die Navigation im System:
- pwd
- ls
- cd

#### Befehle zur Manipulationen von Files:
- chmod
- chown
- chgrp

#### Befehle zur Benutzerverwaltung:
- adduser
- addgrp

#### Befehle zur Manipulation der Ausgabe:
- grep
- awk
- sed

#### Befehle zur Anzeige/Bearbeitung von Dateien:
- cat
- nano

#### Diverse nützliche Befehel:
- command -v / Alternative dpkg -l | grep "Paketname"
- → Verlauf zu letzt verwendete Befehel

## Kapitel 4: Benutzer- und Rechteverwaltung
Da wir uns nun mit einigen der wichtigsten Befehlen, inklusive der ersten Befehle zur Benutzerverwaltung vertraut gemacht haben, möchten wir tiefer in das Thema einsteigen.
## Kapitel 5: Softwareverwaltung
## Kapitel 6: Systemüberwachung und -protokollierung
## Kapitel 7: Netzwerkkonfiguration
## Kapitel 8: Automatisierung und Skripting
## Kapitel 9: Datensicherung und Wiederherstellung
## Kapitel 10: Systemwartung und Troubleshooting
## Glossar:
#### GNU-Projekt:
#### Lizenzen:

## Anhang:
#### **Quellen:**
#### **Weiterführende Links:**
**[ubuntuusers.de:](https://ubuntuusers.de/)** Die Seite ubuntusers.de ist mitlerweile zu meinem täglichen Begleiter geworden. Ich würde es als Allround Werkzeug für die Arbeit mit Linux betiteln. Anders als der Seitentitel erahnen lässt, wird selbstverständlich nicht nur die Distribution Ubunutu behandelt.

youtube

acronis linode

#### **Weiterführende Literatur:**
#### **Rechtlicher Hinweis:**
„Alle genannten Marken- und Produktnamen sind Warenzeichen der jeweiligen Unternehmen.“

#### Linux_Pocketguide © 2024 by Kevin Wehrli is licensed under CC BY-NC-SA 4.0. To view a copy of this license, visit https://creativecommons.org/licenses/by-nc-sa/4.0/