# 1. Cos'è Git e Cos'è GitHub

## Git

Git è un sistema di controllo versione che permette di:

- Tenere traccia delle modifiche ai file
- Tornare a versioni precedenti
- Lavorare su funzionalità separate tramite branch
- Collaborare con altri sviluppatori

## GitHub

GitHub è una piattaforma online che ospita repository Git.

Con GitHub puoi:

- Salvare il codice nel cloud
- Collaborare con altri sviluppatori
- Gestire versioni e rilasci
- Condividere progetti

---

# 2. Prima Configurazione

Verifica installazione Git:

```bash
git --version
```

Configura nome utente:

```bash
git config --global user.name "Mario Rossi"
```

Configura email:

```bash
git config --global user.email "mario@email.com"
```

Visualizza configurazione:

```bash
git config --list
```

---

# 3. Creare un Nuovo Repository

```bash
mkdir mio-progetto
cd mio-progetto
git init
```

Output:

```text
Initialized empty Git repository
```

---

# 4. Controllare lo Stato

```bash
git status
```

Mostra:

- File modificati
- File non tracciati
- File pronti per commit

---

# 5. Aggiungere File

## Singolo file

```bash
git add index.html
```

## Tutti i file

```bash
git add .
```

---

# 6. Creare un Commit

```bash
git commit -m "Primo commit"
```

---

# 7. Cronologia

<!-- git log --stat -->

```bash
git log
```

Versione breve:

<!-- git log --oneline  -all --graph -->
<!-- git log --oneline -all -->

```bash
git log --oneline
```

---

# 8. Creare Repository su GitHub

1. Accedi a GitHub
2. Clicca **New repository**
3. Inserisci nome repository
4. Clicca **Create repository**

Esempio URL:

```
https://github.com/utente/mio-progetto.git
```

---

# 9. Collegare Git a GitHub

## Aggiungere remote

```bash
git remote add origin https://github.com/utente/mio-progetto.git
```

## Verificare remote

```bash
git remote -v
```

---

## 🔁 Modificare URL repository (IMPORTANTE)

### Verifica attuale

```bash
git remote -v
```

### Stato del repositoty

```bash
git remote show origin
```

## Rinominare

```bash
git remote rename <nome originale> <nuovo nome>
```

### Cambiare URL

```bash
git remote set-url origin https://github.com/utente/progetto-nuovo.git
```

### Oppure SSH

```bash
git remote set-url origin git@github.com:utente/progetto-nuovo.git
```

### Verifica

```bash
git remote -v
```

### Test connessione

```bash
git fetch
```

---

## 🧹 Alternativa: rimuovere e ricreare remote

```bash
git remote remove origin
git remote add origin https://github.com/utente/progetto-nuovo.git
```

---

## Comandi remote essenziali

```bash
git remote -v
git remote set-url origin <url>
git remote remove origin
git remote add origin <url>
```

---

# 10. Inviare progetto su GitHub

```bash
git push -u origin main
```

Successivamente:

```bash
git push
```

---

# 11. Clonare un Repository

```bash
git clone https://github.com/utente/progetto.git
cd progetto
```

---

# 12. Scaricare Aggiornamenti

```bash
git pull
```

oppure:

```bash
git pull origin main
```

---

# 13. Branch

## Visualizzare branch

```bash
git branch
```

## Creare branch

```bash
git branch login-page
```

## Cambiare branch

```bash
git switch login-page
```

## Creare + cambiare

```bash
git switch -c login-page
```

---

# 14. Merge

```bash
git switch main
git merge login-page
```

---

# 15. Eliminare branch

```bash
git branch -d login-page
```

Forzato:

```bash
git branch -D login-page
```

---

# 16. Annullare modifiche

```bash
git restore index.html
git restore .
```

---

# 17. Annullare commit

Mantiene modifiche:

```bash
git reset HEAD~1
```

Elimina tutto:

```bash
git reset --hard HEAD~1
```

⚠️ Attenzione: distruttivo

---

# 18. Rimuovere file

```bash
git rm file.txt
git rm -r cartella
git commit -m "Rimozione file"
```

---

# 19. Confrontare modifiche

```bash
git diff
git diff HEAD~1 HEAD
```

---

# 20. Workflow quotidiano

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
