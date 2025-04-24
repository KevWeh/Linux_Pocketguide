| Verzeichnis | Zweck/Funktion | Sicherheitsaspekte | Typische Inhalte | Backup-Relevanz | Besonderheiten Debian/Ubuntu |
|-------------|----------------|---------------------|------------------|------------------|------------------------------|
| `/bin` | Essenzielle Binärdateien für Systemstart und Single-User-Modus | Nur root darf schreiben; andere dürfen lesen und ausführen | Shells (`bash`, `sh`), grundlegende Tools (`cp`, `mv`, `ls`) | **Hoch**, falls nicht `/usr/bin` | Ab Debian 10 / Ubuntu 20.04 meist Symlink auf `/usr/bin` |
| `/boot` | Enthält Bootloader, Kernel & Initial-Ramdisk | Schreibgeschützt für normale User; root benötigt Schreibrechte | `vmlinuz`, `initrd.img`, `grub/` | **Sehr hoch**, besonders für Kernel-Wiederherstellung | Eigene Partition empfohlen bei Verschlüsselung |
| `/dev` | Gerätedateien – Interface zur Hardware | Verwaltet durch `udev`; restriktive Rechte für Gerätezugriffe | `/dev/sda`, `/dev/null`, `/dev/tty`, etc. | **Gering** – Inhalte werden beim Booten neu erzeugt | Dynamisch durch Kernel und `udev` |
| `/etc` | Systemweite Konfigurationsdateien | Nur root darf schreiben; lesbar für Benutzer (mit Einschränkungen) | `fstab`, `hosts`, `passwd`, `network/interfaces` | **Sehr hoch**, zentrale Konfiguration | Unterschiede bei Konfig-Dateien je nach Init-System (Systemd vs. SysVinit) |
| `/home` | Benutzerverzeichnisse | Nutzer haben nur Zugriff auf ihr eigenes Home | `.bashrc`, `Downloads/`, `Documents/` etc. | **Sehr hoch**, enthält persönliche Daten | Kann auf separater Partition liegen |
| `/lib`, `/lib64` | Shared Libraries für `/bin` & `/sbin` | Nur root darf schreiben; andere lesen | Bibliotheken, Kernel-Module (`modules/`) | **Moderat**, rekonstruktierbar aus Paketen | Seit „merged /usr“ oft Symlink auf `/usr/lib` |
| `/media` | Automount für externe Datenträger | Zugriff je nach Mount-Optionen (z. B. via `udisks`) | USB-Sticks, externe Festplatten | **Gering**, temporäre Inhalte | Mountpunkt durch Desktop-Umgebung verwaltet |
| `/mnt` | Temporäre Mountpunkte | Nur root darf schreiben | Beliebig – z. B. zum Test-Mounten | **Gering** | Für Admin-Zwecke, keine automatische Nutzung |
| `/opt` | Drittanbieter-Software | Nur root darf schreiben | Software außerhalb Paketverwaltung | **Optional**, je nach Nutzung | Häufig leer in Minimal-Installationen |
| `/proc` | Virtuelles Dateisystem für Kernel/Prozesse | Dynamisch erzeugt; nur lesbar | `/proc/cpuinfo`, `/proc/meminfo`, `/proc/PID/` | **Keine**, Inhalte flüchtig | Vom Kernel verwaltet, wichtig für Debugging |
| `/root` | Heimatverzeichnis des root-Users | Nur root darf lesen/schreiben | `.bashrc`, systemweite Skripte | **Hoch**, für Wiederherstellung nützlich | Separate Beachtung bei Backups nötig |
| `/run` | Laufzeitdaten nach Boot | Flüchtig, nur root vollzugriffsberechtigt | PID-Dateien, Sockets, `systemd`-Runtime | **Gering**, wird beim Booten neu aufgebaut | Ersetzt `/var/run`; wichtig für Systemdienste |
| `/sbin` | Systemadministrative Tools | Nur root darf schreiben; Ausführung durch root oder sudo | `fsck`, `mount`, `reboot` | **Moderat**, bei Systemreparatur relevant | Symlink auf `/usr/sbin` (merged layout) |
| `/srv` | Daten für angebotene Dienste (z. B. Webserver) | Konfigurierbar je Dienst; root Eigentümer | `/srv/www`, `/srv/ftp` | **Hoch**, wenn Dienste aktiv | Nutzung optional; nicht immer vorkonfiguriert |
| `/sys` | Virtuelles Dateisystem für Kernel/Hardware | Nur root darf schreiben; viele lesbare Infos | `/sys/class/`, `/sys/block/`, Geräte-Infos | **Keine**, wird dynamisch erstellt | Wichtig für `udev`, Power-Management |
| `/tmp` | Temporäre Dateien | Schreibbar für alle (`1777` Sticky-Bit) | `.X0-lock`, temporäre Session-Dateien | **Gering**, Inhalte bei Reboot verloren | Bei sensiblen Systemen per `tmpfs` im RAM |
| `/usr` | Programme, Bibliotheken, Dokumentation (nicht essentiell fürs Booten) | Nur root darf schreiben | `/usr/bin`, `/usr/lib`, `/usr/share` | **Hoch**, außer bei vollständigem Reinstall | Merged Layout: viele Symlinks aus `/bin`, `/sbin`, etc. |
| `/var` | Variable Daten: Logs, Mail, Cache, Spools | Differenziert – `/var/log` nur für root beschreibbar | `/var/log`, `/var/cache`, `/var/lib`, `/var/spool` | **Sehr hoch**, speziell für Logs & Datenbanken | Wichtig bei Log-Rotation, Datenbankzustand, Spools |

### 📌 Anmerkungen & Hinweise
1️⃣ **Backup-Tipp:** Verzeichnisse wie `/proc`, `/sys`, `/run`, `/dev` sollten **nicht** mitgesichert werden – sie enthalten flüchtige oder systemgenerierte Inhalte.
2️⃣ **Sicherheits-Tipp:** `/tmp` und `/var/tmp` sollten mit **noexec**, **nosuid**, und ggf. **nodev** gemountet werden, um Skript-Exploits zu verhindern.
3️⃣ **Distributionen:** Debian ist konservativer bzgl. Systemd-Einsatz und Konfigurationslayout. Ubuntu nutzt zusätzlich eigene Strukturen wie Snap (`/var/lib/snapd/`, `/snap`).

