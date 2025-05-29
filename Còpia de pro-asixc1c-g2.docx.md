# **EC21-2:**

## **FAIL2BAN:**

<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>

## **DUCKDNS ON PREMISE:**

<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
---

# **EC22:**

## **BASE DE DADES:**

* **Empleats**:  
  * Identificador: DNI.  
  * Atributs: Nom, cognoms, adreça, telèfon.  
  
* **Departaments**:  
  * Identificador: Codi.  
  * Atributs: Nom complet del departament, telèfon.  
  
* **Grup-nivell**:  
  * Identificador: Codi (ex. A1, B1, etc.).  
  * Atributs: Salari total, període de prova, dies de vacances.  
  
* **Conveni**:  
  * S'ha de basar en el **conveni col·lectiu de Consultoria, Tecnologies de la Informació i Estudis de Mercat i de l'Opinió Pública**, àrea 2\.  
  * Utilitzar la **taula salarial actualitzada de 2024** per als salaris, períodes de prova i vacances.  
  * Incloure un empleat per cada grup i nivell de l'àrea 2 del conveni.  
  
* **Implementació**:  
  * Disseny entitat-relació (E-R).  
  * Transformació a model relacional.  
  * Implementació en un SGBD (MySQL/MariaDB o AWS RDS).  
  * Introducció d'un nombre significatiu de dades.

### 

### **1\. Disseny Entitat-Relació (E-R)**

#### **Entitats i Relacions**

* **Entitat: Empleat**  
  * Atributs: DNI (clau primària), Nom, Cognoms, Adreça, Telèfon.  
  
  * Relacions:  
  
    * Pertany a un **Departament** (relació N:1).  
    
    * Assignat a un **Grup-Nivell** (relació N:1).  
    
* **Entitat: Departament**  

  * Atributs: Codi (clau primària), Nom, Telèfon.  
  
  * Relacions:  
  
* **Entitat: Grup-Nivell**  
  * Atributs: Codi (clau primària), Salari Total, Període de Prova, Dies de Vacances.  
  * Relacions:  
    * Assignat a **Empleats** (relació 1:N).

#### **Diagrama E-R:**

\[Empleat\] \-- N:1 \--\> \[Departament\]  
   |                    Atributs:  
   |                    \- Codi (PK)  
   |                    \- Nom  
   |                    \- Telèfon  
   |  
   Atributs:  
   \- DNI (PK)  
   \- Nom  
   \- Cognoms  
   \- Adreça  
   \- Telèfon  
   |  
   |  
   N:1 \--\> \[Grup-Nivell\]  
             Atributs:  
             \- Codi (PK)  
             \- Salari Total  
             \- Període de Prova  
             \- Dies de Vacances  
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>
<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>



**Investigar i comparar eficiència energètica amb altres proveïdors del núvol. Com els diferents proveïdors ofereixen solucions de CPD administrats per aquestes empreses i com donen cobertura als requeriments exposats anteriorment.**

**Els principals proveïdors del núvol (Google Cloud, Microsoft Azure i AWS) estan molt compromesos amb la sostenibilitat i l’eficiència energètica dels seus Centres de Processament de Dades (CPD).**

**Tots utilitzen CPDs propis i gestionats, amb certificacions que garanteixen la bona gestió energètica i ambiental.**

* **Google Cloud** destaca per tenir un PUE molt baix (\~1.10) i funciona amb energia 100% renovable des de fa anys, amb l’objectiu d’operar sense emissions les 24 hores el 2030\.

* **Microsoft Azure** també aposta per la renovabilitat total abans del 2025 i vol ser “carbon negative” el 2030\.

* **AWS** està avançant cap al 100% renovable el 2025 i manté un PUE lleugerament superior (\~1.14).

* **OVHcloud** ofereix una opció molt eficient amb un PUE excel·lent (\~1.09) i refrigeració per aire lliure, especialment pensada per al mercat europeu.



**IP ELASTICA**  

per assignar una ip elastica hem d’anar a xarxa i seguretat i clicar a direccions ip elastiques. 

