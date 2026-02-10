# Seconda ora di laboratorio – Testing di API con Postman

In questa attività useremo **Postman** per inviare richieste HTTP a **API pubbliche** e analizzare le risposte del server.

L’obiettivo è prendere confidenza con:
- metodi HTTP
- URL ed endpoint
- status code
- struttura delle risposte JSON

---

## API di riferimento

Useremo l’API pubblica:

```
https://jsonplaceholder.typicode.com
```

Si tratta di un servizio di test che fornisce dati fittizi e accetta richieste REST.

---

## Esercizio 1 – Recuperare una lista di risorse

**Metodo:** `GET`  
**Endpoint:**
```
/posts
```

**URL completo:**
```
https://jsonplaceholder.typicode.com/posts
```

### Osserva:
- status code della risposta
- tipo di dato restituito (array o oggetto)
- campi presenti in ogni elemento

### Domande:
- quante risorse vengono restituite?
- i campi sono sempre gli stessi?

---

## Esercizio 2 – Recuperare una singola risorsa

**Metodo:** `GET`  
**Endpoint:**
```
/posts/1
```

### Osserva:
- differenza rispetto all’esercizio precedente
- struttura del JSON

### Domande:
- perché ora non riceviamo una lista?
- cosa rappresenta il numero nell’URL?

---

## Esercizio 3 – Risorsa inesistente

**Metodo:** `GET`  
**Endpoint:**
```
/posts/9999
```

### Osserva:
- status code
- contenuto della risposta

### Domanda:
- come comunica il server che la risorsa non esiste?

---

## Esercizio 4 – Creare una nuova risorsa

**Metodo:** `POST`  
**Endpoint:**
```
/posts
```

### Body (raw → JSON)
```json
{
  "title": "Seconda ora di laboratorio",
  "body": "Test con Postman",
  "userId": 1
}
```

### Osserva:
- status code
- dati restituiti dal server
- presenza di un nuovo `id`

### Domanda:
- i dati vengono davvero salvati sul server? Perché?

---

## Esercizio 5 – Metodo sbagliato

**Metodo:** `DELETE`  
**Endpoint:**
```
/posts
```

### Domande:
- ha senso questa richiesta?
- cosa dovrebbe fare un server reale?
- perché esistono regole sui metodi HTTP?

---

## Esercizio 6 – Modifica di una risorsa

**Metodo:** `PUT`  
**Endpoint:**
```
/posts/1
```

### Body (raw → JSON)
```json
{
  "id": 1,
  "title": "Post modificato",
  "body": "Contenuto aggiornato",
  "userId": 1
}
```

### Osserva:
- risposta del server
- differenza concettuale tra `POST` e `PUT`

---

## Attività di riflessione finale

Per ogni esercizio indica:
- metodo usato
- URL
- status code
- tipo di risposta (oggetto / array)
- eventuali errori

---

## Obiettivo finale

Alla fine della lezione dovresti essere in grado di:
- leggere una richiesta HTTP
- capire se una risposta è corretta
- individuare errori di metodo o di URL
- usare Postman come strumento di test

Postman è solo lo strumento.  
**HTTP e REST sono il vero argomento.**
