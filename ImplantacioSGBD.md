Implantació de sistemes gestors de bases de dades corporatius
=========================

* [Resum](https://gitpitch.com/jrodr236/ABD-UF2/master?p=ImplantacioSGBD)
* Exercicis teòrics: _pendent_
* Exercicis pràctics: _pendent_

Utilització de fitxers segons la seva organització
-------------------------

En els dispositius d’emmagatzematge secundari, la base de dades s’organitza en
un o diversos **fitxers**.

Cada fitxer està format per una sèrie de **registres**, i cada registre es divideix en
diversos **camps**.

Normalment, els registres corresponen a entitats: persones, objectes, esdeveniments, etc., i els camps són aquells atributs o propietats que volem conèixer sobre
les entitats: el nom de cada persona, el color de l’objecte, la data de l’esdeveniment,
etc.

Un **bloc** o **pàgina** és la unitat mínima de transferència entre disc i memòria
principal.

Normalment, caben diversos registres de dades en un mateix bloc. Si un registre
no cap en un sol bloc, es repartirà entre uns quants.



Índexs
----------------------

Els **índexs** són estructures d’accés que s’utilitzen per accelerar l’accés als
registres en resposta a certes condicions de cerca.


Dispositius d’emmagatzematge
--------------------

### DAS

Direct attached storage (DAS), o emmagatzematge adjuntat directament, és el
mètode tradicional d’emmagatzematge i el més senzill. Consisteix a connectar
el dispositiu d’emmagatzematge directament al servidor o estació de treball, és a
dir, físicament connectat al dispositiu que en fa ús.
Fonamentalment hi ha quatre tipus de dispositius:
1. Intelligent drive electronics (IDE).
2. Serial ATA (SATA).
3. Small computer system interface (SCSI).
4. Serial attached SCSI (SAS).



### SAN

Una xarxa d’àrea d’emmagatzematge, en anglès storage area network (SAN),
és una xarxa concebuda per connectar servidors, matrius (arrays) de discos i
biblioteques de suport. Principalment, està basada en tecnologia fibre channel
i més recentment en iSCSI. 

Una xarxa SAN es distingeix d’altres formes d’emmagatzematge en xarxa per la
manera d’accés a baix nivell. El tipus de trànsit en una SAN és molt similar al
dels discos durs com ATA, SATA i SCSI. En altres mètodes d’emmagatzematge
(com SMB o NFS) el servidor requereix un fitxer determinat, per exemple,
/home/usuari/fitxer. En una SAN el servidor requereix el bloc 6000 del disc 4.


### NAS
NAS (de l’anglès network attached storage) és el nom donat a una tecnologia
d’emmagatzematge dedicada a compartir la capacitat d’emmagatzematge d’un
sistema (servidor o sistema específic) amb ordinadors personals o servidors clients a través d’una
xarxa (normalment TCP/IP), fent ús d’un sistema operatiu optimitzat per donar
accés amb els protocols CIFS, NFS, FTP o TFTP.

Els protocols de comunicacions NAS estan basats en fitxers; d’aquesta manera el
client demana el fitxer complet al servidor i el maneja localment.


### RAID

Un arranjament RAID es basa en un sistema
d’emmagatzemament de la informació que combina diversos discos durs d’igual
capacitat que davant del sistema funcionen com una única unitat lògica. Aquest enfocament
millora el rendiment i la fiabilitat respecte a les unitats de disc individuals.

Poden utilitzar-se RAIDs en qualsevol dels tipus de dispositius explicats abans (DAS, SAN o NAS).

Les formes bàsiques més comunes d’arranjaments RAID utilitzats són:

- RAID 0
- RAID 1
- RAID 10 o 1+0
- RAID 5
- RAID 6


Evolució i funcions dels SGBD
-----------------------

### Evolució dels SGBD

![Evolució dels SGBD](https://ioc.xtec.cat/materials/FP/Materials/2251_ASIX/ASIX_2251_M10/web/html/WebContent/u3/media/ic10m10u3_01.png)

_(Actualitat = Anys 2000)_

**Present:**
- Volums de dades gegantines
- Dades desestructurades
- noSQL


### Objectius i funcionalitats dels SGBD

Els següents son les funcionalitats indispensables per al bon funcionament d'un SGBD:
- Possibilitar les consultes no predefinides de qualsevol complexitat.
- Garantir la independència física i la independència lògica de les dades.
- Evitar o solucionar els problemes derivats de la redundància.
- Protegir la integritat de les dades.
- Permetre la concurrència d’usuaris.
- Contribuir a la seguretat de les dades.


Models de bases de dades
-----------------
Un model de dades és bàsicament una “descripció” del
contenidor de dades (on es desa la informació), i també dels mètodes per desar
i recuperar informació d’aquests contenidors.

Aquests son els models de bases de dades principals:

- Bases de dades en xarxa
- Bases de dades jeràrquiques
- Bases de dades relacionals
- Bases de dades NoSQL



Instal·lació i desinstal·lació d’un SGBD
---------------------------

Com a administradors d’un Sistema gestor de bases de dades haureu de fer, primer
de tot, un estudi exhaustiu de l’entorn que us envolta i en el qual heu d’instal·lar
l’SGBD.

També heu d’estar assabentats de la finalitat i l’ús que es donarà al vostre sistema al
final del procés d’instal·lació. Per exemple, és important fer una aproximació del
nombre d’usuaris finals que tindrà connectats en un determinat moment el nostre
sistema, així com conèixer aproximadament quin tipus d’operacions es faran de
forma reiterada (consultes de dades, insercions de noves dades, modificacions de
dades existents), ja que depenent d’aquests factors ens decantarem per un o altre
sistema gestor dels existents en el mercat actualment.


### Creació de l’entorn per a l’SGBD

Una de les tasques més importants que s’ha de fer com a DBA és escollir i instal·lar
un SGBD adient per tal de satisfer les necessitats del client. Això comporta tenir
ben present, entre altres coses:
- El maquinari del qual disposa el client per muntar el servidor.
- La plataforma o sistema operatiu que utilitzarà per moure’l.
- L’ús final que es donarà al sistema.

Les principals tasques per crear un entorn de treball amb un o diversos SGBD són:
- Escollir un SGBD adient.
- Escollir l’arquitectura de l’SGBD.
- Escollir el tipus de clusterització.

### Escollir un SGBD adient

Hem d’intentar reduir el nombre d’SGBD diferents en el nostre entorn de treball.

Aquests son alguns dels productes disponibles al mercat:
1. DB2 Universal Database (IBM Corporation).
2. Oracle (Oracle Corporation).
3. SQL Server (Microsoft Corporation).
4. PostgreSQL (programari lliure amb llicència BSD).
5. MySQL (Oracle Corporation) / MariaDB
6. SQLite

Per escollir un SGBD hem de tenir en compte, entre altres coses:
- El suport per als nostres sistemes operatius.
- Tipus de client que ens demana l’SGBD.
- El joc de proves (benchmarking).
- L’ampliació d’usuaris i/o maquinari d’emmagatzematge està suportada.
- Els tècnics qualificats.
- El cost del producte.
- L’actualització de versions del producte.

### Clusterització de l'SGBD

Entenem com a **clusterització** l’ús de sistemes de computació múltiples i
independents com un de sol. La majoria dels programaris actuals ofereixen
aquesta funcionalitat.

Es poden distingir dos tipus de clusterització:

- **Compartició de disc (shared-disk)**. Es tracta de tenir diverses CPU i
memòries treballant en els mateixos discos durs, els quals estan connectats
en xarxa. 
- **Arquitectura no compartida (shared-nothing)**. Es tracta
d’utilitzar varis equips. La interconnexió s’ha de fer mitjançant la xarxa, i es passaran informació d'una CPU a l'altra. Les dades físiques
no es comparteixen, sinó que cada disc és independent de l’altre. El sistema
s’encarrega d’enviar cada consulta a la CPU que disposa de la informació
demanada.

### Requeriments de l'SGBD

És primordial tenir ben present que s’han de complir els prerequisits
que estableixi el sistema gestor per tal de dur a terme la instal·lació. Aquests
prerequisits poden anar des de la utilització de la versió correcta del sistema
operatiu fins a tenir prou memòria RAM o prou espai al disc dur per instal·lar-
hi el programari.

Haurem de tenir en compte, també, l'espai que ocuparan les dades que posteriorment introduirem en
l’SGBD.