<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>

després hem de clicar a ASSIGNAR DIRECCION IP ELASTICA per crear una ip per assignar.

<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>

**cliquem a assignar**

<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>

**i ja tindrem una ip elastica, ara només falta assignar-la a l’instancia adequada**

<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>

**cliquem a l’IP i despres a DIrecció IP elastica associada.**

<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>

**aqui, el que farem es assignar l’IP elastica a l’instancia que pertoca, en aquest cas posem l’instancia EC23**

<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>

**després posem l’IP privada que té la instància** 

<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>

**i cliquem a associar**

<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>

**per comprovar que ha funcionat hem d’anar a Instàncies i clicar a la instància a la qual hem assignat l’IP, i podrem comprovar que ja l’hem assignat.**

<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>

<center>[Ver captura de instalación](ruta/a/imagen1.png)</center>

* Disseny i implementació d’una base de dades

Es tracta de dissenyar i implementar una base de dades per la gestió del personal de l’empresa. Els requisits que es demanen són els següents:

\-Els empleats s’identifiquen pel seu DNI. A més hem d’enregistrar el nom, cognoms, adreça i telèfon.  
Aquest empleats estan assignats a un determinat departament. Els departaments s’identifiquen amb un codi i també guardarem el nom complert del departament i el telèfon.

Cada empleat té assignat un grup-nivell. Un grup-nivell s’identifica per un codi (A1, B1, etc.) i també enregistrarem el salari total, el període de prova i els dies de vacances.

\-Cal tenir en compte que a la vostra base dades hi ha un empleat/da de cada grup i nivell de l’àrea 2 del conveni “Consultoria, tecnologies de la informació i estudis de mercat i de l’opinió pública”. Com sabeu, aquest és un dels convenis que més s’apliquen en el vostre sector. D’aquests empleats \-mirant el conveni-, heu de posar el salari total, el període de prova i les vacances.

- Hay que añadir roles y controlar el acceso a las tablas.

*Cal tenir en compte una puntualització important. Existeix el conveni, però també la taula salarial actualitzada del 2024\. Tota la informació rellevant pel vostre sector es troba al conveni, però el sou que heu d’utilitzar, es el de la revisió salarial 2024\.*

Es demana fer el disseny entitat-relació, la transformació a relacional i la implementació en un Sistema Gestor de Bases de Dades (MySQL, Oracle, etc.) amb la introducció d’un nombre significatiu de dades.

**Mesures aplicades en matèria de prevenció de riscos laborals en un Centre de Processament de Dades (CPD)**

Els CPD són instal·lacions crítiques que allotgen servidors i equips informàtics essencials per a empreses, i presenten riscos específics com incendis, descàrregues elèctriques, caigudes o problemes ergonòmics. Aquest informe recull les principals mesures preventives implementades per garantir la seguretat dels treballadors, basant-me en normatives com la Llei 31/1995 de Prevenció de Riscos Laborals i en pràctiques habituals del sector.

**1\. Identificació dels riscos en un CPD**

Abans d’aplicar mesures, és clau identificar els riscos més comuns en un CPD:

* **Riscos elèctrics**: Contacte amb cables, sobrecàrregues o curtcircuits.  
* **Incendis**: Deguts a la gran quantitat d’equips elèctrics i la càrrega tèrmica.  
* **Riscos físics**: Caigudes per cables mal col·locats, lesions per aixecar equips pesants o sorolls elevats dels sistemes de refrigeració.  
* **Riscos ergonòmics**: Males postures en tasques de manteniment o monitors mal ajustats.  
* **Riscos ambientals**: Temperatures extremes per sistemes de climatització o exposició a gasos en cas de fuites.

**2\. Mesures preventives aplicades**

Per abordar aquests riscos, s’han implementat les següents mesures, agrupades per categories:

**2.1. Prevenció de riscos elèctrics**

