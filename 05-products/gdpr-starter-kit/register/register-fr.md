# Registre des activités de traitement — Article 30 RGPD

> **Modèle documentaire — à adapter à votre situation.**
>
> Ce registre est un modèle rédigé sur la base de l'article 30 du Règlement
> (UE) 2016/679 (RGPD) et des recommandations publiques de la CNIL
> (notamment le modèle de registre publié en 2022). Il n'est pas un conseil
> juridique individuel. Pour une situation complexe ou sensible (données de
> santé, mineurs, profilage automatisé, secteurs régulés, traitements à
> grande échelle), consultez un avocat ou un DPO certifié avant de le
> publier comme votre registre officiel.
>
> Version v0.1 — 2026-04-21. Langue : français. Version anglaise en
> préparation.

---

## Note préalable — quel registre, pour qui

L'article 30 RGPD impose **deux registres distincts** qui se complètent :

- **Article 30, paragraphe 1 — registre du responsable de traitement.**
  Il recense les traitements que votre entreprise opère *pour son propre
  compte* : gestion de ses salariés, marketing, facturation, recrutement,
  etc. C'est l'objet principal du présent document.
- **Article 30, paragraphe 2 — registre du sous-traitant.** Il recense les
  traitements que votre entreprise opère *pour le compte d'un tiers*,
  typiquement vos clients B2B quand vous êtes éditeur SaaS. Un modèle
  d'entrée de ce second registre figure en **Annexe A** et fait le lien
  avec l'annexe 1 du DPA (description du traitement) déjà livrée aux
  clients.

