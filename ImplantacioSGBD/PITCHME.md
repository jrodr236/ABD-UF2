Implantació de SGBD corporatius
=========================

[Veure Teoria](https://jrodr236.github.io/ABD-UF2/ImplantacioSGBD.html)

---

Utilització de fitxers segons la seva organització
-------------------------

Conceptes:

Fitxers, registres, camps, blocs.

---

Índexs
----------------------

Els **índexs** són estructures d’accés que s’utilitzen per accelerar l’accés als
registres en resposta a certes condicions de cerca.

+++

Tipus:

**Índexs B-tree** (arbre): objectiu accés des d'inici a final passant per tots els valors.

**Índexs hash**: objectiu accedir directament a un valor concret.

---

Dispositius d’emmagatzematge
--------------------

- DAS
- SAN
- NAS
- RAID

---

Suports de còpies de seguretat
------------------------

Escollir-ho depèn de: mida de l’organització, el volum de dades, el cost,
etc.

+++

Alguns exemples:
* Cintes
* Biblioteques de còpia
* Discos òptics
* Discos durs

---

Evolució i funcions dels SGBD
-----------------------

### Evolució dels SGBD

![Evolució dels SGBD](https://ioc.xtec.cat/materials/FP/Materials/2251_ASIX/ASIX_2251_M10/web/html/WebContent/u3/media/ic10m10u3_01.png)

_(Actualitat = Anys 2000)_

+++

**Present:**
- Grans volums de dades
- Dades desestructurades
- noSQL

+++

### Objectius i funcionalitats dels SGBD

Funcionalitats indispensables:

- Permetre consultes complexes
- Independència física i lògica de les dades
- Evitar o solucionar els problemes derivats de la redundància.
- Protegir integritat de les dades.
- Permetre concurrència d’usuaris.
- Contribuir a la seguretat de les dades.

---

Models de bases de dades
-----------------
Un model de dades és bàsicament una “descripció” del
contenidor de dades (on es desa la informació), i també dels mètodes per desar
i recuperar informació d’aquests contenidors.

+++

Models de bases de dades principals:

- Bases de dades en xarxa
- Bases de dades jeràrquiques
- Bases de dades relacionals
- Bases de dades NoSQL

---

Instal·lació i desinstal·lació d’un SGBD
---------------------------

Primer de tot, estudiar:
- Entorn a instal·lar l'SGBD
- Finalitat del sistema
  - Usuaris finals
  - Tipus d'operacions

+++

### Creació de l’entorn per a l’SGBD

Tenir en compte:
- Maquinari
- Plataforma o SO
- L’ús final

+++

Tasques per crear l'entorn de treball:
- Escollir un SGBD adient.
- Escollir l’arquitectura de l’SGBD.
- Escollir el tipus de clusterització.

+++

### Escollir un SGBD adient

Intentar reduir el nombre d’SGBD diferents.

+++

Alguns productes existents:
1. DB2
2. Oracle
3. SQL Server
4. PostgreSQL
5. MySQL / MariaDB
6. SQLite
7. MongoDB
8. Apache Cassandra

+++

Per escollir SGBD, tenir en compte:
- El suport per als nostres sistemes operatius.
- Tipus de client que ens demana l’SGBD.
- El joc de proves (benchmarking).
- L’ampliació d’usuaris i/o maquinari d’emmagatzematge està suportada.
- Els tècnics qualificats.
- El cost del producte.
- L’actualització de versions del producte.
- Etc...

+++

### Clusterització de l'SGBD

_Es veurà al proper tema_

+++

### Requeriments de l'SGBD

- Ús de la versió correcta del SO
- Tenir prou RAM
- Tenir prou disc dur
  (quan ocuparan les dades?)
- Etc...