* **Instal·lacions certificades**: Tots els sistemes elèctrics compleixen la normativa del Reglament Electrotècnic de Baixa Tensió. Es fan revisions periòdiques per detectar anomalies.  
* **Proteccions**: Interruptors diferencials i magnetotèrmics en quadres elèctrics per evitar descàrregues.  
* **Formació**: Els tècnics reben formació específica sobre seguretat elèctrica, incloent l’ús de guants aïllants i eines certificades.  
* **Senyalització**: Zones d’alta tensió marcades amb cartells de perill i accés restringit.

**2.2. Prevenció d’incendis**

* **Sistemes de detecció**: Detectors de fum i calor instal·lats en tot el CPD, connectats a una central d’alarmes.  
* **Extinció automàtica**: Sistemes d’extinció amb gas inert (com FM-200) que no danya els equips i és segur per als treballadors. També hi ha extintors de CO₂ a mà.  
* **Materials ignífugs**: Cables i revestiments amb certificació de resistència al foc.  
* **Simulacres**: Es fan simulacres anuals per entrenar el personal en evacuacions i ús d’extintors.

**2.3. Prevenció de riscos físics**

* **Ordre i neteja**: Els cables estan canalitzats en safates elevades per evitar ensopegades. El terra és antilliscant i lliure d’obstacles.  
* **Manipulació de càrregues**: S’usen carros elevadors o plataformes per moure servidors pesants, i es forma el personal en tècniques d’aixecament segur.  
* **Control de soroll**: Els treballadors que operen prop de sistemes de refrigeració usen protectors auditius quan el nivell de decibels supera els 85 dB.  
* **Il·luminació**: Llums LED amb intensitat adequada per evitar fatiga visual, especialment en tasques de manteniment.

**2.4. Prevenció de riscos ergonòmics**

* **Estacions de treball**: Monitors i teclats ajustables per mantenir postures neutres. Es proporcionen cadires ergonòmiques per a tasques administratives al CPD.  
* **Pausos**: S’estableixen descansos cada dues hores per a tècnics que fan tasques repetitives, com la instal·lació de cablejat.  
* **Formació**: Sessions sobre ergonomia per conscienciar sobre postures correctes i ajustos dels equips.

**2.5. Prevenció de riscos ambientals**

* **Climatització**: Sistemes de refrigeració redundants mantenen la temperatura entre 18-24 ºC i la humitat al 40-60%, evitant cops de calor o molèsties.  
* **Ventilació**: Filtres d’aire per reduir partícules i garantir la qualitat de l’aire.  
* **Control de gasos**: Sensors de CO₂ i protocols per detectar fuites en sistemes de refrigeració.

**3\. Organització i formació**

* **Pla de prevenció**: El CPD té un pla de prevenció de riscos laborals actualitzat, amb avaluacions periòdiques dels llocs de treball.  
* **Formació contínua**: Els treballadors reben cursos anuals sobre RRLL, incloent primers auxilis, evacuació i ús d’equips de protecció individual (EPI).  
* **EPI**: Es proporcionen guants aïllants, calçat de seguretat, ulleres protectores i protectors auditius segons la tasca.  
* **Comitè de seguretat**: Un comitè de salut laboral revisa incidents i proposa millores.

**4\. Integració amb el projecte InnovateTech**

En el context del nostre projecte InnovateTech, aquestes mesures s’han aplicat al CPD d’EC22 (ip-172-31-21-192). Per exemple:

* Hem assegurat que la base de dades innovat\_db i els servidors estiguin en un entorn segur, amb detectors d’incendis i climatització adequada.  
* Els tècnics que accedeixen al CPD per manteniment (e.g., backups a /backups i S3) usen EPI i segueixen protocols d’ordre.  
* Hem compartit aquestes pràctiques amb el meu company per resoldre el seu problema de connexió, ja que un entorn segur facilita tasques com l’accés a empleats.php en EC21.

**Conclusió**

Les mesures de prevenció de RRLL al CPD garanteixen un entorn segur per als treballadors i protegeixen els equips crítics. Des de la prevenció d’incendis fins a l’ergonomia, cada aspecte s’ha abordat amb rigor, complint la normativa i adaptant-se a les necessitats del projecte InnovateTech.
