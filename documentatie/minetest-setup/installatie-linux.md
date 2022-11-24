# Installatie op Ubuntu

Ik ga hier even door de installatie op Ubuntu 22.04 LTS omdat deze de recentste LTS release is en dus lang ondersteuning heeft. Als je een andere Linux distributie gebruikt zijn de stappen gelijkaardig maar moet je de commandos aanpassen als je geen `apt` gebruikt om packages te installeren.

De installatieprocedure is ook beschikbaar op de pagina [quickstart](https://miney.readthedocs.io/en/latest/quickstart.html#linux) van de Miney documentatie.

We installeren eerst wat packages die we nodig hebben, zoals `python`, `pip` en `git`. Ook `python-is-python3` zodat we niet steeds `python3` moeten typen maar gewoon `python`.

```shell
sudo apt install python3 python3-pip git idle3 luajit lua-socket lua-cjson
```


```shell
$ sudo apt-get install minetest fonts-crosextra-caladea fonts-crosextra-carlito minetest-mod-moreblocks minetest-mod-moreores minetest-mod-pipeworks minetest-server minetestmapper

$ sudo apt-get install luajit lua-socket lua-cjson idle3 python3-pip git

$ pip3 install miney
```

Dan start je best Minestest eens op zodat de folder `.minetest` aangemaakt wordt. Dit is een goed moment om je controls goed in te stellen want die zijn standaard voorzien voor querty-toetsenbord. Sluit Minetest af en installeer de mineysocket mod in Minetest:

```shell
$ cd ~/.minetest/mods

$ git clone https://github.com/miney-py/mineysocket.git
```