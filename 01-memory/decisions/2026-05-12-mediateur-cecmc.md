# Médiateur de la consommation — shortlist et arbitrage requis

> Document de décision destiné à Baq. Marcus prépare la matière, Baq tranche.
> Date : 2026-05-12. Statut : à arbitrer en daily ou en mission dédiée.
> Bloque : article 15 CGV (placeholder médiateur), ouverture boutique Gumroad
> (Phase 1 Canal A), mention en page produit.

---

## Pourquoi cette décision maintenant

L'article 15 de la CGV SoBaq (v0.3, livrée 08/05) porte un placeholder
« médiateur de la consommation » à remplir avant publication. La mission
Baq groupée d'ouverture boutique Gumroad (cible jeudi 14 ou vendredi 15
mai) ne peut être émise tant que ce placeholder est ouvert.

Cible du document : produire une matière d'arbitrage propre, sourcée,
qui ferme la décision en moins de quinze minutes côté Baq.

---

## Décomposition par poids (Principe I) — pas par analogie

Avant de comparer des prestataires, décomposer le besoin réel.

**Le besoin légal.** Le Code de la consommation (art. L. 611-1 à
L. 616-3) impose à tout professionnel qui vend à un **consommateur**
(personne physique agissant hors activité professionnelle, art.
liminaire Code conso) de :

1. Adhérer à un médiateur référencé CECMC.
2. Mentionner ses coordonnées sur les CGV et tout document
   précontractuel.
3. Notifier le médiateur au consommateur dans la réponse à une
   réclamation non résolue.

Sanction du manquement : amende administrative **3 000 €** pour
entreprise individuelle, 15 000 € pour société. Source : Service
Public Entreprendre (page F33338, vérifiée 12/05).

**L'exemption B2B.** L'obligation **ne s'applique pas** aux
transactions entre professionnels. Le Code de la consommation parle
exclusivement de « litiges entre consommateur et professionnel ». Les
litiges B2B relèvent du droit commercial commun, pas de la médiation
consumériste. Source identique + portail-autoentrepreneur.fr.

**Le cas SoBaq.** Le kit *GDPR Starter Kit — First B2B Customer*
s'adresse explicitement, par ICP et par contenu, à des entreprises
(SaaS, PME). Le DPA est un instrument juridique controller-to-processor
qui n'a juridiquement aucun sens dans une relation B2C. L'acheteur
naturel est une entreprise.

**Mais Gumroad n'est pas une plateforme B2B.** Sa boutique accepte
tout paiement, peu importe le porteur de carte. Un particulier curieux
peut en théorie acheter — la probabilité est faible (prix 149 €,
contenu technique, ICP étroit) mais non nulle.

D'où deux chemins juridiquement défendables, à arbitrer.

---

## Chemin A — Kit B2B-only, pas de médiateur

**Mécanique.** Modifier la CGV pour restreindre la vente aux
**acheteurs professionnels agissant dans le cadre de leur activité**.
Ajout d'une clause d'attestation côté Gumroad : champ SIRET / VAT
obligatoire, ou case à cocher pré-validation déclarant la qualité
professionnelle de l'acheteur. Refus actif d'un acheteur consommateur.

**Coûts.**
- Coût d'adhésion : **0 €/an**.
- Modification CGV : un article supplémentaire, ~15 lignes, déjà
  cohérent avec l'ICP affiché et l'avertissement L. 71-1130.
- Configuration Gumroad : une case ou un champ supplémentaire au
  checkout. Probable mais à vérifier — Gumroad supporte les champs
  custom (à confirmer côté Baq lors de la mission d'ouverture).
- Trace en cas d'audit : la clause CGV + la trace Gumroad du
  consentement = défense recevable.

**Risques.**
- Un particulier ignore la clause et achète. Le particulier ne peut
  pas saisir un médiateur consumériste (pas de médiateur référencé) ;
  il peut en revanche **dénoncer** SoBaq à la DGCCRF pour défaut
  d'adhésion. Risque administratif : 3 000 € si la DGCCRF estime
  que l'exclusion B2B n'est pas effective.
- Probabilité subjective : faible. ICP étroit (DPO, CTO, fondateur
  SaaS), prix 149 € hors cible consommateur naturelle. Aucun signal
  publicitaire grand public.

**Avantages structurels.**
- Alignement avec l'ICP affiché — pas de discordance entre marketing
  et structure juridique.
- Aucun engagement annuel récurrent.
- Pas de placeholder à maintenir en CGV (changement de médiateur =
  modification CGV).
- Le DPA, instrument controller-to-processor, n'a *aucun sens* pour
  un consommateur — la clause B2B est défendable au fond, pas
  artificielle.

---

## Chemin B — Adhésion à un médiateur référencé CECMC

**Mécanique.** Adhésion à un des médiateurs de la liste CECMC,
mention en CGV, en page produit Gumroad, et en réponse à toute
réclamation non résolue.

**Coûts.**
- Coût d'adhésion : **13 € à 50 € par an** selon prestataire (cf.
  shortlist ci-dessous).
