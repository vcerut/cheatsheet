# Cheatsheet Version Control

*Cheatsheet creata da Valeria Cerutti*

1. [Comandi Essenziali](#comandi-essenziali)
2. [Cambiare Branch](#cambiare-branch)
3. [Repository Remote](#repository-remote)
***
Le repository di git sono le cartelle contenenti i file .git. 
<br> <br>

### Comandi essenziali
```bash
git init
```
Aggiunge un file nascosto .git che rende una cartella una repository.
<br><br>

```bash
git status
```
Dice lo status delle commit all'interno delle repository. Praticamente ci fa vedere il punto a cui noi siamo con le modifiche ai file.
<br><br>

```bash
git add + #nome dei file/cartelle modificati
```
Realmente, è un file all'interno della cartella .git che contiene uno storico dei file modificati. "Salva" le modifiche apportate ai file, ma non è una commit.
<br><br>

```bash
git add .
```
"Salva" tutte le modifiche.
<br><br>

```bash
git commit
```
Salva su cloud le modifiche ai file o alle cartelle. Apre un editor che fa aggiungere un commento alla commit. Il commit va sul branch corrente. Se si vuole fare un commit su un altro branch, spostarsi sul branch desiderato.
<br><br>

```bash
git commit -m 'commento'
```
Comando per la commit, ma aggiunge direttamente dalla shell il commento della commit, senza passare dall'editor di testo.
<br><br>

```bash
git log
```
Storico dei commit
<br><br>

### Cambiare branch
```bash
git checkout #nome del branch/nome della commit a cui si vuole navigare
```
Comando che permette di navigare i branch e di crearne di nuovi. Per navigare a un log precedente rispetto a quello in cui siamo, si possono copiare da git log i primi caratteri della commit.
```bash
git checkout -b + #nome del nuovo branch che si vuole creare
```
Con -b si va a aggiungere un nuovo branch a quello in cui ci si trova. <br>
Ogni tanto git potrebbe perdere le modifiche fatte su un branch. Questo potrebbe succedere perchè potremmo non aver dato un’”etichetta” a un nostro checkout, perchè al posto di usare il comando
`git checkout -b + #nomebranch` abbiamo usato `git checkout + #nomebranch`.
 Stiamo infatti creando un branch separato dal branch main. Quando succede una cosa simile, viene sullo schermo una notifica che dice che siamo in “detatched mode”. A schermo ci viene anche dato il suggerimento per creare un nuovo branch mantenendo le modifiche fatte.
 Suggerisce di dare il comando 
```bash
git switch
```
Che significa spostarsi da un branch all’altro. Combinando switch e checkout si può andare a un commit molto precedente rispetto a dove siamo ora e creare un branch a partire da allora.
```bash
git switch -c
```
Si crea un branch detatched.

*La differenza tra `switch` e `checkout` è che switch opera solo sui branch, mentre checkout è un comando un po' più universale.*

```bash
git merge + #nome del branch da aggiungere al branch in cui ci troviamo
```
Comando per fare il merge del branch al branch su cui si è attualmente.
```bash
git log --all --decorate --oneline --graph
```
Comando per vedere in modo grafico le modifiche e i vari branch creati

### Repository remote
La cosa più importante per quando si sincronizzano i cambiamenti su una repository remota, nel nostro caso GitLab, è avere l'account collegato al nostro git personale tramite una chiave SSH.
Una volta che si ha un account collegato, seguire questo procedimento:
1. Creare un gruppo
2. Creare un progetto (nel nostro caso, partendo da un "blank project")
3. GitLab suggerirà tre metodologie per inizializzare un progetto; nel nostro caso, si deve seguire la teza metodologia, in quanto si va a collegare il progetto con un progetto già esistente sul nostro pc. Usare quindi questi comandi:
```bash
git remote add origin git@gitlab.com: #nomeutente/nomegruppo.git
```
Si dà l'indirizzo su dove si condividono le cose.
```bash
git push -u origin --all
```
Comando da inserire dopo aver confermato i commit dal nostro Git personale.
Si sincronizzano i cambiamenti del file di origine alla repository remota. Se dovesse dare errore potrebbe essere perchè non si ha ancora una chiave SSH collegata al profilo.
```bash
git push #nome origine #nome branch che si vuole pushare
```
Comando che serve per fare il push sulla repository remota solo di un branch.
Quando si lavora in gruppo solitamente prima di fare il merge bisogna fare una richiesta. La richiesta di merge su fa sempre solo dal sito GitLab/GitHub.
```bash
git pull
```
Aggiorna la repository locale alla versione remota più recente.