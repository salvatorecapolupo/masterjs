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
    * **Design:** Implementa una colorazione dinamica **HSL** (Arcobaleno) e un effetto "ghosting" (scia) per rendere l'animazione
