# Linux
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
Besten Dank für dein Interesse an diesem Cheatbook. Mein Name ist Kevin und der Einfachheit halber verwende ich die Du-Form. Als grosser Fan von Linux, Open Source Projekten und Werken, die das nötige Wissen kurz und bündig vermitteln, ist es mir ein Anliegen, selbst ein solches Handbuch zu verfassen und auf GitHub zur Verfügung zu stellen.
Ich selbst erhebe nicht den Anspruch darauf ein Linux-Profi zu sein (hoffe es aber im Laufe des Schreibens zu werden), also verzeiht mir den einen oder anderen Fehler, der mir unterlaufen wird.
Viel Spass beim Lesen, Nachmachen und Lernen.

## Kapitel 0: Open Source
***Offenheit - Transparenz - gemeinschaftliche Zusammenarbeit*** oder in den Worten des Linux-Kernel-Entwicklers:
> **"Software is like sex: it's better when it's free."**
> 
> *- Linus Torvalds*

Da in vielen Linux-Lehrbüchern das Thema Open Source meiner Meinung nach zu wenig thematisiert wird, möchte ich es an dieser Stelle besser machen und der doch sehr relevanten Angelegenheit das Kapitel 0 widmen.

### Was bedeuted Open Source?
Wenn man den Begriff Open Source hört, kommen einem häufig die Begriffe freie/kostenlose Software und Linux in den Sinn. Dies ist insofern korrekt, da Open Source Software in der Regel kostenlos und Linux ein Open-Source-Projekt ist. Der eigentliche Gedanke hinter Open Source geht jedoch viel tiefer und bezieht sich darauf, dass der Quellcode der entsprechenden Software frei zugänglich ist, von der Öffentlichkeit eingesehen und je nach Art der [Lizenzierung](#lizenzen) modifiziert und weiterverbreitet werden kann.

Dies bringt einige Vorteile mit sich, die bei Closed Source Software (das Gegenteil von Open Source – der Quellcode ist nicht öffentlich zugänglich) nicht existieren:
- **Transparenz:** Da der Code öffentlich zugänglich ist und überprüft werden kann, lässt sich sicherstellen, dass keine versteckten Funktionen und Tracking-Mechanismen vorhanden sind. Potenzielle Fehler oder Schwachstellen können schneller entdeckt werden, was wiederum zur allgemeinen Qualitätssicherung beiträgt.
- **Sicherheit:** Dadurch, dass der Code von der breiten Masse eingesehen werden kann, können bei einer aktiven Community Sicherheitslücken schneller entdeckt und durch gemeinschaftliche Zusammenarbeit beseitigt werden.
- **Kostenersparnis:** Open-Source-Software ist in der Regel kostenlos, wodurch teils hohe Lizenzkosten vermieden werden. Dies ist auch einer der Gründe, weshalb Linux so verbreitet ist und weltweit auf so vielen Servern zum Einsatz kommt. Je nach Anwendung oder Betriebssystem muss jedoch berücksichtigt werden, dass dennoch Kosten für Implementierung, Anpassungen, Schulungen und Support anfallen können.
- **Flexibilität:** Die Benutzer können, entsprechende technische Fähigkeiten und Ressourcen vorausgesetzt, die Software auf ihre eigenen Anwendungsfälle anpassen, optimieren und weiterentwickeln.

Open Source beschränkt sich dabei nicht ausschliesslich auf Software. In den folgenden Bereichen findet der Ansatz ebenfalls seine Anwendung:
| Bezeichnung          | Erklärung                                                         | Beispiele                                           |
|----------------------|-------------------------------------------------------------------|-----------------------------------------------------|
| Open Content         | Inhalte zur kostenlosen Nutzung und Weiterverbreitung.            | Wikipedia, Internet Archive, OpenStreetMap          |
| Open-Source-Hardware | Öffentlich einsehbare Baupläne für Hardwareprojekte.              | Arduino, RISC-V, Tinkerforge                        |
| Open Access          | Öffentlicher Zugang zu wissenschaftlicher Literatur im Internet.  | arXiv, PubMed Central, Directory of Open Access Journals (DOAJ) |

Die Open Source Bewegung hat ihre Upsrünge in der Do-it-yourself-Bewegung, die nach dem Ersten Weltkrieg ihren Aufschwung erlebte, ebenfalls dazu beigetragen hat die Hacker-Bewegungen der 1960er/1970er Jahre und die Freie-Software-Bewegung der 1980er Jahre, aus welcher das [GNU-Projekt](#gnu-projekt) entstanden ist.

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





## Kapitel 1: Einführung in Linux
## Kapitel 2: Installation und Konfiguration
## Kapitel 3: Grundlegende Befehle und Navigation
## Kapitel 4: Benutzer- und Rechteverwaltung
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
