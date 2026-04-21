# GDPR Starter Kit — Statut de production

> Mis à jour en fin de chaque session de travail.

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
