# Installatie Miney op Windows

Miney helemaal zelf installeren op Windows is nogal ingewikkeld, daarom is er een voorgeconfigureerde package gemaakt waar zo goed als alles al in zit.

Wat hebben we nodig?

 - Miney distributie
 - Visual Studio Build Tools

In dit document gaan we:

 - Visual Studio Build Tools installeren
 - Miney installeren
 - Verifiëren dat alles werkt
 - Toetsenbord configureren

## Visual Studio Build Tools

Ga naar [visualstudio.microsoft.com/downloads]

![visualstudio.microsoft.com/downloads](./assets/windows-install-001.png)

Scroll naar beneden voorbij **All Downloads** en klik op **Other Tools, Frameworks, and Redistributables**

![Other Tools, Frameworks, and Redistributables](./assets/windows-install-002.png)

Klik op **Download** naast **Microsoft Visual C++ Redistributable for Visual Studio 2022**

![Download MS Visual C++ Redistributable VS 2022](./assets/windows-install-003.png)

Wanneer de download klaar is klik je op *Bestand openen*, zet het vinkje aan naast *I agree to the license terms and conditions* en klik je op *Install*.

![Install MS Visual C++ Redistributable VS 2022](./assets/windows-install-004.png)

Klik op *Ja*.

![Wijzigingen toestaan](./assets/windows-install-005.png)

Na een paar seconden is de setup klaar en klik je op *Close*.

![Wijzigingen toestaan](./assets/windows-install-006.png)

## Miney

Nu kunnen we Miney installeren. Dat is een bundel met onder andere Minetest met de mineysocket mod, Python met voorgeïnstalleerde miney library en een starter om snel te kunnen beginnen met code schrijven zonder dat je nog allerlei zaken moet configureren.

Ga naar de [Miney distributiepagina](https://github.com/miney-py/miney_distribution/releases) en download **miney_windows_x64.zip**.

![Miney downloaden](./assets/windows-install-007.png)

In die download vind je een map *miney_x64*, zet deze ergens waar je uitvoerrechten hebt, zoals in *Documenten* bijvoorbeeld.

Dit kan eventjes duren..

![Miney kopieren naar Documenten](./assets/windows-install-008.png)

Daarna heb je een map *miney_x64* met daarin *miney_launcher.exe*.

![miney_launcher.exe](./assets/windows-install-009.png)

Gebruik deze om Miney te starten. Je krijgt eerst een scherm **Uw pc wordt beschermd**, klik op *Meer informatie*

![Meer informatie](./assets/windows-install-010.png)

En vervolgens op *Toch uitvoeren*

![Toch uitvoeren](./assets/windows-install-011.png)

Dan krijg je het Miney startscherm te zien.

![Miney startscherm](./assets/windows-install-012.png)

## Testen of alles werkt

In het Miney-startscherm klik op **Quickstart**. Dit opent Minetest meteen in een spel met de juiste mods en ook IDLE, de IDE die samen met Python geïnstalleerd wordt.

Je moet Minetest nog rechten geven om het netwerk te gebruiken, dat hebben we misschien later nodig als je een server wil hosten waar je met je vrienden samen kan spelen.

Zet het vinkje aan voor *Particuliere netwerken* en klik op *Toegang toestaan*.

![Firewall](./assets/windows-install-013.png)

Dan heb je normaal een beeld dat er zo uitziet. Minetest zit in een spel en een Python shell die wacht op jouw invoer.

![wacht op input](./assets/windows-install-014.png)

We gaan eens testen of een simpel commando werkt. In Python werkt het meestal zo:

 - we importeren de libraries die we nodig hebben, in dit geval `miney`
 - we maken objecten aan die we gaan gebruiken om dingen te doen
 - we schrijven code om instructies te geven aan die objecten

Dus we importeren de library `miney`:

```python
import miney
```

We maken een object dat we `mt` noemen, als afkorting voor MineTest. Dit object is een `Minetest`-object dat beschreven is in de `miney` library dus we moeten dit zo schrijven:

```python
mt = miney.Minetest()
```

Nu we een Minetest object hebben kunnen we dat gebruiken, bijvoorbeeld om een chatbericht te sturen naar iedereen op de server:

```python
mt.chat.send_to_all("Dag iedereen!")
```

De hele blok testcode ziet er zo uit:

```python
import miney

mt = miney.Minetest()

mt.chat.send_to_all("Dag iedereen!")
```

Bij het uitvoeren van die laatste regel zien we in het spel het chatbericht verschijnen.

![Chatbericht](./assets/windows-install-015.png)

Als dat werkte is alles goed ingesteld om te beginnen spelen met Python

## Toetsen configureren

Standaard staat Minetest ingesteld voor een Querty-toetsenbord. Druk op **Escape** en klik op **Toetsen aanpassen**. Ik stel voor van minstens dit aan te passen:

  - Vooruit: Z
  - Links: Q
  - Weggooien: A
  - Zoomen: W

![Toetsen aanpassen](./assets/windows-install-016.png)

Nu zijn we helemaal klaar voor wat fun in de Coderdojo, probeer de uitdagingen te volbrengen en kijk hoe ver je kan geraken.