Une SaaS B2B qui vend un service à d'autres entreprises est typiquement
**à la fois responsable de traitement** (pour ses propres opérations) **et
sous-traitant** (pour le service qu'elle fournit à ses clients). Les deux
registres doivent exister et être tenus à jour. L'autorité de contrôle
(CNIL en France) peut les demander à tout moment (art. 30.4 RGPD).

Ce modèle est volontairement scopé sur une SaaS de moins de 50 personnes
ayant décroché son premier client B2B. Si vous dépassez ce cadre
(données de santé, scoring, profilage, secteurs régulés), ajoutez les
traitements spécifiques et faites relire le registre par un DPO certifié.

---

## 1. Fiche d'identification

**Raison sociale :** [NOM DE LA SOCIÉTÉ]
**Forme juridique :** [SAS / SARL / ...]
**SIREN :** [NUMÉRO]
**Siège social :** [ADRESSE]
**Représentant légal :** [NOM, QUALITÉ]

**Délégué à la protection des données (DPO) :**
- [ ] Désigné — nom, coordonnées : [NOM] · [EMAIL] · [TÉLÉPHONE]
- [ ] Non désigné (non obligatoire au sens de l'article 37 RGPD —
  à réévaluer dès que le traitement de données devient à grande
  échelle ou régulier et systématique)

**Référent protection des données interne** (si pas de DPO formel) :
[NOM, FONCTION, EMAIL]

**Date d'ouverture du registre :** [AAAA-MM-JJ]
**Dernière mise à jour :** [AAAA-MM-JJ]
**Périodicité de revue :** annuelle + à chaque nouveau traitement ou
modification substantielle.

---

## 2. Table synthétique des traitements

Cette table est le résumé exécutif du registre. Chaque ligne renvoie à
une fiche détaillée au §3.

| # | Traitement | Finalité principale | Base légale | Personnes concernées | Durée de conservation principale |
|---|---|---|---|---|---|
| T-01 | Gestion des comptes clients | Fourniture et administration du service | Exécution du contrat (art. 6.1.b) | Utilisateurs admin des clients B2B | Durée du contrat + 3 ans |
| T-02 | Facturation et recouvrement | Émission, encaissement, recouvrement | Exécution du contrat + obligation légale | Contacts facturation clients | 10 ans (comptable) |
| T-03 | Support client | Traitement des demandes, bugs, questions | Exécution du contrat + intérêt légitime | Utilisateurs des comptes clients | 3 ans après clôture du ticket |
| T-04 | Analytics produit | Compréhension de l'usage, priorisation roadmap | Intérêt légitime (art. 6.1.f) | Utilisateurs du service | 25 mois |
| T-05 | Marketing et CRM | Communication commerciale, nurture prospects | Intérêt légitime B2B + opt-out / consentement B2C | Prospects et clients | 3 ans après dernier contact |
| T-06 | Recrutement | Traitement des candidatures | Mesures précontractuelles + consentement (post-processus) | Candidats | 2 ans post-dernier contact (avec consentement) |
| T-07 | Gestion RH | Contrat de travail, paie, formation | Exécution du contrat + obligation légale | Salariés | 5 ans post-contrat (paie), selon matière pour le reste |
| T-08 | Monitoring technique | Sécurité, détection d'incidents, debug | Intérêt légitime (sécurité) | Utilisateurs (indirect) | 6 mois standard / 12 mois sécurité |

Ajoutez une ligne à cette table pour tout nouveau traitement identifié.
Si un traitement proposé ne trouve pas sa place ici (ex : modération
de contenu utilisateur, enrichissement par IA générative, scoring
crédit), **il faut une fiche dédiée et vraisemblablement une analyse
d'impact (AIPD, art. 35 RGPD)**.

---

## 3. Fiches détaillées par traitement

Chaque fiche couvre les huit colonnes attendues par la CNIL : finalité,
base légale, catégories de personnes, catégories de données,
destinataires, transferts hors UE, durée de conservation, mesures de
sécurité.

Les valeurs entre crochets `[...]` sont à renseigner ou adapter par le
client. Les valeurs non crochetées sont des défauts raisonnables pour
une SaaS EU < 50 personnes, à challenger si votre contexte diffère.

### T-01 — Gestion des comptes clients

**Responsable de traitement :** [NOM DE LA SOCIÉTÉ]
**Responsable opérationnel :** [CTO / Head of Product / ...]

**Finalité.** Permettre aux utilisateurs des clients B2B d'accéder au
service, d'administrer leurs paramètres, leurs équipes, leurs droits et
leur facturation. Assurer la traçabilité des actes d'administration pour
des raisons de sécurité et d'auditabilité.

**Base légale.** Exécution du contrat conclu avec le client B2B
(art. 6.1.b RGPD). Les utilisateurs admin accèdent au service en vertu
de ce contrat. Pour les logs d'authentification et les journaux
d'administration, **intérêt légitime** (art. 6.1.f) — sécurité du
service.

**Catégories de personnes concernées.**
- Utilisateurs admin des clients B2B (employés de l'entreprise cliente).
- Le cas échéant, utilisateurs invités (collaborateurs externes, partenaires).

**Catégories de données.**
- Données d'identification : nom, prénom, email professionnel.
- Données d'authentification : identifiant, hash du mot de passe (jamais
  en clair), facteur(s) d'authentification (MFA).
- Données de rôle : rôle dans l'organisation, permissions, équipe
  d'appartenance.
- Données de préférence : langue, fuseau horaire, notifications.
- Journaux d'activité : horodatages de connexion, IP, user agent,
  actions d'administration significatives.

**Destinataires.**
- En interne : équipes produit, support, sécurité, avec droits gradués.
- Sous-traitants : hébergeur cloud (ex : [AWS Frankfurt / OVHcloud /
  Scaleway]), fournisseur d'authentification (ex : [Auth0 / Clerk /
  Keycloak self-hosted]), outil de gestion des accès (ex : [Okta /
  interne]).

**Transferts hors UE.**
- Si hébergement en région UE (ex : AWS `eu-central-1`, OVHcloud Gravelines) :
  **pas de transfert**. Attention à la question du CLOUD Act
  américain — à documenter dans la note transferts du kit.
- Si fournisseur auth US (Auth0) : transfert encadré par **Clauses
  Contractuelles Types** (SCC, décision 2021/914, module 2) et
  éventuellement **adhésion au Data Privacy Framework (DPF)** si
  applicable.

**Durée de conservation.**
- Comptes actifs : durée du contrat commercial avec le client B2B.
- Après résiliation : conservation 3 ans pour preuves contractuelles
  (prescription commerciale, art. L. 110-4 Code de commerce), puis
  anonymisation ou suppression.
- Journaux d'authentification : 6 mois par défaut (recommandation CNIL),
  12 mois si logs de sécurité.

**Mesures de sécurité.**
- Mots de passe stockés sous forme de hash (Argon2id ou bcrypt, jamais
  MD5/SHA-1 seul).
- MFA disponible, imposé pour les comptes à privilèges.
- TLS 1.2 minimum (TLS 1.3 recommandé) sur toutes les communications.
- Cloisonnement des accès par rôle (principe du moindre privilège).
- Journalisation des actions d'administration (création / suppression
  de compte, élévation de privilèges).
- Revue trimestrielle des comptes internes (rotation, désactivation
  des comptes orphelins).

