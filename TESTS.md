# Journal des tests manuels

Chaque entrée indique la version testée. Le commit est celui de la branche au moment du test. La version affichée dans l'application a la forme `version-branche-date-commit-ci-OS`.

Statuts : ✅ fonctionne · ❌ bug · ⚠️ partiel

---

## 2026-11-18 — production — iPhone 13

- **Branche / commit** : `production` @ `f0b87a9` (« removes white noise in gong »)
- **Version affichée** : non notée
- **Appareil** : iPhone 13 (iOS ?, navigateur ?)

| Fonction | Statut | Remarque |
|---|---|---|
| Wakelock pendant la méditation | ✅ | L'écran reste allumé |
| Wakelock relâché en quittant la session | ❌ | Toujours actif après la sortie de la session ; relâché seulement quand on quitte l'application |
| Gong | ✅ | |
| Plein écran | ⚠️ | Fonctionne, mais un bandeau blanc apparaît en bas de l'écran noir pendant la session |

**Bugs ouverts :**
1. Le wakelock n'est pas relâché à la sortie de la session de méditation.
2. Un bandeau blanc s'affiche en bas de l'écran en plein écran pendant la session.

---

## 2026-02-15 — `cfa4132` — iPhone et Android (application Reso)

Repris de l'ancien fichier `versions/versions.md`.

| Fonction | iPhone | Android |
|---|---|---|
| Wakelock 1 min | ✅ | ✅ |
| Wakelock relâché après « Retour » | ❌ mode veille réactivé | ❌ mode veille réactivé |
| Gong de début | ✅ | ✅ |
| Gong de fin | ✅ | ✅ |
| Plein écran | ⚠️ bandeau blanc en bas | ✅ |
| Pas de bug « page non trouvée » | ✅ | ✅ |
