Veriti è un plugin QGIS, sviluppato da OPENGIS.ch. Veriti, permette di
importare i dati provenienti dal portale PR cantonale in QGIS per
modificarli e permette di verificare che i vincoli di integrità tra i
dati siano conformi alle direttive cantonali (documento Descrizione del
geodato e della sua trasmissione al Cantone).

## Releases

| Versione | Data | Modifiche |
| --- | --- | --- |
| 3.0.0 | 07.11.2019 | Prima versione per QGIS 3 |
| 3.0.1 | 11.11.2019 | Corregge creazione svg path su Windows |
| 3.0.2 | 11.11.2019 | Corregge errore encoding su Windows |
| 3.1.0 | 13.11.2019 | Validazione form nell\'import dialog, aggiunta di campi \"joinati\" con simbolo e piano grafico nelle geometrie, implementazione della funzione importa shapefile |
| 3.1.1 | 19.11.2019 | Mostra messaggi di errore comprensibili se non trova Java o non è la versione corretta |
| 3.2.0 | 20.11.2019 | Implementa la maschera per gestire gli attributi delle definizioni di zona e elemento |
| 3.2.1 | 22.11.2019 | Modifica il Vincolo 24. Adesso è: Una definizione in vigore deve avere almeno una geometria in vigore *o nuova* |
| 3.3.0 | 27.11.2019 | Corregge un problema che impediva di copiare geometrie e aggiunge il pulsante per ricreare tutte le relazioni con i piani grafici |
| 3.3.1 | 28.11.2019 | Corregge errore encoding su Windows durante export e chiede di esportare solamente come `.itf` |
| 3.3.2 | 24.01.2020 | Corregge l\'errore quando si seleziona un simbolo se nessuna geometria di una determinata definizione di elemento comunale è assegnata a un piano grafico |
| 3.3.3 | 20.02.2020 | Corregge errore in attributi elemento |
| 3.3.4 | 20.02.2020 | Imposta titolo del progetto |
| 3.3.5 | 24.03.2020 | Corregge problema con valori vuoti nella tabella gestione attributi e altre piccole correzioni |
| 3.3.6 | 06.05.2020 | Nuovo link per la documentazione (<http://veriti.opengis.ch/>) |
| 3.4.0 | 21.10.2021 | Compatibilità con VeriGR |
| 3.4.1 | 21.10.2021 | Modifiche documentazione e deploy script |
| 3.4.2 | 21.10.2021 | VeriGR |
| 3.4.3 | 26.10.2021 | Aggiunta simbologia VeriGR |
| 3.4.4 | 02.11.2021 | Gestione automatica simbologia VeriGR |
| 3.4.5 | 05.11.2021 | Simbologia usando Darstellencode in VeriGR |
| 3.4.7 | 06.11.2021 | Installazione automatica di ili2pg migliorata |
| 3.4.8 | 26.11.2021 | Ignora Kantonalen Typen topics in VeriGR export |
| 3.4.9 | 26.11.2021 | Imposta widgets e valori di default in VeriGR |

## Requisiti tecnici

- QGIS 3 (3.4 o superiore)
- Java JDK `1.8.0`
- PostgreSQL 9.4 o superiore (massimo versione 11 per attuale
    incompatibilità con QGIS (novembre 2019)) con estensione PostGIS
    (3.1)

## Definizione dei termini

- Veriti
- Progetto QGIS
- Modello INTERLIS
- File data transfer INTERLIS