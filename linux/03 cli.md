---
marp: true
theme: ubuntu
author: Pascal Thong
paginate: true
size: 16:9
---

<!-- _class: title -->
<!-- _paginate: false -->

# Les 3: Werken met de CLI

Mappen en bestanden beheren in Ubuntu

Navigeren, kopiëren & bewerken ~~zoeken en werken met beheerdersrechten.~~

---

<!-- _class: table -->

## Programma van vandaag

| Onderdeel                    | Tijd       |
| ---------------------------- | ---------- |
| Inchecken & Terugblikken     | 15 minuten |
| Terminal short-cuts          | 1 minuut   |
| Bestanden en mappen kopieren | 28 minuten |
| Nano, vi & vim?!             | 32 minuten |
| Je eigen website ontwikkelen | 30 minuten |
| Afsluitingsopdracht          | 15 minuten |

> Start je geïnstalleerde Ubuntu-VM en log in met je eigen account.

---

## Wat ga je leren?

Na deze les kun je:

- Schakelen tussen de grafische omgeving en de tekstconsole;
- Je locatie bepalen en absolute en relatieve paden gebruiken;
- Bestanden en mappen kopiëren
- Tekstverwerken in de CLI
- Een programma installeren
- Je eigen website ontwikkelen

---

<!-- _class: table -->

## Terugblik: dit heb je al gedaan

Les 1: Ubuntu installeren
les 2: Ubuntu-instellingen bekijken en basiscommando's oefenen.

| Commando          | Wat doet het?                                    |
| ----------------- | ------------------------------------------------ |
| `cd` / `cd ..`    | Naar je persoonlijke map / één map omhoog.       |
| `cd /`            | Naar de hoofdmap van het bestandssysteem.        |
| `ls`              | De inhoud van een map tonen.                     |
| `ls -l` / `ls -1` | Details tonen / één naam per regel tonen.        |
| `mkdir naam`      | Een map maken.                                   |
| `touch naam.txt`  | Een leeg bestand maken als het nog niet bestaat. |

---

## Van GUI naar CLI, en weer terug

**GUI:** de grafische omgeving met vensters, knoppen en een muis.
**Terminal:** een CLI-venster waarin je opdrachten typt.
**TTY:** een afkorting van teletypewriter, waarmee je volledig over gaat naar de CLI

- **Ctrl + Alt + T:** opent een terminalvenster in de GUI.
- **Ctrl + Alt + F3:** schakelt naar een teletypewriter (TTY).
  **Ctrl + Alt + F2**.
- In de tekstconsole log je opnieuw in met je eigen account.
- Je grafische sessie blijft op de achtergrond draaien.

![tty](../assets/tty.png)

---

<!-- _class: demo -->

## Probeer het: de tekstconsole

1. Klik in je Ubuntu-VM en druk op **Ctrl + Alt + F3**.
2. Vul je gebruikersnaam in en druk op Enter.
3. Typ je wachtwoord en druk op Enter. Je ziet geen tekens.
4. Navigeer naar `Documents` met `cd`.
5. Maak een directory `huiswerk`.
6. Maak een bestand genaamd `mijn-configuratie.txt`
7. Typ `exit` om uit te loggen uit de tekstconsole.
8. Ga terug naar de GUI met **Ctrl + Alt + F2**.
9. Controleer of je directory en bestandje is aangemaakt.

---

## Waar ben ik? Gebruik pwd

`pwd` staat voor **print working directory**: toon de huidige map.

```bash
cd
pwd
```

Bijvoorbeeld: `/home/thong-thong`. Bij jou staat je eigen gebruikersnaam.

`ls` vertelt **wat er in een map staat**;
`pwd` vertelt **waar je bent**.

---

<!-- _class: table -->

## Paden: hoe wijs je een bestand en directories aan?

