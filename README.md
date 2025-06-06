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
inserisci tutto nella stessa cartella

.
├── main.py                   # Script principale
├── ESEMPIO.docx              # Documento di input (da pulire)
├── ESEMPIO_FILTRATO.docx     # Documento intermedio dopo pulizia
└── RES_FINALE.docx           # Risultato finale (parlanti unificati) questo e quello da usare

🚀 Come si usa
Inserisci il file .docx da elaborare nella cartella del progetto. Puoi chiamarlo ESEMPIO.docx oppure cambiare il nome nel codice.

Esegui lo script:
```bash
python main.py

Verranno generati:
ESEMPIO_FILTRATO.docx: documento filtrato e pulito
RES_FINALE.docx: documento finale, ottimizzato e leggibile

🔧 Personalizzazione
🧠 Riconoscimento parlanti
Apri main.py e vai a questa sezione:

python

francesca_pattern = re.compile(r'^FRANCESCA BELLESIA$', re.IGNORECASE)
alina_pattern = re.compile(r'^ALINA KOSTIUK$', re.IGNORECASE)

Per aggiungere un nuovo interlocutore:
Modifica
nuovo_pattern = re.compile(r'^NOME COGNOME$', re.IGNORECASE)

🧹 Rimozione frasi brevi/inutili
Nel blocco frasi_inutili, puoi aggiungere o togliere termini considerati "rumore":

frasi_inutili = {
    "ok", "hmm", "yes", "no", "yeah", "sure", "right", "i see", "thanks",
    "thank you", "interesting", "mh", "uh huh", "exactly", "mhm", "mm",
    "va bene", "perfetto"
}

🔧 Soglia per blocchi da ignorare
Puoi modificare il numero minimo di caratteri richiesti per considerare un blocco "utile".
Nel main script, cambia col numero che preferisci:
pulisci_docx_con_blocchi(input_file, output_file, soglia_caratteri=40)

