## Cheatsheet Version Control
***
Le repository di git sono le cartelle contenenti i file .git. 
<br> <br>

Di seguito i comandi essenziali:
```bash
git init
```
Aggiunge un file nascosto .git che rende una cartella una repository.
```bash
git status
```
Dice lo status delle commit all'interno delle repository. Praticamente ci fa vedere il punto a cui noi siamo con le modifiche ai file.
```bash
git add #[nome dei file/cartelle modificati]
```
Realmente, è un file all'interno della cartella .git che contiene uno storico dei file modificati. "Salva" le modifiche apportate ai file, ma non è una commit.
```bash
git add .
```
"Salva" tutte le modifiche.
```bash
git commit
```
Salva su cloud le modifiche ai file o alle cartelle. Apre un editor che fa aggiungere un commento alla commit. Il commit va sul branch corrente. Se si vuole fare un commit su un altro branch, spostarsi sul branch desiderato.
```bash
git commit -m 'commento'
```
Comando per la commit, ma aggiunge direttamente dalla shell il commento della commit, senza passare dall'editor di testo.
```bash
git log
```
Storico dei commit
```bash
git checkout #[nome del branch/nome della commit a cui si vuole navigare]
```
Comando che permette di navigare i branch e di crearne di nuovi. Per navigare a un log precedente rispetto a quello in cui siamo, si può copiare da git log i primi caratteri della commit. 
```bash
git checkout -b #[nome del nuovo branch che si vuole creare]
```
Con -b si va a aggiungere un nuovo branch a quello in cui ci si trova.