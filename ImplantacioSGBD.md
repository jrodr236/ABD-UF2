Implantació de sistemes gestors de bases de dades corporatius
=========================

* [Resum](https://gitpitch.com/jrodr236/GBD-UF3/master?p=ImplantacioSGBD)
* Exercicis teòrics: _pendent_
* Exercicis pràctics: _pendent_

Utilització de fitxers segons la seva organització
-------------------------

En els dispositius d’emmagatzematge secundari, la base de dades s’organitza en
un o diversos **fitxers**.

Cada fitxer està format per una sèrie de **registres**, i cada registre es divideix en
diversos **camps**.

Normalment, els registres corresponen a entitats: persones, objectes, esdeveni-
ments, etc., i els camps són aquells atributs o propietats que volem conèixer sobre
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
i més recentment en iSCSI. La seva funció és la de connectar de manera ràpida,
segura i fiable els diferents elements que la conformen.

Una xarxa SAN es distingeix d’altres formes d’emmagatzematge en xarxa per la
manera d’accés a baix nivell. El tipus de trànsit en una SAN és molt similar al
dels discos durs com ATA, SATA i SCSI. En altres mètodes d’emmagatzematge
(com SMB o NFS) el servidor requereix un fitxer determinat, per exemple,
/home/usuari/fitxer. En una SAN el servidor requereix el bloc 6000 del disc 4.
La majoria de les SAN actuals utilitzen el protocol SCSI per accedir a les dades
de la SAN, encara que no facin servir interfícies físiques SCSI. Aquest tipus de
xarxes de dades s’han utilitzat i s’utilitzen tradicionalment en grans ordinadors
centrals, com en IBM, SUN o HP.


### NAS
NAS (de l’anglès network attached storage) és el nom donat a una tecnologia
d’emmagatzematge dedicada a compartir la capacitat d’emmagatzematge d’un
computador (servidor) amb ordinadors personals o servidors clients a través d’una
xarxa (normalment TCP/IP), fent ús d’un sistema operatiu optimitzat per donar
accés amb els protocols CIFS, NFS, FTP o TFTP.

Generalment, els sistemes NAS són dispositius d’emmagatzematge específics a
què s’accedeix des dels equips per mitjà de protocols de xarxa (normalment
TCP/IP). També es podria considerar un sistema NAS un servidor (Linux, Win-
dows...) que comparteix les seves unitats per xarxa, però la definició se sol aplicar
a sistemes específics.


Els protocols de comunicacions NAS estan basats en fitxers; d’aquesta manera el
client demana el fitxer complet al servidor i el maneja localment, i per aquesta raó
estan orientats a informació emmagatzemada en fitxers de petita grandària i gran
quantitat. Els protocols usats són protocols de compartició de fitxers com NFS o
el Microsoft common Internet file system (CIFS).


### RAID

L’enfocament RAID (matriu redundant de discos independents) és la manera
estàndard per manejar tant el rendiment com la fiabilitat de les limitacions de
les unitats de disc individuals. Un arranjament RAID es basa en un sistema
d’emmagatzemament de la informació que combina diversos discos durs d’igual
capacitat que davant del sistema funcionen com una única unitat lògica.

Poden utilitzar-se RAIDs en qualsevol dels tipus de dispositius explicats abans (DAS, SAN o NAS).

Les formes bàsiques més comunes d’arranjaments RAID utilitzats són:

- RAID 0
- RAID 1
- RAID 10 o 1+0
- RAID 5
- RAID 6

La tècnica del RAID millora el rendiment, en distribuir la informació entre
diverses unitats, i pot oferir redundància per augmentar la seguretat.

El RAID pot ser per programari o per maquinari. Si és per programari és més lent,
i si és per maquinari és transparent al sistema operatiu.



Suports de còpies de seguretat
------------------------

L’elecció del dispositiu de còpia de
seguretat depèn sempre de la mida de l’organització, el volum de dades, el cost,
etc.

### Cintes

ins fa poc les cintes eren el dispositiu més habitual als servidors. Quan es parla
de capacitats de les unitats de cinta cal tenir en compte que n’hi ha amb compressió
o sense.

Hi ha diferents tipus de dispositius de cinta:
* Digital audio tape (DAT)
* Digital linear tape (DLT)
* Advanced intelligent tape (AIT)
* Linear tape open (LTO)

### Biblioteques de còpia

Es pot donar el cas que la nostra organització manipuli quantitats de dades que
ocupin diverses cintes de còpia al dia. En aquest cas, una sola persona es passaria
el dia fent còpies de seguretat, i no acabaria mai. Quina és la solució per a aquests
volums d’informació tan grans? Hi ha uns dispositius anomenats biblioteques de
còpia. Són externs, amb uns braços articulats, i contenen des de vint fins a dues
mil cintes de còpia de seguretat (són com robots).


### Enregistrament de discos òptics

Una unitat de cinta és un component car i moltes vegades resulta difícil accedir
(demana un temps considerable) a les dades que contenen. Per això, de vegades
es considera la gravadora de DVD com una opció de còpies de seguretat. Ens
permetrà fer còpies de DVD gravables i regravables de 4,7 i 9,4 GB. Tot i que
aquests són els volums més estàndard, podem trobar volums de DVD gravables
una vegada fins de 17 GB.


### Discos durs

En sistemes crítics, i més tenint en compte el cost i la capacitat actual d’aquests
dispositius, no s’ha de descartar mai la possibilitat de fer una còpia de seguretat (o
fins i tot de copiar tota la informació) en un altre disc dur només dedicat a aquesta
unció. L’estratègia és fer una primera còpia de seguretat en aquest disc dur (es
pot fer amb un procediment automàtic i diverses vegades al dia, si cal), i d’aquest
disc, posteriorment, se’n farà una còpia de seguretat en un altre dispositiu (que pot
ser una cinta).

De vegades, aquesta estratègia és necessària si el procediment de còpia necessita
bloquejar la informació a la qual accedeix i és, per exemple, una gran base de
dades de la qual depèn tota l’organització. La còpia de disc a disc, en funcionar
internament, pels busos del sistema i amb velocitats de transferència molt elevades,
necessita bloquejar molt poc temps la informació per fer la còpia. Així, doncs, la
interrupció per fer aquesta tasca és pràcticament imperceptible.

Gràcies a la proliferació de xarxes SAN o dispositius NAS que permeten una
gran quantitat d’espai per emmagatzemar, s’utilitzen cada cop més els discos com
a dispositiu de còpia. Els proveïdors mateixos ofereixen eines específiques que
permeten fer aquestes còpies transparents al sistema mateix.



Altres tipus d’emmagatzematge d’informació
-------------------------

### Fitxers

En determinades situacions la millor opció per emmagatzemar la informació és en un fitxer.

Els tipus de fitxers més utilitzats per organitzar informació son:

- XML: és un llenguatge de marques generalitzat que pretén dotar els continguts
(documents) d’estructura lògica de manera que puguin ser manipulats com a dades
per una màquina i es pugui intercanviar informació amb independència de la
plataforma, l’arquitectura i la base de dades.
- JSON (JavaScript Object Notation): és un estàndard obert basat en text dissenyat per a intercanvi de dades llegible per humans. Deriva del llenguatge script JavaScript, per a representar estructures de dades simples i llistes associatives, anomenades objectes.

### Serveis de directori (LDAP)

n general un directori és una
llista d’informació sobre algun tipus d’objecte, com per exemple persones. Els
directoris es poden emprar per cercar informació sobre un objecte concret o en
sentit invers per poder trobar aquells objectes que compleixen un determinat
requisit.

El protocol més utilitzat per accedir a directoris i oferir una manera
normalitzada d’accés a les dades dels  és l'LDAP _(lightweight directory access
protocol)_.

