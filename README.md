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

