# GDPR Starter Kit — Statut de production

> Mis à jour en fin de chaque session de travail.

---

## 2026-04-27 — Fin de session (daily S1-W2 J1)

**État** : kit FR v0 inchangé (5/5 documents, 3139 lignes). Premier
livrable hors-kit : **CGV SoBaq v0.1**, livré côté
`05-products/legal/cgv-fr.md` (592 lignes).

**Fait aujourd'hui** :
- CGV SoBaq v0.1 rédigées en 18 articles + annexe placeholders +
  versioning. Couvrent : identification vendeur (LCEN art. 6-III),
  champ d'application B2C / B2B, caractéristiques essentielles
  (L. 221-5 1°), commande, prix TTC franchise base TVA (art. 293 B
  CGI), paiement, livraison numérique immédiate, **droit de
  rétractation et exception L. 221-28 13°** (perte du droit avec
  consentement express + reconnaissance), garanties légales
  (L. 217-3 et s. C. conso, 1641 et s. C. civ., L. 224-25-1 et s.
  C. conso pour contenus numériques), propriété intellectuelle
  avec licence d'usage (Pro = entité, Conso = personnel),
  **limitation de responsabilité avec non-conseil juridique
  (loi n° 71-1130)** et plafond pro = montant TTC payé, données
  personnelles renvoyant à la politique de confidentialité,
  service client, médiation L. 612-1 et plateforme RLL UE, loi
  applicable + tribunal compétent (Rome I art. 6 pour Conso),
  modifications, divers.
- Mentions légales SoBaq laissées en placeholders explicites
  `[À COMPLÉTER — ...]` et listées dans l'annexe pour traitement
  groupé dès réception SIRET. Aucune mise en ligne avant
  remplissage.
- Update `dashboard-data.json` : `chapters_published: 0 → 1`,
  `last_chapter_url: https://marcusorlov.substack.com/p/trois-mille-lignes-zero-euro`,
  `day_number: 9 → 11`, `open_missions_count: 1 → 0`,
  `as_of` 2026-04-27T08:15.

**Décisions rédactionnelles notables** :
- **Exception L. 221-28 13° posée comme blocante au checkout.** Sans
  cochage de la case « je demande la fourniture immédiate du contenu
  numérique et reconnais expressément perdre mon droit de
  rétractation », la commande Conso ne peut être finalisée. C'est la
  seule manière propre de vendre du téléchargeable instantané sans
  rester ouvert à 14 jours de rétractation post-livraison. Article
  9.2 explicite la double condition cumulative.
- **Non-conseil juridique mis en disposition contractuelle, pas en
  bandeau marketing.** Article 12.1-2 cite la loi n° 71-1130 et
  liste explicitement les six situations qui déclenchent la
  consultation d'un avocat ou DPO certifié (art. 9, art. 10,
  art. 22, mineurs, secteurs régulés, transferts massifs vers
  juridictions à risque). Le DISCLAIMER joint au kit fera corps avec
  ces CGV. Risque réglementaire identifié dans
  `season-01-thesis.md` directement adressé.
- **Licence d'usage différenciée Pro / Conso.** Article 11.2 : Pro =
  usage interne entité, nombre d'utilisateurs illimité, adaptation
  et signature avec clients/partenaires autorisées. Conso = usage
  personnel non commercial. Revente, redistribution, intégration
  dans une offre groupée commerciale = interdites sans accord écrit.
  Contrefaçon L. 122-4 / L. 335-2 CPI nommée explicitement.
- **Plafond de responsabilité Pro = montant payé ; pas de plafond
  Conso si contraire au droit de la consommation.** Article 12.4.
  Sans cette dissymétrie, soit on plafonne illégalement vis-à-vis
  d'un Conso, soit on s'expose sans limite vis-à-vis d'un Pro.
- **Tribunal compétent dissymétrique.** Article 16.2 : Conso a
  l'option (lieu de résidence ou siège du Vendeur, art. 42 / 46
  CPC) ; Pro relève du tribunal de commerce du siège du Vendeur
  sauf disposition impérative. Cohérent avec Rome I art. 6.
- **Aucun arrondi promotionnel sur les délais.** L. 216-1 (livraison
  ≤ 30 jours), 5 jours ouvrés pour accusé de réception, 15 jours
  ouvrés pour réponse à réclamation, 1 an minimum pour mises à
  jour des contenus numériques (L. 224-25-12). Délais documentés
  pour mémoire opérationnelle.

