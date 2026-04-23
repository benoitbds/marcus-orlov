# Note — Transferts internationaux de données personnelles

> Annexe opérationnelle au DPA et au registre Article 30 du *GDPR Starter
> Kit — First B2B Customer*. Rédigée pour un acheteur B2B exigeant qui
> demande à son sous-traitant : *"Comment encadrez-vous les transferts
> hors UE ?"* — et qui attend mieux qu'un renvoi vague aux « SCC ».
>
> Version 0.1 — 2026-04-23. Document modèle. Ne constitue pas un conseil
> juridique personnalisé. Pour une situation complexe (données de santé,
> scoring, mineurs, profilage, cloud souverain imposé par un secteur
> régulé), consulter un avocat ou un DPO certifié.

---

## 1. Objet

Cette note explicite, pour un SaaS européen qui opère sous RGPD et fait
appel à des sous-traitants établis hors de l'EEE (ou à des sous-traitants
EEE dont la maison mère est extra-EEE et soumise à une loi d'accès —
`CLOUD Act`, `FISA §702`), le cadre de légalité des transferts et la
manière dont ces transferts sont documentés, évalués, et présentés à un
client B2B qui en fait la demande.

Elle couvre trois questions pratiques :

1. **Quel outil de transfert utiliser** selon le cas ?
2. **Quelles décisions d'adéquation** sont en vigueur et à quelles
   conditions ?
3. **Comment construire un TIA** (*Transfer Impact Assessment*) minimal
   défendable, sans prétendre au travail d'une DPIA approfondie ?

Elle ne remplace pas le DPA (qui porte les obligations contractuelles
bilatérales), ni le registre Article 30 (qui répertorie les traitements
et leurs transferts), ni la politique de confidentialité (qui informe
les personnes concernées). Elle les relie.

---

## 2. Cadre juridique, en une page

Les transferts vers un pays tiers sont régis par le **Chapitre V du
RGPD** (articles 44 à 50). La règle générale est interdiction, sauf
garantie. Six catégories de garanties sont admises, par ordre de
préférence d'emploi :

1. **Décision d'adéquation** (art. 45) — la Commission européenne a
   reconnu que le pays tiers assure un niveau de protection
   essentiellement équivalent. Transfert autorisé sans autre formalité.
2. **Clauses contractuelles types** (art. 46 §2.c), dites *SCC*,
   adoptées par la Commission — **décision d'exécution
   (UE) 2021/914** du 4 juin 2021.
3. **Règles d'entreprise contraignantes** (*BCR*, art. 47) — uniquement
   pour les groupes multinationaux qui ont fait valider leur BCR par
   une autorité chef de file.
4. **Code de conduite approuvé** ou **certification** (art. 46 §2.e-f).
   Peu répandu en pratique.
5. **Clauses ad hoc** approuvées par une autorité (art. 46 §3.a). Très
   peu répandu.
6. **Dérogations** (art. 49) — consentement explicite, exécution d'un
   contrat avec la personne concernée, intérêt vital, etc. Interprétation
   stricte, réservée à des cas ponctuels et non-structurels.

Pour un SaaS B2B qui sous-traite à des prestataires américains, **les
deux outils réalistes sont la décision d'adéquation (si applicable) et
les SCC 2021/914**. Les autres ne sont ni accessibles à une petite
structure, ni adaptés à un flux récurrent.

**Arrêt *Schrems II* (CJUE, 16 juillet 2020, C-311/18)** — point
structurant que le kit doit acter : l'usage des SCC n'est plus, depuis
2020, un label automatique. L'exportateur doit, pour chaque transfert,
évaluer si le droit et la pratique du pays destinataire n'annulent pas
les garanties contractuelles — et **documenter cette évaluation**. C'est
l'objet du TIA (§6).

> — *Note à l'éditeur.* Cette note cite volontairement les références
> exactes (article, règlement, décision, arrêt) parce qu'un client B2B
> rigoureux les vérifiera. Ne pas les retirer sans les remplacer par
> l'équivalent à jour.

---

## 3. Les quatre modules SCC (2021/914)

La décision 2021/914 ne publie pas quatre contrats, elle publie **un
seul contrat modulaire** dans lequel les parties sélectionnent le
module applicable à leur rôle respectif.

