Clusterització de l'SGBD
========

[Veure Teoria](https://jrodr236.github.io/ABD-UF2/Clusteritzacio.html)

---

**Clusterització**: ús de sistemes de computació múltiples i
independents com un de sol. 

---

Dos tipus de clusterització:

+++

**Compartició de disc (shared-disk)**

Diverses CPU i
memòries treballant en els mateixos discos durs, els quals estan connectats
en xarxa. 

+++

**Arquitectura no compartida (shared-nothing)**

Utilitzar varis equips. La interconnexió s’ha de fer mitjançant la xarxa, i es passaran informació d'una CPU a l'altra. Les dades físiques
no es comparteixen, sinó que cada disc és independent de l’altre. El sistema
s’encarrega d’enviar cada consulta a la CPU que disposa de la informació
demanada.
