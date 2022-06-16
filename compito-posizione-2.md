# VERIFICA: Fondamenti di version control

Informazioni sul GitFlow utilizzato:

    - branch main
        branch da cui vengono staccate le release:
        contiene una copia sempre consistente del progetto (il programma funziona correttamente)

    - branch develop
        branch di sviluppo da cui partono e su cui convergono i feature branch:
        contiene tutte le feature il cui sviluppo è stato completato (il programma funziona correttamente)

    - feature branch
        branch di sviluppo su cui vengono implementate le nuove features;
        i feature branch vanno allineati su origin (saranno utilizzati per la valutazione),
        e possono eventualmente essere in stato inconsistente (il programma non necessariamente funziona)

    - release branch
        rappresentano una versione deliverable (di produzione) del programma

    - alternative branch
        rappresentano una versione alternativa del programma: vengono staccati da main e con esso rimangono allineati

Punti di attenzione: - i release branch sono rami 'congelati' (non effettuare commit su questi branch) \* in alternativa ai branch di release, git offre la possibilità di usare i tag, ma in questa prova non è necessario - i feature branch vanno sempre staccati da 'develop': le commit di nuove funzionalità vanno effettuate sui feature branch - il branch di develop è il branch su cui verranno fatti convergere i feature branch (con la merge): non effettuare commit
sul branch di develop

### Posizione 2

# SPRINT 1

Obiettivo dello sprint: implementare nell'applicazione le seguenti funzionalità:
1- anagrafica clienti
2- anagrafica fornitori
3- elenco articoli
4- elenco fatture
5- giacenze magazzino
6- impostazioni di sistema

## Step 1 (3 punti)

- Creare il branch 'feature/sprint01-anafor' partendo da 'develop' ed effettuare gli sviluppi su questo branch
- In 'index.html' sostituire la voce di esempio del menù con una voce '2. Anagrafica fornitori' che linka alla pagina 'anafor.html'
- Creare il file 'anafor.html' partendo dal file 'template.html' (copiando e NON cancellando il file template), personalizzando:

  - Titolo: Anagrafica fornitori
  - Sottotitolo:
    Can you ballpark the cost per unit for me the horse is out of the barn but close
    the loop all hands on deck, yet eat our own dog food no need to talk to users,
    just base it on the space calculator.

- Verificare il funzionamento dell'applicazione (dall'index deve essere raggiungibile la nuova pagina e da essa deve essere raggiungibile l'index)
- Fare la commit di tutte le modifiche e la push del nuovo branch su origin
- ATTENZIONE: verificare che il branch su origin sia stato effettivamente creato correttamente, la valutazione verrà fatta esclusivamente su origin

## Step 2 (4 punti)

- Spostarsi sul branch 'develop'
- Effettuare un riallineamento da origin (git pull)
- Verificare che l'app funzioni correttamente, in caso contrario correggere eventuali errori su index.html
- effettuare su 'develop' il merge del proprio feature branch
- correggere eventuali conflitti mantenedo l'ordine delle voci del menu
- effettuare il push di 'develop' su origin
- ATTENZIONE: verificare che su origin il push sia stato effettuato correttamente

## Team sync (3 punti per ciascun membro del team): rilascio prima versione

- dopo il completamento di tutti gli step precedenti o dopo un tempo massimo di 30 minuti
  - partendo dal branch 'develop' effettuare una pull
  - verificare di avere in develop l'applicazione con tutte le features sviluppate in modo completo dal team
  - allineare il branch 'main' a 'develop' (quindi spostarsi su 'main' e fare la merge di 'develop')
  - verificare che sul branch 'main' il programma funzioni ancora correttamente
  - staccare da 'main' un release branch chiamato 'release/1.0'
  - effettuare la push su origin del nuovo release branch

# SPRINT 2

Obiettivo dello sprint: nuove vesti grafiche e contenuti aggiornati

