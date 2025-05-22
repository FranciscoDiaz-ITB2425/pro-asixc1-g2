# pro-asixc1-g2

# Proposta de CPD

## Ubicació física

El nostre **CPD**, preparat per suportar fins a **8.000 connexions simultànies**, s’ubicarà a la **planta baixa d’una nau industrial**, en una zona interior, **sense finestres** i **protegida de l’exterior**. Aquesta elecció respon a criteris de:

- **Seguretat**
- **Eficiència energètica**
- **Adequació tècnica**

La nau ofereix un espai ampli i robust per integrar sistemes crítics com:

- Refrigeració
- Subministrament elèctric
- Control d’accessos

La ubicació interior, no visible des de l’exterior, redueix riscos físics i ambientals, i facilita el manteniment segur i eficient del CPD.

La nau estarà situada al **Parc Empresarial Granland Badalona Sud (Barcelona)**, amb accés:

- Metro, tramvia i RENFE
- Ronda de Dalt (sortides 25, 26 i 27)
- Accés a Barcelona per Diagonal Mar i Gran Via

📷 **[Veure imatge de la ubicació](URL)**


---

## Sistemes de climatització

Fem servir un sistema de **refrigeració natural**, aprofitant l’aire fresc exterior per mantenir:

- Temperatura: **18 °C - 27 °C**
- Humitat relativa: **45% - 55%**

Característiques del sistema:

- Filtres HEPA per a neteja de l’aire
- Circulació interna mitjançant **ventiladors automàtics**
- Regulació per **sensors ambientals**
- Expulsió de l’aire calent per sortides d’extracció
- Distribució de l’aire fred per sota, al costat dels racks

Inclou un sistema de **detecció de fums VESDA** per a major seguretat.

📷 **[Veure esquema del sistema de refrigeració](URL)**

---

## Mesures per dificultar la identificació de la sala

Per evitar la identificació del CPD:

- **Cap rètol visible**
- **Porta d’accés discreta**, similar a la resta
- **Segona porta** interna per accedir als servidors
- **Control biomètric + PIN Pad**
- **Només personal autoritzat** coneix la ubicació exacta

📷 **[Veure imatge de la porta i sistemes de seguretat](URL)**

---

## Distribució i gestió del cablejat

Per garantir ordre i seguretat:

- **Separació del cablejat elèctric i de dades**
- Canals independents per evitar interferències
- **Cables de xarxa pel terra tècnic**
- **Cables d’alimentació sota terra tècnic**
- **Etiquetatge i codificació per colors**

📷 **[Veure esquema de distribució de cablejat](URL)**

---

## Terra tècnic i sostre tècnic

Disposem d’un **terra tècnic elevat (50 cm)** que permet:

- Canalització d’aire fred
- Distribució segura del cablejat elèctric
- Accés fàcil per a manteniment

El terra tècnic estarà enfonsat al terra de la nau, amb **reixes i portes d’accés**.

📷 **[Veure imatge del terra tècnic](URL)**

---

## Esbós de la sala de servidors

Característiques:

- **Quadre elèctric** abans de la sala principal
- **Ordinador de control** del CPD
- **Aire condicionat** de suport
- **SAIs** (1 per rack) per mantenir operativitat en cas de fallada elèctrica

**Dimensions de la sala:** 5m x 4m

📷 **[Veure plànol de la sala de servidors](URL)**

---

## Estructuració dels racks

Comptem amb **3 racks de 42U**, organitzats en una fila horitzontal:

- **Rack 1:** Servidors i sistemes de virtualització
- **Rack 2:** Emmagatzematge i còpies de seguretat
- **Rack 3:** Comunicacions i xarxa (switches, firewall, etc.)

Cada rack inclou:

- **PDU intel·ligents**
- **Etiquetatge i organització interna**

Aquesta estructura facilita el manteniment, millora l’eficiència energètica i permet escalar la infraestructura segons necessitats.

📷 **[Veure imatge dels racks](URL)**

# Infraestructura IT

Per desenvolupar aquesta proposta, s’han investigat les tendències actuals en hardware per a centres de dades, utilitzant fonts fiables com especificacions de fabricants (Dell, Cisco, Panduit) i estàndards de la indústria. S’han prioritzat components que equilibren rendiment, eficiència energètica i sostenibilitat, considerant les necessitats específiques d’Innovate Tech. La selecció s’ha centrat en hardware compatible amb un entorn híbrid (núvol i local) per maximitzar l’escalabilitat i minimitzar l’impacte ambiental.

