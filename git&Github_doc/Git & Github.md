Ecco il tuo file **pulito, integrato e senza duplicazioni**, con la sezione **rebase inserita in modo coerente** e i riferimenti sistemati.

Puoi incollarlo direttamente in Obsidian.

---

````markdown
# 1. Cos'è Git e Cos'è GitHub

## Git

Git è un sistema di controllo versione che permette di:

- Tenere traccia delle modifiche ai file
- Tornare a versioni precedenti
- Lavorare su funzionalità separate tramite branch
- Collaborare con altri sviluppatori

## GitHub

:contentReference[oaicite:0]{index=0} è una piattaforma online che ospita repository Git.

Permette di:

- Salvare codice nel cloud
- Collaborare con altri sviluppatori
- Gestire versioni e rilasci
- Condividere progetti

---

# 2. Prima configurazione

## Verifica installazione

```bash
git --version
````

## Configurazione utente

```bash
git config --global user.name "Mario Rossi"
git config --global user.email "mario@email.com"
```

## Visualizzare configurazione

```bash
git config --list
```

---

# 3. Creare un repository

```bash
mkdir mio-progetto
cd mio-progetto
git init
```

---

# 4. Stato del repository

```bash
git status
```

Mostra:

* file modificati
* file non tracciati
* file pronti per commit

---

# 5. Aggiungere file

```bash
git add nomefile
git add .
```

---

# 6. Commit

```bash
git commit -m "Primo commit"
```

---

# 7. Cronologia

```bash
git log
git log --oneline
```

---

# 8. Repository su GitHub

Creazione manuale su GitHub e copia URL:

```
https://github.com/utente/mio-progetto.git
```

---

# 9. Collegare Git a GitHub

```bash
git remote add origin <url>
git remote -v
git remote show origin
```

## Modificare remote

```bash
git remote set-url origin <nuovo-url>
git remote remove origin
git remote add origin <url>
```

---

# 10. Push

```bash
git push -u origin main
git push
```

---

# 11. Clone

```bash
git clone <url>
```

---

# 12. Pull

```bash
git pull
git pull origin main
```

---

# 13. Branch

```bash
git branch
git branch feature
git switch feature
git switch -c feature
```

---

# 14. Merge

```bash
git switch main
git merge feature
```

---

# 15. Rebase

## Cos’è

Il rebase serve a **spostare i commit di un branch sopra un altro branch**, creando una storia lineare.

---

## Esempio

Prima:

```
main:    A --- B --- C
                 \
feature:           D --- E
```

Dopo rebase:

```
main:    A --- B --- C --- D' --- E'
```

---

## Uso base

```bash
git switch feature
git rebase main
```

---

## Aggiornare da remoto

```bash
git fetch origin
git rebase origin/main
```

---

## Rebase interattivo

```bash
git rebase -i HEAD~3
```

Permette di:

* squash commit
* modificare messaggi
* riordinare commit
* eliminare commit

---

## Conflitti

```bash
git status
git add .
git rebase --continue
```

Annullare:

```bash
git rebase --abort
```

---

## Rebase vs Merge

### Merge

```bash
git merge main
```

* mantiene la storia originale
* crea commit di merge
* più sicuro in team

### Rebase

```bash
git rebase main
```

* storia lineare
* riscrive commit
* più pulito ma da usare con attenzione

---

## ⚠️ Regola importante

Non usare rebase su branch già pubblicati su GitHub.

✔ Usalo su branch locali
❌ Evitalo su branch già pushati

---

# 16. Eliminare branch

```bash
git branch -d feature
git branch -D feature
```

---

# 17. Ripristino modifiche

```bash
git restore file.txt
git restore .
```

---

# 18. Reset commit

```bash
git reset HEAD~1
git reset --hard HEAD~1
```

---

# 19. Rimuovere file

```bash
git rm file.txt
git rm -r cartella
```

---

# 20. Diff

```bash
git diff
git diff HEAD~1 HEAD
```

---

# 21. Workflow quotidiano

```text
modifica file
↓
git status
↓
git add .
↓
git commit -m "msg"
↓
git push
```

---

# 📌 Comandi fondamentali

```bash
git status
git add .
git commit -m ""
git push
git pull
git log --oneline
git branch
git switch
git merge
git rebase
git diff
git restore .
```

```

---

Se vuoi, posso fare il passo successivo e trasformarlo in:
- 🧠 **scheda di ripasso ultra sintetica (1 pagina)**
- 📊 **tabella comparativa merge vs rebase vs reset**
- 🧩 **template Obsidian con link tra note (tipo vault Git completo)**
```
