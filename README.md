# 📰 3Cat-benchmarking

Aquest repositori conté dues llibretes (*notebooks*) que permeten **avaluar models de llenguatge en la classificació de notícies** segons els criteris del llibre d’estil de 3Cat.  

Els criteris avaluats són:
- **Pluralisme**
- **Diversitat**
- **Minories**
- **Paritat**
- **Compromís**
- **Veracitat**
- **Imparcialitat**

Aquests criteris corresponen directament a les seccions del llibre d’estil de 3Cat.  

L’objectiu del repositori és oferir una eina per **comparar diferents models de llenguatge** en la tasca de classificació periodística. S’han fet proves amb els models *4.5* i *4.1*, i es proporcionen resultats de referència. A partir d’aquí, és possible generar nous resultats amb altres models i **comparar-los amb els de referència**.

---

## 📂 Estructura del repositori

### `prompts/`
Conté les **prompts** dels criteris del llibre d’estil en format `.txt`.  
Si es volen modificar els criteris o les instruccions, cal editar aquests fitxers.

### `resultats/`
Inclou les **sortides dels experiments en format JSON**.  
A partir d’aquests fitxers es poden fer comparatives entre models.

### 📒 Notebooks
- **`benchmark.ipynb`** → Executa els benchmarks automàticament a partir dels prompts.  
- **`comparison.ipynb`** → Genera comparatives entre resultats i mostra gràfics.  

### 📄 Altres
- **`README.md`** → Documentació del repositori.  

---

## ⚙️ Funcionament

El flux de treball del repositori es divideix en dues fases principals: **generació d’avaluacions** i **comparació de resultats**.

### 1. Generar resultats amb `benchmark.ipynb`
- Aquest notebook serveix per **executar les proves amb el model que es vulgui avaluar**.  
- Està implementat amb **LangChain**, per tant, només cal **seleccionar el model** a la part indicada al principi del notebook.  
- Després, cal **executar totes les cel·les de dalt a baix**.  
- L’última cel·la permet **guardar els resultats en un fitxer JSON** dins la carpeta `resultats/`.  
- És important **assignar un nom clar al fitxer** per identificar a quin model correspon.  
- Un cop obtingut el JSON, ja es pot passar al pas de comparació.

### 2. Comparar resultats amb `comparison.ipynb`
- Aquest notebook permet **comparar dues avaluacions diferents**.  
- Al principi del notebook es poden **seleccionar dos fitxers JSON** de la carpeta `resultats/`.  
- En executar totes les cel·les, es mostren:
  - **Comparacions numèriques** entre els models.  
  - **Gràfics visuals** per entendre millor les diferències.  
- Es recomana utilitzar com a **model de referència** el JSON del *4.5* o del *5*, i comparar-lo amb el nou model generat.  

Així es pot veure **com es comporta un nou model en relació amb els models de referència** i valorar-ne els punts forts i febles.

---

✍️ Aquest repositori serveix com a **marc de referència per mesurar i comparar el rendiment de models de llenguatge** aplicats a la classificació de notícies segons els criteris periodístics de 3Cat.
