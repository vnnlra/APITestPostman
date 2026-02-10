# Introduzione a Postman

In questa attività useremo **Postman**, uno strumento professionale utilizzato per **testare API HTTP**.

Postman permette di inviare richieste a un server e di analizzare le risposte **senza scrivere codice**.  
Lo useremo come *client*, mentre il server sarà già pronto (API pubbliche).

L’obiettivo non è “imparare Postman”, ma **capire come funzionano le API REST**.

---

## Cos’è Postman (in pratica)
Postman è un **client HTTP** che consente di:
- inviare richieste `GET`, `POST`, `PUT`, `DELETE`
- specificare URL, header e body
- ricevere e leggere le risposte del server
- osservare **status code** e **dati JSON**

Postman simula il comportamento di un programma client (browser, app, frontend), ma in modo più controllato e tecnico.

---

## Perché lo usiamo
Useremo Postman per:
- capire come un client comunica con un server
- testare un’API **prima** di avere un’applicazione completa
- verificare se un servizio funziona correttamente
- osservare cosa succede quando i dati sono corretti o sbagliati

Questo è il modo in cui le API vengono testate anche nel mondo professionale.

---

## Struttura di una richiesta HTTP
Ogni richiesta che invieremo con Postman è composta da:

1. **Metodo HTTP**
   - `GET` → richiede dati
   - `POST` → invia dati
   - `PUT` → modifica dati
   - `DELETE` → elimina dati

2. **URL**
   - indirizzo della risorsa sul server  
     (es. `/posts`, `/users/3`)

3. **Header** (opzionali)
   - informazioni aggiuntive sulla richiesta

4. **Body** (solo per alcuni metodi)
   - dati inviati al server, spesso in formato JSON

---

## Le risposte del server
Dopo aver inviato una richiesta, il server risponde con:

- **Status code**
  - `200 OK` → richiesta corretta
  - `201 Created` → risorsa creata
  - `400 Bad Request` → errore del client
  - `404 Not Found` → risorsa inesistente
  - `500 Internal Server Error` → errore del server

- **Body della risposta**
  - spesso in formato **JSON**
  - contiene i dati richiesti o un messaggio di errore

Imparare a leggere la risposta è più importante che “ottenere il risultato”.

---

## JSON: non è testo, è struttura
Il formato JSON rappresenta dati strutturati:
- oggetti (`{}`)
- array (`[]`)
- coppie chiave/valore

Quando osservi una risposta JSON chiediti sempre:
- è un oggetto o una lista?
- quali campi contiene?
- che tipo di dati rappresenta?

---

## Testing: cosa significa davvero
Testare un’API **non** significa solo vedere se “funziona”.

Significa anche:
- usare il metodo sbagliato
- inviare dati incompleti
- modificare l’URL
- osservare come il server reagisce agli errori

Un’API ben progettata:
- risponde sempre
- comunica chiaramente cosa è andato storto
- usa correttamente gli status code

---

## Regole del laboratorio
- Non serve capire tutto subito
- Sbagliare richieste è parte dell’attività
- Ogni risposta del server è informazione utile
- Concentrati su **protocollo, struttura e logica**, non sullo strumento

---

## Collegamento con il percorso
Quello che faremo oggi serve per:
- comprendere meglio il modello client/server
- progettare API corrette
- testare i servizi che realizzeremo noi stessi

Postman è solo lo strumento.  
**HTTP e REST sono il vero argomento.**
