
Sistemes de bases de dades i comunicacions
====================================

Implantació de sistemes gestors de bases de dades corporatius
=========================

* [Resum](https://gitpitch.com/jrodr236/ABD-UF2/master?p=SistemesDeBasesDeDadesIComunicacions.)
* Exercicis teòrics: _pendent_
* Exercicis pràctics: _pendent_

Sistemes centralitzats
--------------------

Els **sistemes de bases de dades centralitzats** són aquells que s’executen en un únic sistema informàtic sense interaccionar amb cap altre ordinador.

Aquests sistemes comprenen el rang des dels sistemes de bases de dades monousuari que s’executen en ordinadors personals fins als sistemes de bases de dades d’alt rendiment que s’executen en grans sistemes.

![Sistemes centralitzats](https://ioc.xtec.cat/materials/FP/Materials/2251_ASIX/ASIX_2251_M10/web/html/WebContent/u3/media/ic10m10u3_05.png)

Bases de dades client/servidor
-----------

Els sistemes client-servidor tenen la seva funcionalitat dividida entre el sistema servidor i múltiples sistemes clients.

Un  **client**  és un procés que sol·licita serveis específics als processos d’un servidor. Un  **servidor**  és un procés que proporciona serveis sol·licitats pels clients.

Els processos client i servidor poden estar al mateix ordinador o en diferents, sempre que estiguin connectats per una xarxa.

### Sistema client/servidor de 2 capes

En un sistema client/servidor de 2 capes un client sol·licita serveis directament al servidor.

![Sistema client/servidor de 2 capes](https://ioc.xtec.cat/materials/FP/Materials/2251_ASIX/ASIX_2251_M10/web/html/WebContent/u3/media/ic10m10u3_06.png)

### Sistema client/servidor de 3 capes

En un sistema client/servidor de 3 capes, les sol·licituds del client són manejades per servidors intermedis, i són aquests els que s’encarreguen de coordinar l’execució de les sol·licituds del client amb altres servidors subordinats.

![Sistema client/servidor de 3 capes](https://ioc.xtec.cat/materials/FP/Materials/2251_ASIX/ASIX_2251_M10/web/html/WebContent/u3/media/ic10m10u3_07.png)

Alguns exemples de normes desenvolupades per fer l'interfície entre clients i servidors son ODBC i JDBC.


