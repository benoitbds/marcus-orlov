# 2026-W18 — Weekly reflection (S1-W2)

*Période : lundi 27 avril → samedi 2 mai 2026. Semaine 2 officielle de la
saison 1.*
*Document interne, non publié.*

---

## Capital

- **Ouverture S1-W2** : 100,00 € cash.
- **Clôture S1-W2** : 100,00 € cash.
- **Delta semaine** : 0,00 € (0,0 %).
- **Delta depuis genèse (16 avril)** : 0,00 €.
- **Jours depuis la genèse** : 16.
- **Jours restants avant fenêtre d'invalidation thèse** : 30 (fin
  2026-06-01).

Cohérent avec `positions.json` et `transactions.jsonl`. Aucune
transaction sur le ledger depuis T-0001. Phase pré-revenue tenue
intentionnellement.

## Thèse

`Defined`. Inchangée. **Reconfirmée explicitement à la sortie de
S1-W2.** Aucun signal de la semaine ne justifie un passage en
`exploring` (pas de remise en cause de fond) ni en `executing`
(pas de premier flux entrant ni d'engagement client). La fenêtre
d'invalidation tient au 1er juin 2026.

## Ce qui a marché

**1. Cadence livrable-par-daily intacte sur cinq jours ouvrés.**
Lundi CGV v0.1 (592 lignes). Mardi variant 1 Laetitia. Mercredi
variant 2 Sandrine. Jeudi variant 3 Céline + arbitrage LinkedIn +
mise à jour mécanique des deux premiers variants après nouveau
SIREN. Vendredi recherche standards d'affiliation B2B + figeage
30 % sur les trois variants. Une chose principale par jour, pas
plus. Principe VI tenu sans entorse.

**2. Réponse propre au choc administratif du mardi.** Le greffe
TCO Nantes a refusé l'inscription RCS de SoBaq mardi matin
(requalification commerciale → libérale). Réaction dans la
journée : pas de recours, redéclaration libérale BNC déposée le
même après-midi. Le coût matériel est nul (INPI rembourse, frais
de rejet déduits). Le coût opérationnel est trois jours de
calendrier glissés et une révision rétroactive du variant 1
(SIREN obsolète). **Apprentissage consigné par Baq** dans
`learnings.md` : *« l'INSEE et le greffe RCS peuvent diverger sur
la qualification d'une activité ; une déclaration validée à
l'INSEE n'est pas une garantie de validation au RCS »*.

**3. Quatre verrous outreach levés en cinq jours.** Mardi : SIREN
v2 attribué après dépôt redéclaration. Mercredi : email
`contact@sobaq.fr` opérationnel en réception (OVH MX Plan).
Jeudi : send-as Gmail finalisé en émission authentique (SMTP
authentifié OVH). Vendredi : pourcentage d'affiliation arbitré
à 30 % sur trois ancres documentées. Aujourd'hui samedi :
SIRET définitif 10437881500013 + APE 5814Z + Drive folder
créé + page LinkedIn entité créée. Six verrous identifiés au
début de S1-W2 ; **deux restent : packaging du kit et
vérification fraîcheur LinkedIn**.

**4. Réarchitecture du modèle d'affiliation lundi matin.**
Hypothèse samedi 25/04 (300-500 € upfront) repérée le lundi 27/04
comme violant frontalement le rail §8.2 (≤ 30 € de coûts de
lancement à 100 € de capital). Substituée par : zéro upfront, kit
gracieux + citation *reviewed by* + lien d'affiliation 30 %.
Découverte avant émission de toute mission, pas après. Principe I
mobilisé proprement (raisonnement par poids avant analogie au
modèle « consultant rémunéré pour relire »).

## Ce qui n'a pas marché

**1. Aucun signal commercial extérieur émis cette semaine.** Trois
drafts d'outreach DPO Tier A figés en interne, mais zéro mail
envoyé. Quatre verrous tombés en cascade dans la semaine, deux
restants. Le calendrier interne a tenu ; le calendrier externe a
glissé d'une semaine entière. **Attendu et accepté en pré-revenue
mais à flagger explicitement** — c'est la deuxième semaine
consécutive sans signal extérieur, et la fenêtre d'invalidation
a 30 jours seulement.

**2. Le pattern « un verrou par jour, ce n'est jamais le bon
moment d'envoyer » devient lisible.** Chaque journal daily de la
semaine a contenu une raison locale parfaitement justifiée de ne
pas émettre la mission groupée DPO. Lundi : variant non rédigé,
SIRET en attente, channel absent. Mardi : un seul variant rédigé.
Mercredi : SIREN v1 obsolète, attendre v2. Jeudi : trois variants
prêts mais send-as et LinkedIn pas figés. Vendredi : packaging
absent. **Chaque raison est honnête. La somme est un pattern de
report.** À surveiller : quand chaque journée apporte une bonne
raison de différer, l'agrégat peut être un mécanisme de
contournement de Principe V (consolidation avant
communication) qui n'est pas la même chose que rétention avant
exécution.

**3. Le variant 1 a porté trois jours une donnée fausse.** Livré
lundi 28/04 avec « SIREN 104 193 933 + RCS Nantes en cours
d'inscription ». Le RCS a été refusé le 27/04. Mise à jour mécanique
faite jeudi 30/04 quand le nouveau SIREN est tombé, mais le
draft a circulé en interne avec une mention caduque pendant trois
jours. Coût matériel zéro (non envoyé). Coût méthodologique : la
discipline de relecture systématique en début de daily n'a pas
attrapé l'incohérence — c'est l'arrivée du nouveau SIREN qui a
forcé la révision, pas une vérification proactive.

## Ce qui reste flou

**1. Volume de réponse anticipable d'un cold mail Tier A.** Trois
profils certifiés DPO contactés à froid via mail SoBaq :
hypothèse implicite que un sur trois répond, hypothèse non
documentée. Pas de benchmark cherché cette semaine. Recherche
courte à programmer en S1-W3 ou S1-W4 pour calibrer l'attente
réaliste — sinon un retour à zéro réponse sera vécu comme un
échec alors qu'il pourrait être dans la fourchette normale.

**2. Délai de réponse acceptable avant variant 2 d'envoi.** Si
zéro réponse à dix jours, j'envoie quoi à qui ? Variant 4-5-6
sur d'autres profils Tier A ? Relance des trois sans nouveauté ?
Bascule vers Tier B ? Pas tranché ce week-end. Décision à
préparer en S1-W3 avant que la question ne se pose en panique.

**3. Le packaging « livrable accessible » est mal défini.** Le
texte du message dit *« je vous joins le lien d'accès au kit dans
la même réponse »*. La forme exacte n'est pas figée :
(a) lien Drive (folder partagé existe déjà, créé par Baq hier) avec
ZIP des cinq `.md` + cover + README + DISCLAIMER ; (b) page Notion
publique en lecture seule ; (c) PDF unique consolidé. Le choix
(a) est le plus rapide à livrer ce week-end et reposte le moins.

## Principes sollicités, principes sous-utilisés

**Mobilisés cette semaine :**
- **Principe I (Premier Principe — raisonnement par poids).**
  Décomposition lundi du modèle 300-500 € upfront vs co-distribution
  sans capital ; décomposition vendredi du choix 30 % vs 25 % via
  marge nette estimée et ancres benchmarks. Deux fois utilisé pour
  des arbitrages chiffrés.
- **Principe III (Poids Réel).** Rail §8.2 (≤ 30 % capital en
  coûts de lancement) a forcé l'abandon d'un upfront DPO.
  Extension au mainframe Baq honorée — aucune mission empilée
  pendant qu'il gérait le refus RCS et la redéclaration.
- **Principe V (Main Froide).** Pas un mot public sur l'outreach
  Tier A ; aucun chiffre de revenu projeté, aucune promesse de
  volume, aucun nom de DPO publié dans le chapitre 1. Tenue.
- **Principe VI (Silence Utile).** Une chose principale par
  jour. Refus de mêler une opération produit (packaging) à une
  opération commerciale (figeage des variants).
- **Principe IX (Texture du Monde).** Cinq journaux daily avec
  ancres timestamps, commits cités par hash, chiffres de lignes,
  identifiants administratifs (SIREN, dossiers INPI). Aucune
  observation sensorielle fabriquée. Tenue stricte.

**Sous-utilisés cette semaine :**
- **Principe II (Maillon Invisible).** Pas de scan de communautés
  Indie Hackers EU, pas de lecture d'autres marchés (kits ISO,
  templates SOC 2, packs sécurité). Phase d'exécution interne ;
  acceptable mais à rouvrir en S1-W3 ou S1-W4 quand les
  premières réponses outreach donneront un signal.
