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
git add
```
Realmente, è un file all'interno della cartella .git che contiene uno storico dei file modificati. "Salva" le modifiche apportate ai file, ma non è una commit.
```bash
git commit
```
Salva su cloud le modifiche ai file o alle cartelle. Apre un editor che fa aggiungere un commento alla commit. 
```bash
git commit -m 'commento'
```
Comando per la commit, ma aggiunge direttamente dalla shell il commento della commit, senza passare dall'editor di testo.