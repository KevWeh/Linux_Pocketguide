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
13. [Weiterbildung und Zertifizierungen](#kapitel-11-weiterbildung-und-zertifizierungen)
13. [Glossar](#glossar)
14. [Anhang (Quellen, weiterführende Links etc.)](#anhang)

## Einleitung
Besten Dank für dein Interesse an diesem Cheatbook. Mein Name ist Kevin und der Einfachheit halber verwende ich die Du-Form. Als grosser Fan von Linux, Open-Source-Projekten und Werken, die das nötige Wissen kurz und bündig vermitteln, ist es mir ein Anliegen, selbst ein solches Handbuch zu verfassen und auf GitHub zur Verfügung zu stellen.
Ich selbst erhebe nicht den Anspruch darauf ein Linux-Profi zu sein (hoffe es aber natürlich im Laufe des Schreibens zu werden), also verzeiht mir den einen oder anderen Fehler, der mir unterlaufen wird.
Viel Spass beim Lesen, Nachmachen und Lernen.

## Kapitel 0: Open Source
***Offenheit - Transparenz - gemeinschaftliche Zusammenarbeit*** oder in den Worten des Linux-Kernel-Entwicklers:
> **"Software is like sex: it's better when it's free."**
> 
> *- Linus Torvalds*

Da in vielen Linux-Lehrbüchern das Thema Open Source meiner Meinung nach zu wenig thematisiert wird, möchte ich es an dieser Stelle anders machen und der doch sehr relevanten Angelegenheit das Kapitel 0 widmen.

### Was bedeutet Open Source?
Wenn man den Begriff Open Source hört, kommen einem häufig die Begriffe kostenlose Software und Linux in den Sinn. Dies ist insofern korrekt, da Open-Source-Software in der Regel kostenlos und Linux ein Open-Source-Projekt ist. Der eigentliche Gedanke hinter Open Source geht jedoch viel tiefer. Er bezieht sich darauf, dass der Quellcode der entsprechenden Software frei zugänglich ist. Dieser kann von der Öffentlichkeit eingesehen und je nach Art der [Lizenzierung](#lizenzen) modifiziert und weiterverbreitet werden.

Dies bringt einige Vorteile mit sich, die bei Closed Source Software (das Gegenteil von Open Source – der Quellcode ist nicht öffentlich zugänglich) nicht existieren:
- **Transparenz:** Da der Code öffentlich zugänglich ist und überprüft werden kann, lässt sich sicherstellen, dass keine versteckten Funktionen und Tracking-Mechanismen vorhanden sind. Potenzielle Fehler oder Schwachstellen können schneller entdeckt werden, was wiederum zur allgemeinen Qualitätssicherung beiträgt.
- **Sicherheit:** Dadurch, dass der Code von der breiten Masse eingesehen werden kann, können bei einer aktiven Community, Sicherheitslücken schneller entdeckt und durch gemeinschaftliche Zusammenarbeit beseitigt werden.
- **Kostenersparnis:** Open-Source-Software ist in der Regel kostenlos, wodurch teils hohe Lizenzkosten vermieden werden. Dies ist auch einer der Gründe, weshalb Linux so verbreitet ist und weltweit auf so vielen Servern zum Einsatz kommt. Je nach Anwendung oder Betriebssystem muss jedoch berücksichtigt werden, dass trotzdem Kosten für Implementierung, Anpassungen, Schulungen und Support anfallen können.
- **Flexibilität:** Die Benutzer können, entsprechende technische Fähigkeiten und Ressourcen vorausgesetzt, die Software auf ihre eigenen Anwendungsfälle anpassen, optimieren und weiterentwickeln.

Nicht alles ist Gold, was glänzt. So hat natürlich auch Open-Source-Software ihre Nachteile:
- **Abhängigkeit der Community:** Aufgrund der Abhängigkeit von der Community und den freiwilligen Entwicklern kann es zu Verzögerungen in der Weiterentwicklung oder zum Abbruch des Projekts kommen, wenn wichtige Teilnehmer das Projekt verlassen. Dies kann unter anderem auch zu einem Sicherheitsrisiko werden, da der Quellcode im Internet frei zugänglich ist und potentielle Angreifer Schwachstellen entdecken und für ihre Zwecke missbrauchen können. Ausserdem ist die Dokumentation oft weniger vollständig als bei Closed-Source-Software, da sie meist von der Community bereitgestellt wird.
- **Verantwortung und Haftung:** Insbesondere in kritischen Anwendungsfällen kann es ratsam sein, eine Closed-Source-Anwendung einer Open-Source-Alternative vorzuziehen. So hat man eine zentrale Instanz, die im Supportfall kontaktiert werden kann oder bei korrekter Anwendung unter Umständen eine Garantie bietet.
- **Einschränkungen der Anwendungen:** Manchmal müssen bei Open-Source-Anwendungen gegenüber einer vergleichbaren Closed-Source-Anwendung Abstriche in Bezug auf Aussehen, Benutzerfreundlichkeit oder Funktionalität gemacht werden.

Open Source beschränkt sich dabei nicht ausschliesslich auf Software. In den folgenden Bereichen findet der Ansatz ebenfalls seine Anwendung:
| Bezeichnung          | Erklärung                                                         | Beispiele                                           |
|----------------------|-------------------------------------------------------------------|-----------------------------------------------------|
| Open Content         | Inhalte zur kostenlosen Nutzung und Weiterverbreitung.            | Wikipedia, Internet Archive, OpenStreetMap          |
| Open-Source-Hardware | Öffentlich einsehbare Baupläne für Hardwareprojekte.              | Arduino, RISC-V, Tinkerforge                        |
| Open Access          | Öffentlicher Zugang zu wissenschaftlicher Literatur im Internet.  | arXiv, PubMed Central, Directory of Open Access Journals (DOAJ) |

Die Open Source Bewegung hat ihre Urpsrünge in der Do-it-yourself-Bewegung, die nach dem Ersten Weltkrieg ihren Aufschwung erlebte, ebenfalls dazu beigetragen hat die Hacker-Bewegungen der 1960er/1970er Jahre und die Freie-Software-Bewegung der 1980er Jahre, aus welcher das GNU-Projekt entstanden ist.

### Beispiele zu Open Source Anwendungen und Betriebssystemen
Für viele Anwendungen und Betriebssystem (OS) mit teils hohen Lizenzkosten gibt es heutzutage eine Open Source Alternative. Anbei ein kleiner Vergleich:
| Anwendungs-/OS-Art      | Closed Source                  | Open Source    |
|-------------------------|--------------------------------|----------------|
| Bildbearbeitung:        | Adobe Photoshop                | GIMP           |
| Illustration:           | Adobe Illustrator              | Inkscape       |
| Betriebssystem (Client):| Microsoft Windows, Apple macOS | Linux (Ubuntu, Fedora etc.), FreeBSD |
| Betriebssystem (Server):| Microsoft Windows Server       | Linux (Debian, CentOS etc.)         |
| Betriebssystem (mobile):| Apple iOS                      | Android (grösstenteils Open Source)|
| Office Suiten:          | Microsoft Office               | LibreOffice   |

Weitere bekannte Beispiele für Open-Source-Anwendungen sind der Webbrowser Mozilla Firefox, das E-Mailprogramm Mozilla Thunderbird und der Webbserver Apache.

### Zusammenfassung
Das Open Source Konzept zeigt auf, dass mit Hilfe einer engagierten Community grosses geleistet werden kann. Fehler und Schwachstellen können schneller und effizienter entdeckt und behoben werden. Es besteht ausserdem kein grosser Anreiz für Entwickler versteckte Funktionen und Tracking-Mechanismen zu implementieren.  
Open Source bezieht sich dabei nicht alleine nur auf das Thema Software und findet noch in anderen Gebieten ihre Anwendung. Sollte man einmal nicht zwingend auf eine properitäre Software angewiesen sein, lohnt es sich nach einer Open Source Alternative Ausschau zu halten. 



## Kapitel 1: Einführung in Linux
Für viele ist Linux ein weiteres Betriebssystem, welches neben Windows und macOS auch noch existiert. Dass hinter Linux jedoch nicht nur ein weiteres Betriebssystem steckt, was es mit dem Linux-Kernel-Projekt und dessen Entwickler Linus Torvalds auf sich hat, möchte ich gerne in diesem Kapitel genauer erläutern.

### Geschichte
Um die Entstehungsgeschichte des Linux-Kernel-Projekts besser zu verstehen, müssen wir einige Jahrzente zurückgehen.   

#### Die Anfänge: Unix und Minix
In den 1960er Jahren begannen Ken Thompson, Dennis Ritchie, Douglas McIlroy und Joseph Ossanna bei den Bell Labs die Entwicklung des Multiuser-Betriebssystems Unix. Für die damalige Zeit war es ein revolutionäres System und legte den Grundstein für viele zukünftige Betriebssysteme. Unix war portabel und liess sich auf verschiedenen Computersystemen implementieren, wodurch es bei Universitäten und Entwicklern sehr beliebt wurde. Der Muttergesellschaft der Bell Labs, AT&T, war es zum Zeitpunkt der Entwicklung von Unix verboten, neue Märkte wie den Computermarkt zu erschliessen. Aus diesem Grund wurde verschiedenen Universitäten das Betriebssystem zu den Kosten des Datenträgers zur Verfügung gestellt.

In den 1980er Jahren entwickelte Professor Andrew S. Tanenbaum das Unix-ähnliche Betriebssystem Minix. Es wurde mit dem Ziel entwickelt, die Grundlagen eines Betriebssystems aufzuzeigen. Das Betriebssystem selbst gewann nicht die verdiente Aufmerksamkeit, diente jedoch dem Linux-Kernel-Entwickler Linus Torvalds als Inspiration für die Entwicklung seines eigenen Betriebssystems Linux.

#### 1983: Die Gründung des GNU-Projekts
Im Jahr 1983 startete Richard Stallman das GNU-Projekt (GNU steht für "GNU's Not Unix") mit dem Ziel, ein komplett freies und offenes Unix-ähnliches Betriebssystem zu entwickeln. Stallman und das GNU-Projekt entwickelten viele essenzielle Systemwerkzeuge und -bibliotheken, darunter der GNU Compiler Collection (GCC), der GNU Debugger (GDB), und die GNU C Library (glibc). Diese Werkzeuge bildeten die Grundlage für ein vollständiges Betriebssystem, allerdings fehlte noch ein freier [Kernel](#kernel).

#### 1991: Der Beginn von Linux
1991 kündigte der finnische Informatikstudent Linus Torvalds die erste Version des Linux-Kernels an. Torvalds war von Minix inspiriert, wollte jedoch ein leistungsfähigeres und flexibleres Betriebssystem schaffen. Der Linux-Kernel, kombiniert mit den GNU-Werkzeugen, ergab ein vollständiges freies und offenes Betriebssystem, das oft als "GNU/Linux" bezeichnet wird. Diese Kombination ermöglichte die Schaffung verschiedener Linux-Distributionen, die mittlerweile weltweit verbreitet und sehr populär sind.

#### Linux heute
Seit seiner Entstehung im Jahr 1991 hat sich Linux zu einem der weltweit führenden Betriebssysteme entwickelt. Heute gibt es eine Vielzahl von Linux-Distributionen, die für unterschiedliche Zwecke und Zielgruppen optimiert sind, wie Ubuntu, Fedora, Debian und CentOS.

Linux hat sich vor allem im Serverbereich etabliert und ist das bevorzugte Betriebssystem für Webserver, Datenbankserver und andere kritische Infrastrukturen. Mehr als 90% aller Webserver weltweit laufen auf Linux-basierten Systemen. Auch im Bereich der Supercomputer ist Linux führend: Über 90% der weltweit schnellsten Supercomputer laufen unter Linux. Dies liegt an der Flexibilität, Skalierbarkeit und Stabilität des Betriebssystems.

Darüber hinaus hat Linux in den letzten Jahren an Bedeutung im Bereich der eingebetteten Systeme gewonnen, z.B. in Smart-Home-Geräten, Automotive-Systemen und IoT-Geräten. Auch auf dem Desktop gewinnt Linux immer mehr Nutzer, die Wert auf Freiheit, Datenschutz und Anpassbarkeit legen.

Insgesamt ist Linux heute eine vielseitige und weit verbreitete Plattform, die in vielen Technologiebereichen eine entscheidende Rolle spielt.

### "Everything is a file."
Unter Linux wird vom Dateisystem, bis auf ganz wenige Ausnahmen, alles als eine Datei betrachtet. Dies beschränkt sich dabei nicht nur auf gewohnte Dateien wie Dokumente, Fotos und Videos. Sämtliche Geräte, Prozesse und sogar Systemkonfigurationen sind als Dateien im System unter den jeweiligen Verzeichnissen abgelegt. Dies bietet unter anderem den Vorteil, dass die Konfigurationsdateien uneingeschränkt bearbeitet werden können, wobei je nach Konfigurationsdatei natürlich mit der nötigen Vorsicht vorgegangen werden muss! Anders als eventuell von Windows gewohnt, müssen Linux-Dateien keine Dateiendungen aufweisen. So kann zum Beispiel ein Shell-Skript den Namen "beispiel.sh" tragen, es könnte jedoch auch einfach nur "beispiel" heissen und würde noch identisch bearbeitet oder ausgeführt werden können.

### Der Linux-Kernel
Beim Linux-Kernel (Betriebs-/Systemkern) handelt es sich um die unterste oder besser gesagt um die Softwareschicht, die am nächsten an der Hardware dran ist. Somit besitzt er die Möglichkeit, direkt mit der Hardware zu kommunizieren. Beim Aufstarten des Betriebssystems wird der Kernel direkt vom [Bootloader](#bootloader) nach erfolgreichem Bootvorgang angesprochen und gestartet. Neben der Kommunikation mit der Hardware verrichtet der Kernel noch unzählige weitere Aufgaben und ist während des gesamten Betriebs des OS am Arbeiten. Zu seinen Hauptaufgaben gehört die Verwaltung der einzelnen Dateien und Prozesse. Da unter Linux das Motto "Everything is a file." gilt, übernimmt der Kernel somit die Verwaltung des gesamten Betriebssystems.

### Distributionen
Durch den Open Source Charakter von Linux, wurden zahlreiche Entwickler dazu ermutigt eigenen Abwandlungen für spezifische Einsatzzwecke zu programmieren. Diese Abwandlungen nennt man Distributionen. 

In der nachfolgenden Tabelle möchte ich etwas genauer auf die bekanntesten Distributionen im Desktop- und Serverbereich eingehen:

| Name                           | Eigenschaften und Eigenheiten                                                                                                 | Einsatzbereich   | Für Anfänger geeignet | Paketmanagement | Installationsbefehl | Oberfläche (GUI, CLI etc.)       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------|-----------------------|-----------------|---------------------|----------------------------------|
| Debian                         | Stabilität und Zuverlässigkeit, Grundlage für viele andere Distributionen (inkl. Ubuntu). Konservative Paketaktualisierungen. | Desktop + Server | Bedingt               | dpkg / apt      | sudo apt install    | Desktop: GUI + CLI / Server: CLI |
| Ubuntu                         | Eine der bekanntesten und am weitverbreitetsten Distributionen. Grosse Community und gute Online-Dokumentation vorhanden.     | Desktop + Server | Ja                    | dpkg / apt      | sudo apt install    | Desktop: GUI + CLI / Server: CLI |
| CentOS                         | Community-getriebene, kostenlose Version von RHEL. Bekannt für Stabilität und Langzeitunterstützung.                          | Desktop + Server | Nein                  | rpm / yum (dnf) | sudo yum install    | Desktop: GUI + CLI / Server: CLI |
| Red Hat Enterprise Linux (RHEL) | Kommerzielle Distribution mit professionellem Support und Zertifizierungen. Fokus auf Unternehmen und deren Anforderungen.    | Desktop + Server | Nein                  | rpm / yum (dnf) | sudo yum install    | Desktop: GUI + CLI / Server: CLI |
| Kali Linux                     | Speziell für Penetrationstests und Sicherheitsanalysen entwickelt. Enthält zahlreiche vorinstallierte Sicherheitstools.       | Desktop + Server | Nein                  | dpkg / apt      | sudo apt install    | Desktop: GUI + CLI / Server: CLI |
| Arch Linux                     | Rolling-Release-Modell, sehr anpassbar und schlank. Benutzer müssen viel manuell konfigurieren, daher hohe Lernkurve.         | Desktop          | Nein                  | pacman          | sudo pacman -S      | Desktop: GUI + CLI               |
| Linux Mint                     | Basierend auf Ubuntu, bietet eine benutzerfreundliche Erfahrung mit Multimedia-Support out-of-the-box.                        | Desktop          | Ja                    | dpkg / apt      | sudo apt install    | Desktop: GUI + CLI               |
| Fedora                         | Cutting-Edge-Technologien und Innovationen. Community-getrieben, dient oft als Testbett für RHEL.                             | Desktop + Server | Bedingt               | rpm / dnf       | sudo dnf install    | Desktop: GUI + CLI / Server: CLI |
| openSUSE                       | Zwei Versionen: Leap (stabil, geeignet für Unternehmen) und Tumbleweed (Rolling Release). Yast als zentrales Verwaltungstool. | Desktop + Server | Bedingt (Leap: Ja)    | rpm / zypper    | sudo zypper install | Desktop: GUI + CLI / Server: CLI |


### Bedienungsmöglichkeiten
Bei der Bedienung des Betriebssystems kommen zwei Hauptarten der Navigation im Betriebssystem zum Einsatz: die grafische Oberfläche (GUI) und die Kommandozeile (CLI). Je nach Distribution hat man teilweise die Qual der Wahl, wie man das OS bedienen möchte. Bei der Desktopvariante stehen einem in der Regel immer beide Bedienmöglichkeiten zur Verfügung. In der Serverversion muss man sich meistens mit der Kommandozeile abfinden. Dies soll keinesfalls abschätzig verstanden werden, da die CLI diverse Vorteile gegenüber der GUI aufweist. In den nächsten zwei Abschnitten gehen wir genauer darauf ein. 
#### GUI
Die grafische Oberfläche, respektive GUI (Graphical User Interface), ist auf die Bedienung mit Maus und Tastatur ausgelegt. Verzeichnisstrukturen oder Applikationen werden als grafische Elemente dargestellt, die mit einem Mausklick geöffnet werden können. Die Bedienung unterscheidet sich in diesem Sinne nicht von einem macOS- oder Windows-Betriebssystem. Für Linux-Neulinge stellt dies eine kleinere Hürde dar als die Arbeit mit einem CLI-only-Betriebssystem.
#### CLI
Die Kommandozeile oder CLI (Command Line Interface) wird ausschliesslich mit der Tastatur bedient. Auf grafische Elemente wird mit Ausnahme von [ASCII-Art](#ascii-art) verzichtet. Da keine grafische Oberfläche dargestellt werden muss, sind die Anforderungen an die Hardwareressourcen für die Bedienung und Darstellung des Betriebssystems deutlich geringer. Dies ist insbesondere für den Einsatz auf leistungsschwächerer Hardware (Embedded Systems, IoT Devices etc.) interessant. Dennoch werden auch hochperformante Systeme ausschliesslich über die CLI bedient, wodurch die Hardware effizienter für rechenintensive Aufgaben genutzt werden kann. Neben der geringeren Hardwarebelastung ist die Bedienung des Systems über die Kommandozeile, Systemkenntnisse vorausgesetzt, deutlich schneller. Ein Nachteil ist, dass viele Befehle auswendig gelernt oder nachgeschlagen werden müssen, was im Falle einer Recherche den Geschwindigkeitsvorteil bei der Bedienung wieder aufheben kann.
##### Shell
Die sogenannte Shell ist das Programm, das auf der Kommandozeile läuft. Die CLI dient in diesem Fall als Eingabewerkzeug, respektive als Anzeige für die von der Shell zur Verfügung gestellten Inhalte. Bei der am häufigsten verwendeten Shell handelt es sich um die Bash-Shell. In der Linux-Welt existieren jedoch noch weitere Shell-Versionen.

- **Bash (Bourne Again Shell):** Die am weitesten verbreitete Shell, welche Scripting, Kommando-Historie und Alias-Einstellungen unterstützt. Bei den meisten Linux-Distributionen ist sie als Standard-Shell bereits vorinstalliert.
- **Zsh (Z Shell):** Die Zsh ist eine überarbeitete Version der Bash und besitzt erweiterte Funktionen wie bessere Autovervollständigung und Plugin-Systeme. Sie besitzt ebenfalls mehr Anpassungsmöglichkeiten und ist in der Benutzung etwas anwenderfreundlicher. Die Befehle sind grösstenteils kompatibel zur Bash. Unter macOS kommt ebenfalls die Z Shell zum Einsatz.
- **Fish (Friendly Interactive Shell):** Die Fish hat einen klaren Fokus auf Benutzerfreundlichkeit. Sie besitzt eine verbesserte Syntaxhervorhebung und bietet Vorschläge für Befehle in Echtzeit. Zusätzlich ist die Scripting-Syntax intuitiver als bei anderen Shells.

Neben den oben genannten Shells existieren noch weitere, die jeweils ihre eigenen Vorzüge bieten. Wenn gewünscht oder erforderlich, können neben der Standard-Shell weitere Shells installiert werden. In der Benutzerkonfigurationsdatei kann jeweils festgelegt werden, bei welchem User welche Shell zum Einsatz kommt.

Aufgrund der grossen Verbreitung werden wir in den nächsten Kapiteln jeweils mit Bash arbeiten.

### Dateizugriff und Berechtigungen
Einzelne Objekte oder besser gesagt fast das komplette Betriebssystem bestehen bei Linux bekanntermaßen aus Dateien. Damit nicht jeder beliebige User jede beliebige Datei willkürlich bearbeiten oder unter Umständen die Systemstabilität gefährden kann, kommen mehrere Mechanismen zum Einsatz, welche unter anderem Linux den Ruf als sicheres Betriebssystem verschaffen. Einerseits gibt es sogenannte versteckte Dateien, diese sind jeweils am Punkt vor dem Dateinamen (z.B. .Testfile.txt) zu erkennen. Wenn man nun die Dateien in einem Verzeichnis mittels des Befehls im nachfolgenden Abschnitt auflisten lassen möchte, werden die versteckten Dateien nicht einfach so angezeigt. Um sie dennoch einsehen zu können, muss eine Option ausgewählt werden. Mehr dazu jedoch später, wenn wir auf den Befehl genauer eingehen.

Des Weiteren besitzt jede einzelne Datei eine individuelle Berechtigung. Um dies genauer erläutern zu können, kommen wir nun zum ersten CLI-Befehl in diesem Pocketguide. Damit wir die individuelle Berechtigung eines Files anzeigen können, lautet der Befehl `ls -l`. Dabei steht `ls` für list und wird verwendet, um die Dateien im aktuellen Verzeichnis anzuzeigen. Die Option `-l` gibt dem Befehl `ls` die Anweisung, die aufgelisteten Files im Langformat darzustellen. Ohne die Option `-l`, respektive die Anzeige im Langformat, würden wir die Berechtigungen nicht sehen können. Damit das Ganze nun etwas bildlicher vorgestellt werden kann, wechseln wir nun zu einem Code-Block:
```bash
walter@linux-server:~$ ls -l
total 4
-rwxr-xr-- 1 walter walter   95 Jul 23 21:35 Testfile1.txt
-rwxrwxr-x 1 walter white   165 Jul 23 21:37 Testfile2.txt
-r-xr--r-- 1 walter walter   14 Jul 23 21:41 Testfile3.txt
drwxr-xr-x 1 walter walter 4096 Jul 23 21:48 Testfolder
```
Die obige Darstellung mag auf den ersten Blick noch etwas unübersichtlich erscheinen. Wir werden die einzelnen Spalten jedoch im Kapitel Befehle noch genauer auseinandernehmen. Im Zusammenhang mit den Berechtigungen fokussieren wir uns in erster Linie beim `Testfile1.txt` auf die Spalten `-rwxr-xr--` und `walter walter`.

`-rwxr-xr--` stellt eine Kombination aus Dateityp und Berechtigungen dar und muss zum besseren Verständnis in einzelne Sektionen zerlegt werden, welche wie folgt aussehen: `- rwx r-x r--`. Der erste Bindestrich `-` deutet in diesem Fall darauf hin, dass es sich um eine einzelne Datei handelt. Würde es sich bei dem File um ein Verzeichnis handeln, wäre an dieser Stelle der Buchstabe `d` hinterlegt. Nach dem Bindestrich folgen die drei Berechtigungskategorien in jeweils einer Dreiergruppe. Am Beispiel vom `Testfile1.txt` wären dies `rwx` für den Benutzer, welcher die Datei zugewiesen ist. Die zweite Dreiergruppe `r-x` steht für die Gruppe, welche die Zuweisung erhalten hat. Die dritte Dreiergruppe `r--` steht für alle anderen, sprich alle, bei denen es sich weder um den Besitzer noch um Mitglieder der Gruppe der Datei handelt. Die Buchstabenkombinationen geben dabei Auskunft über die Art der Berechtigung.
| Buchstaben | Bedeutung | Beschreibung |
|:----------:|-----------|--------------|
| r | read | Leseberechtigung - Der Dateiinhalt kann angesehen, jedoch weder bearbeitet, gelöscht noch ausgeführt werden |
| w | write | Schreibberechtigung - Der Dateiinhalt kann bearbeitet und gelöscht werden.|
| x | execute | Ausführberechtigung - Die Datei kann ausgeführt werden. Dies spielt vor allem eine Rolle im Zusammenhang mit Programmen, Skripten und Verzeichnissen. Ohne die `x`-Berechtigung kann z.B. ein Ordner nicht geöffnet oder ein Programm oder Skript gestartet werden. |

Um nochmals auf das `Testfile1.txt` zurückzukommen: Der Benutzer der Datei kann den Text im File anzeigen lassen, diesen modifizieren oder die Datei selbst löschen. Die Gruppe und alle anderen hingegen, können die Datei nur lesen, jedoch keine Veränderungen vornehmen, geschweige denn die Datei löschen.

Beim `Testfile2.txt` mit der Berechtigung `-rwxrwxr-x` hingegen hat die Gruppe ebenfalls die Berechtigung, den Dateiinhalt abzuändern oder gar die Datei zu löschen.

Beim `Testfile3.txt` hat selbst der Besitzer der Datei keine Berechtigung, diese zu bearbeiten oder zu löschen.

Die Berechtigungen können mit dem später noch genauer vorgestellten Befehl `chmod` angepasst werden.

Nun haben wir über Besitzer und Gruppe gesprochen. Bei dem obigen Code-Block wird bei der Auflistung vom Verzeichnisinhalt bei fast allen Dateien `walter walter` angegeben. In diesem Fall handelt es sich beim ersten `walter` um den Besitzer. Wenn ich mit dem User Walter eingeloggt bin und die Datei erstelle, wird hier standardmäßig walter hinterlegt. Da ich als User walter gleichzeitig der Gruppe walter angehöre, steht das zweite `walter` für die Gruppe. Beachtet man nun das `Testfile2.txt`, ist zu erkennen, dass das Dokument im Besitz vom User `walter` ist, jedoch die Gruppenzuweisung auf `white` verweist. Somit haben alle Benutzer, die der Gruppe white zugewiesen sind, dieselben Zugriffsrechte wie der User walter. Der Besitzer oder die zugewiesene Gruppe können jeweils mit den Befehlen `chown` und/oder `chgrp` geändert werden.



## Kapitel 2: Installation und Konfiguration
Bei der Installation von Linux muss man sich nicht nur für eine der zahlreichen Distributionen entscheiden, teilweise wird einem auch noch auferlegt die Entscheidung zwischen einer Distribution mit oder ohne grafischer Oberfläche (GUI) auszuwählen. Wird auf ein Betriebssystem ohne GUI gesetzt, erfolgt die Ausgabe am Bildschirm in der sogenannten Kommandozeile (CLI). Dabei wird, mit Ausnahme von  Anzeigen von ASCII-Art, auf grafische Darstellungen verzichtet. Im ersten Moment kann dies abschreckend wirken (wie soll man das komplette Betriebssystem nur mit der Kommandozeile bedienen, könnte einem in den Sinn kommen). Stellt man sich jedoch vor, für Aussenstehende wie ein Hacker auszusehen, wirkt dies relativ motivierend und man macht schnell Fortschritte. Der Verzicht der grafischen Darstellungen bringt einige Vorteile mit sich. Die vorhandenen Ressourcen können so rechenintensiven Aufgaben zur Verfügung gestellt werden und müssen nicht für die Anzeige des GUIs zur Verfügung stehen. Ausserdem kann man einiges schneller im Betriebssystem navigieren. Nichts desto trotz ist bei den allermeisten Linux Distributionen mit grafischer Oberfläche selbstverständlich auch ein Terminal installiert, so hat man das Beste erlebnis aus beiden Welten, wenn auch nicht ganz den ressourcensparenden Effekt wie bei einer Version, welche nur über eine CLI verfügt. Ein wichtiger Hinweis noch vorab, das CLI bietet dem Benutzer die Möglichkeit mit dem System über Befehle zu interagieren. Das Programm welche die Befehle verarbeitet ist die sogenannte Shell. Hiervon gibt es unterschiedliche Versionen, welche jeweils eigene Vor- und Nachteile haben. Die am Häufigsten eingesetzte Shell ist dabei die sogenannte Bash (Bourne Again Shell).

Gerne möchte ich nachfolgend einige Möglichkeiten vorstellen, wie man Linux erleben und erlernen kann. Dabei gehe ich von der einfachsten zur schwierigsten Möglichkeit vor. Da ich mich persönlich mit Ubuntu am Besten auskenne, zeige ich die jeweiligen Installationstypen an Hand von Ubuntu auf. Jeder Distribution hat ihre Eigenheiten, im Grossen und Ganzen ist der Installationsablauf jedoch ähnlich.

### Express/Einfach:
Wer jetzt nicht länger warten möchte, dem Empfehle ich die Cloudvariante Linode von Akamai. Neben den vielen Cloudanbietern, welche heutzutage existieren, hat sich Linode auf das Deployment von Linux spezialisiert. Wer nun denkt, dass diese Variante mit hohen Kosten verbunden ist, den kann ich beruhigen. Man erhält ein Startguthaben in der Höhe von $100. Wenn dies aufgebraucht oder abgelaufen ist, belaufen sich die Kosten auf ca. $5 - $15 pro Monat, sofern man sich für eine ressourcensparende Variante entscheidet. Der einzige "Nachteil", wenn man ihn denn so nennen darf, ist dass lediglich Linux Distributionen mit CLI zur Verfügung stehen.
Zu Beginn muss man sich ein Konto einrichten (evtl. Kreditkarte???)
Die Verbindung mit der in der Cloud bereitgestellten Linux VM erfolgt folgendermassen:

### Einfach:
#### Windows:
Im Jahr 2016 unter Windows 10 hat Microsoft das sogenannte Windows-Subsystem für Linux (WSL) ins Leben gerufen.

##### macOS:
Da der Apple Kernel? auf dem Unix System basiert, ist bei den Geräten mit macOS bereits ein Terminal installiert. Als Shell kommt die so genannte Z shell (zsh) zum Einsatz diese ist jedoch (grösstenteils?) Kompatibel zu der am häufigsten eingesetzten Bash Shell, welche auf den meisten Linux Distributionen als Standard-Shell vorhanden ist. Unter macOS kann man auf Grund dessen im Betriebssystem gleich navigieren wie unter einer reinen Linux Installation.

### Mittel:
Mit etwas mehr Aufwand ist die Installation einer Virtuellen Maschine (VM), worauf dann eine Distribution der Wahl installiert werden kann. Bei einer VM kommt ein so genannter Hypervisor zum Einsatz. Dieser gaukelt dem zu installierenden System vor, ein eigener Computer mit eigener Hardware zu sein. Als VM-Software kann ich, nicht nur auf Grund der Open Source Natur der Anwendung, Oracle VM VirtualBox empfehlen. In erster Linie werden wir uns die Installation der VirtualBox anschauen. Im Anschluss erfolgt die Installation von Ubuntu auf der VirtualBox selbst.

### Schwierig:
Als letztes erfolgt eine Bare Metal ("blankes Metall"). Hierbei erfolgt die Installation des Linux Betriebssystem direkt auf der Hardware. Der Grundsätzliche Installationsprozess unterscheidet sich dabei nicht gross von der Installation auf einer VM. Dennoch gibt es die eine oder andere Eigenheit, welche es zu beachten gilt.

## Kapitel 3: Grundlegende Befehle und Navigation
Im nächsten Kapitel behandeln wir die Arbeit in der Kommandozeile. Als Shell kommt dabei Bash zum Einsatz. Eines vorweg, in der Linux CLI gibt es nicht den einen richtigen Weg um eine Aufgabe zu erledigen. Man kann jede Aufgabe auf gefühlt 1'000 unterschiedliche Arten erledigen und kommt dabei zu einem ähnlichen, wenn nicht gar identischen Ergebniss. Daher wird bei den nachfolgenden Befehlen jeweils versucht auch den einen oder anderen Alternativweg aufzuzeigen.

### Wichtiger Hinweis:
Das Betriebssystem Linux mit seinen sämtlichen Befehlen, ist was die Kommandozeile anbelangt Case Sensitive. Dies bedeutet, dass zwischen Gross- und Kleinschreibung unterschieden wird. Anders als unter Windows und macOS eventuell angewöhnt, kann es gerade z.B. bei der Suche nach einer Datei auf einem Linux-System dazuführen, dass man die Datei findet oder eben nicht. Daher meine Empfehlung, man sollte sich daran gewöhnen, dass alles klein geschrieben wird, ausser es sei z.B. in einem Skript notwendig die Ausgabe in Gross- und Kleinschreibung anzeigen zu lassen. Der Hinweis bezüglich der Case Sensitivity kommt an dieser Stelle, weil es bei den Befehlen (welche im Übrigen immer klein geschrieben werden), Optionen gibt, welche zu einem komplett anderen Ergebniss führen können, wenn man den jeweiligen Buchstaben klein oder gross schreibt.

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
## Kapitel 11: Weiterbildung und Zertifizierungen
## Glossar:
#### ASCII-Art:
#### Bootloader:
#### Kernel:
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