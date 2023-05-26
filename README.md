**1. Tabella Dipartimento:**

La tabella "Dipartimento" rappresenta i dipartimenti all'interno dell'università. Ho scelto di includere questa tabella perché è una unità organizzativa fondamentale all'interno di un'università.

- ID_Dipartimento: rappresenta un identificativo univoco per ogni dipartimento. L'ho impostato come chiave primaria per garantire l'unicità.
- Nome: rappresenta il nome del dipartimento.

**2. Tabella Corso_di_Laurea:**

La tabella "Corso_di_Laurea" rappresenta i vari corsi di laurea offerti all'interno di ciascun dipartimento.

- ID_Corso_di_Laurea: un identificativo univoco per ogni corso di laurea. L'ho impostato come chiave primaria.
- Nome: il nome del corso di laurea.
- ID_Dipartimento: questo è una chiave esterna che si riferisce all'ID_Dipartimento nella tabella Dipartimento. Questo rappresenta la relazione "uno a molti" tra Dipartimento e Corso_di_Laurea, il che significa che un dipartimento può offrire molti corsi di laurea, ma ogni corso di laurea appartiene a un solo dipartimento.

**3. Tabella Corso:**

La tabella "Corso" rappresenta i corsi individuali all'interno di ciascun corso di laurea.

- ID_Corso: un identificativo univoco per ogni corso, impostato come chiave primaria.
- Nome: il nome del corso.
- ID_Corso_di_Laurea: una chiave esterna che si riferisce all'ID_Corso_di_Laurea nella tabella Corso_di_Laurea. Questa rappresenta la relazione "uno a molti" tra Corso_di_Laurea e Corso, il che significa che un corso di laurea può comprendere molti corsi, ma ogni corso appartiene a un solo corso di laurea.

**4. Tabella Insegnante:**

La tabella "Insegnante" rappresenta gli insegnanti dell'università.

- ID_Insegnante: un identificativo univoco per ogni insegnante, impostato come chiave primaria.
- Nome e Cognome: rappresentano il nome e il cognome dell'insegnante.

**5. Tabella Corso_Insegnante:**

La tabella "Corso_Insegnante" collega i corsi agli insegnanti. Questa è una tabella di associazione utilizzata per gestire la relazione "molti a molti" tra i corsi e gli insegnanti, in quanto un corso può essere insegnato da più insegnanti e un insegnante può insegnare più corsi.

- ID_Corso e ID_Insegnante: queste sono entrambe chiavi esterne che si riferiscono all'ID_Corso nella tabella Corso e all'ID_Insegnante nella tabella Insegnante. Insieme, queste due

colonne fungono da chiave primaria per la tabella Corso_Insegnante.

**6. Tabella Esame:**

La tabella "Esame" rappresenta gli esami per ogni corso.

- ID_Esame: un identificativo univoco per ogni esame, impostato come chiave primaria.
- Nome: il nome dell'esame.
- ID_Corso: una chiave esterna che si riferisce all'ID_Corso nella tabella Corso. Questo rappresenta la relazione "uno a molti" tra Corso e Esame, il che significa che un corso può avere molti esami, ma ogni esame è associato a un solo corso.

**7. Tabella Studente:**

La tabella "Studente" rappresenta gli studenti dell'università.

- ID_Studente: un identificativo univoco per ogni studente, impostato come chiave primaria.
- Nome e Cognome: rappresentano il nome e il cognome dello studente.
- ID_Corso_di_Laurea: una chiave esterna che si riferisce all'ID_Corso_di_Laurea nella tabella Corso_di_Laurea. Questo rappresenta la relazione "uno a molti" tra Corso_di_Laurea e Studente, il che significa che un corso di laurea può avere molti studenti, ma ogni studente è iscritto a un solo corso di laurea.

**8. Tabella Iscrizione_Esame:**

La tabella "Iscrizione_Esame" registra le iscrizioni degli studenti agli esami.

- ID_Studente e ID_Esame: queste sono entrambe chiavi esterne che si riferiscono all'ID_Studente nella tabella Studente e all'ID_Esame nella tabella Esame. Queste colonne insieme fungono da chiave primaria per la tabella Iscrizione_Esame, in quanto ogni riga rappresenta un'iscrizione unica di uno studente a un esame.
- Voto: rappresenta il voto che lo studente ha ottenuto nell'esame.

Le relazioni "uno a molti" sono state create tra Studente e Iscrizione_Esame e tra Esame e Iscrizione_Esame. Questo significa che uno studente può essere iscritto a molti esami e un esame può avere molti studenti iscritti, ma ogni iscrizione a un esame è unica per uno studente e un esame.