| Notatie      | Betekenis                   | Voorbeeld                        |
| ------------ | --------------------------- | -------------------------------- |
| Absoluut pad | Begint bij de hoofdmap `/`. | `/home/thong/Documents/huiswerk` |
| Relatief pad | Begint bij je huidige map.  | `huiswerk`                       |
| `~`          | Je eigen home-directory.    | `~/les3.txt`                     |
| `.`          | De huidige map.             | `.`                              |
| `..`         | De bovenliggende map.       | `cd ..`                          |

Linux maakt onderscheid tussen hoofdletters en kleine letters.

---

## Kopieren

### Synopsis

```bash
cp [options] ... SOURCE DESTINATION
```

```bash
cp -i note.txt ~/Documents
```

- `cp`: het commando - kopiëren
- `note.txt`: SOURCH: de bron, het bestand dat je kopieert.
- `~/Documents`: DESTINATION: het doel, het bestand waarin de kopie komt.

Wil je weten waar de -i voor staat? Voer de commando uit: `man cp`

Vermijd bestanden en directory namen met spaties.
Heb je ze? Zet dan namen met spaties tussen quotes:
`touch "mijn notities.txt"`.

---

<!-- _class: demo -->

## Bestanden kopiëren met cp (demo)

1. Bekijk het resultaat van de opdracht uit les 2.
2. Verplaats de gemaakte directories (en bestanden) naar ~/Documents

Het bronbestand blijft bestaan. Succesvol kopiëren geeft meestal geen uitvoer.

![mappenstructuur h:400](../assets/mappenstructuur.png)

---

## Voorkom onbedoeld overschrijven

Gewoon `cp` kan een bestaand doelbestand zonder vraag overschrijven.
Gebruik `-i` als je eerst een bevestiging wilt.

```bash
cp -i note.txt ~/Documents
```

`note.txt` bestaat al. Lees de vraag en antwoord **n** om de
bestaande kopie te behouden. of **y** om de kopie over te schrijven.

Controleer vóór het kopiëren altijd de bron en het doel.

---

## Een hele map kopiëren met cp -r

`-r` betekent **recursief**: kopieer de map met alle inhoud en submappen.

```bash
cp -r ~/documenten ~/backup
```

---

<!-- _class: work -->

## Bestanden kopiëren met cp (check)

1. Bekijk het resultaat van de opdracht uit les 2 of maak het opnieuw.
   ![mappenstructuur h:200](../assets/mappenstructuur.png)
2. Verplaats de gemaakte directories (en bestanden) naar ~/Documents
3. Verwijder de bestanden op `~/Desktop` met de commando `rm`
4. Kom je er niet uit probeer de handleiding te lezen via de commando `man rm`

> Noobs verwijderen de bestanden via de GUI.

---

## Nano

**Nano** is een teksteditor die je rechtstreeks in de terminal gebruikt.

- Je maakt en bewerkt tekstbestanden, zoals notities en configuraties.
- Je kunt meteen typen en met de pijltjestoetsen door de tekst bewegen.
- Onderaan staan de belangrijkste sneltoetsen in beeld.

**vi en vim** zijn andere teksteditors. In deze oefening gebruiken we Nano.

---

<!-- _class: demo -->

## Nano: een bestand openen of maken

1. Open met een text-bestand met `nano ~/Documents/notes/linux/week1.md`
2. Schrijf op wat je is bijgebleven vanuit les 1
3. Sla het op met ^o
4. Sluit het af met ^q
5. Bekijk je notitie met de commando `cat week1.md`
6. Herhaal stap 1 t/m 4 zelfstandig voor .../linux/week2.md
7. Maak een nieuw bestand genaamd `commandos.md`
8. Schrijf een lijst met commando's dat je kent en beschrijf de commando's. (hoe meer hoe beter).

- Bestaat het bestand al? Dan opent Nano de bestaande inhoud.
- Bestaat het nog niet? Dan begin je met een leeg bestand.

Het nieuwe bestand wordt pas op schijf aangemaakt als je het opslaat.

---

## Nano: opslaan en afsluiten