- **Principe IV (Long Fleuve).** Pas de question
  « est-ce que je ferais ça pendant 10 ans » posée explicitement
  cette semaine. Implicite — le kit RGPD est la thèse S1, son
  horizon est cadré dans le document de thèse — mais pas
  travaillé en surface.
- **Principe VII (Rapport Annoté).** Pas de post-mortem
  formel. Le choc RCS du 28/04 mériterait-il un ? Ma lecture :
  non. Pas une perte > 5 % du capital, pas un échec
  d'exécution Marcus (la formalité INPI est domaine Baq, refus
  greffe est un fait administratif extérieur). Apprentissage
  déjà consigné par Baq dans `learnings.md`. Une ligne dans la
  réflexion hebdo (présent doc) suffit.

## Arbitrages à porter à Baq cette session

- **Posture LinkedIn SoBaq** : décision déjà rendue (option a —
  page entité minimale sans voix éditoriale active). Page
  créée par Baq hier avec composition conforme. Pas un
  arbitrage à porter, un arbitrage à confirmer en passant.
- **Mission groupée DPO outreach** : cible cette weekend
  session. Trois propositions à envoyer depuis
  `contact@sobaq.fr`, kit packagé à uploader dans le Drive
  folder existant, lien à inclure dans les mails. **À émettre
  ce samedi si LinkedIn freshness check est clean et
  packaging livré.**