Evolució i funcions dels SGBD
-----------------------

### Evolució dels SGBD

![Evolució dels SGBD](https://ioc.xtec.cat/materials/FP/Materials/2251_ASIX/ASIX_2251_M10/web/html/WebContent/u3/media/ic10m10u3_01.png)


### Objectius i funcionalitats dels SGBD

Tots els SGBD del mercat volen assolir una sèrie d’objectius i oferir una sèrie de
funcionalitats, amb més o menys encert, que actualment es consideren indispen-
sables per al bon funcionament de qualsevol sistema d’informació:
- Possibilitar les consultes no predefinides de qualsevol complexitat.
- Garantir la independència física i la independència lògica de les dades.
- Evitar o solucionar els problemes derivats de la redundància.
- Protegir la integritat de les dades.
- Permetre la concurrència d’usuaris.
- Contribuir a la seguretat de les dades.


Models de bases de dades
-----------------
Un model de dades és bàsicament una “descripció” d’una cosa coneguda com a
contenidor de dades (on es desa la informació), i també dels mètodes per desar
i recuperar informació d’aquests contenidors. Els models de dades no són coses
físiques: són abstraccions que permeten la implementació d’un sistema eficient de
base de dades; per norma general es refereixen algoritmes i conceptes matemàtics.

Aquests son els models de bases de dades principals:

- Bases de dades en xarxa
- Bases de dades jeràrquiques
- Bases de dades relacionals
- Bases de dades NoSQL


Arquitectura dels SGBD
----------------

### Esquemes i nivells

![Nivells en una base de dades](https://ioc.xtec.cat/materials/FP/Materials/2251_ASIX/ASIX_2251_M10/web/html/WebContent/u3/media/ic10m10u3_04.png)

En definir un esquema extern, només s’inclouran els atributs i entitats que interessin, els podrem reanomenar, podrem definir dades derivades, podrem definir
una entitat de tal manera que les aplicacions que utilitzen aquest esquema extern
creguin que en són dues, o podrem definir combinacions d’entitats perquè en
semblin una de sola, etc.

En l’esquema conceptual, es descriuran les entitats tipus, els seus atributs, les
interrelacions i també les restriccions o regles d’integritat.

L’esquema intern o físic contindrà la descripció de l’organització física de la BD:
camins d’accés (índexs, hashing, apuntadors...), codificació de les dades, gestió
de l’espai, mida de la pàgina, etc.


### Components funcionals dels SGBD

El components funcionals dels SGBD més importants són el gestor d’emmagatzemament i el processador de consultes.

El gestor d’emmagatzemament proporciona la interfície entre les dades, considerades a baix nivell, i les consultes i els programes que accedeixen a la BD.

El processador de consultes ajuda l’SGBD a simplificar l’accés a les dades. Les
vistes a alt nivell contribueixen a assolir aquest objectiu, ja que eviten que els
usuaris hagin de conèixer detalls de la implementació física del sistema. Però
això no treu que el sistema no hagi de perseguir l’eficàcia en el processament de
les consultes i de les actualitzacions de dades.
De fet, el sistema ha de traduir les instruccions escrites, en un nivell lògic, en un
llenguatge no procedimental (típicament, SQL), a una seqüència d’operacions de
nivell físic, amb uns mínims d’eficiència.



Tipus d’usuari de l’SGBD
----------------------

### Usuaris convencionals

1) Usuaris externs. Són usuaris no sofisticats, que no interactuen directament
amb el sistema, sinó mitjançant alguna aplicació informàtica desenvolupada
prèviament per altres persones amb aquesta finalitat.

2) Usuaris sofisticats. Interactuen directament amb el sistema, sense utilitzar les
interfícies proporcionades per programes intermediaris. Formulen les consultes
en un llenguatge de BD (normalment, SQL), des de dins de l’entorn que el SGBD
posa a la seva disposició.

