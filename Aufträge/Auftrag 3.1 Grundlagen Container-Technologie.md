# Grundlagen Container-Technologie

## Was ist Container-Technologie oder Container-Virtualisierung?
Container-Technologie hilft dabei, Apps so zu verpacken, dass sie überall gleich gut funktionieren, egal wo sie laufen. Man kann sich das vorstellen wie eine Art Box, in der alles, was die App zum Laufen braucht, sicher verstaut ist. Diese Boxen sind leicht und man kann sie schnell von einem Computer zum anderen verschieben. Das ist praktisch, weil man sich keine Sorgen machen muss, dass die App plötzlich nicht mehr richtig funktioniert, nur weil sie auf einem anderen Computer läuft.


### Vorteile von Containern gegenüber VMs:
Effizienz: 
Container benötigen weniger Ressourcen (wie CPU und Speicher) als VMs, weil sie das Betriebssystem des Hosts teilen und nicht jedes Mal ein eigenes Betriebssystem hochfahren müssen.

Schnellere Startzeiten: 
Container starten fast augenblicklich, weil sie nicht ein ganzes Betriebssystem booten müssen. VMs dagegen benötigen mehr Zeit, da sie ein vollständiges Betriebssystem laden.

Portabilität: 
Container enthalten alle Abhängigkeiten, die eine Anwendung benötigt. Dadurch lassen sie sich leicht von einer Umgebung in eine andere verschieben, ohne dass Konfigurationsprobleme auftreten.

Ressourcennutzung: 
Da Container direkt auf dem Host-Betriebssystem laufen, können sie effizienter mit Systemressourcen umgehen und diese bei Bedarf teilen.


### Nachteile von Containern gegenüber VMs:
Sicherheit: 
VMs bieten eine bessere Isolation, da jede VM ihr eigenes Betriebssystem hat. Bei Containern, die den Host-Kernel teilen, könnte ein kompromittierter Container theoretisch ein Sicherheitsrisiko für andere Container darstellen.

Kompatibilität: 
Container teilen sich den Kernel des Host-Betriebssystems, was bedeutet, dass ein Container nur auf Betriebssystemen laufen kann, die mit diesem Kernel kompatibel sind. VMs können dagegen verschiedene Betriebssysteme ausführen, unabhängig vom Host-System.

Vollständige Isolation: 
VMs sind komplett isoliert und betreiben ihre eigenen Kernels, was sie ideal für Anwendungen macht, die vollständige Isolation erfordern.

Verwaltung: 
VMs können einfacher zu verwalten sein, wenn es um sehr komplexe Netzwerk- oder Speicheranforderungen geht, da sie wie unabhängige Computer behandelt werden können.


## Welche Produkte kennen Sie im Zusammenhang mit virtuellen Servern und Container?
Ich kenne Docker wo man container darauf laufen lassen kann.
Ich kenne VM workstation wo man drauf VMs erstellen kann ich kenne ebenfalls Virtual Box und Proxmox.





## Wie unterscheiden sich die Technologien VM und Container in Bezug auf Bereitstellung, Speicherplatz, Portabilität, Effizienz und Betriebssystem (Kernel)?


 Bereitstellung:

VMs: 
Langsamer, da sie ein ganzes Betriebssystem starten müssen.

Container: 
Schneller, da sie direkt auf dem Betriebssystem des Hosts laufen.

Speicherplatz:

VMs: 
Benötigen mehr Speicherplatz, da sie ein komplettes Betriebssystem speichern.
Container: 
Effizienter im Speicherplatz, weil sie sich Teile des Betriebssystems mit dem Host teilen.

Portabilität:

VMs: 
Weniger portabel, abhängig von der Virtualisierungsplattform.
Container: 
Sehr portabel, leicht von einer Umgebung zur anderen zu bewegen.

Effizienz:

VMs: 
Verbrauchen mehr Ressourcen (CPU, Speicher).
Container: 
Effizienter, weil sie weniger Ressourcen benötigen.

Betriebssystem (Kernel):

VMs: 
Jede VM verwendet ihren eigenen Kernel.

Container: 
Teilen sich den Kernel des Host-Betriebssystems.





## Können virtuelle Server immer durch Container ersetzt werden?

Nein Grunde dafür:

Sicherheit:
Virtuelle Maschinen bieten eine vollständige Isolation mit eigenem Betriebssystem, was sie sicherer macht.

Betriebssystem-Vielfalt: 
VMs können unterschiedliche Betriebssysteme ausführen, während Container den Kernel des Host-Betriebssystems teilen müssen.

Legacy-Software: 
Alte Software, die spezielle Systemanforderungen hat, kann oft besser auf VMs laufen.

Ressourcenintensive Anwendungen: 
VMs können dedizierte Ressourcen nutzen, was sie für sehr anspruchsvolle Anwendungen geeigneter macht.

Compliance-Anforderungen:
Manche regulatorischen Vorgaben können leichter mit der strengeren Isolation von VMs erfüllt werden.








## Was ist unterschied zwischen Self-Managed und Fully Managed? Notieren Sie sich die wichtigsten Merkmale und diskutieren Sie die Ergebnisse in der Gruppe.