| Module | Exportateur | Importateur | Cas typique SaaS B2B |
|---|---|---|---|
| **Module 1** | Responsable de traitement | Responsable de traitement | Échange de fichier client entre deux entités juridiquement distinctes. *Rare pour un SaaS qui sous-traite*. |
| **Module 2** | Responsable de traitement | Sous-traitant | **Cas standard** : le SaaS sous-traite à AWS, GCP, OpenAI, Intercom. |
| **Module 3** | Sous-traitant | Sous-traitant ultérieur | Le SaaS (sous-traitant du client B2B) fait appel à son propre sous-traitant hors EEE. Le flux à travers le SaaS engage ce module. |
| **Module 4** | Sous-traitant | Responsable de traitement | Rare — renvoi de données d'un sous-traitant vers un responsable hors EEE. Pas couvert par défaut dans ce kit. |

**Conséquence pratique pour le SaaS vendu ici.** Le DPA client du SaaS
(annexe 4 du kit) active **Module 2** par défaut. Pour les flux SaaS →
sous-traitant hors EEE (AWS US, OpenAI, etc.), l'engagement utile est
**Module 3** : c'est le SaaS (sous-traitant direct du client B2B) qui
signe des SCC Module 3 avec son propre sous-traitant ultérieur hors
EEE. Ces SCC Module 3 ne sont pas reproduites dans ce kit car elles
sont signées *par* le fournisseur tiers (c'est AWS, Google, OpenAI,
etc. qui fournit le DPA et les SCC du côté importateur).

**Annexes obligatoires des SCC**, pour chaque module :

- **Annexe I.A** — parties et coordonnées.
- **Annexe I.B** — description du transfert (catégories de personnes,
  de données, finalités, durée, fréquence, transferts ultérieurs
  envisagés).
- **Annexe I.C** — autorité de contrôle compétente (celle de l'État
  membre d'établissement de l'exportateur, ou de son représentant
  désigné art. 27).
