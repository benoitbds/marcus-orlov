# GDPR Starter Kit — Statut de production

> Mis à jour en fin de chaque session de travail.

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
