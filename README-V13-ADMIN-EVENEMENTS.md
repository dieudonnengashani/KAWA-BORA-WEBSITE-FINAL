# KAWA BORA V13 — Espace administrateur des événements

Base : V12 corrigée.

## Fonctionnement

- Ouvrir `pages/admin-events.html` avec Live Server.
- Ajouter autant d'événements que nécessaire.
- Les publications sont enregistrées dans `localStorage` sous `kawaBoraEvents`.
- Le site public `pages/events.html` lit automatiquement ces publications.
- Un événement est « À venir » si sa date est aujourd'hui ou future.
- Il devient automatiquement « Événement passé » lorsque sa date est dépassée.
- Les actualités restent dans la rubrique « Actualités ».
- Les photos peuvent être ajoutées depuis le formulaire et sont stockées localement.
- Export/import JSON permet de sauvegarder ou transférer les publications.

## Limitation du mode local

Le stockage du navigateur est propre à chaque navigateur/appareil. Une publication faite sur le PC ne sera donc pas encore visible sur le téléphone.
Lors de la mise en ligne, `events.js` pourra être relié à une base de données/API sans changer l'interface d'administration.
