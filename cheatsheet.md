## Cheatsheet Version Control
***
Le repository di git sono le cartelle contenenti i file .git. 
<br> <br>

Di seguito i comandi essenziali:
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

```bash
git checkout #nome del branch/nome della commit a cui si vuole navigare
```
Comando che permette di navigare i branch e di crearne di nuovi. Per navigare a un log precedente rispetto a quello in cui siamo, si possono copiare da git log i primi caratteri della commit.
```bash
git checkout -b + #nome del nuovo branch che si vuole creare
```
Con -b si va a aggiungere un nuovo branch a quello in cui ci si trova. <br>
Ogni tanto git potrebbe perdere le modifiche fatte su un branch. Questo potrebbe succedere perchè potremmo non aver dato un’”etichetta” a un nostro checkout, perchè al posto di usare il comando
```bash
git checkout -b + #nomebranch
```
abbiamo usato
```bash
git checkout + #nomebranch
```
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
```bash
git merge + #nome del branch da aggiungere al branch in cui ci troviamo
```
Comando per fare il merge del branch al branch su cui si è attualmente. Per muoversi da un branch all’altro ricordiamo che si usa il comando