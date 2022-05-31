## Database University

# studente:
- id:                   Primary key (PK), NOTNULL, UNIQUE, INDEX,
- nome:                 VARCHAR(50), NOTNULL
- cognome:              VARCHAR(50), NOTNULL
- anni:                 YEAR, NOTNULL
- email:                VARCHAR(250), NOTNULL
- matricola:            VARCHAR(250), NOTNULL, UNIQUE
- codice_fiscale:       VARCHAR(250), NOTNULL
- domicilio:            VARCHAR(60), NOTNULL
- telefono:             VARCHAR(15), NOTNULL
- corso_di_laurea:      VARCHAR(100)
- carriera:             VARCHAR(50)


# dipartimenti:
- id:                   Primary key (PK), NOTNULL, UNIQUE, INDEX,
- nome:                 VARCHAR(50), NOTNULL
- descrizione:          VARCHAR(250)



# corsi_laurea
- id:                   Primary key (PK), NOTNULL, UNIQUE, INDEX,
- nome:                 VARCHAR(50),  NOTNULL, UNIQUE
- codice:               TINIINT, NOTNULL, UNIQUE
- corsi_id              //ogni corso di laurea prevede diversi corsi
- studente_id           // ogni studente è scritto ad un solo corso di laurea


# corso
- id:                   Primary key (PK), NOTNULL, UNIQUE, INDEX,
- nome:                 VARCHAR(70), NOTNULL
- codice_corso:         TINYINT, NOTNULL, UNIQUE
- durata_corso:         VARCHAR(20), NOTNULL
- cfu_richiesti:        INT, NOTNULL
- programma_corso       VARCHAR(100), NOTNULL
- elaborati:            VARCHAR(150), NOTNULL
- forum_corso:          VARCHAR(60), NOTNULL    
- materiale_studio:     VARCHAR(255), NOTNULL    
- esami_da_sostenere    TINYINT, NOTNULL
- insegnanti_id         // ogni corso può essere tenuto da diversi insegnanti


# insegnanti
- id:                   Primary key (PK), NOTNULL, UNIQUE, INDEX,
- nome:                 VARCHAR(50), NOTNULL
- cognome:              VARCHAR(50), NOTNULL
- eta:                  TINYINT, NOTNULL
- insegnamento:         VARCHAR(50), NOTNULL     
- pubblicazioni:        VARCHAR(250),NOTNULL
- carriera:             VARCHAR(250), NOTNULL


# appelli_esame
- id:                   Primary key (PK), NOTNULL, UNIQUE, INDEX,
- nome_materia:         VARCHAR(100), NOTNULL
- codice_materia:       TINYINT,NOTNULL,UNIQUE
- data:                 DATE
- durata_esame:         TIME, NOTNULL
- aula:                 VARCHAR(10)
- regolamento:          VARCHAR(250)
- posti_disponibili:    TINYINT,NOTNULL 
- id_studenti; //ogni studente può iscriversi a più appelli d'esame

# risultato_appello

- nome_studente:        VARCHAR(50), NOTNULL
- cognome_studente:     VARCHAT(50), NOTNULL
- email_studente:       VARCHAR(150), NOTNULL
- materia_sostenuta:    VARCHAR(100), NOTNULL   
- data:                 DATATIME, NOTNULL
- votazione:            FLOAT(2,2), NOTNULL
- esito:                VARCHAR(10), NOTNULL


