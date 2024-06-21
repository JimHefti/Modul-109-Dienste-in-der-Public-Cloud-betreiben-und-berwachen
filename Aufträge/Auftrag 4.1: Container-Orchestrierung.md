# Container-Orchestrierung

## Warum braucht man Container-Orchestrierung?
Mit der Container-Orchestrierung können Sie folgende Aufgaben automatisieren und verwalten:

1. Provisionierung und Deployment
2. Konfiguration und Planung 
3. Ressourcenzuweisung
4. Container-Verfügbarkeit 
5. Skalieren oder Entfernen von Containern, um Workloads gleichmäßig über Ihre Infrastruktur zu verteilen
6. Load Balancing und Traffic Routing 
7. Überwachen des Containerzustands
8. Konfigurieren von Anwendungen basierend auf dem Container, in dem sie ausgeführt werden
9. Sichern von Interaktionen zwischen Containern



## Wie funktioniert Container-Orchestrierung?
Wenn Sie ein Container-Orchestrierungs-Tool wie Kubernetes verwenden, beschreiben Sie die Konfiguration einer Anwendung in einer YAML- oder JSON-Datei. Die Konfigurationsdatei teilt dem Konfigurationsmanagement-Tool mit, wo sich die Container-Images befinden, wie ein Netzwerk eingerichtet wird und wo Protokolle gespeichert werden.

## Welche Container-Orchestrierung Technologien kennen Sie?


## Was versteht man unter "Scaling Containers"?

Stellen Sie sich vor, Sie haben eine Website, die in Containern läuft – das sind kleine Pakete, die alles enthalten, was die Website zum Funktionieren benötigt. Wenn nun plötzlich viele Leute gleichzeitig Ihre Website besuchen, brauchen Sie mehr von diesen Containern, damit die Website schnell bleibt und nicht abstürzt. Das Hinzufügen weiterer Container, um die Last zu bewältigen, nennt man "Scaling Out". Wenn weniger Besucher auf der Seite sind, können einige Container entfernt werden, was als "Scaling In" bezeichnet wird.


## Was gibt es für Deployment Strategien?


Rolling Deployment: 

Bei dieser Methode wird die neue Version der Anwendung schrittweise ausgerollt, wobei einzelne Instanzen der Anwendung nach und nach aktualisiert werden. Dies minimiert die Ausfallzeiten, da immer eine gewisse Anzahl von Instanzen in Betrieb bleibt.

Blue-Green Deployment: 

Hier werden zwei identische Produktionsumgebungen eingerichtet, die als "Blue" und "Green" bezeichnet werden. Zuerst wird die neue Version in der Green-Umgebung vollständig bereitgestellt und getestet. Wenn alles gut funktioniert, wird der Netzwerkverkehr von Blue zu Green umgeleitet. Falls Probleme auftreten, kann man schnell zur Blue-Umgebung zurückkehren.

Canary Deployment: 

Bei dieser Strategie wird die neue Version zunächst nur einer kleinen Gruppe von Nutzern zugänglich gemacht. Diese "Kanarienvögel" testen die neue Version unter realen Bedingungen. Wenn keine Probleme auftreten, wird die neue Version nach und nach für alle Nutzer freigegeben.

A/B Testing Deployment: 

Ähnlich wie beim Canary Deployment wird die neue Version bei dieser Strategie einer ausgewählten Nutzergruppe angeboten. Der Unterschied ist, dass A/B-Tests oft verwendet werden, um neue Funktionen oder Änderungen zu bewerten, indem man das Verhalten oder die Reaktion der Nutzer auf die Änderungen misst.

Recreate Deployment: 

Bei dieser Strategie wird die alte Version vollständig heruntergefahren, bevor die neue Version hochgefahren wird. Dies führt zu einer Ausfallzeit, bietet jedoch eine klare Trennung zwischen den Versionen, was in bestimmten Szenarien nützlich sein kann.

Dark Launching: 

Dabei werden neue Funktionen in der Produktionsumgebung versteckt ("im Dunkeln") bereitgestellt. Die Funktionen sind vorhanden, aber nur für das interne Team sichtbar, bis sie vollständig getestet sind und für alle Benutzer aktiviert werden.