## Servidor: Dell PowerEdge R670

**Especificacions tècniques:**
- **Processador:** 2x Intel Xeon Scalable de 4a generació (32 nuclis per CPU, 2.1 GHz)
- **Memòria RAM:** 256 GB DDR5, escalable fins a 8 TB
- **Emmagatzematge:** 4x SSD NVMe de 3.84 TB en RAID 10
- **Eficiencia energètica:** Dell Smart Cooling i OpenManage Power Manager

**Propòsit:**
- Serveis web i transcodificació de vídeo en temps real
- Suport per a àudio i compartició de dades

### Sostenibilitat:

#### ODS 7:
- **Fonts d'alimentació de categoria Titanium:** Eficiència >94%
- **OpenManage Power Manager:** Monitoratge i optimització del consum
- **Dell Smart Cooling:** Reducció de fins a un 20% del consum de refrigeració

#### ODS 12:
- **Disseny modular:** Facilita l’actualització sense substituir tot l’equip
- **Materials reciclables:** Programes com Dell Asset Recovery Services

#### ODS 13:
- **Materials i processos sostenibles:** Alumini reciclat redueix fins a un 95% d’emissions respecte alumini verge

**Justificació:**  
Els PowerEdge R760 són ideals per gestionar entre 8000 i 9500 connexions simultànies amb un rendiment alt, mantenint l’eficiència energètica i escalabilitat modular (ODS 9).

---

## Patch Panels: HYCONNECT HPP-94802F

**Especificacions tècniques:**
- **48 ports RJ45 Cat6** (fins a 10 Gbps)
- **Compatibilitat:** Cat6
- **Disseny modular** amb ports numerats

**Propòsit:**
- Organització de connexions de xarxa entre servidors, switches i dispositius auxiliars
- Suport per a streaming 2K de 8000-9500 connexions simultànies (48-57 Gbps)

### Sostenibilitat:

#### ODS 7:
- Component passiu, no consumeix energia

#### ODS 12:
- Disseny modular i materials reciclables (plàstics/metalls reutilitzables)

#### ODS 13:
- Menor extracció de recursos, disseny compacte per eficiència energètica

---

## Switches: Cisco Nexus 93600CD-GX (2 unitats)

**Especificacions tècniques:**
- **28 ports 100/400GbE QSFP-DD + 8 ports 10/25GbE SFP28**
- **Capacitat total:** 12.8 Tbps
- **Característiques:** VXLAN, EVPN, segmentació de xarxa, Cisco EnergyWise

**Propòsit:**
- Gestió del tràfic de 48-57 Gbps de 8000-9500 connexions simultànies
- Connexió amb núvols (AWS/Google Cloud)
- Latència <1 ms i alta fiabilitat

### Sostenibilitat:

#### ODS 7:
- Fonts d’alimentació d’alta eficiència (92%+)
- Cisco EnergyWise: Reducció fins a un 15% del consum en ports inactius

#### ODS 12:
- Disseny escalable per evitar substitucions
- Materials reciclables i programes de reciclatge

#### ODS 13:
- Fabricació amb menor petjada de carboni

