Di seguito sono elencati i gruppi di layer e i layer cce vengono caricati
in QGIS da VeriTi. I layer rappresentano le tabelle del modello
cantonale. Vengono caricate in QGIS come layer anche le tabelle che non
contengono geometrie.

## Simboli

Questo gruppo contiene i layer con i dati dei simboli. Gli elementi di
questi layer sono defniti dal cantone e non è previsto cce vengano
modifcati dall'utente.

| Layer | Geometrie | Modificabile | Tabella database |
| --- | --- | --- | --- |
| Simboli| No| No| t_simbolo|
| Categorie| No| No| t_categoria_simbolo|
| Famiglie|  No| No| t_famiglia_simbolo|

## Piani grafici

Questo gruppo contiene il layer con la definizione dei piani grafici e i
layer che rappresentano le associazioni tra geometrie e piani grafici (e
simboli).

| Layer | Geometrie | Modificabile | Tabella database |
| --- | --- | --- | --- |
| Piani grafici|  No| Sì| t_piano_grafico|
| Elemento punto -- piano grafico| No| Sì| t_elemento_punto_piano_grafico|
| Elemento linea -- piano grafico| No| Sì| t_elemento_linea_piano_grafico|
| Elemento poli -- piano grafico|  No| Sì| t_elemento_poli_piano_grafico|
| Testo -- piano grafico|No|Sì| t_testo_piano_grafico|
| Zona base -- piano grafico| No|Sì| t_zona_base_piano_grafico|
| Zona sovr -- piano grafico| No|Sì| t_zona_sovr_piano_grafico|

## Definizioni cantonali

Questo gruppo contiene tutti i layer che riguardano le definizioni
cantonali. Gli elementi di questi layer sono definiti dal cantone e non
è previsto che vengano modificati dall'utente.

| Layer | Geometrie | Modificabile | Tabella database |
| --- | --- | --- | --- |
| Elemento cantone| No|No| t_elemento_cantone|
| Def elemento cantone| No|No| t_def_elemento_cantone|
| Elemento CH| No|No| t_elemento_ch|
| Elemento cantone att cantone| No|No| t_elemento_cantone_att_cantone|
| Attributo cantone|  No|No| t_attributo_cantone|
| Valore attributo cantone|No|No| t_valore_attributo_cantone|
| Zona cantone|No|No| t_zona_cantone|
| Def zona cantone| No|No| t_def_zona_cantone|
| Zona CH|No|No| t_zona_ch|
| Zona cantone att cantone|No|No| t_zona_cantone_att_cantone|

## Definizioni comunali

Questo gruppo contiene tutti i layer che riguardano le definizioni
comunali.

| Layer | Geometrie | Modificabile | Tabella database |
| --- | --- | --- | --- |
| Elemento comune| No|Sì| t_elemento_comune|
| Attributo elemento comune| No|Sì| t_attributo_elemento_comune|
| Zona comune|   No|Sì| t_zona_comune|
| Attiributo zona comune| No|Sì| t_attributo_zona_comune|

## Geometrie divise per piano grafico

Nel gruppo `Geometrie divise per piano grafico`{.verbatim}, sono
presenti i layer che contengono delle geometrie, suddivisi in
sottogruppi, uno per piano grafico. Lo stesso oggetto può essere
presente in più sottogruppi se lo stesso è attribuito a più piani
grafici. Viene aggiunto anche un ulteriore gruppo chiamato
`PG non definito`{.verbatim}, dove sono presenti i layer che contengono
geometrie non (ancora) associate ad un piano grafico. La scelta di
raggruppare per piano grafico, è stata fatta per semplificare l'utilizzo
da parte dell'utente e permettere la rappresentazione dello stesso
oggetto con simboli differenti a seconda del piano grafico sul quale
viene rappresentato.

| Layer | Geometrie | Modificabile | Tabella database |
| --- | --- | --- | --- |
| Testo - ...| Sì|Sì| tgeo_testo|
| Elemento punto - ...| Sì|Sì| tgeo_elemento_punto|
| Elemento linea - ...| Sì|Sì| tgeo_elemento_linea|
| Elemento poligono - ...| Sì|Sì| tgeo_elemento_poligono|
| Zona sovrapposta - ...|  Sì|Sì| tgeo_zona_sovrapposta|
| Zona base - ...| Sì|Sì| tgeo_zona_base|

## Tutte le geometrie

Nel gruppo `Tutte le geometrie`{.verbatim}, è presente un layer per tipo
di geometria, contente tutte le geometrie di quel tipo, senza
suddivisione per piano grafico.

| Layer | Geometrie | Modificabile | Tabella database |
| --- | --- | --- | --- |
| Testo| Sì|Sì| tgeo_testo
| Elemento punto| Sì|Sì| tgeo_elemento_punto|
| Elemento linea| Sì|Sì| tgeo_elemento_linea|
| Elemento poligono| Sì|Sì| tgeo_elemento_poligono|
| Zona sovrapposta|  Sì|Sì| tgeo_zona_sovrapposta|
| Zona base| Sì|Sì| tgeo_zona_base|

## Altre informazioni

Per maggiori informazioni sulla struttura e il contenuto del modello
dati, è possibile consultare il manuale del cantone
`Descrizione del geodato e della
|  sua trasmissione al Cantone`. |