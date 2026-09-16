---
marp: true
theme: ubuntu
author: Pascal Thong
paginate: true
size: 16:9
---

<!-- Kopieer dit bestand voor een nieuwe les en vervang de voorbeeldinhoud.
Elke --- begint een nieuwe dia. _class geldt alleen voor de huidige dia.
Opmaak staat in ../theme/ubuntu.css; inline CSS is niet nodig.
Afbeeldingspaden zijn relatief aan dit Markdown-bestand. -->

<!-- _class: title -->
<!-- _paginate: false -->

# Linux: Orientatie

Les 02 - Wegwijs, basisinstellingen en systeemidentiteit

---

# Overzicht

<style scoped>
table { width: 100%; table-layout: fixed; font-size: 20px; line-height: 1.3; border-collapse: collapse; }
th, td { padding: 9px 12px; text-align: left; vertical-align: top; border-bottom: 1px solid #dedede; }
th { color: #77216f; }
th:first-child, td:first-child { width: 5%; }
th:nth-child(2), td:nth-child(2) { width: 35%; }
</style>

| Les | Kern                                              | Inhoud                                                                                             |
| --- | ------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| 1   | VMware voorbereiden en Ubuntu installeren         | Voorbereiding, ISO, virtuele hardware, installatie en zelfstandig starten.                         |
| 2   | Wegwijs, basisinstellingen en systeemidentiteit   | Oriëntatie, veilige CLI, hostnaam, gebruiker, home en basisconfiguratie.                           |
| 3   | Bestanden, directories, paden en basiscommando's  | GUI-bestandsbeheer, absolute/relatieve paden en veilige terminalroute.                             |
| 4   | Gebruikers, groepen en minimale rechten           | Users, groups, root, sudo, home-directories en authenticatie/autorisatie.                          |
| 5   | Software, standaardapps en systematisch opleveren | App Center, repositories, apt, installatie/verwijdering, bestandskoppeling, herstel en overdracht. |
| 6   | Integrale praktijktoets                           | Zelfstandig inrichten, controleren, herstellen en opleveren.                                       |

---

# Programma van vandaag

- Ubuntu goed geinstalleerd?
- Orienteren in GUI & CLI
- Secure werken volgens een systeem configuratie kaart

---

## Wat ga je leren?

- Met ctrl + alt T kan je de terminal openen.
- sudo hostnamectl set-hostname nieuwe-hostnaam
- ai-prompts.png

- ik wil de scroll neutraal. Naar beneden scrollen is ook echt naar beneden.
- ik wil dat de scrollbar altijd zichtbaar is.
- Ik wil mijn cursor extra groot
- ik wil een achtergrond met een inspirerende quote.

---

<!-- _class: section -->

# 3 type studenten

- 3 type studenten

---

<!-- _class: gallery -->

## Installatiecontrole

![Goed: Ubuntu toont het aanmeldscherm met je eigen account](../assets/good-install.png) ![Niet goed: Ubuntu toont opnieuw het installatieprogramma](../assets/bad-install.png)

<!-- Vraag studenten hun virtuele machine te starten en hun scherm te vergelijken.
Links: het aanmeldscherm met een eigen account. Laat studenten inloggen.
Rechts: het installatieprogramma met de taalkeuze. Controleer of de installatie
is afgerond en of de virtuele machine vanaf de virtuele schijf start. -->

---

### Stappen

1. Start Ubuntu en controleer of het bureaublad volledig laadt.
2. Open de terminal met Ctrl + Alt + T.
3. Controleer of er geen foutmeldingen verschijnen tijdens het opstarten.
4. Test een herstart en controleer of alles weer normaal opstart.
5. Controleer tijd, netwerk en pakketupdates om de installatie te beoordelen.

---

## Voorbeeldtheorie: wat is Ubuntu?

**Linux** is de kernel: de kern die de hardware en systeemprocessen beheert.

Een **distributie** combineert deze kernel met programma's en hulpmiddelen tot een bruikbaar besturingssysteem. Ubuntu is daar een voorbeeld van.

> Onthoud: de kernel vormt de basis; de distributie levert het complete pakket.

---

<!-- _class: table -->

## Overzicht

| Begrip         | Betekenis                              | Voorbeeld       |
| -------------- | -------------------------------------- | --------------- |
| Distributie    | Linux met programma's en hulpmiddelen  | Ubuntu          |
| Directory      | Een map met bestanden of andere mappen | `/home`         |
| Home-directory | Persoonlijke map van een gebruiker     | `/home/student` |
| Terminal       | Venster waarin je commando's invoert   | `pwd` uitvoeren |

---

<!-- _class: demo -->

## Stappenplan: verken je home-directory

1. Open de terminal.
2. Typ `cd ~` en druk op Enter.
3. Toon je huidige locatie met `pwd`.
4. Bekijk de inhoud met `ls`.
5. Vergelijk de uitvoer met de bestandsbeheerder.

---

<!-- _class: terminal -->

## Voorbeeldcommando's

```bash
# Ga naar je persoonlijke map
cd ~

# Toon de huidige locatie en de inhoud
pwd
ls
```

Welke directories herken je in de uitvoer?

---

## Theorie met een afbeelding

![bg right:35% contain](../assets/ubuntu.webp)

Ubuntu is een Linuxdistributie waarmee we tijdens deze lessen oefenen.

- Een grafische omgeving voor dagelijks gebruik.
- Een terminal voor commando's.
- Een pakketbeheerder voor software.

---

<!-- _class: gallery -->

## Lesmateriaal: meerdere afbeeldingen

<!-- Plaats de afbeeldingen op één regel, zonder lege regels ertussen. -->

![Linuxboek](../assets/linuxboek.png) ![Hoofdstukken van het boek](<../assets/hoofdstukken boek.png>) ![Studentenwerkboekjes](<../assets/studenten werkboekjes.png>)

---

<!-- _paginate: false -->

<!-- Voor een afbeelding over de hele dia: bg contain behoudt de hele afbeelding. -->

![bg contain](../assets/waarom-linux.png)

---

<!-- _class: work -->

## Zelf aan de slag

**Opdracht:** verken je persoonlijke map.

1. Open je home-directory in de bestandsbeheerder.
2. Open dezelfde directory in de terminal.
3. Noteer drie directories die je op beide plekken ziet.

**Opleveren:** een screenshot van de terminal met een korte toelichting.

**Tijd:** 10 minuten.

---

<!-- _class: recap -->

## Terugblik

- Wat is het verschil tussen Linux en Ubuntu?
- Waarvoor gebruik je een home-directory?
- Wat laten `pwd` en `ls` zien?

**Volgende les:** [onderwerp en voorbereiding].