🔗 **Enllaç oficial:**  
[Cisco Nexus 93600CD-GX Switch](https://www.cisco.com/site/us/en/products/networking/switches/nexus-9000-series-switches/index.html)

---

## Planells i diagrames

📷 **[Vista esquemàtica de la sala del CPD](https://i.imgur.com/EsquemaSalaCPD.jpg)**  
📷 **[Distribució de racks i cablejat](https://i.imgur.com/DistribucioRacks.jpg)**  
📷 **[Flux d'aire i refrigeració](https://i.imgur.com/FluxRefrigeracio.jpg)**  
📷 **[Connexió entre servidors i switches](https://i.imgur.com/ConnexionsSwitches.jpg)**  


# Infraestructura Elèctrica

## Sistemes d’Alimentació Redundant

### Doble font d’alimentació externa
- Connexió a **dues línies elèctriques independents** (proveïdor principal i secundari).
- Cada línia connectada a un **quadro elèctric independent** amb **interruptors automàtics** de protecció contra sobrecàrregues i curtcircuits.

### Generador elèctric d’emergència
- **Tipus:** Generador dièsel de **100 kVA**
- **Cobertura:** Servidors, climatització, il·luminació i sistemes de seguretat.
- **Temps d’engegada:** 10-15 segons després de la pèrdua de corrent.
- **Dipòsit:** Autonomia per a **24 hores**, amb **contracte de reposició ràpida**.
- **Ubicació:** Àrea externa ventilada, protegida contra incendis i amb accés restringit.

## Distribució elèctrica interna

- Sistema de distribució amb **busbars** (barres conductores).
- Quadres de distribució amb **circuits segregats**:
  - Servidors (racks)
  - Climatització
  - Sistemes auxiliars
- **Cablejat:** Coure amb aïllament ignífug.
- **Capacitat màxima:** 80 kW

### Redundància N+1
- Per a **tots els components crítics** (transformadors, quadres elèctrics, SAIs).
- **Exemple:** Si es necessiten 2 transformadors, s’instal·len 3.

---

## SAI (Sistema d’Alimentació Ininterrompuda)

### Capacitat i especificacions
- **SAIs modulars**, capacitat total: **80 kVA**
  - 60 kW per servidors
  - 20 kW per climatització i sistemes auxiliars
- **Tecnologia:** Doble conversió online
- **Eficiència energètica:** ≥95% (ODS 7)

### Nombre de bateries

- **Tipus:** 
  - Plom-àcid segellades (VRLA)
  - Bateries de liti (Li-ion)

#### Càlcul de la càrrega
- **Consum estimat:** 80 kW  
- **Temps d’autonomia requerit:** 15 minuts  
- **Energia necessària:**  
  `80 kW × (15/60) h = 20 kWh`

#### Supòsit de bateries
- **Bateria tipus:** 48V, 100 Ah → 4,8 kWh/bateria  
- **Nombre mínim:** `20 kWh ÷ 4.8 = 4.16` → **5 bateries (amb marge)**

#### Configuració
- **2 bancs de bateries en paral·lel (N+1)**:
  - **3 bateries per banc**
  - Permet manteniment sense interrupcions

---

## Components addicionals

- **Mòduls de bypass automàtic**
- **Sistema de monitoratge remot**:
  - Estat de càrrega
  - Temperatura
  - Cicles de vida
  - Alertes en temps real
- **Armaris de bateries**:
  - Ventilació
  - Protecció contra incendis (RIPCI)

---

## Temps de funcionament sense corrent

- **Objectiu:** 15 minuts per servidors i sistemes crítics
- **Escalabilitat:** Possibilitat d’ampliació a 30 minuts afegint més bancs

---

## Sostenibilitat

- Ús de **bateries reciclables** amb **certificació de baix impacte ambiental**
- Configuració del SAI en **mode ECO** en càrregues baixes
- **Gestió responsable del reciclatge** de bateries amb un proveïdor autoritzat


# Seguretat Física del CPD

## 1. Elements de Control d’Accés

Per garantir la seguretat del CPD, cal implementar un sistema robust de control d’accés que restringeixi l’entrada només a personal autoritzat.

### Portes de seguretat amb tancament electromagnètic
- Portes blindades amb **tancaments electromagnètics**.
- Resistents a intrusions i amb **protecció contra incendis** (classificació RF-60 o superior).

### Sistemes d’autenticació biomètrica i/o targetes RFID
- **Lectors d’empremtes dactilars** o **escàners d’iris**.
- **Targetes RFID** personalitzades amb codis únics.
- **Doble factor d’autenticació**: combinació de biometria i PIN o targeta.

### Registre d’accessos
- Sistema centralitzat que **enregistra hora, data i identitat** de cada accés o intent.
- Integració amb software de gestió per monitoratge en temps real.

### Sala de control adjacent
- Sala propera amb **personal de seguretat** per verificar autoritzacions.

### Mesures per dificultar la identificació
- **Absència de senyalització externa** sobre el CPD.
- Portes **sense identificadors visuals** i acabats discrets.

---

## 2. Videovigilància

### Càmeres IP d’alta resolució
- Resolució mínima **4K** amb visió nocturna.
- Ubicació: entrades, passadissos, racks i zones perimetrals.
- **Angle de visió de 360°** o càmeres **PTZ**.

### Enregistrament i emmagatzematge
- Gravació contínua **24/7**.
- Emmagatzematge en **servidor dedicat** amb **RAID 5**.
- **Retenció de dades:** 30 dies (complint RGPD).

### Monitoratge en temps real
- Connexió amb **sala de control** per supervisió directa.
- **Alertes automàtiques** en cas de moviment no autoritzat.

### Seguretat del sistema
- **Xifratge de transmissió** de vídeo.
- Accés restringit amb **autenticació de dos factors**.

---

## 3. Sistemes de Prevenció, Detecció i Extinció d’Incendis

### Prevenció
- **Materials ignífugs** per parets, terres i sostres (RF-120).
- **Cablejat ignífug**, ordenat en safates.
- **Control climàtic**:
  - Temperatura: 18–27°C
  - Humitat relativa: 40–60%

### Detecció
- **Sensors de fum i calor** òptics i tèrmics (sostre i sota terra tècnic).
- **Sistemes d’alarma** visuals i sonors connectats al panell central.
- **Monitoratge contínua** via sistema BMS.

### Extinció
- **Gas net**: FM-200 o Novec 1230 (segurs per equips i persones).
- **Extintors manuals** de CO₂ i pols ABC, revisats periòdicament.
- **Tancament automàtic** de portes cortafocs.

---

## 4. Vies d’Evacuació

### Rutes clarament senyalitzades
- **Senyals lluminosos i reflectants** visibles fins i tot amb fum.
- Mínim de **dues sortides independents**, accessibles en menys de 50 m.

### Portes d’emergència
- Amb **barres antipànic**, obertura cap a l’exterior.
- Connexió directa a **escales protegides o zones segures**.

### Il·luminació d’emergència
- **Llums LED** amb bateries independents.
- Autonomia mínima: **2 hores**.

### Simulacres i formació
- **Pla d’evacuació documentat**.
- **Simulacres periòdics**.
- **Cartells informatius** amb plànol de sortida.

---

## 5. Diagrames, Planells i Fotografies

### Planells

#### Plànol de la sala del CPD
- Distribució de:
  - Portes de seguretat
  - Càmeres de videovigilància
  - Sensors de fum/calor
  - Extintors
  - Vies d’evacuació
- Ubicació dels sistemes de control d’accés.
- Escala recomanada: **1:100**

#### Diagrama de flux de seguretat
- Esquema del procés d’accés:
  - Autenticació
  - Registre
  - Verificació
- Connexions entre sistemes i sala de control.

### Diagrames

#### Diagrama de videovigilància
- Xarxa de càmeres IP
- Servidor d’enregistrament
- Protocols de xifratge i flux de dades

#### Diagrama del sistema antiincendis
- Sensors
- Alarmes
- Dipòsits de gas net
- Connexió al panell central

### Fotografies
- Imatges (reals o simulades) de:
  - Portes de seguretat amb biometria
  - Càmeres instal·lades
  - Extintors i senyals d’evacuació


# Seguretat Lògica

## 1. Restricció d’Accés per Autorització

### Control d’accés electrònic
- Instal·lació de **lectors de targeta d’identificació**.
- Només el **personal autoritzat** disposarà de targeta.
- La **persona responsable de la seguretat** haurà d’habilitar la targeta.
- Possibilitat d’**autoritzacions temporals**, també requeriran aprovació explícita.

### Registre d’accés (logs)
- Registre automàtic de:
  - **Hora d’entrada/sortida**
  - **Identitat de la persona**
  - **Motiu de l’accés** (si és possible)
- **Integració** amb sistemes de **control horari** o de **presència**.

---

## 2. Firewalls

### Política per defecte
- **Bloqueig total** inicial: només es permetrà el tràfic explícitament autoritzat.

### Regles per tràfic entrant (extern cap al CPD)
- **HTTP/HTTPS (ports 80 i 443)**:
  - Permetre només connexions cap a **servidors que hostegen plataformes de streaming**.
  
- **Ports de Streaming (RTSP, RTP, etc.)**:
  - Permetre només connexions de **clients autoritzats** (per ex. RTSP 554).

- **Bases de dades**:
  - Permetre tràfic exclusivament entre les **aplicacions de streaming i els servidors de base de dades**:
    - MySQL (3306)
    - PostgreSQL (5432)

- **SSH**:
  - Permetre només a **usuaris de confiança**.

- **Altres serveis**:
  - Permetre només els ports estrictament **necessaris pels serveis futurs**.

---

## 3. Monitorització

### Eines utilitzades
- **Nagios** i **Wireshark** per a monitorització de:
  - Xarxa
  - Bases de dades
  - Web

### Funcionalitats
- Alertes de **caigudes de serveis**.
- Revisió de **logs i esdeveniments**.
- **Anàlisi de dades** i **identificació de tendències** per a millores contínues.

---

## 4. Còpies de Seguretat / Backups

### Estratègia de còpies
- **Còpia completa**:
  - Diumenges a les **23:00** (moment de menor activitat).
  
- **Còpies diferencials**:
  - La resta de dies laborables.

### Tipus d’emmagatzematge
- **Dos tipus diferents**:
  - Discs durs locals
  - Emmagatzematge al núvol

- **Còpia fora de lloc**:
  - Garanteix la **recuperació de dades** en cas de desastre físic al CPD.

---

## 5. RAID (Redundant Array of Independent Disks)

### Configuració recomanada: **RAID 5**

#### Avantatges
- **Alta disponibilitat i redundància**:
  - Mitjançant **paritat distribuïda**, es pot recuperar la informació si un disc falla.

- **Ús eficient de l’espai**:
  - A diferència de RAID 1, no es redueix la capacitat total a la meitat.

- **Bon rendiment de lectura**:
  - Lectura paral·lela gràcies a la distribució de dades entre discos.

- **Cost i escalabilitat**:
  - Bona relació **cost/benefici**.
  - Possibilitat d’**afegir discos** per ampliar la capacitat.

---
# Sostenibilitat

## Optimització del consum d’energia

- Ús d’**energies renovables** i contractació d’**energia verda certificada**.
- Programació de tasques intensives (ex: backups, replicacions) en horaris de **tarifa reduïda**.
- Integració d’**energia solar**.
- Optimització de la distribució elèctrica per evitar conversions innecessàries d’**AC-DC-AC**.
- Implementació de **PDU intel·ligents** per mesurar el consum per rack o dispositiu.
- Automatització de l’activació/desactivació de recursos segons la càrrega.
- Alarmes per detectar **sobreconsum**, ineficiències o calor excessiu.
- Apagat o posada en **mode estalvi** dels equips no essencials fora d’hores punta.
- Ús de servidors, switches i equips amb certificació **Energy Star** o equivalents.

## Ús d’energia verda pel CPD

- Contractació d’un pla d’energia **100% renovable** (solar, eòlica, hidroelèctrica, etc.).
- Empreses d’energia verda recomanades: [Holaluz - Energia verda](https://www.holaluz.com/energia-verde)
- Integració d’energia solar per autoconsum.

## Estalvi en longitud de cablejat

- Organització dels racks i servidors a prop dels **commutadors de xarxa (switches)** i dels quadres elèctrics.
- Ús de càmeres de videovigilància **inalàmbrica** en comptes de cablejades.
- Agrupació dels equips que necessiten connexió entre ells per reduir la necessitat de cables llargs.
- Ús, si és possible, de **racks de comunicacions centrals** per minimitzar la dispersió del cablejat.

## Sistemes de circulació d’aire que aprofitin condicions naturals

- Sistema de ventilació natural que aprofita l’aire exterior quan la temperatura i humitat són adequades.
- L’aire fresc entra filtrat per canals controlats i circula per la sala mitjançant un flux natural, amb suport de ventiladors eficients si cal.
- L’aire calent s’expulsa cap a l’exterior, reduint al mínim el consum d’energia en refrigeració.

## Parada d’equips de comunicacions quan no hi ha càrrega

- Els equips de xarxa i comunicacions es configuren per aturar-se automàticament o reduir l’activitat en absència de trànsit de dades.
- Inclou ports de xarxa, servidors virtualitzats i dispositius redundants, evitant consum innecessari en hores de baixa activitat.

## Equips de baix consum energètic

- Servidors, switches i sistemes d’emmagatzematge seleccionats per la seva eficiència energètica (etiquetes Energy Star o equivalents).
- Aquests equips ofereixen el mateix rendiment amb menor consum elèctric i generen menys calor, reduint la necessitat de refrigeració.
