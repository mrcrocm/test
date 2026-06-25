Ecco la tua versione **ottimizzata per Obsidian**, più ordinata, con struttura coerente, titoli puliti e stile da appunti tecnici.

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

Output:

```text
Initialized empty Git repository
```

---

# 4. Stato del repository

```bash
git status
```

Mostra:

* File modificati
* File non tracciati
* File pronti per commit

---

# 5. Aggiungere file

## Singolo file

```bash
git add index.html
```

## Tutti i file

```bash
git add .
```

---

# 6. Commit

```bash
git commit -m "Primo commit"
```

---

# 7. Cronologia

## Log completo

```bash
git log
```

## Versione compatta

```bash
git log --oneline
```

---

# 8. Repository su GitHub

1. Creare nuovo repository su GitHub
2. Copiare URL

Esempio:

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

## Modificare remote

### Visualizzare stato remoto

```bash
git remote show origin
```

### Cambiare URL

```bash
git remote set-url origin https://github.com/utente/progetto-nuovo.git
```

### Oppure SSH

```bash
git remote set-url origin git@github.com:utente/progetto-nuovo.git
```

### Rimuovere remote

```bash
git remote remove origin
```

### Ricreare remote

```bash
git remote add origin <url>
```

---

# 10. Push su GitHub

## Prima volta

```bash
git push -u origin main
```

## Successive

```bash
git push
```

---

# 11. Clone repository

```bash
git clone https://github.com/utente/progetto.git
cd progetto
```

---

# 12. Pull aggiornamenti

```bash
git pull
```

---

# 13. Branch

## Visualizzare branch

```bash
git branch
```

## Creare branch

```bash
git branch feature
```

## Cambiare branch

```bash
git switch feature
```

## Creare + switch

```bash
git switch -c feature
```

---

# 14. Merge

```bash
git switch main
git merge feature
```

---

# 15. Eliminare branch

## Locale

```bash
git branch -d feature
```

## Forzato

```bash
git branch -D feature
```

---

# 16. Ripristino modifiche

```bash
git restore file.txt
git restore .
```

---

# 17. Reset commit

## Mantiene modifiche

```bash
git reset HEAD~1
```

## Distruttivo ⚠️

```bash
git reset --hard HEAD~1
```

---

# 18. Rimuovere file

```bash
git rm file.txt
git rm -r cartella/
git commit -m "Rimozione file"
```

---

# 19. Diff (confronto modifiche)

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
git commit -m "messaggio"
↓
git push
```

---

# 📌 Comandi fondamentali

```bash
git status
git add .
git commit -m "msg"
git push
git pull
git log --oneline
git branch
git switch
git merge
git rebase   # attenzione: non usare su commit già pushati su remoto
git diff
git restore .
```

```