- Coût par litige effectif : 60 € à 150 € (rare).
- Engagement durée : généralement 3 ans, non révocable unilatéralement.
- Modification CGV : remplir le placeholder existant (5 lignes).

**Avantages structurels.**
- Tout acheteur est accepté sans friction au checkout.
- Posture défensive « tout est en ordre » lisible par un acheteur
  attentif (DPO côté client par exemple).
- Pas de calibration Gumroad spécifique.

**Risques.**
- Engagement récurrent — passe le seuil 100 € sur la durée totale
  (3 ans × 50 € = 150 €), donc requiert validation Baq formelle au
  titre du Charter §8.3 (déjà en cours d'arbitrage par le présent
  document, cohérent).
- Si le médiateur retenu se fait retirer de la liste CECMC (cf.
  Médicys), il faut tout recommencer (modification CGV + adhésion
  nouvelle).

---

## Shortlist Chemin B — deux candidats sourcés

### 1. CM2C — *Centre de Médiation et Conciliation Consommation*

- **Coût** : **48 € pour 3 ans** (catégorie 0-10 salariés, applicable
  micro-entreprise sans salarié) — soit **16 €/an**. Source :
  cm2c.net/tarifs.php, vérifié 12/05.
- **Couverture sectorielle** : généraliste. Pas de
  sectorisation exclusive. CM2C est référencé par l'Alliance du
  Commerce (récupération de la suite Médicys, mai 2025).
- **Statut CECMC** : référencé, vérifié sur la liste data.gouv.fr.
- **Inscription** : page `cm2c.net/inscription-professionnel.php`,
  individuelle. Modalité exacte (en ligne / papier) à confirmer au
  moment de l'inscription.
- **Notoriété** : médiateur historique du commerce français,
  reconnu CAPEB, Alliance du Commerce.
- **Position dans la grille** : option **basse-coût**, structurellement
  solide.

### 2. SAS Médiation Solution-Conso

- **Coût** : **147 € pour 3 ans**, tarif unique tous secteurs et
  toutes tailles confondus — soit **49 €/an**. Avec convention
  partenariat : 30 € HT/an. Source :
  sasmediationsolution-conso.fr/faq, vérifié 12/05.
- **Couverture sectorielle** : généraliste, sans distinction de
  taille d'entreprise ni de chiffre d'affaires ni de secteur.
- **Statut CECMC** : référencé.
- **Inscription** : email contact@sasmediationsolution-conso.fr
  ou téléphone +33 (0)4 82 53 93 06. Modalité en ligne à confirmer.
- **Notoriété** : structure consolidée, partenaire notamment
  FFPABC.
- **Position dans la grille** : option **médiane**, sans
  spécialisation marquée.

### Hors shortlist — pourquoi

- **Médicys** : mentionné dans mon journal du 11/05 comme candidat.
  **Retiré de la liste CECMC par décision de la commission** —
  retrait postérieur à novembre 2019, date d'agrément initial.
  Source : alliancecommerce.org (annonce du passage CM2C). À ne
  **pas** retenir, et à signaler comme apprentissage : la
  fraîcheur de la liste CECMC se vérifie à chaque arbitrage.
- **AME CONSO, CNPM Médiation Consommation** : également
  référencés CECMC, non détaillés ici par souci de proportion —
  deux candidats suffisent pour départager. Réintroduction possible
  si Baq rejette les deux premiers.

---

## Recommandation Marcus

Je ne tranche pas. Le choix est capital + structurel et engage SoBaq
sur trois ans minimum si Chemin B retenu.

**Mon poids préférentiel — Chemin A.** Trois raisons.

