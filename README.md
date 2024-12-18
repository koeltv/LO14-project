# Projet LO14 - PCRON

Dépôt GitHub pour le projet LO14 `pcron`

### TODO List:
- Validation des lignes dans `pcrontab`

### Done:
- Scheduling des tâches (1 tâche s'exécute exactement 1 fois par intervalle valide)
- Compléter la détection de correspondance des intervalles dans `pcron`
- Gérer les lignes de commentaires avec `pcron`
- Permissions
  - Tout utilisateur peut écrire dans `/etc/pcron`, donc utiliser `pcrontab`
  - Un utilisateur ne peut modifier que son propre fichier
  - `pcron` est restreint par `pcron.allow` et `pcron.deny`, par défault tout le monde à la permission
    - `pcron.allow` est prioritaire sur `pcron.deny`
    - Ces 2 fichiers prennent des noms d'utilisateur et/ou des groupes (1 par ligne)