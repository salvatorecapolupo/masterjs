# 🚀 Dal Suono allo Spazio: JavaScript in Contesti PRO
**Progetto di Laboratorio TPSIT - Classe 5EL**

Questo repository contiene il codice sorgente e la documentazione per il percorso laboratoriale che esplora le capacità avanzate di JavaScript nel browser: dall'ingegneria del suono (Web Audio API), alla grafica 3D (Three.js), fino all'elaborazione di dati scientifici reali (NASA API).

---

## 📂 Struttura del Progetto

Il progetto è diviso in tre macro-aree tematiche:

### 🎵 1. Audio Engineering (Web Audio API)
Visualizzazione in tempo reale del flusso audio del microfono.

* **`oscilloscopio.html`**
    * **Cosa fa:** Visualizza l'onda sonora nel **dominio del tempo**.
    * **Tecnica:** Usa `analyser.getByteTimeDomainData()` e disegna su Canvas HTML5 usando vettori (`moveTo`, `lineTo`).
    * **Feature:** Include il *Kill Switch* per spegnere fisicamente il microfono e rilasciare le risorse hardware.
* **`spettroscopio.html`**
    * **Cosa fa:** Visualizza le frequenze (Bassi, Medi, Alti) nel **dominio della frequenza**.
    * **Tecnica:** Usa `analyser.getByteFrequencyData()`.
    * **Design:** Implementa una colorazione dinamica **HSL** (Arcobaleno) e un effetto "ghosting" (scia) per rendere l'animazione fluida.

### 🧊 2. Il Mondo 3D (Three.js)
Creazione e manipolazione di oggetti in uno spazio tridimensionale.

* **`monitor2.html` (Hello World 3D)**
    * **Cosa fa:** Setup base di una scena 3D con testo fluttuante.
    * **Ingredienti:** Scene, PerspectiveCamera, WebGLRenderer.
* **`monitor3.html` (Interattività Avanzata)**
    * **Cosa fa:** Permette di modificare il testo 3D e muovere una luce in tempo reale.
    * **Controlli:**
        * **Regex:** Impedisce l'inserimento delle lettere 'P' e 'R' (filtro input).
        * **Luci:** Slider per muovere una `PointLight` sugli assi X e Y.

### 🪐 3. Dati Reali & Matematica (NASA API)
* **`monitor1.html`**
    * **Cosa fa:** Scarica dati reali sugli asteroidi "Near Earth Objects" dalla NASA.
    * **Tecnica:**
        * **Async/Await:** Gestione asincrona delle chiamate di rete.
        * **.map():** Trasformazione dei dati JSON grezzi.
        * **Trigonometria:** Usa `Math.cos` e `Math.sin` per disporre gli asteroidi in orbita circolare attorno alla Terra.

### 📄 4. Documentazione
* **`presentazione.tex`**
    * Sorgente LaTeX (Beamer) per la presentazione finale.
    * Tema: *Madrid/Beaver* con palette colori personalizzata ad alto contrasto (Dark Mode).

---

## 🛠️ Tecnologie Utilizzate

* **HTML5 & CSS3:** Struttura e layout responsive (Flexbox, Grid).
* **JavaScript (ES6+):**
    * `Web Audio API` (Analisi segnale).
    * `Three.js` (Rendering 3D).
    * `Fetch API` & `Async/Await` (Networking).
    * `Regex` (Validazione stringhe).
* **LaTeX:** Per la produzione delle slide.

---

## 🚀 Istruzioni per l'uso

### Per i file Web (.html)
Basta trascinare i file all'interno di un browser moderno (Chrome, Edge, Firefox).

> **⚠️ Nota Importante sulla Privacy:**
> I file audio richiederanno il permesso di usare il microfono. Se il browser blocca l'accesso, è consigliabile usare l'estensione **Live Server** di VS Code o un server locale Python (`python -m http.server`).

### Per la Presentazione (.tex)
Il file `.tex` richiede un compilatore LaTeX (come TeX Live o MiKTeX).
1.  Aprire il file su **Overleaf** (consigliato) o in un editor locale.
2.  Impostare il compilatore su `pdflatex`.
3.  Compilare per generare il PDF.

---

## 🧠 Concetti Chiave (Cheat Sheet)

* **Kill Switch:** `stream.getTracks().forEach(t => t.stop())` -> Spegne il LED rosso della webcam/mic.
* **Ghosting:** Usare un `fillRect` semitrasparente invece di `clearRect` per creare scia.
* **Mesh:** Geometria (Forma) + Materiale (Colore/Riflesso).
* **Canvas:** La "tela" di pixel su cui JavaScript disegna.

---

**Autori:** Classe 5EL - TPSIT
**Professore:** Prof. Capolupo
**Data:** Febbraio 2024