1. **Alignement de fond.** Le DPA est un instrument B2B par nature.
   Restreindre la vente aux professionnels n'est pas un artifice ;
   c'est la cohérence du produit avec sa structure légale.
2. **Coût zéro récurrent.** Le Principe III (Poids Réel) favorise
   les engagements minimaux à capital faible. 48 € sur trois ans
   n'est pas une somme — mais c'est une obligation à maintenir,
   un placeholder CGV vivant, et un médiateur à surveiller (cf.
   Médicys).
3. **Cible étroite.** À 149 € sur Gumroad, l'ICP affiché est
   structurel — pas un curieux qui passe.

**Mon poids alternatif — Chemin B avec CM2C.** Trois raisons.

1. **Aucune calibration Gumroad spécifique.** L'ouverture boutique
   est déjà chargée en composantes (MoR, IBAN, ZIP, page produit,
   politique privacy). Une case à cocher SIRET en plus, c'est un
   point de friction supplémentaire à valider opérationnellement.
2. **Posture défensive simple.** « Médiateur référencé mentionné,
   tout est en ordre » est une phrase lisible en 10 secondes par
   un DPO côté client. Le Chemin A demande une lecture de l'article
   B2B de la CGV pour conclure pareil.
3. **Coût absolu faible.** 16 €/an chez CM2C. Le différentiel
   versus Chemin A est ~50 € sur 3 ans, c'est un irritant
   marginal sur le capital S1.

**Décision à porter par Baq.** Trois questions à trancher
sciemment :

- **(Q1)** Est-ce que je préfère structurellement aligner SoBaq
  sur un statut B2B-only, ou ouvrir la porte consommateur avec
  l'assurance médiateur ?
- **(Q2)** Si Chemin B, est-ce que CM2C (16 €/an) ou Solution-Conso
  (49 €/an) ?
- **(Q3)** Quel calendrier d'adhésion ? L'inscription CM2C ou
  Solution-Conso prend probablement 1 à 3 jours ouvrés selon
  modalité de paiement et délai de confirmation. À porter dans la
  mission Baq groupée ou en amont.

---

## Conséquences sur la CGV

**Si Chemin A :**
- Article 1 ou nouvelle clause de réserve (avant l'article 15) :
  « La présente vente s'adresse exclusivement à des acheteurs
  professionnels agissant dans le cadre de leur activité, à
  l'exclusion des consommateurs au sens de l'article liminaire du
  Code de la consommation. »
- Article 15 (médiateur) : suppression du placeholder, remplacement
  par une mention de la clause B2B-only.
- Trace Gumroad : champ obligatoire SIRET ou case à cocher
  « j'agis dans le cadre de mon activité professionnelle » avec
  enregistrement de la coche dans le reçu.

**Si Chemin B :**
- Article 15 : remplir le placeholder avec nom du médiateur retenu,
  adresse postale, site web, modalités de saisine.
- Trace Gumroad : mention médiateur en pied de page produit.
- Pas de modification de l'article 1.

Dans les deux cas, modification mécanique côté Marcus une fois la
décision rendue, à intégrer dans la même passe que les autres
placeholders restants (URL boutique, URL politique privacy).

---

## Ce qui reste à arbitrer hors ce document

- Hébergement de la politique de confidentialité (placeholder
  parallèle, à arbitrer aujourd'hui ou demain — voir journal
  12/05).
- Calendrier d'émission de la mission Baq groupée d'ouverture
  boutique Gumroad (cible jeudi 14 ou vendredi 15 mai).

---

## Sources

- Service Public Entreprendre, *Médiation des litiges de la
  consommation*, page F33338 — articles L. 611-1 à L. 616-3 Code
  consommation, sanctions, obligations.
- data.economie.gouv.fr, *Annuaire des médiateurs de la
  consommation*, jeu de données officiel CECMC.
- cm2c.net/tarifs.php, *Grille tarifaire CM2C*.
- sasmediationsolution-conso.fr/faq/obligations-du-professionnel/
  combien-coute-une-adhesion, *Tarif SAS Médiation Solution-Conso*.
- portail-autoentrepreneur.fr, *Médiation de la consommation :
  obligations pour un auto-entrepreneur*.
- alliancecommerce.org, *Nouveau médiateur de la consommation —
  Alliance du Commerce signe avec CM2C* (référence pour le retrait
  Médicys).
