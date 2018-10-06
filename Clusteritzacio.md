Clusterització de l'SGBD
========
* [Resum](https://gitpitch.com/jrodr236/ABD-UF2/master?p=Clusteritzacio)
* Exercicis teòrics: _pendent_
* Exercicis pràctics: _pendent_

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
