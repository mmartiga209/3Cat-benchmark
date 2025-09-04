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


## 🚀 Com executar els projectes

Cada projecte inclòs al repositori segueix un patró bàsic de funcionament:

1. **Backend**  
   - Desplaça’t al directori del projecte corresponent.  
   - Executa el fitxer `server.py` per aixecar el servidor backend:  
     ```bash
     python server.py
     ```
   - Per defecte, el servidor s’aixeca en un port local (normalment `http://localhost:8000/`).  

2. **Frontend**  
   - Un cop el servidor està actiu, obre el fitxer `index.html` (o equivalent) situat al directori de *frontend*.  
   - El navegador es connectarà al servidor i l’aplicació es podrà utilitzar amb normalitat.  

3. **Pujar el servidor (entorn de producció)**  
   - Canvia la configuració del port i/o host al fitxer `server.py` perquè escolti en la IP pública o al port requerit (per exemple `0.0.0.0:8080`).  
   - Revisa els paràmetres habituals de seguretat i desplegament (firewall, gestor de processos com `pm2` o `gunicorn`, etc.).  

---

✍️ Aquest repositori serveix com a **marc de referència per mesurar i comparar el rendiment de models de llenguatge** aplicats a la classificació de notícies segons els criteris periodístics de 3Cat.
