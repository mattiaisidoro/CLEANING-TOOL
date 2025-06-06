# CLEANING-TOOL
# 🎙️ DOCX Dialog Cleaner

Script Python per ripulire e organizzare trascrizioni `.docx` di conversazioni.  
Riconosce automaticamente i parlanti, unisce le frasi consecutive, elimina interruzioni inutili (es. "ok", "mh", ecc.) e produce un documento ordinato e leggibile.

---

## ✨ Funzionalità principali

- ✅ Riconoscimento automatico degli interlocutori (es. `FRANCESCA BELLESIA`, `ALINA KOSTIUK`)
- ✅ Unione dei blocchi di testo consecutivi dello stesso speaker
- ✅ Eliminazione di timestamp (es. `0:45`, `1 h 20 m`, `30 s`)
- ✅ Rimozione automatica di frasi brevi, inutili o di riempimento
- ✅ Esportazione finale in un file `.docx` pulito e leggibile

---

## 📦 Requisiti

### Software necessario

- Python **3.6 o superiore**

### Librerie Python da installare

```bash
pip install python-docx


📁 Struttura del progetto
bash
Copia
Modifica
.
├── main.py                   # Script principale
├── ESEMPIO.docx              # Documento di input (da pulire)
├── ESEMPIO_FILTRATO.docx     # Documento intermedio dopo pulizia
└── res_finale.docx           # Risultato finale (parlanti unificati)
