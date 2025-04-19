I vincoli di integrità tra dati sono stati realizzati sulla base di
quanto definito nel documento Descrizione del geodato e della sua
trasmissione al Cantone. Alcuni dei vincoli non è possibile realizzarli
perché comportano la lettura di altre banche dati del cantone non
accessibili. Ai vincoli cantonali sono stati aggiunti due vincoli
(Vincolo_A01 e Vincolo_A02) che aiutano nella verifica della correttezza
dei dati creati in VeriTi. I test, vengono eseguiti sui dati contenuti
nella banca dati di VeriTi, indipendentemente dai layer mostrati in
QGIS, tuttavia, la selezione dei risultati sbagliati è possibile solo
sui layer mostrati in QGIS.

| Vincolo       | Descrizione                                                                                             | Output in caso di errore / osservazioni                                                                                     |
| ------------- | ------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Vincolo 01    | Devono esserci dati nel file INTERLIS                                                                   | Messaggio                                                                                                                   |
| Vincolo 02    | Gli stati abrogazione/nuovo devono essere coerenti tra loro                                             | Messaggio e selezione degli elementi sbagliati nei layer del gruppo `tutte le geometrie`                       |
| Vincolo 03    | Se un oggetto è dichiarato in vigore allora deve esistere nella banca dati cantonale PR-PUC             | Non realizzabile senza accedere alla banca dati cantonale.                                                                 |
| Vincolo 04    | Se un oggetto è dichiarato in vigore allora deve avere questo stato nella banca dati cantonale PR-PUC   | Non realizzabile senza accedere alla banca dati cantonale.                                                                 |
| Vincolo 05    | Tutti gli attributi cantonali obbligatori devono essere specificati                                     | Messaggio e selezione degli elementi sbagliati nei layer Elemento comune e Zona comune                                    |
| Vincolo 06    | I valori degli attributi cantonali su domini devono essere conformi                                     | Messaggio e selezione degli elementi sbagliati nei layer Elemento comune e Zona comune                                    |
| Vincolo 07    | Una definizione nuova non può avere geometrie in vigore                                                 | Messaggio e selezione degli elementi sbagliati nei layer del gruppo `tutte le geometrie`                       |
| Vincolo 08    | Una definizione nuova non può avere geometrie abrogate                                                  | Messaggio e selezione degli elementi sbagliati nei layer del gruppo =tutte le geometrie                                   |
| Vincolo 09    | Una definizione abrogata deve essere in vigore nella banca dati SST                                     | Non realizzabile senza accedere alla banca dati cantonale.                                                                 |
| Vincolo 10    | Una definizione abrogata non può avere geometrie in vigore                                              | Messaggio e selezione degli elementi sbagliati nei layer del gruppo `tutte le geometrie`                       |
| Vincolo 11    | Una definizione abrogata non può avere geometrie nuove                                                  | Messaggio e selezione degli elementi sbagliati nei layer del gruppo `tutte le geometrie`                       |
| Vincolo 12    | Un nuovo piano grafico deve avere geometrie                                                             | Messaggio e selezione degli elementi sbagliati nel layer `Piano grafico`                                        |
| Vincolo 13    | Un piano grafico nuovo non può avere geometrie abrogate                                                 | Messaggio e selezione degli elementi sbagliati nei layer del gruppo `Tutte le geometrie`                       |
| Vincolo 14    | Un piano grafico abrogato non può avere geometrie nuove                                                 | Messaggio e selezione degli elementi sbagliati nei layer del gruppo `Tutte le geometrie`                       |
| Vincolo 15    | Un piano grafico abrogato deve essere in vigore nella banca dati SST                                    | Non realizzabile senza accedere alla banca dati cantonale.                                                                 |
| Vincolo 16    | Una geometria nuova deve essere associata ad almeno un piano grafico                                    | Messaggio e selezione degli elementi sbagliati nei layer del gruppo `Tutte le geometrie`                       |
| Vincolo 17    | Una geometria abrogata deve essere in vigore nella banca dati SST                                       | Non realizzabile senza accedere alla banca dati cantonale.                                                                 |
| Vincolo 18    | Una nuova geometria non può essere associata ad un piano grafico abrogato                               | Non realizzato. Uguale al Vincolo 14.                                                                                     |
| Vincolo 19    | Una geometria abrogata non può essere associata ad un piano grafico nuovo                               | Non realizzato. Uguale al Vincolo 13                                                                                       |
| Vincolo 20    | Le zone base del risultato intermedio non devono sovrapporsi                                            | Viene generato un layer di nome `Errori - Sovrapposizioni nelle zone base` contente tutte le porzioni di geometria che si sovrappongono. |
| Vincolo 21    | Le geometrie del risultato intermedio non devono avere duplicati                                        | Messaggio e selezione degli elementi sbagliati nei layer del gruppo `Tutte le geometrie`                       |
| Vincolo 22    | Non devono esistere vuoti pianificatori                                                                 | Viene generato un layer di nome `Errori - Vuoti nelle zone base`, contenente i buchi presenti nelle zone base. |
| Vincolo 23    | Una nuova definizione deve avere almeno una geometria nuova                                             | Messaggio e selezione degli elementi sbagliati nei layer `Elemento comune` e `Zona comune`         |
| Vincolo 24    | Una definizione in vigore deve avere almeno una geometria in vigore o nuova                             | Messaggio e selezione degli elementi sbagliati nei layer `Elemento comune` e `Zona comune`         |
| Vincolo A01   | Il tipo di attributo (Testo/Numero) deve essere rispettato                                              | Messaggio e selezione degli elementi sbagliati nei layer `Attributo elemento comune` e `Attributo zona comune` |
| Vincolo A02   | Tutti gli attributi definiti devono avere un valore                                                     | Messaggio e selezione degli elementi sbagliati nei layer `Attributo elemento comune` e `Attributo zona comune` |