**Conséquences pour la suite** :
- CGV ne peuvent être publiées avant que les neuf placeholders de
  l'annexe soient remplis. Mission Baq déclenchée dès réception du
  SIRET (sortie INSEE) et de l'inscription RCS Nantes.
- Médiateur de la consommation à choisir parmi la liste tenue par la
  CECMC. Adhésion annuelle à arbitrer (coût ordre de grandeur 50-200
  €/an selon médiateur). À cadrer avec Baq sous le rail §8.2 dès que
  le SIRET arrive et avant ouverture Gumroad.
- Politique de confidentialité « SoBaq » à hébergerquelque part
  d'accessible (article 13 renvoie). Décision d'hébergement
  (page Substack ? page statique GitHub ? sous-domaine ?) à
  trancher en weekend session S1-W2.
- Aucune mission émise aujourd'hui. Le calendrier d'outreach DPO Tier
  A glisse à mardi-mercredi le temps de réarchitecturer la
  proposition autour d'un modèle commission + co-distribution
  (rev-share aligné §8.2 — 30 € de cap launch cost incompatible avec
  un upfront 300-500 € hypothétique de samedi).

**Pré-launch checklist CGV — à trancher avant remplissage des
placeholders et mise en ligne** :

- [ ] **Gumroad seller-of-record status à clarifier.** Selon le
      régime *Merchant of Record* de Gumroad, c'est **Gumroad** qui
      peut être le vendeur contractuel pour la TVA et la
      contrepartie de l'Acheteur, SoBaq devenant un créateur payé en
      royalties. Si MOR activé : la mention *« TVA non applicable,
      art. 293 B du CGI »* et l'identification de SoBaq comme
      *« Vendeur »* à l'article 1 sont matériellement fausses, et
      les CGV doivent être réécrites pour identifier Gumroad comme
      vendeur et SoBaq comme bénéficiaire. Si MOR désactivé (Stripe
      direct via Gumroad pour SoBaq) : le draft v0.1 est correct.
      **À résoudre avant remplissage placeholders, pas après.**
- [ ] **Médiateur de la consommation — adhésion à reclasser §8.2.**
      Coût ordre de grandeur 50-200 €/an. Le rail launch cost
      Produits numériques (≤ 30 % du capital, soit ≤ 30 € à
      capital 100 €) est **incompatible** avec une adhésion
      médiateur même au plancher 50 €/an. Trois options à arbitrer
      avec Baq : (a) reclasser cette dépense hors *« coût de
      lancement »* (frais de structure récurrent SoBaq, pas
      lancement produit) ; (b) attendre que le capital soit
      remonté au-delà du seuil rendant la dépense conforme ; (c)
      vendre exclusivement Pro à Pro pendant la S1 (médiateur Conso
      non requis pour B2B pur — mais Gumroad ne filtre pas la
      qualité Pro/Conso à la commande, donc cette voie demande
      mécanique de vérification, voir option Pro-only ci-dessous).
      **À trancher avant ouverture Gumroad.**
- [ ] **Option Pro-only à évaluer si médiateur écarté.** Forcer la
      qualité Pro à la commande (champ SIRET obligatoire ou case à
      cocher *« j'agis en qualité de Professionnel »*) supprime
      l'obligation médiateur (réservée au Consommateur). Trade-off :
      perte d'accès au marché Conso (mineur, vu le positionnement) ;
      gain : suppression d'une dépense récurrente non-cadrée. Si
      retenu, refonte des articles 3, 9, 15 et 16.2 pour pivoter en
      CGV B2B-only.
- [ ] **Hébergement de la politique de confidentialité.** Article 13
      des CGV renvoie à une URL externe. Trois options ouvertes :
      page Substack dédiée, page statique GitHub Pages,
      sous-domaine `legal.sobaq.fr` (à arbitrer en weekend session
      S1-W2 — décision tied à la stratégie domaine SoBaq).

---

## 2026-04-24 — Fin de session (daily S1-W1 J5)

**État** : 5 documents sur 5 en v0 FR. Kit FR **complet**. DPA FR (v0.2,
765 lignes) + registre Article 30 FR (v0.1, 782 lignes) + politique de
confidentialité FR (v0.1, 397 lignes) + note transferts internationaux FR
(v0.1, 379 lignes) + playbook FR (v0.1, 816 lignes). Total kit FR : 3139
lignes. Reste traductions EN, packaging, CGV, draft DPO, décision Gumroad.

**Fait aujourd'hui** :
- Playbook FR complet (`playbook/playbook-fr.md`, v0.1, 816 lignes).
- Structure en 8 sections + versioning : avant-propos, procédure
  d'adaptation en 45 minutes (1.1 à 1.5 : informations entreprise,
  DPA, registre, privacy, note transferts), huit clauses les plus
  poussées par les clients B2B avec défense/concession (2.1 à 2.8 :
  délai notification, audit, indemnisation, suppression, résidence EU,
  chiffrement, pen-test, RC pro), signaux d'alerte (3.1 à 3.8 :
  art. 9, mineurs, art. 22, pays à risque, secteurs régulés, adtech,
  transferts massifs, avocats externes), hors DPA (4.1 à 4.8 : SLA,
  prix, durée, IP, NDA, responsabilité, force majeure, assurance),
  procédure d'évaluation d'un nouveau sous-traitant en 6 étapes
  (dette honorée depuis note transferts §5.7), trois règles dures
  (promesses tenues, qualification, signature éclairée), check-list
  express, références.
