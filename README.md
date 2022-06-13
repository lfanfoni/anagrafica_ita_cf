# anagrafica_ita_cf
Gruppo di domande Limesurvey 3.X in lingua Italiano (default) con domande su dati anagrafici, con autocomplete per il luogo di nascita (compresi stati esteri e comuni cessati) e controllo non bloccante sul codice fiscale.

Il gruppo di domande contiene le seguenti domande (tra parentesi i codici di domanda):
- Nome (codice Qnome).
- Cognome (codice Qcognome).
- Codice Fiscale (codice Qcodfis): contiene controllo sintattico con espressione regolare su posizione di numeri e lettere del codice fiscale. Vedi impostazione di logica/equazione di convalida.
- Data di nascita (codice Qdatanascita).
- Luogo di nascita (codice Qluogonascita): domanda con script di aurocompletamento del testo per selezionare i Comuni (compresi i cessati) italiani e gli Stati Eesteri (compresi i cessati) da una lista in formato csv (luoghi_nascita.csv) da caricare nella sottocartella "files" della survey. In alternativa si può modificare lo script e farlo puntare alla risorsa online (seguire le istruzioni nei commenti dello script). Se si cerca e seleziona la stringa "Non trovato", viene visualizzata la domanda successiva. Gli ultimi 4 caratteri delle voci in elenco rappresentano il cosiddetto "codice catastale" e consente di effettuare il controllo di congruenza con il codice fiscale.
- Altro luogo di nascita (codice Qaltroluogo): viene mostrato solo se si seleziona "Non trovato" nell'elenco dei luoghi di nascita
- Sesso (codice Qsesso).
- Testo di controllo del codice fiscale (codice txtCheckCF): viene visualizzato solo se i controlli di congruenza tra codice fiscale, nome, cognome, sesso, data e luogo di nascita, hanno esito negativo. Il controllo non è bloccante, dal momento che sono possibili casi di falsi errori relativamente al codice fiscale.

Installazione:
- Importare il file dati_anagrafici_ita.lsg in una survey già creata nella versione 3.X di Limesurvey. Da verificare la compatibilità con la versione 4.
- Fare l'upload del file luoghi_nascita.csv nella sottocartella "files" della survey dove si è importato il gruppo. Per effettuare questa operazione con le funzioni standard di LimeSurvey, andare sulle Impostazioni di indagine (tab a sinistra) e fare click sulla voce Risorse posta in basso nel menù di sinistra.
- E' possibile evitare l'upload del file csv e utilizzare il csv online con le voci dei luoghi di nascita. Per questa operazione, andare in modifca della domanda codice Qluogonascita, visualizzare il sorgente di domanda, e seguire le istruzioni contenuti nei commenti del javascript.
- Per definire un file csv personalizzato su altra posizione, operare sempre sul javascript come nel punto precedente.


 
 
 

