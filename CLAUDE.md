# CLAUDE.md

## Branches

- **`main`** : branche de développement. Tout le travail courant y est commité (directement ou via des branches de feature fusionnées dans `main`).
- **`preproduction`** : version de test avant la mise en production. Mise à jour depuis `main` quand une version doit être validée.
- **`production`** : déployée automatiquement par Netlify. Ne jamais commiter directement dessus ; elle ne reçoit que des fast-forwards depuis `main` (ou `preproduction`).

Les branches de feature éventuelles partent de `main` et y reviennent.

### Mise en production

```sh
git push origin main:preproduction   # pour tester
git push origin main:production      # déploie sur Netlify
```

Ne pas forcer (`--force`) ces push sans accord explicite : si le push est refusé, c'est que `production` contient des commits absents de `main`, à fusionner d'abord dans `main`.
