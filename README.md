# ETOURMY J.M : home one-page (direction "Sable")

Implémentation réelle de la direction **1a, Sable** du mockup `ETOURMY - Home.dc.html` (projet Claude Design). Un seul fichier `index.html`, sans framework ni build, même logique que MC Peinture / CB Sols : léger, responsive, SEO local.

## Photos

Toutes les photos dans `/assets` sont **réelles**, scrapées depuis [etourmy-jm.fr](https://www.etourmy-jm.fr/) (page d'accueil + page Références) à la demande explicite du client, sauf `logo-etourmy.png` (logo officiel, même source). Aucune photo de stock.

⚠️ Le mockup design fourni contenait 3 photos corrompues (tronquées à la limite de lecture de l'outil) et 2 fichiers **mal nommés à la source** (`ph-piscine-1.jpg` contenait en réalité une photo de sol, `ph-douche.jpg` contenait la piscine), repérés en comparant les hash. Tout a été revérifié visuellement et renommé correctement avant intégration.

## ⚡ Points forts

- **Léger & sans build** : un seul `index.html`, police Google Fonts (Hanken Grotesk / Instrument Sans / Space Mono), photos auto-hébergées dans `/assets`.
- **Responsive mobile-first** + barre d'action fixe (Appeler / Devis) sur mobile.
- **SEO on-page** : title/description géolocalisés, H1/H2 avec « Nieul-sur-Mer » / « La Rochelle » / « Île de Ré », alt text descriptifs, canonical, Open Graph.
- **Données structurées Schema.org** : `HomeAndConstructionBusiness` (adresse, géo, horaires, zone desservie, SIREN, prestations), `FAQPage`. **Pas d'`aggregateRating`** : je n'ai pas de note chiffrée vérifiée (Google ne montre que 3 avis texte, sans note ni nombre), ne jamais en inventer une.
- **Accessibilité** : lien d'évitement, focus visibles, `<details>` natifs pour la FAQ, `prefers-reduced-motion`, contrastes AA.

## ✅ Déjà vérifié (données réelles)

- Nom légal, SIREN 480 567 932, NAF 4333Z, adresse, téléphone, email, horaires : confirmés via etourmy-jm.fr + societe.com.
- Fondation **1978** (texte réel du site actuel). Le mockup design indiquait à tort « 2005 », corrigé ici.
- 3 avis clients : copiés texte pour texte depuis etourmy-jm.fr, non attribués (le site source ne montre ni nom ni note).

## 🔧 À confirmer avant mise en ligne

1. **Prix** : retirés de la page à la demande du client (plus aucune fourchette affichée sur les cartes prestations).
2. **« Chape liquide & traditionnelle » comme service à part entière** : le site actuel d'ETOURMY ne mentionne que Plâtrerie sèche/isolation, Carrelage/faïence/pierres et Pose de pierres, pas de "chape" en service autonome. La page ci-contre reprend le positionnement stratégique proposé dans le mockup (carrelage + chape + piscine par la même équipe) : à valider avec le client avant publication, ce n'est peut-être pas encore une offre commercialisée telle quelle.
3. **Effectif ("15 personnes" dans le mockup original)** : non vérifiable publiquement, volontairement retiré de cette version. Le réintégrer seulement si confirmé.
4. **Formulaire de devis** : démo uniquement (alert JS, aucun backend). Brancher sur Formspree, Netlify Forms ou un CRM.
5. **Mentions légales / RGPD** : page à créer.
6. **Réseaux sociaux en footer** : Facebook et LinkedIn trouvés sur le site actuel, pas encore ajoutés visuellement (liens dans le JSON-LD `sameAs` uniquement).

## 🗺️ Pages zones

`zones.html` liste les 3 secteurs (Île de Ré / La Rochelle & agglo / Aunis élargi) avec une carte schématique minimaliste (un seul pin sur Nieul-sur-Mer, non contractuelle, aucun fond de carte réel type OSM/Google).

`zones/la-rochelle.html` est la **page type** à dupliquer par commune pour du SEO local (une page = une ville). Pour créer une nouvelle zone : copier ce fichier, remplacer "La Rochelle" par la commune dans le `<title>`, la meta description, le H1, l'intro, la FAQ et le JSON-LD (`name` du breadcrumb + `areaServed`), puis lier la commune correspondante dans `zones.html` (voir le lien sur le pill "La Rochelle").

## 🚀 Mise en ligne rapide (GitHub Pages)

`Settings` → `Pages` → Source : branche `main`, dossier `/root`. Pour la prod réelle, ce fichier est prévu pour remplacer/compléter le site WordPress actuel sur `etourmy-jm.fr`.
