---
marp: true
theme: ubuntu
author: Pascal Thong
lang: nl
paginate: true
size: 16:9
---

<!-- _class: title -->
<!-- _paginate: false -->

# Les 5: Softwarebeheer

Installeren, instellen, herstellen en opleveren.

Linux · Ubuntu · System Engineering

---

## Wat kun je na deze les?

- Software vinden en de bron herkennen.
- Een app installeren, controleren en verwijderen.
- Uitleggen wat `apt update` en `apt upgrade` doen.
- Een standaardapp kiezen en de bestandskoppeling testen.
- Een fout herstellen en je werk aantoonbaar opleveren.

---

<!-- _class: table -->

## Programma van vandaag

| Onderdeel                           | Richttijd |
| ----------------------------------- | --------- |
| Start, begrippen en softwarebronnen | 10 min    |
| App Center: voordoen en oefenen     | 15 min    |
| APT: voordoen en oefenen            | 25 min    |
| Standaardapps en bestandskoppeling  | 10 min    |
| Verwijderen en herstellen           | 15 min    |

---

<!-- _class: check -->

## Startklaar in je Ubuntu-VM

1. Log in met je eigen account met sudo-rechten.
2. Controleer in de browser of internet werkt.
3. Open de terminal met **Ctrl + Alt + T**.
4. Maak een werkmap voor deze les:

```bash
mkdir -p ~/les5
```

> installeren vraagt vaak beheerdersrechten;
> Maak gebruik van **sudo** om het als superuser uittevoeren.

---

## Waar komt de software vandaan?

Een **repository** is een softwarebron.

- Ubuntu levert ingestelde bronnen voor APT-pakketten.
- De pakketlijst vertelt welke versies beschikbaar zijn.
- Updates komen via de bijbehorende softwarebron.
- Een extra bron toevoegen betekent een extra partij vertrouwen.

**Vandaag:** Gaan we verschillende software installeren.

---

<!-- _class: table -->

## Packetmanagers die je tegenkomt

- App Center is een packetmanager

|             | APT                                              | Snap                                                                                       |
| ----------- | ------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| Bron        | APT-repositories                                 | Gewoonlijk de Snap Store                                                                   |
| Beheer      | `apt` in de terminal                             | App Center / `snap`                                                                        |
| Beveiliging | Software draait met de rechten van de applicatie | Software draait in een geïsoleerde sandbox ( beperkte toegang tot de rest van het systeem) |
| Updates     | APT / Software Updater                           | Gewoonlijk automatisch                                                                     |

> Er zijn vele verschillende package-managers.

---

<!-- _class: demo -->

## Demo: een app beoordelen

1. Open **App Center** via het app-overzicht.
2. Zoek **VLC**, een mediaspeler.
3. Bekijk de beschrijving, uitgever en pakketbron.
4. Kies bij een Snap het kanaal **stable**, als die keuze er is.

**Past deze app bij de vraag? Wie levert de software?**

---

<!-- _class: table -->

## Het apt packetmanager

| Commando                | Wat gebeurt er?                                     |
| ----------------------- | --------------------------------------------------- |
| `sudo apt update`       | Haalt de actuele pakketlijsten op.                  |
| `apt list --upgradable` | Toont pakketten waarvoor een upgrade klaarstaat.    |
| `sudo apt upgrade`      | Installeert beschikbare upgrades van APT-pakketten. |

**`update` installeert zelf geen nieuwe app-versies.**

`upgrade` is geen overstap naar een nieuwe Ubuntu-release.

<!-- Voer tijdens de demo update en list uit. Plan een volledige upgrade buiten het oefenblok wanneer die veel tijd vraagt. APT kan upgrades uitstellen, bijvoorbeeld door gefaseerde updates. Bron: https://manpages.ubuntu.com/manpages/focal/man8/apt.8.html -->

---

<!-- _class: demo -->

## Gedit controlleren, een grafische teksteditor

We willen **gedit**, een grafische teksteditor.

```bash
sudo apt update
apt show gedit
```

---

## Lees het installatievoorstel

```bash
sudo apt install gedit
```

- Welke pakketten worden **nieuw geïnstalleerd**?
- Hoeveel moet worden gedownload? Hoeveel ruimte is nodig?
- Worden er ook pakketten **verwijderd**?
- Begrijp je het voorstel? Bevestig met **J/y**, zoals gevraagd.

**Twijfel je? Kies `n` en bespreek de uitvoer.**

<!-- Gebruik in deze les geen -y: studenten moeten de voorgestelde wijzigingen lezen. Het sudo-wachtwoord toont geen tekens tijdens het typen. Zoeken en bekijken kan zonder sudo. -->

---

<!-- _class: work -->

## Opdracht 2: jij bent de beheerder

**Tijd: 12 minuten.**

