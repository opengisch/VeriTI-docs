Veriti non include strumenti per il backup e il restore della banca dati
utilizzata, perché è previsto che i dati vengano conservati sui server
cantonali accessibili tramite il portale cantonale e localmente sulla
macchina dell'utente i dati sono presenti solamente per il tempo della
modifica e in seguito vengono ricaricati sul portale. Se tuttavia
dovesse essere necessario fare un backup (rispettivamente un restore)
della banca dati, è possibile utilizzare gli strumenti forniti assieme a
PostgreSQL: `pg_dump` e `pg_restore`. Per una
documentazione completa ed esaustiva, vedere
<https://www.postgresql.org/docs/current/static/backup.html>. Pg_dump e
pg_restore sono due strumenti utlizzabili da linea di comando. Da
PgAdmin è possibile chiamare direttamente questi strumenti
dall'interfaccia grafica, tuttavia è stato riscontrato che in alcune
configurazioni non funziona. La soluzione sempre valida è quella di
lavorare da linea di comando. Di seguito vengono mostrati alcuni esempi
di comandi utili, per il resto, fare riferimento alla documentazione
ufficiale.

Per creare un backup della banca dati mydb nel file backup.bak:

``` {.bash org-language="sh"}
pg_dump -Fc -f backup.bak mydb
```

Per creare il backup dello schema myschema della banca dati
(corrispondente a un progetto Veriti)

``` {.bash org-language="sh"}
pg_dump -Fc -f backup.bak -n myschema mydb
```

Per ripristinare i backup:

``` {.bash org-language="sh"}
pg_restore -d mydb backup.bak
```