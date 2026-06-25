# Git & GitHub - Guida Step by Step

## Obiettivo

Questa guida spiega come utilizzare Git e GitHub partendo da zero fino alla gestione di branch e collaborazione su progetti.

---

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

Verificare che Git sia installato:

```bash
git --version
```

Configurare nome utente:

```bash
git config --global user.name "Mario Rossi"
```

Configurare email:

```bash
git config --global user.email "mario@email.com"
```

Visualizzare la configurazione:

```bash
git config --list
```

---

# 3. Creare un Nuovo Repository

## Step 1

Creare una cartella:

```bash
mkdir mio-progetto
```

## Step 2

Entrare nella cartella:

```bash
cd mio-progetto
```

## Step 3

Inizializzare Git:

```bash
git init
```

Output:

```text
Initialized empty Git repository
```

Ora la cartella è sotto controllo versione.

---

# 4. Controllare lo Stato del Repository

Visualizzare lo stato corrente:

```bash
git status
```

Git mostrerà:

- File modificati
    
- File non tracciati
    
- File pronti per il commit
    

---

# 5. Aggiungere File al Repository

## Aggiungere un singolo file

```bash
git add index.html
```

## Aggiungere tutti i file

```bash
git add .
```

Verificare:

```bash
git status
```

I file saranno nello stato:

```text
Changes to be committed
```

---

# 6. Creare un Commit

Un commit rappresenta una fotografia del progetto.

## Creare un commit

```bash
git commit -m "Primo commit"
```

Esempio:

```bash
git commit -m "Aggiunta homepage"
```

---

# 7. Visualizzare la Cronologia

Mostrare tutti i commit:

```bash
git log
```

Versione compatta:

```bash
git log --oneline
```

---

# 8. Creare un Repository su GitHub

## Step 1

Accedere a GitHub.

## Step 2

Cliccare su:

```text
New Repository
```

## Step 3

Inserire:

- Nome repository
    
- Descrizione (opzionale)
    

## Step 4

Cliccare:

```text
Create Repository
```

GitHub mostrerà l'URL del repository.

Esempio:

```text
https://github.com/utente/mio-progetto.git
```

---

# 9. Collegare Git al Repository GitHub

Aggiungere il repository remoto:

```bash
git remote add origin https://github.com/utente/mio-progetto.git
```

Verificare:

```bash
git remote -v
```

Output:

```text
origin https://github.com/utente/mio-progetto.git
```

---

# 10. Inviare il Progetto su GitHub

Inviare il branch principale:

```bash
git push -u origin main
```

Le volte successive:

```bash
git push
```

---

# 11. Clonare un Repository Esistente

Scaricare un repository:

```bash
git clone https://github.com/utente/progetto.git
```

Entrare nella cartella:

```bash
cd progetto
```

---

# 12. Scaricare Aggiornamenti

Recuperare le modifiche dal repository remoto:

```bash
git pull
```

Oppure:

```bash
git pull origin main
```

---

# 13. Utilizzare i Branch

## Perché usare i branch?

Permettono di sviluppare funzionalità senza modificare il codice principale.

---

## Visualizzare i branch

```bash
git branch
```

---

## Creare un branch

```bash
git branch login-page
```

---

## Passare a un branch

```bash
git checkout login-page
```

oppure

```bash
git switch login-page
```

---

## Creare e passare al branch

```bash
git checkout -b login-page
```

oppure

```bash
git switch -c login-page
```

---

# 14. Unire i Branch (Merge)

Passare sul branch principale:

```bash
git switch main
```

Unire il branch:

```bash
git merge login-page
```

Git incorporerà le modifiche nel branch principale.

---

# 15. Eliminare un Branch

Dopo il merge:

```bash
git branch -d login-page
```

Forzare l'eliminazione:

```bash
git branch -D login-page
```

---

# 16. Annullare Modifiche

## Ripristinare un file

```bash
git restore index.html
```

---

## Ripristinare tutti i file

```bash
git restore .
```

---

# 17. Annullare l'Ultimo Commit

Mantenendo le modifiche:

```bash
git reset HEAD~1
```

Eliminando tutto:

```bash
git reset --hard HEAD~1
```

⚠️ Attenzione: il comando --hard elimina definitivamente le modifiche.

---

# 18. Eliminare File dal Repository

Eliminare un file:

```bash
git rm file.txt
```

Eliminare una cartella:

```bash
git rm -r cartella
```

Creare il commit:

```bash
git commit -m "Rimozione file inutili"
```

---

# 19. Confrontare le Modifiche

Visualizzare le differenze:

```bash
git diff
```

Confrontare due commit:

```bash
git diff HEAD~1 HEAD
```

---

# 20. Workflow Quotidiano

Quando modifichi il progetto:

## Verifica

```bash
git status
```

## Aggiungi modifiche

```bash
git add .
```

## Commit

```bash
git commit -m "Descrizione modifiche"
```

## Invio su GitHub

```bash
git push
```

---

# Schema Riassuntivo

```text
Modifica file
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

# Comandi da Memorizzare

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
git diff
git restore .
```

Se impari questi dieci comandi sarai in grado di gestire la maggior parte dei progetti Git e GitHub.