# Dati_Astronomici
Database delle costanti astronomiche.
# Dati_Astronomici
Database delle costanti astronomiche.

## Descrizione
Questo repository ospita i file di dati necessari per il calcolo preciso del tempo astronomico, della posizione solare e dell'equazione del tempo. I dati sono strutturati per essere letti direttamente da applicazioni Python e Android.

## Contenuto del Repository
* **`Bulletin_A.csv`**: Contiene i valori di `UT1-UTC` (DUT1) indicizzati per MJD (Modified Julian Day). Questi dati sono fondamentali per il calcolo del Delta T ($\Delta T$).
* **`Bulletin_A_2.csv`**: Contiene le costanti globali `TT-TAI` e `TAI-UTC` (secondi intercalari).

## Origine dei Dati
I dati relativi ai file Bulletin_A.csv e Bulletin_A_2.csv sono derivati dalle pubblicazioni ufficiali dello **IERS** (International Earth Rotation and Reference Systems Service).

## Utilizzo (Python)
I file possono essere letti direttamente tramite `pandas` utilizzando l'URL "Raw" di GitHub:

```python
import pandas as pd

url = "[https://raw.githubusercontent.com/TUO_UTENTE/Dati_Astronomici/main/Bulletin_A.csv](https://raw.githubusercontent.com/TUO_UTENTE/Dati_Astronomici/main/Bulletin_A.csv)"
df = pd.read_csv(url, sep=";", index_col="MJD")
