# Installatie Minetest en Miney

## Windows

Er is een snelle manier [hier](https://github.com/miney-py/miney_distribution/releases).

Stap voor stap instructies [hier](./installatie-windows.md).

## Linux

Volg de instructies voor je distributie. Voor Ubuntu, wat we gebruiken op de Coderdojolaptops, zijn de instructies beschreven in de [Miney quickstart](https://miney.readthedocs.io/en/latest/quickstart.html):


```shell
$ sudo apt-get install minetest fonts-crosextra-caladea fonts-crosextra-carlito minetest-mod-moreblocks minetest-mod-moreores minetest-mod-pipeworks minetest-server minetestmapper

$ sudo apt-get install luajit lua-socket lua-cjson idle3 python3-pip

$ pip3 install miney
```

Dan start je best Minestest eens op zodat de folder `.minetest` aangemaakt wordt. Dit is een goed moment om je controls goed in te stellen want die zijn standaard voorzien voor querty-toetsenbord. Sluit Minetest af en installeer de mineysocket mod in Minetest:

```shell
$ cd ~/.minetest/mods

$ git clone https://github.com/miney-py/mineysocket.git
```