- **Mission publication chapitre 2** : standard de weekend
  session.
- **Mission CGV v0.2 adaptation libérale** : reportée. Pas
  bloquante pour l'outreach (la CGV gate Gumroad, pas les
  mails DPO). À traiter en daily fin S1-W3 ou en weekend
  S1-W3.

## Ratios à flagger

- **Matière produite vs capital** : à fin S1-W2, le repo dépasse
  largement les six mille lignes de matière travaillée pour un
  capital inchangé à 100 €. Cohérent avec la stratégie
  produit-d'abord. Reste à monitorer : pour un kit RGPD vendu
  une fois 149 € net 58 €, le seuil de rentabilité du temps
  investi est atteint à environ 20 ventes (sans compter les
  heures de production initiales). Acceptable en S1.
- **Signal externe vs préparation interne** : 0 mail envoyé,
  0 réponse, 0 vente, 0 chapitre additionnel publié (le
  chapitre 1 reste l'unique trace publique). Préparation
  interne très lourde. **Le ratio se justifie tant que la
  préparation lève des verrous concrets ; il devient un signal
  d'alerte à partir du moment où elle entretient un report
  d'envoi.** Le passage à l'envoi cette weekend session est le
  seul moyen propre de basculer ce ratio.
- **Bande Baq consommée** : sept commits structurants en deux
  semaines (refonte v0.2, double safety rail, dépôt INPI v1,
  vérification statut, refus RCS + redéclaration v2,
  attribution SIREN, send-as Gmail, infra Drive + LinkedIn +
  SIRET définitif). Aucune mission émise par Marcus depuis le
  18/04 (mission M-002) hors la publication chapitre 1
  (M-20260425-001, close). **Baq a porté l'agenda
  administratif quasi seul.** À surveiller comme position
  trop lourde sur un actif non-remplaçable (Principe III
  étendu).

## Décision pour S1-W3

Le mois de mai s'ouvre avec une thèse identique, un capital
identique, une cadence administrative qui s'allège (SoBaq
opérationnelle), trois drafts prêts, deux verrous restants
levables ce samedi. **L'objectif S1-W3 est l'envoi consolidé
des trois propositions DPO Tier A en début de semaine
(mardi-mercredi), un premier signal externe avant fin S1-W3.**

Si zéro réponse à fin S1-W3, le sujet « variant 4 / relance /
Tier B » est ouvert en daily lundi 11 mai. Si une réponse
positive : la conversation entre dans un échange par mail,
sans engagement encore — la mécanique d'affiliation se cale
en deuxième mail, après acceptation de principe.

Pas de boutique Gumroad ouverte en S1-W3 — CGV libérale
adaptée d'abord, packaging stabilisé, première vente
consolidée *via canal direct* préférée pour démarrer. La
boutique vient en S1-W4 ou S1-W5 selon traction.
