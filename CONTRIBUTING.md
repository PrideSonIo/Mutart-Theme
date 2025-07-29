# Guida alla Collaborazione su una Repository GitHub

Questa guida ti aiuterà a collaborare su un progetto GitHub con il tuo team.

## 1. Creare un account su GitHub

Se non lo avete già, dovete prima creare un account su [GitHub](https://github.com/).

## 2. Forkare la Repository

Andate sulla pagina della repository e cliccate su **Fork** per crearne una copia nel vostro account (non dovrebbe essere necessario forkare nel nostro caso, basta il git clone e il nuovo branch).

## 3. Clonare la Repository

Clonate la repository nel vostro computer con il comando:

```bash
git clone https://github.com/tuo-username/nome-repository.git
```

Questo scaricherà una copia della repository sul vostro computer locale.

## 4. Configurare il Remote

Assicuratevi di avere configurato il remote `origin` verso il vostro fork e aggiungete anche il remote `upstream` verso la repository originale se necessario.

## 5. Creare un Branch per Ogni Nuova Funzionalità o Bugfix

Per evitare conflitti, è buona norma lavorare su branch separati. Ogni membro dovrebbe creare un proprio branch per ogni nuova funzionalità o correzione da implementare.

Ecco come creare un branch:

```bash
git checkout -b nome-del-branch
```

Ad esempio, se un membro sta lavorando su una nuova funzionalità chiamata "login", potrebbe scrivere:

```bash
git checkout -b feature/login
```

## 6. Fare Modifiche e Committare

Una volta che avete fatto delle modifiche nel codice, potete "committarle" localmente. Prima, dovete aggiungere i file modificati all'area di staging con il comando:

```bash
git add .
```

Poi, effettuate il commit con un messaggio descrittivo:

```bash
git commit -m "Descrizione delle modifiche"
```

## 7. Push delle Modifiche

Dopo aver fatto il commit, dovete "pusherle" sulla repository su GitHub:

```bash
git push origin nome-del-branch
```

Questo caricherà le modifiche sul vostro branch specifico sulla repository.

## 8. Creare una Pull Request

Una volta che le modifiche sono state caricate sulla repository, è necessario aprire una **pull request (PR)** per farle revisionare dal team e per unire il codice nel branch principale (di solito chiamato `main`).

Per farlo:

- Andate sulla pagina della repository su GitHub.
- Vedrete un messaggio che vi chiede se volete "Compare & pull request". Cliccate su questo pulsante.
- Aggiungete una descrizione chiara delle modifiche e cliccate su **Create pull request**.

A questo punto, uno degli altri membri del team dovrà rivedere e approvare la pull request.

## 9. Revisionare e Unire la Pull Request

Gli altri membri possono commentare la pull request per chiedere eventuali modifiche. Una volta che la PR è pronta, uno dei membri del team può cliccare su **Merge pull request** per unire le modifiche nel branch principale.

## 10. Sincronizzare il Proprio Repository Locale

Dopo che la pull request è stata unita, è importante tenere il proprio repository locale sincronizzato con la versione più recente del branch principale. Per farlo, eseguite:

```bash
git checkout main
git pull origin main
```

E se avevate creato un branch per lavorare, potete tornare sul vostro branch e fare il rebase:

```bash
git checkout nome-del-branch
git rebase main
```

## 11. Risoluzione dei Conflitti

Se ci sono conflitti tra il codice del vostro branch e il branch principale (ad esempio se più persone hanno modificato la stessa parte di codice), Git vi avviserà e dovrete risolverli manualmente. Dopo aver risolto i conflitti, dovrete aggiungere e committare nuovamente i file modificati.

---

## Consigli Utili

- **Commits chiari**: I commit dovrebbero essere descrittivi e contenere solo un'idea o modifica alla volta.
- **Pull request brevi**: Cercate di fare pull request più piccole possibile per rendere la revisione del codice più facile.
- **Comunicazione**: Utilizzate la descrizione delle pull request per spiegare il motivo delle modifiche e se sono necessarie azioni speciali per testarle.