1. Werk de pakketlijsten bij en zoek `gedit`.
2. Noteer de kandidaatversie en de APT-bron.
3. Installeer gedit en controleer pakket én programma.
4. Maak `~/les5/test.txt` met je naam en één testzin.
5. Sluit de editor en open het bestand opnieuw met gedit.

**Bewijs:** versie, gebruikte commando's en het bewaarde bestand.

<!-- Als gedit al geïnstalleerd is: noteer dit en voer dezelfde controles uit. Gebruik nano ~/les5/oplevering.md om notities te bewaren; Ctrl+O, Enter, Ctrl+X. -->

---

<!-- _class: section -->

# 3. Standaardapps

Welke app opent bij dubbelklikken?

---

## Eenmalig openen of standaard instellen?

- **Openen met:** kies een app voor dit bestand, deze keer.
- **Standaardapp:** de vaste keuze voor een bestandstype.
- Een **bestandstype** vertelt wat voor inhoud een bestand heeft.

Bijvoorbeeld: `text/plain` voor gewone tekstbestanden.
Een koppeling geldt vaak voor méér bestanden dan dit ene `.txt`-bestand.

> De koppeling verandert de appkeuze, niet de bestandsinhoud.

---

<!-- _class: demo -->

## Demo: tekstbestanden openen met gedit

1. Open **Bestanden** en ga naar je home-map → `les5`.
2. Dubbelklik op `test.txt`. Noteer de huidige app.
3. Rechtsklik → **Open with... **.
4. Kies gedit en stel die als standaard in.
5. Sluit de app en dubbelklik opnieuw op `test.txt`.

Soms staat de keuze onder **Eigenschappen → Openen met**.
Alleen eenmalig openen wijzigt de standaard niet altijd.

<!-- Benaming en plaats van de standaardkeuze verschillen per Ubuntu-/GNOME-versie. Controleer of de optie voor altijd gebruiken of standaard instellen actief is. Bron: https://help.ubuntu.com/stable/ubuntu-help/files-open.html.en -->

---

<!-- _class: section -->

# 4. Verwijderen en herstellen

Eerst begrijpen wat verandert. Daarna opnieuw testen.

---

<!-- _class: table -->

## App verwijderen?

| Handeling               | Wat verwijder je?                                 |
| ----------------------- | ------------------------------------------------- |
| `sudo apt remove gedit` | Het pakket; pakketconfiguratie kan blijven staan. |

---

## Verwijder via de juiste beheerroute

- Geïnstalleerd als **APT-pakket**? Gebruik `apt remove`.
- Geïnstalleerd via **App Center**? Open daar de app en kies verwijderen.
- Is de app een **Snap**? APT verwijdert die installatie niet.
- Verwijder geen programmamappen met `rm` als vervanging voor pakketbeheer.

---

<!-- _class: work -->

## Eindopdracht: ontdek je eigen apps

**Tijd: 25 minuten · Jij kiest wat je wilt uitproberen!**

1. Kies **twee apps** die je nog niet kent of hebt gebruikt.
2. Zoek ze via App Center of APT en bekijk de bron.
3. Installeer ze in je Ubuntu-VM. Kies zelf je installatieroute.
4. Probeer per app **minstens twee functies** uit.
5. Maak iets of voer een taak uit waarmee je de app test.

Laat het zien aan de docent.

<!-- Laat studenten zelf zoeken en kiezen. Een tekening maken, een geluidsbestand bewerken, een project opslaan of een spel spelen zijn mogelijke tests. Reserveer ongeveer 5 minuten voor kiezen, 15 voor installeren en ontdekken en 5 voor delen. -->

---

<!-- _class: check -->

## Laat zien wat je hebt ontdekt

Bewaar in `~/les5` per app een screenshot en een korte notitie:

- **Keuze:** hoe heet de app en waarom koos je deze?
- **Installatie:** welke bron en installatieroute gebruikte je?
- **Ervaring:** welke twee functies testte je? Wat vond je ervan?
- **Conclusie:** wil je de app houden? Waarom wel of niet?

**Deel met je buur:** demonstreer je favoriete ontdekking in één minuut.

Een app die je niet wilt houden, mag je weer verwijderen
via de bijbehorende pakketbeheerder.

---

## Naslag

- [Ubuntu: software installeren met App Center](https://help.ubuntu.com/stable/ubuntu-help/addremove-install.html)
- [Ubuntu: pakketbeheer met APT](https://ubuntu.com/server/docs/how-to/software/package-management/)
- [APT-handleiding: update, install, remove en purge](https://manpages.ubuntu.com/manpages/focal/man8/apt.8.html)
- [Ubuntu: bestanden openen en standaardapps kiezen](https://help.ubuntu.com/stable/ubuntu-help/files-open.html.en)
- [Ubuntu: apps verwijderen](https://help.ubuntu.com/stable/ubuntu-help/addremove-remove.html)

Op je eigen systeem: `man apt` — afsluiten met **q**.

---
