
Sistemes de bases de dades i comunicacions
====================================

[Veure Teoria](https://jrodr236.github.io/ABD-UF2/SistemesDeBasesDeDadesIComunicacions.html)

---

Sistemes centralitzats
--------------------

S’executen en un únic sistema informàtic.

<img src="https://ioc.xtec.cat/materials/FP/Materials/2251_ASIX/ASIX_2251_M10/web/html/WebContent/u3/media/ic10m10u3_05.png" height="300px">

---

Bases de dades client/servidor
-----------

Funcionalitat dividida entre el sistema servidor i múltiples sistemes clients.

+++

Un  **client**  és un procés que sol·licita serveis específics als processos d’un servidor.

+++

Un  **servidor**  és un procés que proporciona serveis sol·licitats pels clients.
+++

Els processos client i servidor poden estar al mateix ordinador o en diferents, sempre que estiguin connectats per una xarxa.

+++

### Sistema client/servidor de 2 capes

Un client sol·licita serveis directament al servidor.

<img src="https://ioc.xtec.cat/materials/FP/Materials/2251_ASIX/ASIX_2251_M10/web/html/WebContent/u3/media/ic10m10u3_06.png" height="300px">

+++

### Sistema client/servidor de 3 capes

Les sol·licituds del client són manejades per servidors intermedis.

<img src="https://ioc.xtec.cat/materials/FP/Materials/2251_ASIX/ASIX_2251_M10/web/html/WebContent/u3/media/ic10m10u3_07.png" height="300px">

---

Clusterització de l'SGBD
----


Ús de sistemes de computació múltiples i
independents com un de sol. 

+++

Dos tipus de clusterització:

+++

### Compartició de disc (shared-disk)

Diverses CPU i
memòries treballant en els mateixos discos durs, els quals estan connectats
en xarxa. 

+++

### Arquitectura no compartida (shared-nothing)

Utilitzar varis equips. La interconnexió s’ha de fer mitjançant la xarxa, i es passaran informació d'una CPU a l'altra. Les dades físiques
no es comparteixen (discos independents).
