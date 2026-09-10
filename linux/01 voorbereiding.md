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

# Linux Les 02: Orientatie

---

## Wat ga je leren?

- Met ctrl + alt kan je de terminal openen.
- sudo hostnamectl set-hostname nieuwe-hostnaam
- ai-prompts.png

- ik wil de scroll neutraal. Naar beneden scrollen is ook echt naar beneden.
- ik wil dat de scrollbar altijd zichtbaar is.
- Ik wil mijn cursor extra groot
- ik wil een achtergrond met een inspirerende quote.

---

<!-- _class: section -->

# Theorie

Van begrip naar praktijk

---

## Voorbeeldtheorie: wat is Ubuntu?

**Linux** is de kernel: de kern die de hardware en systeemprocessen beheert.

Een **distributie** combineert deze kernel met programma's en hulpmiddelen tot een bruikbaar besturingssysteem. Ubuntu is daar een voorbeeld van.

> Onthoud: de kernel vormt de basis; de distributie levert het complete pakket.

---

<!-- _class: table -->

## Overzicht in een tabel

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