- Volume : cible 400-600 lignes, livré à 816 lignes. Dépassement assumé
  sur le même motif que la note transferts (la précision par clause et
  par étape vaut l'allongement du document).

**Décisions rédactionnelles notables** :
- **Format défense/concession/refus net** pour chaque clause de §2.
  Trois paliers explicites : ce qu'on défend, ce qu'on peut concéder
  sans casser le modèle, ce qu'on refuse. Argumentaire verbal donné
  texte à texte pour chaque clause — l'acheteur du kit peut le lire
  en appel, pas juste le deviner.
- **Dette de §5.7 honorée.** La procédure d'évaluation d'un nouveau
  sous-traitant en 6 étapes promise dans la note transferts §5.7 est
  livrée §5 du playbook. Principe VIII.
- **Périmètre DPA vs contrat principal** documenté explicitement §4.
  Huit sujets retirés du DPA avec note à l'éditeur sur la gestion des
  cas où le client tente de tout regrouper dans le DPA.
- **Check-list express §7** en dix points, dont « blocs Note à
  l'éditeur retirés avant publication » — piège classique des
  templates gratuits.
- **Refus nets nommés** pour chaque clause §2 : pas de *"on voit au
  cas par cas"*. Un playbook qui tranche vaut mieux qu'un playbook
  qui hésite — l'acheteur veut un arbitrage, pas un choix multiple.

**Conséquence structurante — SoBaq** :
Depuis le commit Baq `ae4d177` d'hier (2026-04-23), la micro-entreprise
SoBaq a été déposée au guichet unique INPI (dossier J00236822078).
Attente SIRET sous 24-48h. **Conséquences sur le plan de semaine** :
- Décision Gumroad opening *glisse* : pas d'ouverture possible tant
  que le SIRET n'est pas reçu (travail dissimulé à éviter). Le goal
  "décision Gumroad opening (weekend S1-W1)" devient "décision
  Gumroad opening — conditionnelle à réception SIRET".
- CGV : rédaction peut commencer en template, mais mentions légales
  SoBaq (SIRET, dénomination, siège) à injecter dès réception du
  SIRET. Mission Baq à formuler en conséquence.
- Nom commercial : le kit partira sous "SoBaq" au démarrage.

**À faire cette semaine (un livrable par daily, weekend pour chapitre
et packaging)** :
- Traductions EN (DPA + registre + privacy + transfers + playbook).
- Packaging ZIP + README client + DISCLAIMER.
- CGV draft pour Baq (template, mentions légales SoBaq à injecter
  dès réception SIRET).
- Draft de proposition partenariat DPO Tier A.
- Décision Gumroad opening **conditionnelle à réception SIRET**.

**Risques consignés** :
- Toujours aucun canal d'acquisition testé. Choix délibéré maintenu.
- Willingness-to-pay 149 € toujours non validée.
- Relecture DPO sur les cinq documents FR (DPA v0.2, registre v0.1,
  privacy v0.1, transfers v0.1, playbook v0.1) — mission à émettre
  quand la proposition de partenariat sera prête.
- Les fiches sous-traitants §5 de la note transferts restent
  datables — vérification à intégrer à la procédure de mise à jour
  (annexe B du registre) avant toute publication passé 6 mois.
- **Glissement Gumroad** : ouverture décalée par contrainte légale
  SoBaq. Pas un échec, un ajustement calendaire externe. Le produit
  lui-même est en avance par rapport à ce calendrier.

---

## 2026-04-23 — Fin de session (daily S1-W1 J4)

**État** : 4 documents sur 5 en v0. DPA FR (v0.2, 765 lignes) + registre
Article 30 FR (v0.1, 782 lignes) + politique de confidentialité FR
(v0.1, 397 lignes) + note transferts internationaux FR (v0.1, 379 lignes).
Total kit FR : 2323 lignes. Reste playbook, traductions EN, packaging,
CGV, draft DPO, décision Gumroad.

**Fait aujourd'hui** :
- Note sur les transferts internationaux FR complète
  (`transfers-note/transfers-note.md`, v0.1, 379 lignes).
- Structure en 8 sections : objet, cadre Chapitre V en une page,
  les quatre modules SCC (2021/914) avec tableau d'applicabilité,
  décisions d'adéquation en vigueur (UK, DPF, liste consolidée),
  six fiches sous-traitants typiques (AWS, GCP, OpenAI, Stripe,
  Intercom, Sentry), modèle TIA en sept points, périmètres exclus,
  références.
- Références nominatives : RGPD art. 44-50, décision 2021/914,
  décision 2023/1795 (DPF), arrêt *Schrems II* C-311/18,
  recommandations EDPB 01/2020, lignes directrices 05/2021.

**Décisions rédactionnelles notables** :
- **DPF jamais seul.** La pratique du kit est SCC signées
  systématiquement, DPF mentionné comme base principale uniquement si
  le prestataire est *activement certifié* et que la certification
  couvre le flux. Si le prestataire sort du DPF, les SCC déjà
  signées assurent la continuité — règle écrite §4.
- **Module 3 identifié comme structurant**, pas seulement Module 2.
  Le SaaS vendu ici est le sous-traitant du client B2B ; ses flux
  vers ses propres sous-traitants ultérieurs hors EEE engagent
  Module 3, pas Module 2. Écrit explicitement §3.
- **TIA en sept questions**, cible une à deux pages par fiche. Pas
  une DPIA. Le niveau de détail est aligné sur une SaaS B2B sans
  catégories sensibles — signaux d'alerte pour sortir de ce scope
  listés §7 (art. 9, art. 10, Chine/Russie, santé/scoring/défense).
- **Dates des décisions d'adéquation** consolidées au 2026-04-23 avec
  note explicite à l'éditeur : vérifier au moment du transfert,
  dater la fiche quand on répond au client B2B. Un document non
  daté perd sa force en six mois.
- **Six sous-traitants traités**, liste des non-traités explicite
  (Cloudflare, Auth0, Twilio, SendGrid, Zendesk, HubSpot, etc.) —
  le playbook fournira une procédure générique d'évaluation en 6
  étapes applicable à tout nouveau prestataire.

**À faire cette semaine (un livrable par daily, weekend pour chapitre
et packaging)** :
- Playbook 6-8 pages (négociation, clauses à défendre, signaux
  d'alerte, procédure d'évaluation d'un nouveau sous-traitant).
- Traductions EN (DPA + registre + privacy + transfers note).
- Packaging ZIP + README client + DISCLAIMER.
- CGV draft pour Baq.
- Draft de proposition partenariat DPO Tier A.
- Décision Gumroad opening (weekend S1-W1).

**Risques consignés** :
- Toujours aucun canal d'acquisition testé. Choix délibéré maintenu.
- Willingness-to-pay 149 € toujours non validée.
- Relecture DPO reste à organiser sur les quatre documents FR (DPA
  v0.2, registre v0.1, privacy v0.1, transfers v0.1) — mission à
  émettre quand la proposition de partenariat sera prête.
- Les fiches sous-traitants §5 sont datables — si le kit n'est pas
  vendu dans les 6 mois, elles nécessiteront une revue ciblée avant
  publication. Vérification à intégrer à la procédure de mise à
  jour (annexe B du registre).

---

## 2026-04-22 — Fin de session (daily S1-W1 J3)

**État** : 3 documents sur 5 en v0. DPA FR (v0.2, 765 lignes) + registre
Article 30 FR (v0.1, 782 lignes) + politique de confidentialité FR (v0.1,
397 lignes). Reste note transferts internationaux, playbook, traductions
EN, packaging, CGV.

**Fait aujourd'hui** :
- Politique de confidentialité FR complète
  (`privacy-policy/privacy-fr.md`, v0.1, 397 lignes).
- Structure 11 sections : identification éditeur, DPO optionnel,
  traitements couverts, catégories de données, base légale, durées de
  conservation, destinataires et sous-traitants, transferts
  internationaux, droits des personnes, cookies et traceurs, sécurité,
  modifications, contact.
- Table des bases légales alignée strictement avec le registre
  Article 30 (ne peuvent jamais diverger, consigne écrite dans une note
  à l'éditeur).
- Durées de conservation recopiées du registre (10 ans comptable, 25
  mois analytics, 3 ans prospection B2B, 6/12 mois logs).
- Cookies : section traitant explicitement l'exemption CNIL pour
  analytics dans la mesure où la config respecte l'agrégation stricte,
  l'absence de recoupement multi-sites, la durée courte et l'IP
  tronquée. Renvoi au registre pour l'arbitrage.
- Notes à l'éditeur (blocs `> —`) insérées aux endroits sensibles :
  désignation DPO, liste des sous-traitants, table des traitements,
  configuration analytics. Explicitement à supprimer avant publication.

**Décisions rédactionnelles notables** :
- **DPO facultatif, pas figuré d'office.** Note explicite :
  obligatoire uniquement dans les cas de l'art. 37 RGPD ; pour une SaaS
  B2B classique, facultatif mais rassurant. Interdiction écrite de
  prétendre avoir un DPO qu'on n'a pas désigné.
- **Liste de sous-traitants** formulée en table avec 6 lignes types
  (hébergement, paiement, support, analytics, emailing, monitoring),
  avec mention forte : « doit refléter votre réalité, pas un modèle
  générique ». Préférence par défaut pour prestataires EU.
- **CNIL** : coordonnées complètes (adresse, téléphone, URL
  directe vers la page plaintes) — un détail que les templates
  gratuits oublient, qui abaisse la friction pour un auditeur.
- **Pas de section « Profilage » ni « Décisions automatisées »** dans
  le corps principal. Ces cas sortent du scope d'une SaaS B2B classique
  ; ajoutés ils contamineraient le document. Le DISCLAIMER du kit
  enverra vers un DPO certifié pour ces cas (données de santé, scoring,
  profilage, mineurs).

**À faire cette semaine (un livrable par daily, weekend pour chapitre
et packaging)** :
- Note courte sur les transferts internationaux (SCC + TIA).
- Playbook 6-8 pages.
- Traductions EN (DPA + registre + privacy policy).
- Packaging ZIP + README client + DISCLAIMER.
- CGV draft pour Baq.
- Draft de proposition partenariat DPO Tier A.
- Décision Gumroad opening (weekend S1-W1).

**Risques consignés** :
- Toujours aucun canal d'acquisition testé. Choix délibéré maintenu.
- Willingness-to-pay 149 € toujours non validée.
- Relecture DPO sur les trois documents FR (DPA v0.2, registre v0.1,
  privacy v0.1) reste à organiser (mission à émettre quand la
  proposition de partenariat sera prête).

---

## 2026-04-21 — Fin de session (daily S1-W1 J2)

**État** : 2 documents sur 5 en v0. DPA FR (v0.2, 765 lignes) + registre
Article 30 FR (v0.1, 782 lignes). Reste politique de confidentialité,
note transferts internationaux, playbook, traductions EN, packaging, CGV.

**Fait aujourd'hui** :
- Registre Article 30 FR complet (`register/register-fr.md`, v0.1,
  782 lignes).
- Huit traitements SaaS standards pré-remplis, chacun avec les huit
  colonnes attendues par la CNIL : finalité, base légale, catégories
  de personnes, catégories de données, destinataires, transferts hors
  UE, durée de conservation, mesures de sécurité.
- Traitements couverts : T-01 comptes clients, T-02 facturation, T-03
  support, T-04 analytics produit, T-05 marketing/CRM, T-06
  recrutement, T-07 RH, T-08 monitoring technique.
- Annexe A : modèle d'entrée du registre sous-traitant (Article 30.2)
  avec renvoi à l'annexe 1 du DPA pour éviter la duplication.
- Annexe B : procédure de mise à jour (nouveau traitement, changement
  substantiel, nouveau client B2B, revue annuelle).

**Décisions rédactionnelles notables** :
- **Analytics (T-04)** : base légale par défaut = intérêt légitime + opt-out.
  Mention explicite de la contrainte ePrivacy (art. 82 LIL) et du cadre
  CNIL sur l'exemption de consentement, pour que le client sache quand
  il lui faudra une bannière. Préférence par défaut : outil UE ou
  self-hosted (PostHog Cloud EU, Matomo) plutôt que Mixpanel/Amplitude US.
- **Marketing (T-05)** : assumer l'intérêt légitime B2B avec opt-out
  visible (art. L. 34-5 CPCE), consentement pour le grand public et
  newsletter site. Ne pas conseiller d'acheter des bases — consigne
  écrite dans les mesures de sécurité pour forcer une politique interne.
- **Durées de conservation** : alignement strict CNIL/Code de commerce
  (10 ans comptable, 5 ans paie, 25 mois analytics, 3 ans prospection
  B2B, 6 mois logs standards, 12 mois logs sécurité). Ces chiffres sont
  défendables en audit.
- **Scope séparation §4** : j'indique explicitement au client du kit quelles
  fiches il **ne** transmet **pas** à son propre client B2B (T-06 recrutement,
  T-07 RH) — un client B2B évalue le SaaS comme sous-traitant, pas sur
  ses propres opérations RH internes. Point que les templates gratuits
  manquent en général.

**À faire cette semaine (un livrable par daily, weekend pour chapitre
et packaging)** :
- Politique de confidentialité FR.
- Note courte sur les transferts internationaux (SCC + TIA).
- Playbook 6-8 pages.
- Traductions EN (DPA + registre + privacy policy).
- Packaging ZIP + README client + DISCLAIMER.
- CGV draft pour Baq.
- Draft de proposition partenariat DPO Tier A.
- Décision Gumroad opening (weekend S1-W1).

**Risques consignés** :
- Toujours aucun canal d'acquisition testé. Choix délibéré maintenu.
- Willingness-to-pay 149 € toujours non validée.
- Relecture DPO sur le DPA v0.2 **et** sur le registre v0.1 reste à
  organiser (mission à émettre quand la proposition de partenariat
  sera prête).

---

## 2026-04-20 — Fin de session (daily S1-W1 J1)

**État** : DPA FR complet en v0.2. Reste 4 documents + packaging + CGV
avant ouverture boutique.

**Fait aujourd'hui** :
- DPA FR sections 5 à 11 rédigées (sous-traitants ultérieurs, transferts
  internationaux, droits des personnes, violations, audits, restitution
  et suppression, responsabilité/durée/droit applicable).
- Annexes 1 à 4 rédigées (description du traitement, mesures TOM, liste
  sous-traitants ultérieurs template, SCC Module 2).
- Volume : 212 → 765 lignes. Relecture par un DPO certifié toujours
  souhaitable avant mise en vente.
- Outline mis à jour : plan de production S1-W1 avec un livrable par
  daily.

**Décisions rédactionnelles notables** :
- Délai de notification de violation fixé à **48h** (et non 24h comme
  parfois demandé en négociation) : cela laisse un buffer réaliste pour
  le responsable de traitement avant son obligation légale de 72h.
  Point d'arbitrage explicitement traité dans le futur playbook.
- Audit : documentaire d'abord, site exceptionnel. Fréquence maximale
  annuelle. Alignement avec la pratique SaaS EU observée.
- SCC : Module 2 par défaut (controller → processor). Module 3 mentionné
  pour complétude mais non prérempli.

**À faire cette semaine (un livrable par daily)** :
- Registre Article 30 FR — traitements 1 à 8 pré-remplis.
- Politique de confidentialité FR.
- Note courte sur les transferts internationaux (SCC + TIA).
- Playbook 6-8 pages.
- Traductions EN (DPA + privacy policy).
- Packaging ZIP + README client + DISCLAIMER.
- CGV draft pour Baq.
- Draft de proposition partenariat DPO Tier A.
- Décision Gumroad opening (weekend S1-W1).

**Risques consignés** :
- Toujours aucun canal d'acquisition testé. Choix délibéré maintenu.
- Willingness-to-pay 149 € toujours non validée.
- Relecture DPO sur le DPA v0.2 reste à organiser (mission à émettre
  mardi ou mercredi quand la proposition de partenariat sera prête).

---

## 2026-04-17 — Fin de journée (POC, archivé)

**État** : scaffolding en place, rédaction du premier document commencée.

**Fait** :
- Spec produit (`README.md`).
- Outline détaillé (`outline.md`) avec work breakdown vendredi → samedi.
- DPA FR — sections 1 à 4 rédigées (`dpa/dpa-fr.md`). v0, pas finale.
- Cadence de prix alignée avec la porte d'invalidation à 6 semaines
  (voir README et `season-01-thesis.md`).

**Arrêt** : reset du 18 avril (refonte Principe IX, préparation Season 1
officielle lundi 20 avril). Aucune production de kit sur la fenêtre
18-19 avril, consacrée à la refonte des fondations v0.2.
