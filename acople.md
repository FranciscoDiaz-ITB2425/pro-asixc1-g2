# Estudi d'Autonomia del CPD d'Innovate Tech

## Introducció

Per determinar durant quant de temps podrien funcionar els servidors del Centre de Processament de Dades (CPD) d'Innovate Tech amb la configuració proporcionada, suposant una interrupció del subministrament elèctric i basant-se únicament en un sistema de suport (com ara un SAI o un generador), cal calcular el consum elèctric total dels tres racks i comparar-lo amb la capacitat d’un sistema de suport típic.

La infraestructura inclou:
- 3 servidors **Dell PowerEdge R760**
- 1 switch principal **Cisco Catalyst 9300-24S**
- 4 sub-switches **Cisco Catalyst 9200-48T**
- 1 patch panel **HYCONNECT HPP-94802F**
- 1 router **Cisco ISR 4451**
- 1 router **Cisco RV340**
- 1 NAS **Dell PowerVault ME5024**
- 6 **PDUs APC AP8881** (2 per rack)
- 3 racks de **42U**

---

## Etapa 1: Càlcul del consum elèctric per rack

### Components i consum estimat

- **Servidors Dell PowerEdge R760** (3 unitats):
  - Especificacions: 2x Intel Xeon Scalable 4a Gen, 512 GB DDR5, 8x SSD NVMe 3,84 TB, GPU NVIDIA H100.
  - Consum estimat: **~2 kW** per unitat.

- **NAS Dell PowerVault ME5024**:
  - 24x SSD 3,84 TB, 4x SFP28.
  - Consum estimat: **~0,6 kW**

- **Switch principal Cisco Catalyst 9300-24S**:
  - Consum estimat: **~0,2 kW**

- **Sub-switches Cisco Catalyst 9200-48T** (4 unitats):
  - Consum estimat: **~0,15 kW** per unitat (total: **~0,6 kW**)

- **Router principal Cisco ISR 4451**: **~0,3 kW**

- **Router Cisco RV340**: **~0,05 kW**

- **Patch panel HYCONNECT HPP-94802F**: **0 kW** (component passiu)

- **PDUs APC AP8881**: **~0,1 kW** per rack (2 unitats de 0,05 kW)

- **Ventiladors per rack**: **~0,2 kW** per rack

### Consum total per rack

- **Rack 1 (processament principal i xarxa central):**  
  `2 + 0,2 + 0 + 0,1 + 0,2 = 2,5 kW`

- **Rack 2 (emmagatzematge i processament secundari):**  
  `2 + 0,6 + 0,3 + 0,1 + 0,2 = 3,2 kW`

- **Rack 3 (xarxa d’empleats i processament addicional):**  
  `2 + 0,3 + 0,3 + 0,05 + 0,1 + 0,2 = 2,95 kW`

### Total consum CPD

**2,5 + 3,2 + 2,95 = 8,65 kW (~8650 W)**

---

## Etapa 2: Autonomia amb SAI

### Model de referència: APC Symmetra PX 10 kVA
- **Capacitat efectiva:** ~9 kW (factor potència 0,9)
- **Bateria estàndard:** 30 minuts a plena càrrega
- **Energia disponible:** 9 kW × 0,5 h = **4,5 kWh**
- **Cost estimat:** 10.000–15.000 USD

### Càlcul d’autonomia

- **CPD complet (8,65 kW):**  
  `4,5 ÷ 8,65 ≈ 0,52 h ≈ 31 minuts`

- **Només servidors (6 kW):**  
  `4,5 ÷ 6 ≈ 0,75 h ≈ 45 minuts`

### Amb SAI de 20 kVA (~9 kWh)

- **CPD complet:** `9 ÷ 8,65 ≈ 1,04 h ≈ 62 minuts`
- **Només servidors:** `9 ÷ 6 ≈ 1,5 h ≈ 90 minuts`
- **Cost estimat:** 20.000–30.000 USD

### Generador de suport

- Potència: **10–15 kVA**
- Cost: **~5000–10.000 USD**
- Arrencada: **1–2 minuts**
- Autonomia amb 100 litres de dièsel: **8–10 hores**

---

## Etapa 3: Temps de funcionament estimat

| Escenari                     | Autonomia estimada |
|-----------------------------|---------------------|
| SAI 10 kVA – CPD complet     | ~31 minuts          |
| SAI 10 kVA – Només servidors | ~45 minuts          |
| SAI 20 kVA – CPD complet     | ~62 minuts          |
| SAI 20 kVA – Només servidors | ~90 minuts          |
| Generador dièsel            | 8–10 hores (100L)   |

---

## Consideracions addicionals

- **Càrrega variable:** amb menys connexions (ex. 4000), el consum pot baixar a 4–5 kW, allargant l’autonomia.
- **Ventilació:** apagar ventiladors (estalvi de ~0,6 kW) pot estendre el temps, però amb risc d’escalfament.
- **Bateries:** es degraden amb el temps (~20% menys autonomia als 3–5 anys sense manteniment).

---

## Resum Final

Amb la configuració actual, el CPD consumeix **8,65 kW**. Amb un **SAI de 10 kVA**, el centre podria funcionar **31 minuts**, o **45 minuts si només es mantenen els servidors**. Amb un **SAI de 20 kVA**, s'arribaria fins a **90 minuts**. Per períodes més llargs, un **generador dièsel** pot garantir **8–10 hores** o més, depenent del combustible.

Els **31–33U lliures per rack (138–147 cm)** permeten ampliar la infraestructura amb SAIs o generadors addicionals en el futur.
