# TutoPerfo — Nouvelle direction artistique

## Structure proposée

```text
TutoPerfo/
├── index.html
├── assets/
│   ├── css/
│   │   └── perfo-tutos.css
│   └── img/
│       ├── logo-perfo.svg
│       └── logo-perfo-blanc.svg
├── Nextcloud/
│   ├── Nextcloud_AppPerfo.html
│   ├── Nextcloud_Client.html
│   └── Talk_Client.html
└── Mailcow/
    ├── Activation_Messagerie.html
    ├── Mot_de_passe_application.html
    └── Informations_Nextcloud_Signature.html
```

## Principe

- `assets/css/perfo-tutos.css` contient toute la DA commune.
- Les logos sont centralisés dans `assets/img/`.
- Les pages dans les sous-dossiers appellent le CSS avec `../assets/css/perfo-tutos.css`.
- La page d’accueil appelle le CSS avec `assets/css/perfo-tutos.css`.

## Réutiliser la DA sur un nouveau tuto

Pour une page située dans un sous-dossier, reprendre le même squelette HTML que les tutos existants, puis placer le contenu dans :

```html
<main class="container">
  <section>
    <h2>Titre de section</h2>
    <ol class="steps">
      <li>Première étape</li>
      <li>Deuxième étape</li>
    </ol>
  </section>
</main>
```

Classes utiles :

- `.notice` : encart important rouge.
- `.info` ou `.tip` : encart information bleu.
- `.steps` : liste numérotée en cartes.
- `.tutorial-grid` + `.tutorial-card` : grille de cartes pour l’accueil.
- `.card-link`, `.card-action` : cartes cliquables pour les liens entre tutoriels.
- `.btn-row`, `.btn`, `.btn.secondary` : anciens boutons conservés dans le CSS au cas où, mais non utilisés dans les pages Mailcow.


## Corrections métier intégrées

- Les pages publiques parlent de AppPerfo, pas du composant technique d’authentification.
- Les pages parlent du portail webmail, pas du nom technique du webmail.
- La connexion mail est décrite avec le bouton Single Sign On du portail webmail.
- Les paramètres IMAP/SMTP sont indiqués uniquement comme secours si l’autodiscover ne configure pas automatiquement le compte.
- Les exemples de comptes utilisent des identités génériques.
