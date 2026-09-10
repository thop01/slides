---
marp: true
theme: ubuntu
paginate: true
size: 16:9
---

<!-- _class: title -->

# Linux les 1

Ubuntu

---

## Het gezicht achter Linux

Linus Torvalds begon in 1991 met de ontwikkeling van de Linux-kernel.
Tux, de pinguïn, is de mascotte van Linux.

![Linus Torvalds h:280](../assets/linus.png) ![Tux, de Linux-mascotte h:280](<../assets/linux mascotte.png>)

---

<!-- _paginate: false -->

![bg contain](../assets/waarom-linux.png)

<!-- Waarom Linux? Overzicht van de voordelen, van ontwikkeltools tot community en terminal. -->

---

## Wat gaan we de komende periode doen?

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

## Lesmateriaal

<style scoped>
p { display: flex; align-items: center; justify-content: center; gap: 24px; }
p img { width: calc((100% - 48px) / 3); height: 460px; object-fit: contain; }
</style>

![Hoofdstukken van het boek](<../assets/hoofdstukken boek.png>)
![Linuxboek](../assets/linuxboek.png)
![Studentenwerkboekjes](<../assets/studenten werkboekjes.png>)

---

# Linux

Linux is een opensourcebesturingsysteem.

- Open source houdt in dat de broncode openbaar is.
- Je mag de software bekijken en aanpassen.
- Aanpassingen moet beschikbaar zijn voor anderen.
- Verkopen mag niet.

**_Deze voorwaarden staan beschreven onder de licentie GPL: General Public license_**

---

## Licenties

- GPL: General Public License
  - Opensource, gratis, verkopen mag niet
- LGPL: Lesser General Public License
  - Onderdelen van de software is closesource
- EULA: End User license Agreement
  - Softwarebedrijf schrijft eigen regels over het gebruik van de broncode.

---

## Distrobuties

Doordat Linux valt onder de GPL-licentie en dus opensource is. Zijn er héél veel versies van linux. Een versie van Linux noemen we distro of distrubtie.

- Er zijn honderden distro's met allemaal hun eigen voor en nadelen.
- https://distrowatch.com/ is een website dat distro's in de gaten houdt.

**_Wij gebruiken de distro Ubuntu_**

![Ubuntu h:120](../assets/ubuntu.webp)

---

## Installatie

Een Linux-besturingssyteem kan je op verschillende manieren installeren

- Je kan je huidige besturingssyteem vervangen met een linux-besturingsysteem
- Je kan naast je huidige besturingsysteem door middel van dualboot linux installeren.
- Je kan een besturingssyteem installeren in je huidige besturingssysteem. Dit noemen we virtualisatie.

**_Voor school doeleinde kiezen wij voor virtualisatie._**

---

## VM-programma's

- VMware Workstation
- Microsfot Hyper-V
- OracleVirtualBox

**_Wij gebruiken VMWare Workstation_**

---
