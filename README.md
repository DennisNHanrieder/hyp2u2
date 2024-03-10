# Übung 2 – Objektorientiertes PHP

HYP2UE_T1 Hypermedia 2 Serverseitige Programmierung | 11.03.2024 | Wolfgang Hochleitner | Code-along

Diese Übung markiert den Start zur objektorientierten Entwicklung mit PHP. In einer code-along Session sollen die wichtigsten Aspekte der Objektorientierung in PHP selbst ausprobiert werden.

## Der Startercode

Im Repository sind zwei Dateien bereits vorgegeben:

- `HYP2UE02/Vehicle.php`: Diese Datei enthält eine noch leere Definition für die Klasse `Vehicle`. Sie befindet sich im Namespace `HYP2UE02` und ist daher auch im gleichnamigen Unterordner abgelegt.
- `index.php`: Die Hauptdatei. Sie wird vom Browser aufgerufen und legt Objekte wie `Vehicle` (und noch andere) an.

Es ist in PHP üblich, zwischen aufgerufenen und inkludierte Dateien zu unterscheiden. Erstere sind in der Regel kleingeschrieben, während Klassen, die nicht direkt aufgerufen werden sollen, groß, d.h. in CamelCase geschrieben sind.

Dateien, die aufgerufen werden, erzeugen auch die Ausgabe, während einzubindende Dateien nur Dinge definieren, d.h. beim Aufruf "weiß bleiben" (also keine Ausgabe erzeugen).

## Ablauf des Beispiels

Dieses Beispiel behandelt die wichtigsten objektorientierten Themengebiete:

### Klassen und Objekte

- Vervollständigen Sie die Klasse Vehikel mit Eigenschaften und Methoden.
- Experimentieren Sie mit verschiedenen Sichtbarkeiten für Eigenschaften (`public`, `protected` und `private`).
- Legen Sie Objekte an.
- Greifen Sie auf Eigenschaften zu.
- Rufen Sie Methoden auf.
- Legen Sie eine statische Variable an und greifen Sie darauf zu.
- Legen Sie eine statische Funktion an und rufen Sie diese auf.
- Legen Sie eine Konstante an und greifen Sie auf diese zu.
- Legen Sie eine readonly Eigenschaft an und greifen Sie auf diese zu.

### Interfaces

- Definieren Sie ein Interface `Movable` mit einer Methode `move()`.
- Weisen Sie das Interface der Klasse `Vehicle` zu.
- Passen Sie die Klasse `Vehicle` so an, dass sie dem Interface entspricht.
- Legen Sie eine Klasse `Robot` an, die ebenfalls das Interface `Moveable` implementiert und erzeugen Sie ein Objekt davon.
- Erstellen Sie ein Array mit den zwei `Vehicle`- und der `Robot`-Instanz, sowie Zahlen und String-Werten.
- Iterieren Sie in einer Schleife über das Array und testen Sie mit `instanceof` ab, ob es sich um eine `Movable`-Instanz handelt. Wenn ja, rufen Sie `move()` auf.

### Vererbung und abstrakte Klassen

- Erzeugen Sie eine Klasse `Car`, die von `Vehicle` erbt.
- Erstellen Sie einen Konstruktor, der den Elternkonstruktor aufruft.
- Legen Sie eine `Car`-Instanz an und geben Sie im Konstruktor die Eigenschaften von `Vehicle` aus, um die Auswirkungen der Sichtbarkeit zu testen.
- Machen Sie `Vehicle` abstrakt und definieren Sie eine abstrakte Methode `start()`.
- `Vehicle`-Objekte können nun nicht mehr instanziiert werden, zudem muss `Car` nun die abstrakte Methode implementieren.

### Traits und Enums

- Erstellen Sie den Trait `Beep` mit der Methode `beep()`.
- Binden Sie den Trait in der Klasse `Robot` ein und rufen Sie `beep()` beim `Robot`-Objekt auf.
- Machen Sie dasselbe beim `Car`-Objekt.
- Erstellen Sie einen Enum `Color`, der die Farben "Red", "Green" und "Blue" enthält.
- Tauschen Sie den Parameter `$color` bei `Vehicle` und `Car` von `string` auf `Color` und passen Sie die Aufrufe an.

## Tipps und Richtlinien

- Verwenden Sie eine IDE, die für die Verwendung mit PHP konzipiert wurde (z.B. PhpStorm). Dies erleichtert Ihnen die Arbeit ungemein, wenn neue Klassen angelegt, Namespaces hinzugefügt oder Dateien eingebunden werden.
- Bei Fragen oder Problemen zur Aufgabe eröffnen Sie ein Issue in ihrem Repository.
