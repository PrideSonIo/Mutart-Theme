# 🤝 Guida alla Collaborazione

Grazie per voler contribuire a questo progetto! Di seguito trovi le linee guida ufficiali per contribuire in modo efficace e collaborativo.

---

## 🚀 Processo di Sviluppo

### 1. Apri una Issue
Prima di iniziare, apri un'issue per:
- Richiedere una nuova funzionalità
- Segnalare un bug
- Discutere un'idea

### 2. Crea un nuovo Branch
I branch devono derivare da `main` o `dev`.

**Naming convention consigliata:**

| Tipo di task      | Nome branch                                   | Esempio                            |
|-------------------|-----------------------------------------------|------------------------------------|
| Nuova funzionalità| `feature/<nome-funzionalità>`                 | `feature/login-google`            |
| Bug fix           | `fix/<descrizione>`                           | `fix/button-crash`                |
| Hotfix urgente    | `hotfix/<nome>`                               | `hotfix/token-expired`            |
| File di struttura | `chore/<nome-file>`                           | `chore/create-readme`             |
| Refactoring       | `refactor/<cosa>`                             | `refactor/auth-service`           |

```bash
git checkout -b feature/dashboard-stats