- **Annexe II** — mesures techniques et organisationnelles, suffisantes
  et spécifiques au transfert. *Non copiable des TOM du DPA de base* —
  les mesures anti-accès gouvernemental (chiffrement avec clés chez
  l'exportateur, pseudonymisation, split processing) doivent y
  apparaître si elles sont mobilisées.
- **Annexe III** — sous-traitants ultérieurs, si Module 2 ou 3.

---

## 4. Décisions d'adéquation en vigueur

État consolidé au 2026-04-23. Les décisions d'adéquation font l'objet
d'un **examen périodique** par la Commission ; le renvoi d'une date
n'exempte pas de vérifier l'état en vigueur au moment du transfert.

| Pays / cadre | Décision | Portée | Vigilance particulière |
|---|---|---|---|
| **Andorre, Argentine, Canada (commercial), Féroé, Guernesey, Île de Man, Israël, Japon, Jersey, Nouvelle-Zélande, Corée du Sud, Suisse, Uruguay, Royaume-Uni** | Décisions historiques (1999-2021), examens périodiques | Variable | Canada : couvre uniquement les entités soumises à la PIPEDA. Japon : complément de protection applicable aux données reçues d'UE. |
| **États-Unis (DPF)** | Décision d'exécution (UE) 2023/1795 du 10 juillet 2023 — *EU-US Data Privacy Framework* | Uniquement pour les entités US **self-certifiées** auprès du Département du Commerce et **listées** sur dataprivacyframework.gov, et pour les catégories de données couvertes par la certification | Vérifier la certification **avant chaque nouveau prestataire** (statut *Active*, catégories HR/non-HR couvrant le flux). Certification valable 1 an, renouvelable. Contentieux en cours ("Schrems III"). |
| **Royaume-Uni** | Décisions 2021/1772 (RGPD) et 2021/1773 (directive police) | Tous flux | Sunset clause — réexamen régulier. Vérifier l'état en vigueur. |

**Règle opérationnelle.** Pour un prestataire américain, le statut DPF
ne dispense **pas** de SCC : il remplace la base juridique. Si le
prestataire sort du DPF (ex. radiation, non-renouvellement), les SCC
déjà signées restent exécutoires et la continuité du transfert est
assurée. La pratique du kit est donc : **SCC signées systématiquement**,
DPF mentionné comme base principale **uniquement** si le prestataire
est activement certifié et que la certification couvre le flux en cause.

> — *Note à l'éditeur.* La liste des pays adéquats change. Vérifier sur
> commission.europa.eu/law/law-topic/data-protection/international-dimension-data-protection/adequacy-decisions_en
> au moment où le client B2B vous le demande, et dater votre réponse.

---

## 5. Cas concrets — sous-traitants fréquents d'une SaaS EU

Pour chaque cas : **qui est l'entité contractante**, **où résident les
données par défaut**, **quelle base de transfert**, **quelles mesures
particulières à documenter**. Ces fiches sont des points de départ
défendables ; elles ne remplacent pas la lecture du DPA du prestataire
concerné au moment de la contractualisation (les conditions évoluent).

### 5.1 AWS (Amazon Web Services)

- **Entité contractante pour un client EU** : Amazon Web Services EMEA
  SARL (Luxembourg), via le *AWS Customer Agreement* et le *AWS GDPR
  Data Processing Addendum*.
- **Résidence des données** : déterminée par le **choix des régions**
  par le client. Régions EU : Irlande (eu-west-1), Francfort
  (eu-central-1), Paris (eu-west-3), Londres (eu-west-2, hors UE),
  Stockholm (eu-north-1), Milan (eu-south-1), Zurich (eu-central-2),
  Espagne (eu-south-2). Pour un SaaS EU, la pratique minimale :
  **verrouiller la région au déploiement**, documenter le choix dans
  le registre.
- **Base de transfert** : pas de transfert vers pays tiers si régions
  EU exclusivement. Cependant, Amazon Web Services Inc. (maison mère
  US) peut être soumise à des demandes d'accès au titre du CLOUD Act
  (Clarifying Lawful Overseas Use of Data Act, 18 USC §2713) pour des
  données stockées par une filiale à l'étranger. AWS conteste en
  justice les demandes non conformes et publie un rapport semestriel.
- **Mesures à documenter (TIA)** : chiffrement au repos KMS (idéalement
  clés gérées par le client, *BYOK* via CloudHSM ou KMS external key
  store), chiffrement en transit TLS 1.2+, contrôle d'accès IAM au
  principe de moindre privilège, *AWS European Sovereign Cloud*
  (Brandebourg) si exigence de souveraineté forte, logs CloudTrail
  conservés 12 mois minimum.

### 5.2 Google Cloud Platform

- **Entité contractante pour un client EU** : Google Cloud EMEA Ltd
  (Irlande), via les *Google Cloud Terms of Service* et le *Data
  Processing Addendum*.
- **Résidence des données** : déterminée par le choix des régions.
  *Assured Workloads* permet de restreindre au périmètre EU
  (residency + operational controls). Offre *Sovereign Cloud* via
  partenaires (S3NS en France avec Thales, T-Systems en Allemagne).
- **Base de transfert** : SCC Module 2 par défaut (DPA Google).
  Maison mère Google LLC aux US, même exposition CLOUD Act que AWS.
- **Mesures à documenter** : CMEK (*Customer-Managed Encryption Keys*)
  ou EKM (*External Key Manager*), VPC Service Controls pour les
  traitements sensibles, logs d'audit exportés vers Cloud Logging avec
  rétention paramétrée.

### 5.3 OpenAI (API)

- **Entité contractante** : OpenAI, LLC (Delaware) ou OpenAI Ireland
  Ltd selon l'offre. Depuis mi-2024, les clients API EU peuvent
  contractualiser via OpenAI Ireland Ltd et bénéficier de résidence
  des données EU pour certains modèles.
- **Résidence des données** : par défaut, requêtes API traitées dans
  l'infrastructure OpenAI (principalement US). Option *Zero Data
  Retention* sur demande et éligibilité (API seulement, pas de
  fine-tuning, pas de assistant tools) — les prompts et complétions
  ne sont **pas stockés au-delà de l'exécution**. Résidence EU en
  option pour les clients éligibles.
- **Base de transfert** : DPA OpenAI + SCC Module 2. DPF si OpenAI
  LLC est certifiée au moment du transfert (à vérifier).
- **Mesures à documenter** : activation du *Zero Data Retention*,
  minimisation côté SaaS (ne transmettre à l'API que le strict
  nécessaire, pas d'identifiants, pas de données de santé sans
  consentement explicite et base légale vérifiée), *content filtering*
  appliqué avant envoi si le flux inclut des champs libres utilisateurs.

### 5.4 Stripe

- **Entité contractante pour un client EU** : Stripe Payments Europe
  Ltd (Dublin, Irlande), via les *Stripe Services Agreement* et le
  *Data Processing Agreement*.
- **Résidence des données** : traitements Stripe effectués
  principalement en Irlande et aux US. Stripe opère en tant que
  **responsable de traitement conjoint** (art. 26 RGPD) pour la
  prévention de la fraude et la conformité réglementaire (qualification
  à re-vérifier selon la ventilation de traitements dans le DPA).
- **Base de transfert** : SCC pour les flux Irlande → US (Stripe Inc.).
- **Mesures à documenter** : minimisation des données transmises à
  Stripe (ne pas envoyer de champs étrangers à la transaction), usage
  de Stripe Elements ou Checkout hébergé pour éviter le passage de
  numéros de carte sur l'infrastructure du SaaS (*SAQ A* niveau PCI-DSS),
  webhooks signés vérifiés côté SaaS.

### 5.5 Intercom

- **Entité contractante pour un client EU** : Intercom R&D Unlimited
  Company (Dublin, Irlande), via le *Master Subscription Agreement* et
  le *Data Processing Addendum*.
- **Résidence des données** : hébergement **au choix du client** entre
  les régions US, EU (Dublin, depuis mi-2022) et Australie, défini au
  moment de la création du compte et **non modifiable** sans migration
  assistée. Pour un SaaS EU, verrouiller la région EU au setup.
- **Base de transfert** : SCC Module 2 + DPF (Intercom Inc. US) si
  région US choisie ou pour les traitements de support opérés depuis
  les US.
- **Mesures à documenter** : choix de la région EU dès la création du
  compte, SSO pour les agents, politique de rétention courte sur les
  conversations (30-90 jours si nature support), gestion des pièces
  jointes (risque de fuite de données non prévues).

### 5.6 Sentry (monitoring d'erreurs)

- **Entité contractante pour un client EU** : Functional Software, Inc.
  (dba Sentry, San Francisco, US) ou **Sentry EU** (*sentry.io* /
  *de.sentry.io*), selon choix du plan. Offre EU-hosted lancée en 2022,
  infrastructure en Allemagne, opérée par la même entité US sous
  garanties contractuelles (SCC).
- **Résidence des données** : EU stricte si plan `sentry.io EU region`
  choisi. Par défaut US.
- **Base de transfert** : DPA Sentry + SCC Module 2. DPF si Sentry Inc.
  certifiée au moment du transfert.
- **Mesures à documenter** : **scrubbing serveur** activé sur les
  champs sensibles (PII, tokens, mots de passe) — Sentry fournit la
  config par défaut, vérifier qu'elle correspond au schéma de données
  du SaaS. Ne **jamais** envoyer de secrets dans les *tags* ou les
  *breadcrumbs*. Rétention courte (30-90 jours) sur les événements.

### 5.7 Sous-traitants non traités ici

Ce kit ne couvre pas par défaut : Cloudflare, Auth0, Twilio, SendGrid,
Zendesk, HubSpot, Salesforce, Segment, Mailchimp, Datadog, New Relic,
Notion, Slack, Linear, GitHub, GitLab, Figma, Airtable, Retool. Le
playbook (livrable ultérieur) fournira une procédure générique
d'évaluation en 6 étapes, applicable à tout nouveau sous-traitant.

> — *Note à l'éditeur.* Cette liste est à jour au 2026-04-23. Les
> entités contractantes changent (restructurations, séparation de
> filiales), les options régionales s'ouvrent et se ferment.
> **Dater explicitement** l'état de votre fiche quand vous répondez à
> un client B2B. Un document non daté perd sa force en six mois.

---

## 6. Modèle de TIA minimal

Un *Transfer Impact Assessment* est une **évaluation documentée** de
la légalité et de la robustesse d'un transfert spécifique. Il n'a pas
de format imposé par le RGPD ni par l'EDPB — ce dernier a publié, en
recommandations 01/2020, les six étapes attendues. Le modèle ci-dessous
est une version courte, défendable pour une SaaS B2B qui n'opère pas
de catégories sensibles.

Pour chaque transfert hors EEE recensé au registre (§ *transferts hors
UE* de chaque traitement), remplir les sept questions ci-dessous.
Longueur cible par fiche : **une à deux pages**. Ne pas sur-écrire.

**Fiche TIA — [nom du sous-traitant], traitement [T-XX du registre]**

1. **Flux et rôles**
   Exportateur : [SaaS]. Importateur : [entité contractante précise,
   pays]. Rôle RGPD de l'importateur : sous-traitant / sous-traitant
   ultérieur / responsable conjoint.
2. **Données transférées**
   Catégories de personnes (clients, salariés, prospects, etc.),
   catégories de données (nom, email, logs techniques, contenu de
   communication, etc.), volume estimé, fréquence.
3. **Outil de transfert**
   Adéquation / SCC Module X / BCR / dérogation. Date de signature de
   l'outil, références.
4. **Évaluation du droit et de la pratique du pays tiers**
   Existe-t-il une loi autorisant des autorités publiques à accéder
   aux données sans protection équivalente à celles de l'UE ? Exemples :
   US — FISA §702 (collectes auprès de *electronic communication service
   providers*), CLOUD Act (demandes à opérateurs US pour données
   détenues à l'étranger), EO 12333. Précédents de demandes publiques
   rapportés par le prestataire dans ses *transparency reports*.
5. **Mesures complémentaires**
   Chiffrement bout-en-bout ? Chiffrement au repos avec clés chez
   l'exportateur ? Pseudonymisation ? Minimisation ? *Split processing* ?
   Dans quelle mesure ces mesures rendent la donnée *inintelligible*
   pour l'autorité étrangère si elle y accédait ?
6. **Garanties organisationnelles du prestataire**
   Publication d'un rapport de transparence, politique de résistance
   aux demandes non conformes, notification au client en cas de
   demande (dans la mesure permise par la loi), *warrant canary*,
   certifications (ISO 27001, SOC 2, C5 allemand, HDS si santé).
7. **Conclusion**
   Le niveau de protection est-il essentiellement équivalent à celui
   du RGPD ? Si oui, justifier en une phrase. Sinon, quelles mesures
   supplémentaires sont prises, ou quel est le plan de sortie ?

**Date de la fiche** : [YYYY-MM-DD]. **Prochain réexamen** : 12 mois
ou à tout changement substantiel.

---

## 7. Ce que ce kit ne prétend pas couvrir

- **Les catégories particulières** de l'article 9 (santé, biométrie,
  opinions, orientation sexuelle) et les données pénales (art. 10) :
  régime renforcé, consultation d'un DPO certifié ou d'un avocat
  spécialisé requise avant tout transfert.
- **Les flux vers la Chine, la Russie, les pays à risque élevé** :
  aucun outil de transfert standard ne suffit seul. Évaluation au cas
  par cas, mesures techniques lourdes obligatoires.
- **Les transferts dans un cadre de coopération judiciaire ou fiscale**
  (art. 48 RGPD) : cadre distinct, instruments dédiés.
- **Les traitements relevant de la loi informatique et libertés
  française pour les secteurs régulés** (données de santé, scoring
  crédit, défense) : consulter la CNIL ou l'autorité sectorielle.

Pour l'un de ces cas, ce kit renvoie à un DPO certifié ou à un avocat
spécialisé. Voir le DISCLAIMER du kit.

---

## 8. Références

- Règlement (UE) 2016/679 — RGPD, Chapitre V (articles 44 à 50).
- Décision d'exécution (UE) 2021/914 du 4 juin 2021 — clauses
  contractuelles types pour les transferts de données à caractère
  personnel vers des pays tiers.
- Décision d'exécution (UE) 2023/1795 du 10 juillet 2023 — *EU-US Data
  Privacy Framework*.
- CJUE, arrêt *Schrems II*, 16 juillet 2020, affaire C-311/18.
- EDPB, recommandations 01/2020 sur les mesures complémentaires aux
  outils de transfert, version 2.0 du 18 juin 2021.
- EDPB, lignes directrices 05/2021 sur l'interaction entre l'article
  3 et le Chapitre V du RGPD, adoptées le 14 février 2023.
- CNIL — dossier thématique *Transferts de données hors UE*.

---

## Versioning

- **v0.1** — 2026-04-23. Première version. Cadre Chapitre V, quatre
  modules SCC, décisions d'adéquation, six sous-traitants typiques
  (AWS, GCP, OpenAI, Stripe, Intercom, Sentry), modèle TIA en sept
  points, périmètres exclus, références.
