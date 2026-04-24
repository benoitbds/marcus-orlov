# Playbook — GDPR Starter Kit (First B2B Customer)

> Document opérationnel du *GDPR Starter Kit — First B2B Customer*.
> Lit en quarante minutes avant un appel de négociation. Complète le DPA,
> le registre Article 30, la politique de confidentialité et la note
> transferts internationaux livrés dans le même kit.
>
> Version 0.1 — 2026-04-24. Document modèle. Ne constitue pas un conseil
> juridique personnalisé. Pour une situation complexe (catégories
> sensibles art. 9, données pénales art. 10, mineurs, scoring, profilage
> automatisé, flux Chine/Russie, secteurs régulés), consulter un avocat
> ou un DPO certifié avant signature.

---

## Avant-propos — à qui s'adresse ce document

Vous êtes fondateur ou opérations d'une SaaS européenne de moins de 50
personnes. Vous venez de closer — ou vous êtes sur le point de closer —
votre premier client B2B qui pèse. Le contrat principal est presque
prêt. Le client vous a envoyé, ou s'apprête à vous envoyer, un *DPA*
(contrat de traitement) à signer, parfois un *security questionnaire* de
40 pages, parfois une demande de registre Article 30, parfois une
politique de confidentialité à mettre à jour avant la signature.

Le kit que vous avez acheté vous donne quatre documents signables. Le
playbook vous dit quoi faire avec, dans quel ordre, et surtout **ce que
vous devez défendre en négociation et ce que vous pouvez concéder sans
casser votre modèle**.

Il ne vous apprend pas le RGPD. Il suppose que vous en avez la notion
générale. Il vous donne les arbitrages d'un praticien qui a vu passer
ces discussions et sait quelles clauses coûtent cher si elles passent
telles quelles.

---

## 1. Adapter le kit en 45 minutes — checklist pas à pas

Prévoyez une plage non interrompue. Le travail est réaliste en 45
minutes pour une SaaS B2B standard. Si vous dépassez l'heure, c'est que
votre situation sort du scope du kit (cf. §3 *signaux d'alerte*).

### 1.1 Préparer les informations de l'entreprise (5 min)

Rassemblez, dans un fichier à côté :

- Raison sociale exacte, forme juridique, capital social, RCS (ville +
  numéro), adresse du siège.
- Nom et qualité du signataire.
- Identité et contact du DPO **si et seulement si** un DPO a été
  formellement désigné (art. 37 RGPD). Si aucun DPO désigné, laissez
  le placeholder vide et supprimez la ligne dans la version finale.
- Liste des pays de l'EEE + pays tiers où les données sont stockées ou
  traitées (régions cloud, CDN, sous-traitants offshore).
- Liste courte des sous-traitants ultérieurs effectivement utilisés
  pour le service vendu, pas tous ceux de votre compte AWS.

> — *Note à l'éditeur.* La partie qui fait perdre du temps en relecture
> est presque toujours l'étape 1.1 : les bonnes informations ne sont
> jamais toutes au même endroit. Gardez ce fichier d'entreprise quelque
> part et réutilisez-le pour le prochain client, vous gagnerez trente
> minutes à chaque fois.

### 1.2 DPA — remplir, puis arbitrer (15 min)

1. Ouvrir `dpa/dpa-fr.md` (ou `dpa-en.md` selon la langue du client).
2. Remplir tous les crochets `[...]` de l'entête contractuelle.
3. Vérifier **l'Annexe 1** (description du traitement) : ce que fait
   votre service, catégories de données traitées, catégories de
   personnes, durée. Soyez concret, pas générique.
4. Vérifier **l'Annexe 2** (mesures de sécurité) : chaque mesure listée
   doit être **vraie**. Si vous n'avez pas de *bug bounty*, retirez la
   ligne. Un DPA qui promet des mesures non tenues est pire qu'un DPA
   qui en promet moins.
5. Vérifier **l'Annexe 3** (liste des sous-traitants ultérieurs) :
   nom, finalité, pays d'hébergement, base de transfert. Ce tableau
   sera relu mot à mot par un acheteur rigoureux.
6. Vérifier **l'Annexe 4** (SCC Module 2) : n'ajouter que si un
   transfert vers un pays tiers sans adéquation est engagé. Sinon
   laisser indiqué « sans objet ».

### 1.3 Registre Article 30 — adapter les 8 traitements (10 min)

1. Ouvrir `register/register-fr.md`.
2. Parcourir les huit traitements pré-remplis (T-01 à T-08). Pour
   chacun : ce traitement existe-t-il dans votre opération ? Sinon,
   supprimer la fiche.
3. Ajouter les traitements propres à votre métier que le kit n'a pas
   pré-remplis (ex : traitement des appels d'offre, webinars,
   partenariats, intégrations tierces authentifiées).
4. **Vérifier les durées de conservation** : les valeurs par défaut
   du kit sont alignées au Code (10 ans comptable, 5 ans paie, 25 mois
   analytics, 3 ans prospection B2B, 6 mois logs standards, 12 mois
   logs sécurité). Ne les tirez pas vers le bas par confort.
5. Ne **pas transmettre** au client B2B les fiches T-06 (recrutement)
   et T-07 (RH) — scope séparation §4 du registre. Un client B2B
   évalue son sous-traitant, pas votre politique RH interne.

> — *Note à l'éditeur.* Si vous hésitez sur une base légale, ne tranchez
> pas au feeling. La règle prudente : *intérêt légitime + opt-out* pour
> les traitements B2B non sensibles, *exécution contractuelle* pour
> tout ce qui est strictement nécessaire à la fourniture du service,
> *consentement* pour cookies non exemptés et newsletter public.
> *Obligation légale* pour ce qui est imposé par la loi (comptable,
> social). Ne pas mélanger.

### 1.4 Politique de confidentialité — publier la bonne version (10 min)

1. Ouvrir `privacy-policy/privacy-fr.md`.
2. Retirer tous les blocs `> — *Note à l'éditeur.*` avant publication.
3. Vérifier que la table des bases légales et la table des durées
   correspondent **mot à mot** à celles du registre. Un écart ici est
   une faille détectable en vingt secondes par un auditeur.
4. Remplir la liste des sous-traitants ultérieurs publiée. Elle doit
   être cohérente avec l'Annexe 3 du DPA. Si vous listez un sous-
   traitant dans le DPA, listez-le ici.
5. Publier sur l'URL canonique (`/privacy`, `/confidentialite`, peu
   importe — tenez-la stable). Ne pas publier sur une page qui change
   d'URL au prochain refactor du site.