---

### T-02 — Facturation et recouvrement

**Responsable de traitement :** [NOM DE LA SOCIÉTÉ]
**Responsable opérationnel :** [CFO / Finance / ...]

**Finalité.** Émettre les factures aux clients, percevoir les
paiements, relancer les impayés, tenir la comptabilité, répondre aux
obligations déclaratives (TVA, déclarations fiscales).

**Base légale.**
- **Exécution du contrat** (art. 6.1.b) pour l'émission des factures et
  le recouvrement.
- **Obligation légale** (art. 6.1.c) pour la conservation des pièces
  comptables (10 ans, art. L. 123-22 Code de commerce).

**Catégories de personnes concernées.**
- Contacts facturation désignés par les clients B2B.
- Représentants légaux des clients, quand nécessaires à la relation
  commerciale.

**Catégories de données.**
- Identification de la société cliente : raison sociale, SIREN/SIRET,
  n° TVA intracommunautaire, adresse de facturation.
- Identification du contact facturation : nom, prénom, fonction,
  email, téléphone professionnel.
- Données de paiement : identifiant de moyen de paiement tokenisé
  (jamais le numéro complet de carte stocké par nos soins), historique
  de paiements, montants, statuts.
- Données de recouvrement : incidents de paiement, relances,
  échéanciers.

**Destinataires.**
- En interne : comptabilité, direction financière, support commercial
  (pour relances de premier niveau).
- Sous-traitants : prestataire de paiement (ex : [Stripe / Mollie /
  Adyen / GoCardless]), outil de facturation (ex : [Pennylane /
  Stripe Billing / interne]), expert-comptable externe.
- Tiers : administration fiscale (via déclarations), commissaire aux
  comptes (le cas échéant).

**Transferts hors UE.**
- Stripe Inc. : siège US. Transferts encadrés par **SCC** + adhésion
  au **DPF**. Données stockées principalement sur infrastructure UE
  pour les flux européens, à confirmer dans le DPA Stripe.
- Mollie, GoCardless Europe : traitements principalement UE, pas de
  transfert significatif.

**Durée de conservation.**
- Factures et pièces comptables : **10 ans** à compter de la clôture
  de l'exercice (art. L. 123-22 Code de commerce).
- Données de paiement tokenisées : conservées par le prestataire de
  paiement selon ses propres durées.
- Données de contact facturation en base active : durée du contrat + 3 ans.

**Mesures de sécurité.**
- Chiffrement au repos des données de facturation (chiffrement de la
  base de données).
- Tokenisation systématique des moyens de paiement : pas de PAN complet
  en base.
- Accès restreint au périmètre finance/compta (principe du moindre
  privilège).
- Traçabilité des exports comptables (qui, quand, quel périmètre).
- Convention écrite avec l'expert-comptable encadrant la confidentialité
  et la protection des données.

---

### T-03 — Support client

**Responsable de traitement :** [NOM DE LA SOCIÉTÉ]
**Responsable opérationnel :** [Head of Support / CTO / ...]