3) Programadors d’aplicacions. Són professionals informàtics que creen els
programes que accedeixen als SGBD i que, posteriorment, són utilitzats pels
usuaris que hem anomenat externs.

### Administradors

Els administradors són uns usuaris especials que realitzen tasques d’administració
i control centralitzat de les dades, i gestionen els permisos d’accés concedits als
diferents usuaris i grups d’usuaris, per tal de garantir el funcionament correcte de
la BD.

Els administradors han d’actuar, evidentment, per solucionar les eventuals atura-
des del sistema, però la seva responsabilitat fonamental consisteix, justament, a
evitar que es produeixin incidents.

La feina dels administradors no és fàcil, tot i que els SGBD incorporen cada vegada
més eines per facilitar-la, i en la majoria dels casos amb interfície visual. Es
tracta, per exemple, d’eines de monitoratge de rendiment, d’eines de monitoratge
de seguretat, de verificadors de consistència entre índexs i dades, de gestors de
còpies de seguretat, etc.
Una llista no exhaustiva de les tasques dels administradors podria ser la següent:
- Crear i administrar els esquemes de la BD.
- Administrar la seguretat: autoritzacions d’accés, restriccions, etc.
- Realitzar còpies de seguretat periòdiques.
- Controlar l’espai de disc disponible.
- Vigilar la integritat de les dades.
- Observar l’evolució del rendiment del sistema i determinar quins processos
consumeixen més recursos.
- Assessorar els programadors i els usuaris sobre la utilització de la BD.
- Fer canvis en el disseny físic per millorar el rendiment.
 Resoldre emergències.


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

#### Escollir un SGBD adient

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

...