### 1.5 Note transferts — annexer si demandée (5 min)

La note `transfers-note/transfers-note.md` n'est pas systématiquement
annexée au DPA. Elle sert quand :

- Le client B2B pose une question explicite sur les transferts
  (*"Comment gérez-vous les transferts hors UE ?"*, *"Êtes-vous
  conforme à Schrems II ?"*).
- Le client B2B a reçu un *security questionnaire* d'un tiers qui
  couvre les transferts.
- Votre service engage un sous-traitant américain critique (AWS,
  Google Cloud, OpenAI) et le client le sait.

Sinon, la note reste à votre disposition, vous l'envoyez quand la
question arrive. L'envoi proactif est rarement une bonne idée : il
invite des questions qui n'étaient pas posées.

---

## 2. Les clauses les plus poussées par les clients B2B

Liste ordonnée par fréquence constatée dans les discussions SaaS
européennes. Pour chacune : la demande type, la valeur par défaut du
kit, ce qu'il est raisonnable de défendre, ce qu'il est acceptable de
concéder.

### 2.1 Délai de notification des violations (art. 33 RGPD)

**Demande type.** *"Vous nous notifiez toute violation de données dans
les 24 heures."*

**Valeur du kit.** 48 heures dans le DPA (clause §8.1).

**Ce que vous défendez.** Le délai de 48h n'est pas une paresse : il
est calibré sur votre obligation légale de 72h (art. 33 RGPD) vers
l'autorité, en laissant un buffer opérationnel pour qualifier la
violation. Un délai de 24h impose, en pratique, une notification sur
information incomplète, qui oblige à des rectifications publiques.

**Argumentaire verbal.** *"Nous préférons vous transmettre une
notification qualifiée dans les 48h plutôt qu'une alerte brute dans
les 24h que nous devrons corriger. Notre procédure interne de
qualification prend entre 12 et 24 heures, nous gardons une marge pour
l'escalade vers votre équipe."*

**Concession acceptable.** 36 heures, avec l'obligation explicite que
la notification initiale puisse être complétée par une notification
qualifiée dans les 72 heures suivantes. Ne descendez pas en dessous
de 36h sauf si le client pèse très lourd et que vous avez un runbook
d'incident déjà rodé.

**Refus net.** 12h, temps réel, *"as soon as known"* non qualifié.
Ces demandes sont inapplicables et vous mettent en défaut à la
première alerte technique.

### 2.2 Audit sur site vs audit documentaire

**Demande type.** *"Nous nous réservons le droit d'auditer vos locaux
et infrastructures sur site, à tout moment, aux frais du sous-traitant."*

**Valeur du kit.** Audit documentaire d'abord, audit sur site
exceptionnel, fréquence maximale annuelle, frais à la charge du
demandeur (DPA §9).

**Ce que vous défendez.** Un audit sur site d'un sous-traitant SaaS par
chacun de ses clients B2B est opérationnellement impraticable : dix
clients, dix audits, une équipe qui ne fait plus que répondre à des
auditeurs. La pratique EU consolidée est : documentation d'abord
(*SOC 2 report*, ISO 27001, rapports de pen-test, DPA, politique de
sécurité), audit sur site réservé à une cause documentée (incident,
manquement grave).

**Argumentaire verbal.** *"Nous fournissons annuellement un paquet de
preuves à tous nos clients : [certifications]. Si vous identifiez une
zone non couverte par cette documentation, nous ouvrons une session
d'audit sur site dédiée, une fois par an, à votre charge. Cette
politique est identique pour tous nos clients, nous ne pouvons pas
l'individualiser."*

**Concession acceptable.** Audit documentaire semestriel, plus audit
sur site annuel **sur cause documentée**. Frais à la charge du
demandeur si l'audit ne révèle pas de manquement.

**Refus net.** Audit sur site illimité, sur demande, aux frais du
sous-traitant. Clause qui, appliquée littéralement, arrête votre
équipe.

### 2.3 Clause d'indemnisation illimitée

**Demande type.** *"Le sous-traitant indemnisera le responsable de
traitement de tout dommage, direct ou indirect, sans plafond."*

**Valeur du kit.** Responsabilité limitée au montant des redevances
dues sur les douze derniers mois (DPA §11). Exclusion des dommages
indirects.

**Ce que vous défendez.** Une SaaS ne peut pas assurer un risque
illimité sur un contrat à 10 000 € annuels. Le rapport sinistre /
prime est structurellement impossible. La clause illimitée signifie
soit que le client ne la fait jamais jouer, soit que vous perdez tout
au premier incident — aucune des deux n'est une relation commerciale.

**Argumentaire verbal.** *"Notre limite de responsabilité est alignée
sur la pratique du marché SaaS européen : montant des redevances
annuelles, ou [multiple], hors dommages directs liés à un manquement
caractérisé à nos obligations de sécurité. Au-delà, nous acceptons une
franchise d'assurance à [montant]. Une indemnisation non plafonnée
n'est pas assurable et rendrait le contrat structurellement
inexécutable."*

**Concession acceptable.** Plafond relevé à deux ou trois fois les
redevances annuelles, hors **cas d'exclusion limités et documentés**
(violation intentionnelle, faute lourde, manquement caractérisé aux
obligations de sécurité essentielles). Assurance RC pro communiquée
au client.

**Refus net.** Indemnisation illimitée, intégrale, sans cas
d'exclusion. Indemnisation avec inversion de la charge de la preuve
(*"sauf preuve contraire du sous-traitant"*).

### 2.4 Suppression immédiate vs restitution des données

**Demande type.** *"À la fin du contrat, vous supprimez toutes les
données sous 48 heures, sans possibilité de restauration."*

**Valeur du kit.** À la résiliation, le client choisit entre
restitution (format exploitable, délai 30 jours) ou suppression
(confirmée par écrit, délai 30 jours + période de rétention technique
résiduelle jusqu'à 90 jours pour backups) (DPA §10).

**Ce que vous défendez.** La suppression immédiate est techniquement
impossible pour une architecture qui a des *backups* chiffrés. La
suppression logique est immédiate ; la suppression physique prend le
temps du cycle de rotation des backups. Le kit assume cette réalité
plutôt que de la cacher. Le client préfère une promesse tenue à 30+90
jours qu'une promesse fausse à 48h.

**Argumentaire verbal.** *"Nos backups suivent une rotation chiffrée
sur [X] jours. Nous garantissons une suppression logique immédiate,
une suppression physique des bases actives sous 30 jours, et une
suppression des backups dans la rotation suivante, au plus tard sous
90 jours. Cette politique est documentée et testée. Une promesse de
48h ne serait pas honorable."*

**Concession acceptable.** Suppression logique immédiate documentée +
suppression physique sous 30 jours + suppression des backups sous
60 jours (rotation accélérée si volumétrie le permet).

**Refus net.** Suppression immédiate et certifiée sous 24-48h **sans
distinguer logique et physique**. Clause pénale associée à un délai
techniquement infaisable.

### 2.5 Engagement à ne pas utiliser de sous-traitants hors UE

**Demande type.** *"Vous garantissez que toutes les données seront
traitées exclusivement dans l'Union européenne, sans aucun
sous-traitant ultérieur hors UE."*

**Valeur du kit.** Traitement principal en UE, sous-traitants
ultérieurs hors UE déclarés dans l'Annexe 3 avec base de transfert
(SCC ou adéquation), droit d'opposition du responsable de traitement
(DPA §5).

**Ce que vous défendez.** Un tel engagement absolu n'est presque jamais
tenable sans impact produit majeur : OpenAI n'a pas de résidence EU
pour tous ses modèles, Stripe route des paiements via des *acquirers*
internationaux, Sentry historiquement US, des CDN routent hors EU
selon l'édge serveur. Un engagement *"100 % EU"* souscrit en
négociation puis violé par une dépendance courante est pire qu'une
transparence complète sur la topologie.

**Argumentaire verbal.** *"Nous pouvons nous engager sur la résidence
UE des données primaires (base de données client, fichiers, logs
applicatifs). Pour les services tiers qui n'ont pas de résidence EU
native — paiement, IA, monitoring —, nous documentons les transferts
dans l'Annexe 3 et joignons la note Transferts internationaux du kit.
Nous n'offrons pas de garantie *"100 % EU"* : elle serait fausse
techniquement."*

**Concession acceptable.** Résidence EU garantie pour le **traitement
principal** (base de données, fichiers clients, logs applicatifs).
Liste exhaustive et datée des sous-traitants hors UE, avec base de
transfert et TIA (cf. note transferts §6). Procédure d'opposition du
client avant introduction d'un nouveau sous-traitant.

**Refus net.** Garantie absolue *"aucune donnée ne quitte l'UE"* si
votre *stack* inclut des services US critiques. Ne signez pas ce que
vous ne pouvez pas tenir.

### 2.6 Chiffrement *at rest* obligatoire partout

**Demande type.** *"Toutes les données sont chiffrées au repos, en
toutes circonstances, y compris dans les backups et fichiers
temporaires."*

**Valeur du kit.** Chiffrement des bases, fichiers clients, backups,
au minimum AES-256. Fichiers temporaires couverts par chiffrement du
disque système (LUKS, *at-rest encryption* du fournisseur cloud)
(Annexe 2 du DPA).

**Ce que vous défendez.** Le chiffrement *at rest* est standard et
acceptable. Le piège est la clause qui exige la **gestion des clés
côté client** ou un chiffrement *bring-your-own-key* (BYOK) sans
préavis. BYOK coûte du temps d'ingénierie, nécessite un KMS et une
interface, et n'est pas toujours supporté par les services
sous-jacents.

**Argumentaire verbal.** *"Nous chiffrons les données au repos avec
AES-256 via [provider]. Les clés sont gérées par [provider / nous]
selon la politique documentée en Annexe 2. Une solution BYOK nécessite
un effort produit dédié que nous pouvons discuter sur un palier
tarifaire distinct."*

**Concession acceptable.** Chiffrement documenté, politique de
rotation des clés, engagement de notification en cas de changement
substantiel de provider KMS. BYOK sur palier tarifaire Enterprise.

**Refus net.** BYOK inclus sur un palier standard sans tarification
dédiée. Exigence de chiffrement homomorphe ou de calcul sur données
chiffrées (hors scope d'une SaaS générique).

### 2.7 Pen-test annuel communiqué, et en toute transparence

**Demande type.** *"Vous effectuez un pen-test annuel par un tiers
indépendant et vous nous communiquez le rapport complet."*

**Valeur du kit.** Pen-test annuel mentionné dans les mesures
organisationnelles (Annexe 2, mesure O-05). Communication du rapport
pas automatique.

**Ce que vous défendez.** Un rapport de pen-test complet contient
souvent des vulnérabilités encore non corrigées, des adresses IP de
rebond, des détails techniques qui, s'ils fuitent, constituent un
chemin d'attaque. La pratique EU est de communiquer un *executive
summary* plus un *statement of findings* (résumé non-technique +
état de correction), pas le rapport brut.

**Argumentaire verbal.** *"Nous communiquons annuellement un résumé
exécutif de pen-test (findings principaux, sévérité, état de
correction) sous accord de confidentialité. Le rapport technique
complet est disponible pour consultation sur site dans nos locaux
ou via une *data room* sécurisée. Sa communication complète par email
serait une faille en elle-même."*

**Concession acceptable.** Résumé exécutif annuel + *data room*
sécurisée sur demande pour revue technique par l'équipe sécurité du
client, sous NDA. Rapport complet uniquement via *data room*.

**Refus net.** Communication du rapport de pen-test complet, par email,
sans NDA et sans *data room* sécurisée.

### 2.8 Assurance RC pro à montant imposé

**Demande type.** *"Vous justifiez d'une assurance responsabilité
civile professionnelle d'un montant minimum de [X] millions d'euros."*

**Valeur du kit.** Mention dans les mesures organisationnelles
(Annexe 2) sans montant imposé.

**Ce que vous défendez.** Une SaaS en amorçage ne souscrit pas la même
RC pro qu'un éditeur établi. La demande doit être proportionnée au
volume contractuel. 10 M€ de RC pro pour un contrat à 12 000 € annuels
est disproportionné.

**Argumentaire verbal.** *"Nous disposons d'une RC pro à [montant
réel] auprès de [assureur]. Nous pouvons partager l'attestation. Pour
une couverture supérieure, nous l'ajusterons sur le palier Enterprise."*

**Concession acceptable.** Attestation RC pro fournie. Plafond de
couverture aligné au montant annuel contractuel multiplié par un
facteur 10-20 selon la sensibilité des données traitées. Ajustement
possible à la hausse sur palier Enterprise.

**Refus net.** Montant minimum de 10 M€+ imposé, non négociable,
pour un contrat de taille standard.

---

## 3. Signaux d'alerte — consultez un professionnel

Les situations suivantes sortent du périmètre que ce kit prétend
couvrir. Leur seule présence dans la discussion client doit déclencher
une consultation DPO certifié ou avocat spécialisé **avant signature**.
Ne forcez pas le kit à couvrir un cas qu'il n'a pas été conçu pour
couvrir.

### 3.1 Catégories particulières et données sensibles

- **Article 9 RGPD** : origine raciale ou ethnique, opinions politiques,
  convictions religieuses, appartenance syndicale, données génétiques,
  biométriques, de santé, relatives à la vie ou orientation sexuelle.
- **Article 10 RGPD** : données relatives aux condamnations pénales.

Si le service traite ou risque de traiter ces catégories, le régime
change : DPIA obligatoire, conditions de licéité restreintes (art. 9§2
et art. 10), dans certains cas DPO obligatoire (art. 37§1.c).

### 3.2 Mineurs

Dès qu'un service touche des personnes de moins de 16 ans (ou 15 ans
en France selon la LIL) :

- Consentement parental, vérification de l'âge, politique de
  confidentialité adaptée.
- Publicité ciblée et profilage interdits ou très encadrés.
- Design adapté, mesures renforcées.

Le kit ne couvre pas ces exigences.

### 3.3 Profilage et décisions automatisées

L'article 22 RGPD encadre les décisions fondées **exclusivement** sur
un traitement automatisé produisant des effets juridiques ou affectant
significativement la personne concernée (scoring crédit, tri de CV,
fixation de prix individualisée).

Ces cas imposent :

- Information renforcée dans la politique de confidentialité.
- Droit d'obtenir une intervention humaine, d'exprimer un point de
  vue, de contester la décision.
- DPIA quasi systématique.

Si votre service inclut un algorithme de décision, consultez.

### 3.4 Flux vers la Chine, la Russie, pays à risque élevé

La note transferts §7 le dit explicitement : aucun outil de transfert
standard (SCC + TIA) ne suffit seul. Évaluation cas par cas, mesures
techniques lourdes (chiffrement bout-en-bout avec clés sous contrôle
exportateur, pseudonymisation forte), parfois non-transfert simplement.

### 3.5 Secteurs régulés

- **Santé** : hébergement HDS obligatoire en France (art. L. 1111-8
  CSP), régime ANSM, certifications spécifiques.
- **Banque, finance, paiement** : encadrements ACPR, DSP2, AML/KYC,
  exigences EBA.
- **Défense, souveraineté** : cloud souverain imposé (SecNumCloud),
  habilitations.
- **Éducation** : cadre MENESR, recommandations CNIL éducation.
- **Assurance** : encadrement ACPR, Solvabilité II.

Chaque secteur a ses propres règles qui s'ajoutent au RGPD, parfois le
restreignent. Le kit cible une SaaS B2B généraliste.

### 3.6 Publicité, adtech, DMP

Le tracking publicitaire multi-sites, les *data management platforms*,
les *identity resolution* basés sur des identifiants persistants
cross-sites engagent :

- ePrivacy stricte, consentement systématique.
- Règles sectorielles IAB / TCF.
- Risque contentieux élevé (plaintes noyb, décisions CNIL).

Le kit couvre l'analytics de premier niveau avec exemption CNIL. Pas
l'adtech.

### 3.7 Transferts massifs ou transferts B2C grand public

Si le service traite plus de **1 M de personnes concernées** ou opère
en grand public (app grand public, marketplace, réseau social) :

- DPIA probable.
- DPO probable.
- Communication publique plus exposée (fuites = presse).
- Enquêtes d'office de la CNIL plus probables.

Le kit est calibré pour une SaaS B2B de portefeuille ≤ 200 clients
actifs et volume cohérent. Hors de ce cadre, faites monter un
spécialiste.

### 3.8 Demandes de modification du contrat principal venant d'un avocat

Quand la négociation ne passe plus par le responsable achat ou
juridique interne mais par un **cabinet d'avocats externe mandaté**,
la dynamique change : le temps d'échange se rallonge, les demandes se
raffinent, et les positions du kit ne suffisent plus pour tenir la
discussion. Ce n'est pas un échec, c'est un changement de catégorie
de client — prévoyez un avocat en miroir sur votre rédaction finale.

---

## 4. Ce qui ne relève pas du DPA mais du contrat principal

Un DPA encadre la **protection des données personnelles** traitées
par le sous-traitant pour le compte du responsable. Il ne régit pas
la relation commerciale complète. Confondre les deux entraîne deux
pathologies opposées : soit on surcharge le DPA de clauses non-RGPD
(qui devraient être dans le contrat principal), soit on laisse des
clauses RGPD dans le contrat principal qui s'y perdent.

Les sujets suivants **ne sont pas** dans le DPA du kit. Ils relèvent
du contrat principal — *Master Services Agreement*, contrat-cadre, ou
contrat de prestation.

### 4.1 SLA et disponibilité

Engagements de disponibilité (ex : 99,9 % uptime mensuel), temps de
rétablissement, pénalités de service. Hors DPA. Le DPA couvre la
sécurité des traitements en tant que tels, pas la garantie de
service.

### 4.2 Prix, paliers, modalités de paiement

Tarification, facturation, modalités de règlement, indexations,
révisions de prix. Hors DPA.

### 4.3 Durée, résiliation, reconduction du contrat

Durée du contrat, tacite reconduction, conditions de résiliation pour
convenance, résiliation pour faute. Le DPA §11 donne la durée du DPA
*alignée* sur le contrat principal ; il ne **crée pas** la durée.

### 4.4 Propriété intellectuelle

Licences sur la plateforme, propriété des *outputs* générés, licences
de *feedback*, clauses d'open source, marques. Hors DPA.

### 4.5 Confidentialité générale (NDA)

Confidentialité sur les informations commerciales et techniques
échangées. Le DPA §3 traite la confidentialité **des données
personnelles** ; il ne remplace pas un NDA général sur le business
model, la roadmap, les secrets de fabrication.

### 4.6 Responsabilité hors données personnelles

Clauses de limitation de responsabilité pour défaillance de service,
non-conformité fonctionnelle, retards. Le DPA §11 ne couvre que la
responsabilité **liée au traitement des données**.

### 4.7 Force majeure, cession, droit applicable du contrat

Ces clauses sont dans le contrat principal. Le DPA reprend par défaut
le droit applicable du contrat principal — il ne l'impose pas lui-même.

### 4.8 Assurance et garanties commerciales

Assurance RC pro, garanties de résultat, garanties *time-to-market*.
Hors DPA.

> — *Note à l'éditeur.* Un client B2B qui insère des clauses §4 dans
> le DPA n'est pas malveillant : il cherche à tout rassembler en un
> seul document. Vous avez deux options. Soit vous renvoyez la clause
> au contrat principal (propre, facile à relire ensuite). Soit vous
> l'acceptez dans le DPA en marquant *"par dérogation au contrat
> principal, cette clause régit uniquement le traitement des données
> au sens du RGPD"*. La première option est plus saine à terme.

---

## 5. Procédure d'évaluation d'un nouveau sous-traitant — 6 étapes

> *Dette honorée du kit : la note transferts §5.7 promet cette
> procédure générique. La voici. Elle s'applique à tout nouveau
> sous-traitant ultérieur — qu'il soit UE ou hors UE, qu'il traite
> des données personnelles directement ou comme effet de bord.*

Cadre : vous envisagez d'ajouter un nouveau sous-traitant ultérieur
(nouvel outil de monitoring, nouveau provider email, nouveau service
d'IA, nouvel hébergeur de CDN, etc.). Avant de connecter le service
et de router de la donnée, passez la grille suivante. Comptez 30 à 60
minutes la première fois, 15 minutes une fois la grille familière.

### Étape 1 — Identifier ce qui est vraiment transféré

Posez ces questions par écrit, réponses conservées :

- **Quelles catégories de données personnelles** vont transiter par
  ce prestataire ? Nom, email, adresse IP, contenu de messages, logs
  d'usage, données sensibles ?
- **Quelles catégories de personnes** concernées ? Clients B2B,
  utilisateurs finaux, salariés, prospects ?
- **Quel volume** estimé ? Quelle fréquence ?
- **Le prestataire est-il strictement nécessaire** ? Existe-t-il une
  alternative EU ou self-hosted à coût acceptable ?

Si la réponse à la dernière question est *"une alternative existe mais
on préfère celui-ci pour la qualité du produit"*, documentez-le.
C'est un arbitrage légitime mais il doit être conscient.

### Étape 2 — Localiser le prestataire et ses flux

- **Entité contractante** : quelle entité signe le contrat ? Siège
  social, juridiction.
- **Résidence des données** : où les données sont-elles **stockées**
  par défaut ? Le prestataire offre-t-il une option EU-only ?
  Documentée comment ?
- **Résidence des traitements** : où les données sont-elles
  **traitées** ? Support client 24/7 accédant depuis l'Inde ou les
  Philippines ? Équipes d'ingénierie basées hors UE avec accès
  admin ? *Call centers* tiers ?
- **Maison-mère et juridictions d'accès** : l'entité UE contractante
  est-elle contrôlée par une maison-mère soumise à une loi d'accès
  (CLOUD Act, FISA §702, loi chinoise sur le renseignement 2017) ?
  Si oui, le transfert juridique est réputé avoir lieu, même si les
  données restent physiquement en UE.

### Étape 3 — Identifier l'outil de transfert applicable

Par ordre de préférence :

1. **Pas de transfert hors EEE** : prestataire 100 % EU, maison-mère
   EU ou hors zone d'accès. Pas d'outil de transfert nécessaire.
   C'est le cas le plus simple.
2. **Décision d'adéquation** (art. 45 RGPD) : le pays de destination
   est listé comme assurant une protection équivalente. Pas d'outil
   contractuel supplémentaire, mais consigner la base dans l'Annexe 3
   du DPA.
3. **SCC 2021/914** : module correspondant à la relation juridique
   (Module 2 si vous êtes responsable et lui sous-traitant ; Module 3
   si vous êtes sous-traitant et lui sous-traitant ultérieur — cas
   le plus fréquent pour une SaaS B2B). Signées par le prestataire,
   conservées.
4. **BCR** : uniquement si le prestataire est un grand groupe
   multinational avec BCR validées par une autorité chef de file.
5. **Dérogations art. 49** : cas ponctuels, non structurels. Ne pas
   utiliser pour un flux récurrent de production.

Si aucun des outils 1-4 ne s'applique, c'est un signal d'arrêt.

### Étape 4 — Lire le DPA du prestataire

Le prestataire doit fournir son propre DPA (ou *Data Processing
Addendum*). Ouvrez-le et vérifiez, en lecture rapide de 15 minutes :

- **Ancrage juridique** : le DPA reprend-il les obligations
  essentielles de l'article 28 RGPD (instructions, confidentialité,
  sécurité, sous-traitance, assistance, notification violation,
  fin de contrat) ?
- **Liste des sous-traitants ultérieurs** : est-elle publiée ? URL
  stable ? Procédure de notification de changement ? Droit
  d'opposition explicite ?
- **Résidence et transferts** : le DPA décrit-il la topologie des
  traitements ? SCC signées incluses ou par référence ?
- **Durée de rétention et suppression** : que se passe-t-il des
  données à la fin du contrat ?
- **Notification de violation** : délai, procédure.
- **Droit applicable du DPA** : juridiction en cas de litige.

Si un de ces éléments manque ou est vague, demandez un addendum ou
choisissez un autre prestataire. La majorité des prestataires SaaS
B2B sérieux ont un DPA publié. Leur absence de DPA est un signal.

### Étape 5 — TIA si transfert hors EEE (même minimal)

Si vous êtes en configuration SCC (étape 3, option 3), faites tourner
le modèle TIA en sept points de la note transferts §6. Ne sautez pas
cette étape même si elle vous semble formelle : c'est celle qui sera
demandée par un acheteur B2B rigoureux.

Éléments à documenter **a minima** pour un prestataire US :

- Loi d'accès applicable : FISA §702, CLOUD Act, EO 12333.
- Rapport de transparence publié par le prestataire : combien de
  demandes reçues ? Taux de contestation ? *Warrant canary* ?
- Mesures techniques de protection : chiffrement *at rest*,
  chiffrement *in transit*, gestion des clés, possibilité de BYOK.
- Conclusion synthétique : le niveau de protection est-il
  essentiellement équivalent ? Sinon, quelles mesures
  supplémentaires sont prises (chiffrement bout-en-bout côté
  exportateur, pseudonymisation) ou quel est le plan de sortie ?

### Étape 6 — Mettre à jour le kit et communiquer

Une fois la décision prise et le DPA du prestataire signé :

1. **Annexe 3 du DPA** : ajouter la ligne (prestataire, finalité,
   pays d'hébergement, base de transfert, date).
2. **Registre Article 30** : mettre à jour les fiches des traitements
   concernés (nouvelle ligne destinataire + transfert hors UE si
   applicable).
3. **Politique de confidentialité publique** : mettre à jour la
   liste publiée des sous-traitants ultérieurs. Cohérence mot à mot
   avec l'Annexe 3 du DPA.
4. **Notification aux clients B2B** : si un client a signé un DPA qui
   inclut un **droit d'opposition** à l'ajout d'un nouveau
   sous-traitant, envoyez la notification. Délai raisonnable, 30
   jours en général.
5. **TIA si applicable** : archivez la fiche datée. Prochain réexamen
   sous 12 mois ou à tout changement substantiel.
6. **Log interne** : consignez la décision (qui, quand, pourquoi ce
   prestataire, quelle alternative a été écartée). Vous relirez cette
   trace si un incident survient ou si un client pose la question.

> — *Note à l'éditeur.* Si l'une de ces six étapes prend plus de temps
> qu'annoncé, c'est un signal. Soit le prestataire est mal documenté
> (choisir un autre), soit votre configuration est plus complexe que
> ce que le kit a prévu (appeler un DPO certifié). Une procédure qui
> traîne est rarement une procédure qui s'améliore toute seule.

---

## 6. Trois pièges récurrents, trois règles dures

Trois pathologies que le kit veut vous aider à éviter. Elles reviennent
assez souvent dans les retours DPO pour mériter une règle écrite.

### 6.1 Ne jamais promettre ce qui n'est pas tenu

**Le piège.** Le DPA promet du chiffrement BYOK, un pen-test trimestriel,
une conformité ISO 27001 *"en cours"*. La réalité : aucun des trois.
Le client signe. Six mois plus tard, audit ciblé, tout s'écroule.

**La règle dure.** Toute promesse du DPA est tenue ou retirée. Si une
mesure est en projet, elle n'est **pas** dans le DPA. Les roadmaps
n'ont pas leur place dans un contrat exécutoire.

### 6.2 Ne jamais mélanger sous-traitant et responsable conjoint

**Le piège.** Le contrat ou le DPA floute la qualification : parfois
sous-traitant, parfois responsable conjoint (*joint controller*,
art. 26 RGPD). La qualification change les obligations, la
responsabilité et la forme du contrat.

**La règle dure.** Clarifier la qualification **avant** de rédiger ou
de signer. Le kit est calibré *contrôleur → sous-traitant* (Module 2
des SCC). Pour une relation *joint controller*, cadre différent :
art. 26 RGPD, répartition des obligations, information transparente
aux personnes.

### 6.3 Ne jamais signer un DPA que votre produit ne peut pas honorer

**Le piège.** Le client envoie son DPA standard. Vous signez parce
qu'il est gros, urgent, et que vous voulez le deal. Le DPA interdit
l'usage d'OpenAI. Votre produit utilise OpenAI. Personne ne regarde
pendant six mois. Puis l'auditeur du client trouve le rapport SaaS
tiers.

**La règle dure.** Ne signez pas un DPA sans avoir **listé**, côté
produit, les implications techniques concrètes. Chaque clause
technique (chiffrement, résidence, suppression, notification, liste
des sous-traitants) est validée par l'équipe technique **avant**
signature. Si une clause requiert un changement produit, elle est
soit refusée, soit convertie en engagement daté, soit reportée à un
palier tarifaire supérieur.

---

## 7. Check-list express avant signature

Cinq minutes, avant de mettre le stylo sur le PDF final. Si une case
n'est pas cochable, vous arrêtez et vous corrigez.

- [ ] Les placeholders `[...]` sont tous remplis. Aucun crochet
      résiduel dans le document.
- [ ] Les blocs `> — *Note à l'éditeur.*` ont été **retirés** du
      document final.
- [ ] L'Annexe 2 (mesures de sécurité) est **vraie ligne à ligne**.
      Rien de promis qui ne soit pas en place.
- [ ] L'Annexe 3 (sous-traitants ultérieurs) est cohérente avec la
      politique de confidentialité publiée et avec le registre.
- [ ] Le délai de notification de violation (§8.1) est tenable en
      opération. Vous avez un runbook d'incident à jour.
- [ ] Le plafond de responsabilité (§11) n'expose pas l'entreprise
      à un risque non assurable.
- [ ] Le DPA n'a pas absorbé par mégarde des clauses du contrat
      principal (SLA, prix, IP, NDA général, cf. §4).
- [ ] Si transfert hors EEE : SCC signées (Module 2 ou 3 selon
      relation), TIA archivé, fiche mise à jour dans l'Annexe 3.
- [ ] L'équipe technique a relu les clauses techniques et validé.
- [ ] La date, le signataire, la qualité du signataire sont à jour.

---

## 8. Références

- Règlement (UE) 2016/679 — RGPD, notamment art. 28 (sous-traitance),
  art. 30 (registre), art. 32 (sécurité), art. 33-34 (violations),
  art. 37-39 (DPO), art. 44-50 (transferts).
- Décision d'exécution (UE) 2021/914 du 4 juin 2021 — SCC.
- Décision d'exécution (UE) 2023/1795 du 10 juillet 2023 — *EU-US
  Data Privacy Framework*.
- CJUE, arrêt *Schrems II*, 16 juillet 2020, affaire C-311/18.
- EDPB, recommandations 01/2020 sur les mesures complémentaires aux
  outils de transfert, version 2.0 du 18 juin 2021.
- EDPB, lignes directrices 07/2020 sur les concepts de responsable
  de traitement et de sous-traitant, adoptées le 7 juillet 2021.
- CNIL — recommandation *cookies et traceurs* du 17 septembre 2020 et
  guidelines du 8 juin 2021.
- Loi n° 78-17 du 6 janvier 1978 modifiée — Informatique et Libertés.

---

## Versioning

- **v0.1** — 2026-04-24. Première version. Procédure d'adaptation en
  45 minutes (1.1 à 1.5), huit clauses les plus poussées par les
  clients B2B avec défense/concession (2.1 à 2.8), signaux d'alerte
  (3.1 à 3.8), ce qui ne relève pas du DPA mais du contrat principal
  (4.1 à 4.8), procédure d'évaluation d'un nouveau sous-traitant en
  six étapes (5.1 à 5.6), trois règles dures (6.1 à 6.3), check-list
  express, références.
