# villatamasha.eu — page d'atterrissage statique

Site web minimaliste de Villa Tamasha. Un seul écran, focus 100 % sur le bouton de réservation.

## Contenu du dossier

```
villatamasha-eu/
├── index.html              # Page principale (un seul fichier, CSS et JS inline)
├── README.md               # Ce fichier
└── assets/
    ├── villa-hero.jpg      # ⚠ À AJOUTER : photo grand format de la villa (au moins 2000×1200 px)
    ├── logo.png            # Logo horizontal (1200×400, depuis branding/)
    ├── favicon.png         # Icône carrée 180×180 (depuis branding/)
    └── icon-512.png        # Icône carrée 512×512 (Apple Touch Icon)
```

## Avant de mettre en ligne

**Ajouter la photo hero** : copiez votre photo de la villa dans `assets/villa-hero.jpg`.
- Format recommandé : JPEG
- Dimensions : au moins 2000 × 1200 px (idéalement 2600 × 1200 ou plus)
- Poids cible après compression : 250 à 600 Ko (vous pouvez la réduire avec https://squoosh.app)
- Cadrage : la photo doit rester lisible avec un overlay navy de 40 % d'opacité par-dessus, donc privilégier une image claire et contrastée

Une fois la photo en place, ouvrez `index.html` dans un navigateur pour vérifier le rendu.

## Caractéristiques

- **Fichier unique** : tout est dans `index.html` (CSS + JS inline). Pas de dépendance à part Google Fonts pour Lora et Lato.
- **Mobile responsive** : adapté à toutes les tailles d'écran.
- **Multilingue** : français, anglais, espagnol. Détection automatique de la langue du navigateur, mémorisation du choix utilisateur en `localStorage`.
- **SEO-friendly** : title, description, Open Graph, Twitter Card.
- **Léger** : ~12 Ko HTML + photo + logo. Charge en moins d'une seconde.
- **Brand-aligned** : couleurs (#1F4E79 navy, #E8D5B7 cream), typographies Lora et Lato, logo horizontal de la marque, favicon avec le gecko.

## Mise en ligne sur Gandi

1. Connecter le domaine `villatamasha.eu` à un hébergement statique :
   - Option simple : **Gandi Web Forwarding** ne suffira pas car on a besoin d'un vrai hébergement statique. Utiliser **Gandi Simple Hosting** (le même type d'instance que pour le CRM Concorvia) ou créer un nouveau plan dédié.
   - Option économique : **GitHub Pages** ou **Netlify** (gratuits) avec un alias DNS pointant vers `villatamasha.eu`. Mise à jour ultra simple par git push.
   - Option intégrée : héberger ces fichiers directement sur l'instance Gandi qui sert le backend de l'app, sous un sous-chemin `/` ou un sous-domaine dédié.
2. Uploader le contenu de `villatamasha-eu/` à la racine du serveur web.
3. Configurer la redirection HTTPS (Let's Encrypt automatique chez Gandi).
4. Tester la page sur https://villatamasha.eu et sur mobile.

## Évolutions prévues

- **Lien App Store / Google Play** : remplacer l'alerte JavaScript du bouton « Télécharger l'application » par les vrais liens stores une fois l'app publiée.
- **Page galerie** (v2) : ajouter une page secondaire `gallery.html` avec photos additionnelles si demande client.
- **Témoignages** (v2) : ajouter une rangée de témoignages clients.
- **Pages légales** : ajouter `privacy.html` et `terms.html` pour la conformité RGPD lors de la publication de l'app sur les stores (ces URLs sont demandées par Apple et Google).

## Références

- Spec : `../Tamasha_App_Spec_v0.7.docx` (section 4.7 sur la réservation directe).
- Brand : `../BRAND.md`.
- Couleurs et typos : sourcées depuis le BRAND.md.
