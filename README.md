# Synchrone Helfer-Systeme für effiziente Quantenschlüsselverteilung
**Autorin**: Nathalia Lietuvaite  

## Abstract
Dieses Projekt präsentiert ein neuartiges Kommunikationsprotokoll, das klassische Signalverarbeitung mit Quantenverschränkung kombiniert, um eine **100% effiziente Quantenschlüsselverteilung (QKD)** zu ermöglichen. Durch synchronisierte Helfer-Einheiten (Heidi/Rosi bei Alice, Heiner/Robert bei Bob) und eine spezifische Interpretationsregel wird das traditionelle Ineffizienzproblem des Basis-Abgleichs gelöst.

## Systemarchitektur
### Komponenten
- **Quantenquelle**: Erzeugt verschränkte Photonenpaare
- **Alices Station**:
  - Messgerät: Detektiert Polarisation (H ≡ ROT, V ≡ GRÜN)
  - Helfer-Einheiten:
    - *Heidi*: Aktiviert bei H-ROT-Messung
    - *Rosi*: Aktiviert bei V-GRÜN-Messung
- **Bobs Station**:
  - Messgerät: Identisch zu Alice
  - Helfer-Einheiten:
    - *Heiner*: Aktiviert bei H-ROT-Messung
    - *Robert*: Aktiviert bei V-GRÜN-Messung

### Protokollablauf
```mermaid
graph TD
    Q[Quantenquelle] -->|Photon A| A[Alice Messung]
    Q -->|Photon B| B[Bob Messung]
    A -->|ROT| H[Heidi aktiv]
    A -->|GRÜN| R[Rosi aktiv]
    B -->|ROT| H2[Heiner aktiv]
    B -->|GRÜN| R2[Robert aktiv]
