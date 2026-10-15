# Puddle

Eine Pixel-Art-Selbstfürsorge-App: Aufgaben erledigen, Stimmung eintragen, Puddle auf Reisen schicken, Wesen, Farben,
Zubehör, Welten und Deko freischalten, Mini-Haustiere finden, Tagebuch führen, atmen. Dazu ein **Multiplayer** mit Freunden.

## Multiplayer

Der Multiplayer läuft **direkt zwischen den Browsern** (WebRTC über [PeerJS](https://peerjs.com)).
Du brauchst dafür keinen eigenen Server und keine Zugangsdaten.

- **Hosten:** *Freunde -> Raum hosten* erzeugt einen 6-stelligen Code.
- **Beitreten:** Code eingeben und *Beitreten* drücken, oder den Link öffnen, den *Link kopieren* erzeugt (`...#raum=CODE`).
- **Im Raum:** Mitspieler erscheinen live als kleine Pixel-Wesen auf deinem Platz. Tippst du auf deine Szene, winkst du allen.
- **Freunde:** In der Liste mit einem Tipp befreunden (der Freundes-Status bleibt in deinem Browser gespeichert), den Freund besuchen
  (du siehst sein Puddle, seine Welt, Deko und Mini-Haustiere) oder ein Geschenk schicken (+3 Tropfen).
- **Gemeinsames Tagesziel:** Die erledigten Aufgaben aller Freunde im Raum zählen zusammen.

### Gut zu wissen

- Der **Host** vermittelt die Verbindungen. Sein Tab muss **offen** bleiben, sonst bricht der Raum ab.
- Geht der Host weg, bekommen die Gäste die Meldung "Der Host hat den Raum verlassen". Das eigene Spiel bleibt unberührt.
- Der Spielstand liegt im `localStorage` deines Browsers und wird nicht synchronisiert. Geteilt werden nur Aussehen, Name, Level, Deko und Fortschritt des Tagesziels.
- Die Verbindung wird über den kostenlosen öffentlichen PeerJS-Server vermittelt. In strengen Firmen- oder Schulnetzen kann sie scheitern.
- Bei WebRTC sehen die Mitspieler technisch die IP-Adressen der anderen. Gib den Code nur an Leute, denen du vertraust.

## Technik

- Reines HTML, CSS und JavaScript, alle Grafiken sind Text-Sprites, gezeichnet auf einem Canvas.
- Externe Abhängigkeiten: PeerJS 1.5.4 (über jsDelivr) und die Schrift "Pixelify Sans" (Google Fonts). PeerJS: MIT-Lizenz.