**Finalité.** Répondre aux demandes des utilisateurs des clients
(questions fonctionnelles, bugs, demandes d'accompagnement),
diagnostiquer les incidents, améliorer le service.

**Base légale.**
- **Exécution du contrat** (art. 6.1.b) : le support est une prestation
  due dans le cadre du service.
- **Intérêt légitime** (art. 6.1.f) pour l'usage anonymisé des tickets
  à des fins d'amélioration produit — avec test de mise en balance
  documenté.

**Catégories de personnes concernées.**
- Utilisateurs des comptes clients (admin ou utilisateurs finaux selon
  le plan).
- Auteurs de la demande (si différent de l'utilisateur concerné).

**Catégories de données.**
- Identité et coordonnées : nom, email, entreprise cliente.
- Contenu du ticket : message texte, captures d'écran éventuelles,
  logs applicatifs joints par l'utilisateur ou l'équipe support.
- Contexte technique : URL concernée, ID utilisateur, ID de ressource,
  horodatage de l'incident.
- Historique : échanges antérieurs, statut, réponses apportées.

**Attention.** Les captures d'écran et logs joints peuvent contenir
accidentellement des données sensibles (données de clients finaux,
informations personnelles). Consigne interne recommandée : ne pas
demander à l'utilisateur de joindre un export brut ; préférer des
identifiants techniques et une reproduction en environnement de test.

**Destinataires.**
- En interne : équipe support, équipe produit et ingénierie pour
  escalade.
- Sous-traitants : outil de ticketing / chat (ex : [Intercom /
  Zendesk / Freshdesk / Crisp / Help Scout]).

**Transferts hors UE.**
- Intercom, Zendesk, Freshdesk : sociétés US. Transferts encadrés par
  **SCC** + **DPF** selon les cas. À documenter précisément dans le DPA
  du prestataire.
- Crisp : éditeur français, données stockées en UE — vérifier.
- Help Scout : US.

**Durée de conservation.**
- Tickets ouverts : durée du traitement.
- Tickets clos : **3 ans** après clôture pour preuve contractuelle et
  analyse de récurrence, puis anonymisation ou suppression.
- Données de contact du demandeur : durée du contrat + 3 ans.

**Mesures de sécurité.**
- Droits d'accès gradués (support L1 / L2 / ingénierie).
- Journalisation des consultations sensibles (accès à un ticket
  contenant des données d'un autre client par exemple).
- Purge automatique des pièces jointes après résolution + délai de
  rétention court (30-90 jours).
- Clauses de confidentialité dans les contrats de travail et dans le
  DPA avec l'éditeur de l'outil de ticketing.

---

### T-04 — Analytics produit

**Responsable de traitement :** [NOM DE LA SOCIÉTÉ]
**Responsable opérationnel :** [Head of Product / Data Lead / ...]

**Finalité.** Comprendre l'usage du produit, mesurer l'adoption des
fonctionnalités, détecter les frictions, prioriser la roadmap. **Pas
de profilage individuel à des fins de décision automatisée** à ce
stade.

**Base légale.**
- **Intérêt légitime** (art. 6.1.f) pour une analytics agrégée et
  pseudonymisée, avec mise à disposition d'un droit d'opposition clair
  et accessible.
- **Consentement** (art. 6.1.a) requis si l'analytics s'appuie sur des
  cookies non strictement nécessaires (directive ePrivacy transposée
  en art. 82 Loi Informatique et Libertés), ou si l'usage va au-delà
  de l'analytics agrégée.

**Note CNIL.** La dispense de consentement pour les cookies analytics
n'est possible que dans des conditions strictes : statistiques
agrégées, pas de recoupement avec d'autres traitements, pas de suivi
inter-sites, durée de conservation limitée. À défaut, bannière de
consentement nécessaire.

**Catégories de personnes concernées.**
- Utilisateurs authentifiés du service.
- Utilisateurs anonymes visitant le site public (traités séparément
  si bannière cookies).

**Catégories de données.**
- Identifiants techniques : `user_id` pseudonymisé (hash stable non
  réversible sans clé), `session_id`, `device_id`.
- Événements produit : actions réalisées (clic, création, export,
  activation de fonctionnalité), horodatage.
- Métadonnées techniques : type d'appareil, OS, navigateur, langue,
  résolution, fuseau horaire.
- **Non collectés** : contenu des formulaires, valeurs saisies,
  documents uploadés, contenu applicatif métier.

**Destinataires.**
- En interne : équipe produit, équipe growth / data.
- Sous-traitants : outil analytics (ex : [PostHog self-hosted EU /
  PostHog Cloud EU / Matomo self-hosted / Mixpanel EU / Amplitude]).

**Transferts hors UE.**
- **Préférence par défaut :** outil hébergé en UE ou self-hosted
  (PostHog Cloud EU, Matomo, PostHog self-hosted) pour éviter la
  question des transferts.
- Si Mixpanel / Amplitude US : **SCC** + **DPF** + documentation du
  TIA (Transfer Impact Assessment). Mixpanel et Amplitude proposent
  une résidence EU en option payante — la privilégier pour une SaaS
  EU.

**Durée de conservation.**
- Événements bruts : **25 mois** maximum (alignement pratique CNIL
  Google Analytics), puis agrégation ou suppression.
- Rapports agrégés : sans limite de durée, car non directement
  identifiants.

**Mesures de sécurité.**
- Pseudonymisation systématique des identifiants utilisateurs (hash
  avec sel interne).
- Séparation logique des tables analytics des tables applicatives.
- Pas de cross-site tracking, pas de revente à des tiers, pas de
  fingerprinting avancé.
- Droit d'opposition (opt-out) exposé dans l'application et dans la
  politique de confidentialité.

---

### T-05 — Marketing et CRM

**Responsable de traitement :** [NOM DE LA SOCIÉTÉ]
**Responsable opérationnel :** [Head of Marketing / Head of Growth / ...]

**Finalité.** Communication commerciale sortante (newsletter, séquences
d'onboarding, annonces produit), qualification des prospects, suivi
des opportunités commerciales.

**Base légale.**
- **Intérêt légitime** (art. 6.1.f) pour la prospection B2B à des
  contacts professionnels (adresse email générique ou nominative
  rattachée à une fonction en lien avec l'offre), **avec opt-out
  visible et fonctionnel dans chaque communication** (art. L. 34-5
  CPCE).
- **Consentement** (art. 6.1.a) pour la prospection vers des personnes
  physiques à titre personnel (B2C) et pour l'inscription à une
  newsletter côté visiteur du site.
- **Exécution du contrat** (art. 6.1.b) pour les communications
  transactionnelles destinées aux clients existants (changements de
  service, factures, conditions).

**Catégories de personnes concernées.**
- Prospects B2B (contacts professionnels qualifiés).
- Inscrits à la newsletter.
- Clients actuels et anciens.

**Catégories de données.**
- Identité et fonction : nom, prénom, email professionnel, entreprise,
  poste, pays.
- Historique d'engagement : ouvertures et clics, pages visitées, temps
  passé, contenus téléchargés.
- Intérêts déclarés ou déduits : cas d'usage, taille d'entreprise,
  secteur, stade de maturité.
- Notes commerciales : échanges, suivi sales (saisies manuelles par
  l'équipe).

**Destinataires.**
- En interne : équipes marketing, sales, customer success.
- Sous-traitants : CRM (ex : [HubSpot / Pipedrive / Attio / Folk]),
  outil d'emailing (ex : [Brevo ex Sendinblue / Mailjet / Mailchimp /
  Postmark / Customer.io]), outil d'enrichissement (ex : [Clearbit /
  Apollo / Dropcontact]).

**Transferts hors UE.**
- HubSpot : US, SCC + DPF. Option résidence UE payante.
- Pipedrive : siège Estonie, traitement principalement UE, possible
  sous-traitance US à documenter.
- Brevo (ex Sendinblue) : société française, stockage UE — préférence
  par défaut pour une SaaS EU.
- Mailchimp : US, SCC + DPF.
- Mailjet : société française (Sinch), stockage UE.

**Durée de conservation.**
- Prospects non contractants : **3 ans** après dernier contact entrant
  (recommandation CNIL B2B), puis suppression.
- Clients en portefeuille : durée du contrat + 3 ans.
- Désinscrits : conservation de l'email sur liste d'exclusion (pour
  honorer l'opt-out) sans autre usage, durée indéfinie.

**Mesures de sécurité.**
- Double opt-in pour les newsletters grand public.
- Lien de désinscription fonctionnel et vérifié dans chaque email.
- Nettoyage périodique de la base (inactifs, bounces).
- Pas d'achat de bases de contacts non qualifiés (politique interne
  écrite, traçabilité des sources).
- Droit d'opposition documenté dans la politique de confidentialité.

---

### T-06 — Recrutement

**Responsable de traitement :** [NOM DE LA SOCIÉTÉ]
**Responsable opérationnel :** [Head of People / RH / Hiring Manager]

**Finalité.** Traiter les candidatures (spontanées et en réponse à
offres), organiser les entretiens, évaluer les candidats, prendre la
décision d'embauche, conserver les candidatures pour des postes futurs
avec consentement.

**Base légale.**
- **Mesures précontractuelles** (art. 6.1.b RGPD) : traitement des
  candidatures en vue de la conclusion éventuelle d'un contrat de
  travail.
- **Consentement** (art. 6.1.a) : pour la conservation d'un dossier
  candidat au-delà du processus en cours (cvthèque / talent pool).

**Catégories de personnes concernées.**
- Candidats à un poste ouvert ou spontanés.
- Éventuellement, références professionnelles transmises par le candidat.

**Catégories de données.**
- Identité et coordonnées : nom, prénom, email, téléphone, adresse
  éventuelle.
- Données de candidature : CV, lettre de motivation, portfolio, liens
  professionnels (LinkedIn, GitHub, Dribbble).
- Données d'évaluation : notes d'entretien, évaluations de tests
  techniques, retours de l'équipe, décision et motif.
- Références : coordonnées professionnelles et retour de référence, si
  fournies par le candidat.

**Pas de collecte.** Pas de données révélant l'origine raciale ou
ethnique, les opinions politiques, religieuses, philosophiques, la santé,
la vie sexuelle. Pas de question sur la situation familiale, la
grossesse, les projets personnels. Consigne écrite aux recruteurs.

**Destinataires.**
- En interne : équipe people, managers recruteurs identifiés dans le
  process.
- Sous-traitants : ATS / outil de recrutement (ex : [Welcome to the
  Jungle ATS / Lever / Greenhouse / Workable / Recruitee]), outil
  d'assessment (ex : [CodinGame / CoderPad / tests maison]), agence de
  recrutement externe (avec contrat encadrant).

**Transferts hors UE.**
- Welcome to the Jungle ATS, Recruitee : éditeurs européens, stockage
  UE.
- Lever, Greenhouse, Workable : US, SCC + DPF.
- CoderPad : US.

**Durée de conservation.**
- Candidats non retenus : suppression à la clôture du poste + 2 mois
  (délai de recours), sauf **consentement explicite** de conservation.
- Avec consentement : **2 ans** à compter du dernier contact, puis
  renouvellement du consentement ou suppression.
- Candidats retenus : données reprises dans le dossier RH (cf. T-07),
  le dossier candidat est purgé ou archivé selon la politique interne.

**Mesures de sécurité.**
- Accès restreint au strict périmètre recrutement (people + manager
  concerné).
- Journalisation des consultations des dossiers candidats sensibles.
- Séparation des données d'évaluation (internes) et des données de
  candidature (partageables avec le candidat sur demande d'accès).
- Information claire du candidat sur le traitement, durée,
  destinataires, droits (articles 13 et 15 RGPD).

---

### T-07 — Gestion RH (salariés)

**Responsable de traitement :** [NOM DE LA SOCIÉTÉ]
**Responsable opérationnel :** [Head of People / Office Manager]

**Finalité.** Gestion du contrat de travail, paie et éléments
variables, administration du personnel (congés, absences, temps de
travail), formation, évaluations, obligations déclaratives sociales
et fiscales.

**Base légale.**
- **Exécution du contrat de travail** (art. 6.1.b RGPD) pour la plupart
  des traitements courants.
- **Obligation légale** (art. 6.1.c) : paie, DSN, déclarations sociales
  et fiscales, affichages obligatoires, médecine du travail.
- **Intérêt légitime** (art. 6.1.f), cadré et documenté, pour certains
  traitements (ex : annuaire interne, évaluations de performance).

**Catégories de personnes concernées.**
- Salariés en CDI et CDD.
- Stagiaires, alternants, apprentis.
- Éventuellement : ayants droit mentionnés dans les dossiers (mutuelle,
  prévoyance).

**Catégories de données.**
- Identité et état civil : nom, prénom, date et lieu de naissance,
  nationalité, NIR (numéro de Sécurité sociale), adresse.
- Coordonnées bancaires : IBAN/BIC pour la paie.
- Données contractuelles : contrat de travail, avenants, fonction,
  classification, rémunération, date d'entrée.
- Données de paie : bulletins, éléments variables, primes, absences,
  congés, arrêts maladie (nature non renseignée sauf obligation).
- Données de formation : attestations, certificats, historique.
- Données d'évaluation : entretiens annuels, objectifs, plans de
  développement.

**Données sensibles éventuelles.**
- Santé : arrêts maladie, aménagements de poste, informations médicales
  minimales pour la médecine du travail — accès strictement limité.
- Handicap / RQTH : selon déclaration volontaire du salarié.
- Adhésion syndicale : uniquement via retenue sur salaire, traitement
  spécifique encadré.

**Destinataires.**
- En interne : people, paie, management direct (pour les données
  nécessaires uniquement).
- Sous-traitants : expert-comptable / cabinet de paie (ex : [Pennylane
  / Silae / Cegid / PayFit]), SIRH éventuel (ex : [PayFit / Lucca /
  Personio / Factorial]), outil d'évaluation (ex : [Leapsome / Lattice]).
- Tiers obligatoires : URSSAF, DGFIP, caisses de retraite, organismes
  de prévoyance et mutuelle, médecine du travail, inspection du travail
  (sur demande).

**Transferts hors UE.**
- En principe, **aucun** transfert hors UE pour la paie et les données
  sociales obligatoires.
- Outils SIRH : vérifier la localisation. PayFit, Lucca, Personio,
  Factorial : hébergement UE en principe.
- Outils d'évaluation US (Leapsome, Lattice) : SCC + DPF si utilisés.

**Durée de conservation.**
- Bulletins de paie : **5 ans** (durée minimum, art. L. 3243-4 Code du
  travail), **durée de vie du salarié + 50 ans** si conservation pour
  retraite (à justifier).
- Dossier du personnel : 5 ans après départ, certains éléments jusqu'à
  10 ans (preuve en cas de litige prud'homal).
- Déclarations sociales (DSN) : 5 ans.
- Évaluations : durée du contrat + 2 ans après départ.

**Mesures de sécurité.**
- Chiffrement des données sensibles au repos.
- Accès strictement limité people + paie + manager direct.
- Séparation stricte des données de santé : accessibles uniquement
  par la médecine du travail et un point de contact interne formé.
- Coffre-fort numérique pour les documents signés (contrats, avenants,
  fiches de paie).
- Contrat explicite avec l'expert-comptable / cabinet de paie
  couvrant les articles 28 et 32 RGPD.

---

### T-08 — Monitoring technique (logs, APM)

**Responsable de traitement :** [NOM DE LA SOCIÉTÉ]
**Responsable opérationnel :** [Head of Engineering / SRE / Security Lead]

**Finalité.** Sécurité du système d'information, détection et réponse
aux incidents, performance du service (APM — Application Performance
Monitoring), diagnostic des erreurs applicatives, traçabilité des
actions d'administration.

**Base légale.**
- **Intérêt légitime** (art. 6.1.f) : sécurité du service, continuité
  de fonctionnement, détection des abus.
- **Obligation légale** (art. 6.1.c) : tenue de certains journaux
  (cybersécurité, obligations sectorielles le cas échéant).

**Catégories de personnes concernées.**
- Utilisateurs du service (de manière indirecte, via les logs applicatifs).
- Équipes internes (traces d'actions d'administration).

**Catégories de données.**
- Logs applicatifs : horodatage, niveau, message, stack trace, contexte
  (endpoint, `user_id` pseudonymisé, `request_id`).
- Logs d'accès : IP source, user agent, URL demandée, code retour,
  latence.
- Logs de sécurité : tentatives d'authentification échouées, escalades
  de privilèges, accès à des endpoints sensibles.
- APM : traces distribuées, métriques techniques (CPU, mémoire, erreurs
  5xx).

**Non collectés.**
- Contenu applicatif sensible (ex : corps de requête avec données
  clients finales). À garantir par des **scrubbers** côté SDK
  (Sentry, Datadog) et par des règles internes de logging.
- Mots de passe, tokens, clés API : interdits en logs (revues de code
  systématiques).

**Destinataires.**
- En interne : équipes ingénierie et sécurité, avec accès gradué.
- Sous-traitants : Sentry, Datadog, Grafana Cloud, New Relic, Logtail,
  Elastic Cloud selon la stack. Hébergement à vérifier.

**Transferts hors UE.**
- Sentry : option **EU region** disponible — à activer par défaut.
- Datadog : option **EU region** (`app.datadoghq.eu`) — à activer.
- New Relic : EU option disponible.
- Si plan US par défaut : SCC + DPF + TIA documenté.

**Durée de conservation.**
- Logs applicatifs standards : **6 mois**.
- Logs d'accès et de sécurité : **12 mois** (alignement avec la
  recommandation CNIL de durée proportionnée pour la traçabilité
  sécurité).
- APM (traces et métriques) : **30 jours à 3 mois** selon le plan
  fournisseur.
- Archives de sécurité (détection d'incidents confirmés) : jusqu'à
  3 ans, à documenter au cas par cas.

**Mesures de sécurité.**
- Rotation et purge automatique selon les durées ci-dessus.
- Filtrage (scrubbing) des champs sensibles en amont (secrets, PII
  d'utilisateurs finaux).
- Accès restreint aux équipes ingénierie et sécurité.
- Journalisation des consultations de logs sensibles (qui a requêté
  quoi, quand).
- Pas de corrélation automatique des logs avec des données marketing.

---

## 4. Transmission au client B2B

Le client B2B qui vient de vous demander votre registre attend
typiquement **une version courte et lisible**, pas les 30 pages
internes. Préparez :

- **Une copie partielle** du présent registre, limitée aux traitements
  où vous êtes **sous-traitant de son périmètre** (cf. Annexe A — le
  client vous évaluera comme sous-traitant, pas comme responsable de
  traitement pour vos propres RH).
- L'annexe 1 du DPA (description du traitement) qui complète le
  registre sous-traitant.
- La liste des sous-traitants ultérieurs (annexe 3 du DPA).
- Les mesures techniques et organisationnelles (annexe 2 du DPA).

Ne transmettez pas les fiches T-06 (recrutement) et T-07 (RH) — elles
concernent vos propres opérations et n'ont pas à figurer dans l'échange
avec un client qui évalue votre rôle de sous-traitant.

---

## Annexe A — Modèle de registre sous-traitant (Article 30.2)

Quand vous fournissez votre service SaaS à un client B2B, vous êtes
**sous-traitant** au sens du RGPD et tenu d'un second registre. Une
entrée-type est proposée ci-dessous ; son contenu reprend en grande
partie l'**Annexe 1 du DPA** déjà livrée au client.

### Entrée ST-01 — Fourniture du service SaaS au client [NOM CLIENT]

**Responsable de traitement (client) :** [RAISON SOCIALE CLIENT],
représenté par [NOM], [fonction], joignable à [email].

**Sous-traitant :** [NOM DE LA SOCIÉTÉ] (nous).

**Représentant du sous-traitant :** [NOM, fonction, email].

**DPO du sous-traitant :** [si applicable].

**Catégories de traitements effectués pour le compte du responsable.**
- Collecte, stockage, mise à disposition et restitution des données
  saisies par les utilisateurs du client dans la plateforme.
- Opérations techniques : sauvegardes, haute disponibilité, maintenance.
- Opérations dérivées : métriques d'usage agrégées et anonymisées,
  journaux applicatifs à fins de support.

**Catégories de personnes concernées (définies par le client).**
- Utilisateurs finaux du client : [exemples à renseigner selon le
  service : salariés du client, clients finaux du client, etc.].

**Catégories de données (définies par le client).**
- Données d'identification des utilisateurs finaux.
- Contenu applicatif saisi par le client dans la plateforme.
- Métadonnées de log.
- [Adapter selon la nature du service.]

**Transferts hors UE.**
- Hébergement : [AWS `eu-central-1` / OVHcloud Gravelines / ...].
- Sous-traitants ultérieurs avec transfert : [Stripe US pour paiement,
  Intercom US pour support, Sentry EU pour monitoring, etc.] —
  encadrement par SCC + DPF selon liste annexe 3 du DPA.

**Mesures de sécurité.** Celles décrites à l'**Annexe 2 du DPA**
(renvoi explicite, sans duplication ici).

**Sous-traitants ultérieurs.** Liste à jour à l'**Annexe 3 du DPA**.

**Durée du traitement.** Durée du contrat principal conclu avec le
client + durée d'archivage prévue au DPA (article 10 Restitution et
suppression).

**Instructions documentées du client.** Contrat principal + DPA +
paramétrages effectués par le client dans la plateforme (configuration
des exports, politiques de conservation, rôles attribués).

### Ajout d'une entrée par client

Ajoutez une entrée `ST-0N` par client B2B signé. En pratique, la
plupart des champs sont identiques (c'est le même service), seuls
changent l'identité du client, les catégories de personnes
spécifiques à son contexte, et les durées convenues.

---

## Annexe B — Procédure de mise à jour

Le registre est mis à jour :

- À **chaque nouveau traitement** identifié (nouvelle fonctionnalité
  produit, nouvel outil interne, nouveau canal d'acquisition).
- À **chaque modification substantielle** : changement de base légale,
  changement de durée de conservation, changement de sous-traitant
  majeur, changement de localisation d'hébergement.
- À **chaque signature d'un nouveau client B2B** (ajout d'une entrée
  sous-traitant `ST-0N`).
- **Annuellement**, lors d'une revue dédiée par le référent protection
  des données (15-30 min par fiche).

Les versions successives du registre sont archivées et horodatées. La
version courante est partageable avec l'autorité de contrôle sur
demande (art. 30.4 RGPD) dans un délai court.

---

## Versioning

- **v0.1** — 2026-04-21. Première version. Huit traitements standards
  SaaS pré-remplis (comptes clients, facturation, support, analytics
  produit, marketing/CRM, recrutement, RH, monitoring technique).
  Annexe A — modèle d'entrée du registre sous-traitant, en lien avec
  l'annexe 1 du DPA. Annexe B — procédure de mise à jour.

## Prochaines étapes

- Traduction EN — planifiée en fin de semaine 1 avec les autres traductions.
- Export `.xlsx` — livré dans le packaging ZIP final (weekend session).
- Relecture par DPO certifié — mission à préparer une fois la
  proposition de partenariat DPO prête (Tier A, cf.
  `01-memory/dpo-candidates-20260417.md`).
