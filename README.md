# alea-hotels

Ce projet associe des **hôtels** (avec coordonnées GPS) aux **zones d’aléa retrait-gonflement des argiles** en France, à partir des données de Géorisques.  
L’objectif est de déterminer, pour chaque hôtel, s’il se trouve dans une zone d’aléa _Faible_, _Moyen_ ou _Fort_, ou hors des zones cartographiées.

---

## Données

- **Shapefile d’aléa argiles**  
  - Exemple : `AleaRG_Fxx_L93/ExpoArgile_Fxx_L93.shp`  
  - CRS d’origine : `EPSG:2154` (RGF93 / Lambert-93)  
  - Champs principaux :
    - `DPT` : code département  
    - `NIVEAU` : niveau d’aléa numérique (`1 = Faible`, `2 = Moyen`, `3 = Fort`)  
    - `ALEA` : niveau d’aléa textuel (`Faible`, `Moyen`, `Fort`)

- **Données hôtels**  
  - DataFrame / CSV avec au moins les colonnes :
    - `Hotel_ID`
    - `Hotel_name`
    - `region`
    - `type_loca`
    - `Latitude`
    - `Longitude`

---

## Installation

Cloner le dépôt :

```bash
git clone https://github.com/faresTMZ/alea-hotels.git
cd alea-hotels