## Step 1 (punti mancanti per il completamento dei task precedenti)

- completare il proprio task dello sprint precedente se incompleto (l'obiettivo è quello di avere su 'develop' il proprio task completato - attenzione alla push su origin)

## Step 2 (2 punti)

- partendo dal branch 'develop': effettuare un riallineamento da origin (git pull)
- Creare il branch 'feature/sprint02-anafor' partendo da 'develop' ed effettuare gli sviluppi su questo branch
- In 'anafor.html' aggiungere un nuovo paragrafo in fondo con il seguente testo:

  Incentivization we need to button up our approach level the playing field, so thinking outside the box.
  Currying favour that jerk from finance really threw me under the bus. Tiger team.
  You gotta smoke test your hypothesis who's the goto on this job with the way forward
  for high performance keywords show pony strategic fit, so win-win-win programmatically.

- Verificare il funzionamento dell'applicazione (dall'index deve essere raggiungibile la nuova pagina e da essa deve essere raggiungibile l'index)
- Fare la commit di tutte le modifiche e la push del nuovo branch su origin
- ATTENZIONE: verificare che il branch su origin sia stato effettivamente creato correttamente, la valutazione verrà fatta esclusivamente su origin
- Spostarsi sul branch 'develop'
- Effettuare un riallineamento da origin (git pull)
- effettuare su 'develop' il merge del proprio feature branch
- effettuare il push di 'develop' su origin
- ATTENZIONE: verificare che su origin il push sia stato effettuato correttamente

## Step 3 (3 punti)

- obiettivo di questo task è di creare una veste grafica alternativa per il prodotto, verrà utilizzato un flow alternativo
- partendo da 'main' staccare un nuovo branch 'alternative/aliceblue'
- spostarsi sul nuovo branch e cambiare il colore di sfondo in 'style.css' in 'aliceblue'
- verificare il funzionamento dell'applicazione con il nuovo colore di sfondo
- effettuare commit della modifica e push del nuovo branch su origin
- partendo da 'alternative/aliceblue' staccare una release alternativa 'release/1.0-aliceblue' (push anche su origin)

## Team sync (3 punti per ciascun membro del team): rilascio seconda versione

- dopo il completamento di tutti gli step precedenti o dopo un tempo massimo di 20 minuti
  - partendo dal branch 'develop' effettuare una pull
  - verificare di avere in develop l'applicazione con tutte le features sviluppate in modo completo dal team
  - allineare il branch 'main' a 'develop' (quindi spostarsi su 'main' e fare la merge di 'develop')
  - verificare che sul branch 'main' il programma funzioni ancora correttamente
  - staccare da 'main' un release branch chiamato 'release/2.0'
  - effettuare la push su origin del nuovo release branch

## Step 3 (3 punti)

- riallineare il branch 'main' (git pull)
- spostarsi sul proprio alternative branch e riallinearlo a main (git merge)
- verificare che le ultime implementazioni dell'applicazione siano integrate, insieme al colore di sfondo alternativo
- rilasciare una nuova versione (staccando un nuovo branch) 'release/2.0-aliceblue' (push anche su origin)

# Teoria (9 punti - 3 per ogni domanda)

- sul branch 'main', creare un nuovo file '<nome>-<cognome>.txt' utilizzando il seguente template:

  Nome: \_**\_
  Cognome: \_\_**
  Fila n.: \_**_
  Posizione n.: _**

  Rispondere alle seguenti domande:

  1. Cosa fa il comando 'git add <file>'? Spiega come funziona la staging area
  2. Descrivi il comando 'git branch <nuovo branch>', spiegando cosa sono i branch e cosa è la HEAD
  3. Cos'è un repository remoto? Descrivi cosa fa il comando 'git fetch'

- effettuare il commit ed il push delle modifiche
- uploadare il file sul sito della FAD (si può fare anche in un secondo momento, ma è necessario per attivare la valutazione)
