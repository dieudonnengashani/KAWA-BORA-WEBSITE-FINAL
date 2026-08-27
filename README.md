# KAWA BORA — Site web professionnel

## Technologies
- HTML5
- CSS3
- JavaScript
- Système de langue intégré : Français / English / Kiswahili
- Aucun framework obligatoire

## Pages
- index.html — Accueil
- pages/about.html — À propos
- pages/cafes.html — Nos cafés
- pages/value-chain.html — Chaîne de valeur
- pages/markets.html — Marchés
- pages/impact.html — Impact
- pages/partners.html — Partenaires
- pages/invest.html — Investir
- pages/gallery.html — Galerie
- pages/contact.html — Contact

## Organisation du code
Les fichiers sont commentés avec des blocs :
PAGE, HEADER, SECTIONS, FOOTER, etc.
Le CSS est également organisé par grandes sections numérotées.

## Langues
Le sélecteur FR / EN / SW se trouve dans le menu et sur la page d'accueil.
Le choix est mémorisé avec localStorage et reste actif lorsqu'on change de page.

## Images
Les quatre photos fournies pour KAWA BORA sont dans images/gallery/.

## Lancer localement
Avec VS Code :
1. Ouvrir le dossier.
2. Installer l'extension Live Server.
3. Clic droit sur index.html.
4. Choisir Open with Live Server.

## Données utilisées
Le contenu institutionnel principal a été structuré à partir du document fourni sur KAWA BORA, complété avec les coordonnées déjà fournies dans le projet.


## Menu professionnel
Le menu principal contient maintenant des sous-menus : À propos, Nos cafés, Nos activités, Marchés et Événements. Sur ordinateur, les sous-menus apparaissent au survol ou au clic. Sur téléphone, ils fonctionnent en accordéon.

## Événements
La page `pages/events.html` contient trois rubriques : événements à venir, événements passés et actualités. Les données sont centralisées dans `js/events.js`. Pour ajouter un événement réel, ajoutez un objet dans `KB_EVENTS` et ses textes dans `js/i18n.js`.


## Publier un événement ou une actualité

1. Ouvrir `js/events.js` dans VS Code.
2. Dans `KB_EVENTS`, ajouter un nouvel objet.
3. Utiliser `type: "upcoming"` pour un événement à venir, `"past"` pour un événement passé ou `"news"` pour une actualité.
4. Ajouter `date`, `image` (optionnelle) et les textes `fr`, `en`, `sw`.
5. Pour une photo, placer le fichier dans `images/events/`, puis indiquer par exemple `image: "../images/events/salon-cafe.jpg"`.
6. Enregistrer puis actualiser `pages/events.html` dans Live Server.

Exemple :
```js
{
  type: "upcoming",
  date: "15 septembre 2026",
  image: "../images/events/salon-cafe.jpg",
  fr: { title: "Salon du café", location: "Goma — RDC", text: "Kawa Bora participe au salon." },
  en: { title: "Coffee Fair", location: "Goma — DRC", text: "Kawa Bora takes part in the fair." },
  sw: { title: "Maonyesho ya kahawa", location: "Goma — DRC", text: "Kawa Bora inashiriki." }
}
```
