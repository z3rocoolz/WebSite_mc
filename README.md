# Mr Mattia Coda — deux maquettes HTML

Un site de démonstration complet en HTML, CSS et JavaScript natifs, avec quatre photographies originales et des polices locales. Aucun framework ni jQuery n’est nécessaire pour afficher le site.

## Ouvrir la maquette

Dans l’archive livrée, décompressez le dossier puis ouvrez `index.html` dans votre navigateur : la nouvelle proposition « Horizon ». La première proposition est conservée dans `version-01.html`. Un lien en haut de chaque page permet de comparer les deux. Gardez `assets/` et `informations.html` à côté du fichier. Toutes les photos et polices sont incluses : la maquette fonctionne hors connexion.

Dans le dépôt de travail, ces fichiers se trouvent dans `dist/`. Vite est un outil facultatif de prévisualisation pour le développement, jamais une dépendance du site livré.

## Fichiers principaux

- `index.html` : maquette 02 « Horizon », nouveau visuel panoramique, interventions, parcours vertical, FAQ et préparation de consultation.
- `version-01.html` : première maquette conservée pour comparaison.
- `informations.html` : nature de la démonstration, accessibilité, confidentialité, crédits.
- `assets/variation-02.css` : nouvelle présentation responsive et variables de couleurs.
- `assets/styles.css` : présentation de la première version.
- `assets/script.js` : menu mobile et fenêtre de préparation ; amélioration progressive.
- `assets/*.webp` : photographies optimisées et variante mobile du portrait.
- `assets/*.woff2` et `*-OFL.txt` : polices et licences.
- `docs/ANALYSE-ET-CONCEPTION.md` : benchmark et choix éditoriaux.
- `docs/VERIFICATION.md` : contrôles de la deuxième maquette et limites.
- `docs/VERIFICATION-VERSION-01.md` : contrôles précédents conservés.
- `docs/preuves/` : résultats bruts des vérifications.

## Personnaliser

La maquette est centrée sur un chirurgien exerçant seul : Mr Mattia Coda, nom fourni par le commanditaire. Compléter son parcours, ses coordonnées et les textes validés ; remplacer les photographies d’illustration par ses visuels autorisés. Les couleurs principales sont définies dans `:root` au début de la feuille CSS. Les identifiants utilisés par les ancres doivent rester uniques. Conserver la hiérarchie des titres, les états du menu, les libellés accessibles et les styles de focus.

Le nom est celui demandé pour la proposition ; les informations professionnelles n’ont pas été vérifiées. Aucun numéro d’inscription, diplôme, adresse ou témoignage n’a été inventé. Les personnes des photos générées ne représentent pas le chirurgien. La fenêtre de préparation ne réserve pas de rendez-vous. Pour le site définitif, relier un bouton à l’URL réelle de réservation ou à ses coordonnées vérifiées.

## Passage à un site public et référencement

1. Faire relire et valider tous les contenus médicaux par le praticien ; renseigner son identité, ses qualifications, sa localisation et les informations de publication réelles.
2. Adapter les titres et descriptions à chaque page et, si pertinent, à la localisation réelle. Créer ensuite une page spécifique par intervention importante pour approfondir indications, limites, risques, suites et questions fréquentes.
3. Remplacer les URL canoniques et `og:url` par les URL HTTPS publiques définitives. Les URL actuelles désignent uniquement l’aperçu privé.
4. Retirer les balises `noindex, nofollow` et remplacer le `Disallow: /` du `robots.txt` par une règle permettant l’exploration. Laisser le noindex sur toute copie de démonstration.
5. Créer un `sitemap.xml` avec les URL définitives, le déclarer dans robots.txt et soumettre le site à Google Search Console. Exemple de structure ci-dessous, à compléter uniquement avec le vrai domaine.
6. Compléter les données structurées avec les informations réelles et visibles du chirurgien. Aucun classement ou affichage enrichi n’est garanti.
7. Compléter les mentions légales et la politique de confidentialité avec les informations exactes de l’éditeur et de l’hébergeur. Adapter cette politique si un service de rendez-vous, de mesure d’audience ou un formulaire est ajouté.
8. Faire réaliser l’audit d’accessibilité complet du site final, notamment au clavier et avec lecteurs d’écran, puis rédiger une déclaration conforme au périmètre applicable.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url><loc>https://votre-domaine.example/</loc></url>
  <url><loc>https://votre-domaine.example/informations.html</loc></url>
</urlset>
```

Cet exemple utilise volontairement un domaine réservé ; ne pas le publier tel quel.

## Vérifier une modification

Téléverser chaque fichier HTML dans https://validator.w3.org/nu/ ou utiliser le Nu HTML Checker local :

```sh
java -jar vnu.jar --html index.html informations.html version-01.html
```

Tester le menu à petite largeur, la navigation par Tab, l’ouverture/fermeture des accordéons et du guide par Entrée et Échap, l’agrandissement du texte et le fonctionnement sans JavaScript. La validation HTML et un test automatisé d’accessibilité vérifient des choses différentes.
