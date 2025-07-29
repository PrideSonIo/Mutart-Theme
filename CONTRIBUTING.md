`# Guida alla Collaborazione su una Repository GitHub  Questa guida ti aiuterà a collaborare su un progetto GitHub con il tuo team.  ## 1. Creare un account su GitHub Se non lo avete già, dovete prima creare un account su GitHub. Potete farlo andando su [GitHub.com](https://github.com/) e cliccando su "Sign Up".  ## 2. Creare una Repository Uno dei membri del team deve creare una repository: - Andate sulla pagina principale di GitHub e cliccate sul pulsante **"+"** nell'angolo in alto a destra e selezionate **"New repository"**. - Inserite un nome per la repository, scegliete se renderla pubblica o privata e aggiungete una descrizione. - Cliccate su **Create repository**.  ## 3. Aggiungere i membri al progetto Se la repository è privata o volete aggiungere dei collaboratori, andate su **Settings** > **Collaborators & teams** > **Add people**. Inserite il nome utente GitHub degli altri membri del team e cliccate su **Add**.  ## 4. Clonare la Repository Ogni membro del team dovrà "clonare" la repository sul proprio computer. Copiate l'URL della repository e utilizzate il comando:  ```bash git clone https://github.com/tuo-utente/nome-repo.git`

Questo scaricherà una copia della repository sul vostro computer locale.

## 5\. Creare un Branch per Ogni Nuova Funzionalità o Bugfix

Per evitare conflitti, è buona norma lavorare su branch separati. Ogni membro dovrebbe creare un proprio branch per ogni nuova funzionalità o correzione da implementare.

Ecco come creare un branch:

`git checkout -b nome-del-branch`

Ad esempio, se un membro sta lavorando su una nuova funzionalità chiamata "login", potrebbe scrivere:

`git checkout -b feature/login`

## 6\. Fare Modifiche e Committare

Una volta che avete fatto delle modifiche nel codice, potete "committarle" localmente. Prima, dovete aggiungere i file modificati all'area di staging con il comando:


`git add .`

Poi, effettuate il commit con un messaggio descrittivo:


`git commit -m "Descrizione delle modifiche"`

## 7\. Push delle Modifiche

Dopo aver fatto il commit, dovete "pusherle" sulla repository su GitHub:


`git push origin nome-del-branch`

Questo caricherà le modifiche sul vostro branch specifico sulla repository.

## 8\. Creare una Pull Request

Una volta che le modifiche sono state caricate sulla repository, è necessario aprire una **pull request (PR)** per farle revisionare dal team e per unire il codice nel branch principale (di solito chiamato `main` o `master`).

Per farlo:

* *   Andate sulla pagina della repository su GitHub.
*     
* *   Vedrete un messaggio che vi chiede se volete "Compare & pull request". Cliccate su questo pulsante.
*     
* *   Aggiungere una descrizione chiara delle modifiche e cliccate su **Create pull request**.
*     

A questo punto, uno degli altri membri del team dovrà rivedere e approvare la pull request.

## 9\. Revisionare e Unire la Pull Request

Gli altri membri possono commentare la pull request per chiedere eventuali modifiche. Una volta che la PR è pronta, uno dei membri del team può cliccare su **Merge pull request** per unire le modifiche al branch principale.

## 10\. Sincronizzare il Proprio Repository Locale

Dopo che la pull request è stata unita, è importante tenere il proprio repository locale sincronizzato con la versione più recente del branch principale. Per farlo, eseguite:

`git checkout main git pull origin main`

E se avevate creato un branch per lavorare, potete tornare sul vostro branch e fare il rebase:

`git checkout nome-del-branch git rebase main`

## 11\. Risoluzione dei Conflitti

Se ci sono conflitti tra il codice del vostro branch e il branch principale (ad esempio se più persone hanno modificato la stessa parte di codice), Git vi avviserà e dovrete risolverli manualmente. Dopo averli risolti, potete continuare con il commit e il push.

* * *

## Consigli Utili

* *   **Commits chiari**: I commit dovrebbero essere descrittivi e contenere solo un'idea o modifica alla volta.
*     
* *   **Pull request brevi**: Cercate di fare pull request più piccole possibile per rendere la revisione del codice più facile.
*     
* *   **Comunicazione**: Utilizzate la descrizione delle pull request per spiegare il motivo delle modifiche e se sono necessarie azioni speciali per testarle.
*     tent here. You can paste directly from Word or other rich text sources.