# VHS Hacking Workshop Tools
Official Repo of the Hacking Course at VHS by Benjamin Koltermann

## Download der Dateien
Zum Download der Dateien folges Kommando in das Kali Linux Terminal eingeben oder kopieren:
```
git clone https://github.com/p4ck3t0/vhs_hacking_workshop.git
```
Nun sollte mit
```
ls
```
der Ordner vhs_hacking_workshop erschienen sein. Mit dem Kommando
```
cd vhs_hacking_workshop
```
wechselt man in diesen Ordner. Hier liegen nun alle Dateien, die wir im Lehrgang benutzt haben.

## Der TCP Ordner
Im Ordner TCP befinden sich die beiden C Programme TCP_client.c und TCP_listener.c welche wir mit dem Kommando
```
ls
```
sehen können. Der listener stellt den Server da und der Client den Client mit dem wir uns auf dem Server verbinden. Das heißt zuerst muss der Server gestartet werden. Hierzu müssen wir die Datei TCP_listener.c zuerst mit der richtigen IP-Adresse configurieren. Mit
```
nano TCP_listener.c
```
können wir die Datei TCP_listener.c bearbeiten und die IP-Adresse anpassen. Diese finden wir etwas weiter unten in der Datei. Speichern können wir indem wir <STR + x> drücken. Anschließend müssen wir die TCP_listener.c Datei noch Compilieren (Ausführbar machen). Hierfür benutzten wir den GNU Compiler mit dem Kommando
```
gcc TCP_listener.c -o Server
```
Jetzt sollte mit ls eine Datei mit dem Namen Server in dem Ordner vorhanden sein. diese können wir mit
```
./Server
```
starten. Anschließend müssen wir den Client noch konfigurieren. Hierzu müssen wir die obigen Schritte wiederholen, und den listener in client ändern.

## Der Exploit_tool Ordner
Im Ordner Exploit_tool befindet sich die Instalationsdatei install_fatrat.sh. Diese Datei dient dazu das Exploit Tool zu Instalieren. Zuerst mussen wir die Datei install_fatrat.sh ausführbar machen. Das Kommando lautet
```
chmod +x install_fatrat.sh
```
Hiernach sollte mit
```
ls
```
eine grüne Datei install_fatrat.sh zu sehen sein. Diese können wir mit dem Befehl
```
./install_fatrat.sh
```
starten. Nun läuft die Instalation. Während der instalation kann es sein, dass noch ein paar Tasten gedrückt werden müssen. Dazu
lesen wir das, was das Terminal uns ausgibt.Hier müssen Sie leider selber entscheiden. Sollten Fehler auftreten, dann ist Google der beste Freund oder die Whatsapp Gruppe oder Die Issues Section von diesem Github Projekt. Nach erfolreicher instalation müssen wir in den neuen Ordner wechslen
```
cd TheFatRat
```
Anschließend können wir mit
```
./fatrat
```
Unser Exploit-Tool starten. Das weitere Vorgehen steht in der Facharbeit. Die von uns genutzte Zahlenkombination lautete:
* 6
* 2
* Dann nur noch die IP, Port Name und die Payload (windows/meterpreter/reverse_tcp)

## Wichtige Kommandos
* cd - in ein Verzeichnis wechslen
* nano - Datei bearbeiten/erstellen
* ls - Dateien im aktuellen Ordner auflisten
* mkdir - Verzeichnis erstellen
* ./Dateiname - Datei starten
* ip addr - IP-Configuration einsehen
* wireshark - wireshark starten
* arpspoof -t Client-IP Gateway-IP
* arpspoof -t Gateway-IP Client-IP