1. Druk op **Ctrl + O** om je tekst op te slaan.
2. Controleer de bestandsnaam en druk op **Enter** om te bevestigen.
3. Druk op **Ctrl + X** om Nano af te sluiten.

Onderaan in het programma staan shortcuts van het programma zoals
**`^O`** dat betekent **Ctrl + O**.

Sluit je af met niet-opgeslagen wijzigingen? Nano vraagt of je wilt opslaan.
Kies het antwoord dat onderaan staat en bevestig zo nodig de bestandsnaam.

**Ctrl + C** annuleert een vraag, bijvoorbeeld bij het opslaan.

---

<!-- _class: work -->

## Probeer het: je eigen Nano-notities

1. Open met Nano het bestand `~/les3/commandos.md`.
2. Schrijf een lijst met commando's dat je kent en beschrijf de commando's. (hoe meer hoe beter).
3. Opzoeken mag, maar je moet ze getest hebben.

---

# Nano, Vi & VIM

- Alle drie de cli-programma's zijn tekstbewerkers.
- **Nano** is de meest eenvoudige tekstbewerker en is in (bijna) alle linux distro's voorgeïnstalleerd.
- **Vi** is geadvanceerder, en is meestal voorgeïnstalleerd.
- **Vim** is het verbeterde versie en is niet altijd voorgeïnstalleerd

> het installeren doe je met de commando `sudo apt install vim`

---

## De twee modi's in Vim. (Het programma dat wij echt gaan leren)

- **Command modus**: dit is de commando modus. Je kunt commando's geven, zoals `i` of `insert` om tekst in te voegen of `:wq` om op te slaan en af te sluiten.
- **Insert modus**: in deze modus typ je tekst. Druk op **Esc** om terug te keren naar de command modus.

---

<!-- _class: demo -->

## Demonstratie: je eigen website gemaakt in vim

1. Installeer Vim met 'sudo apt install vim'
2. Open met Vim het bestand `website/index.html`.
3. Schrijf een website in html
4. Open je browser met `firefox index.html`.

```html
<html>
  <h1>Jouw naam</h1>
  <p>Korte beschrijving van jouw</p>
</html>
```

---

## De volgende commando's heb je nodig om in VIM te werken

| Commando     | Betekenis                                                                                      |
| ------------ | ---------------------------------------------------------------------------------------------- |
| `vim`        | Open een bestand in Vim, bijvoorbeeld `vim notities.txt`.                                      |
| `i`          | Ga naar de insert-modus en voeg tekst in vóór de cursor.                                       |
| `<ins>`      | Ga naar de insert-modus; met Insert wissel je tussen invoegen en overschrijven.                |
| `<esc>`      | Verlaat de insert-modus en ga terug naar de command-modus.                                     |
| `:wq!`       | Sla het bestand op en sluit Vim af; `!` forceert dit waar nodig.                               |
| `:q`         | Sluit Vim af zonder wijzigingen op te slaan.                                                   |
| `dd`         | Verwijder de huidige regel.                                                                    |
| `yy`         | Kopieer de huidige regel.                                                                      |
| `p`          | Plak de gekopieerde of verwijderde tekst na de cursor.                                         |
| `g`          | Begin van een combinatiecommando, bijvoorbeeld `gg` om naar het begin van het bestand te gaan. |
| `G`          | Ga naar het einde van het bestand.                                                             |
| `v`          | Selecteer tekst met Visual-modus.                                                              |
| `/zoekwoord` | Zoek naar `zoekwoord` in het bestand.                                                          |
| `n`          | Ga naar het volgende zoekresultaat.                                                            |

---

<!-- _class: work -->

## Maak je eigen website

1. Installeer Vim met 'sudo apt install vim'
2. Open met Vim het bestand `website/index.html`.
3. Schrijf een website in html
4. Open je browser met `firefox index.html`.

---

# Terugblik

Maak een nieuw bestand aan week3.md en schrijf daar op wat er in deze les is behandeld.

Noem iets op wat je vandaag hebt geleerd.
Hoe gevarieerder, hoe beter! :)

---
