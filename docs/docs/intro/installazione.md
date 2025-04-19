## QGIS

Scaricare e installare QGIS secondo le indicazioni di
<http://www.qgis.org>.

## PostgreSQL

Scaricare e installare PostgreSQL secondo le indicazioni di
<https://www.postgresql.org/>.

## PostGIS 3.1

Per installare PostGIS è sufficiente digitare all\'interno di una query
shell, ad esempio in `pgAdmin`, il seguente comando:

``` {.bash org-language="sh"}
CREATE EXTENSION postgis;
```

## Veriti

Lanciare QGIS e aprire il gestore di plugin di QGIS, tramite il menu
`Plugins
   → Gestisci e installa plugin…`

Scegliere `Impostazioni`, `Aggiungi…` e inserire i
dati del repository contenente il plugin VeriTi: • Nome: Veriti
Repository (o qualsiasi altro nome) • URL:
<https://download.opengis.ch/repos/veriti/plugins.xml>

Premendo su OK, verranno richieste le credenziali del repository. A
questo punto scegliere `Tutto` nella barra a sinistra e
installare il Veriti. Chiudere e riaprire QGIS per applicare tutte le
modifiche effettuate.