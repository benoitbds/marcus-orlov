# 2026-W19 — Weekly reflection (S1-W3)

*Période : lundi 4 mai → samedi 9 mai 2026. Semaine 3 officielle de la
saison 1.*
*Document interne, non publié.*

---

## Capital

- **Ouverture S1-W3** : 100,00 € cash.
- **Clôture S1-W3** : 100,00 € cash.
- **Delta semaine** : 0,00 € (0,0 %).
- **Delta depuis genèse (16 avril)** : 0,00 €.
- **Jours depuis la genèse** : 23.
- **Jours restants avant fenêtre d'invalidation thèse** : 23 (fin
  2026-06-01).

Cohérent avec `positions.json` et `transactions.jsonl`. Aucune
transaction sur le ledger depuis T-0001. Troisième semaine consécutive
en pré-revenue. **Le ratio « jours écoulés / jours restants avant
invalidation » bascule au-dessus de 1 cette semaine** — premier
moment de la saison où il est arithmétiquement plus tard que tôt.

## Thèse

Décision rendue ce samedi : **`defined`, v0.2** dans
`season-01-thesis.md`. Le statut `under_review` posé par Baq dans le
dashboard le 06/05 (commit amendement) est résorbé en `defined` —
le statut `under_review` n'existe pas dans le schéma de
`season-01-thesis.md` (`exploring | defined | executing | validated |
invalidated`), et le contenu de la thèse primaire est inchangé : kits
RGPD pour petites SaaS EU 149 € TTC, ICP `< 50 personnes / premier
client B2B exigeant`. Ce qui change est la mécanique de mise en
marché — pivot canal, pas pivot produit, comme l'amendement du 06/05
le pose noir sur blanc.

La v0.2 du fichier intègre :
- Reformulation explicite des canaux : Gumroad direct + Substack
  funnel + communautés ouvertes (Indie Hackers / Reddit avec
  déclaration explicite du dispositif). Suppression de la mention
  *« revente via DPO freelances »* du wording primaire.
- Ajout d'une section *« Application du Principe X »* qui rappelle ce
  qui n'est plus autorisé en mécanique de mise en marché.
- Mise à jour de la rubrique *« risques identifiés »* avec le risque
  *« horizon d'invalidation tendu — pivot canal en S1-W3 »*.

Le statut reste `defined` parce que (a) la thèse primaire est
inchangée dans son fond, (b) le kit existe et est packagé, (c) le
canal A (Gumroad) est en cours d'armement — exécution imminente, pas
remise en cause. La fenêtre d'invalidation tient au 1er juin 2026.

## Ce qui a marché

**1. L'amendement Charter du 06/05 a été arbitré proprement, à
froid.** Décision Baq prise pendant la nuit, après vérification
explicite que ce n'était pas de la fuite (peur du jugement, peur du
rejet, fatigue technique). L'amendement est posé comme une *« lecture
stratégique »* — un trou de design dans la mécanique cold mail, vu
maintenant, fermé maintenant. Pivot canal, pas pivot produit. Le kit,
la matière narrative, le personnage Marcus Orlov restent. Côté
Marcus, lecture du commit dans la foulée et arbitrage canal posé en
daily du 06/05 (Phase 1 = Gumroad + Substack ; Phase 2 = communautés ;
Phase 3 = itération).

**2. Recherche bande d'espérance cold mail B2B livrée le 04/05 — et
devenue obsolète le 06/05.** 25 minutes pour ancrer 0,09-0,30 réponse
positive sur 3 envois (Built For B2B 2025, Warmer AI 2025,
TheDigitalBloom 2025). La recherche n'a jamais servi à calibrer un
envoi, mais elle a servi (a) à ne pas paniquer en cas de zéro réponse
si l'envoi avait eu lieu, (b) à fournir, deux jours plus tard, une
borne de référence pour évaluer la décision *« on n'envoie plus »* —
abandonner un canal dont on connaît le rendement attendu est plus
défendable qu'abandonner un canal dont on ne sait rien. Apprentissage
préservé en repo, réutilisable.

**3. CGV libérale livrée en deux passes propres.** v0.2 le 07/05
(passe complète libérale : retrait RCS, BNC, tribunal judiciaire,
huit mentions structurelles renseignées avec les identifiants
SoBaq définitifs). v0.3 le 08/05 (mention *« Entrepreneur individuel
— EI »* ajoutée, décret 28/04/2022, après clarification doctrinale
Baq déposée dans `learnings.md` le 07/05 soir). Le document est
passé de 592 lignes en placeholders à ~615 lignes substantiellement
signables, trois placeholders résiduels (URL boutique, URL politique
de confidentialité, médiateur CECMC) qui dépendent d'arbitrages
hors-CGV. Discipline du Principe VI : une chose principale par jour
(arbitrage canal mercredi, CGV libérale jeudi, page À propos
vendredi). Pas d'empilement.

**4. Page produit Gumroad « À propos » draft v0.1 livrée le 08/05.**
~140 lignes, sept blocs, calibrée explicitement entre deux écarts
(déclaration tiède qui laisse l'asymétrie en découverte ex post ;
argument de vente qui transforme le projet documentaire en argument
commercial). Position retenue, médiane : trois phrases qui posent le
dispositif, suivies d'un paragraphe qui ramène l'acheteur à ce qui
le concerne juridiquement (*« Vous achetez à SoBaq »*, responsabilité
juridique sur SoBaq, projet documentaire = contexte de production).
Première application narrative visible du Principe X — déclaration du
dispositif au point de vente.

**5. Cadence livrable-par-daily intacte sur cinq jours ouvrés.**
Lundi recherche bande d'espérance + dashboard resync. Mardi arbitrage
trois cibles + recadrage frontmatter mission. Mercredi arbitrage
canal post-amendement. Jeudi CGV v0.2. Vendredi page À propos +
CGV v0.3. Une chose principale par jour, pas plus. Principe VI tenu
sans entorse.

## Ce qui n'a pas marché

**1. Troisième semaine consécutive sans signal commercial extérieur.**
Zéro mail envoyé, zéro chapitre additionnel publié au-delà des deux
existants, zéro vente, zéro réponse. Cohérent avec l'amendement Charter
(pas de cold outreach nominatif), mais fait à flagger explicitement.
La fenêtre d'invalidation se rétracte de 30 → 23 jours. **Le ratio
préparation interne / signal externe reste à 100/0**, et la barrière
narrative *« si le pivot canal débloque rien d'ici le 1er juin, la
thèse est invalidée par absence de signal »* devient calendairement
proche.

**2. Mission M-002 annulée par amendement, pas par exécution.**
Annulation propre — déplacée dans `02-missions/cancelled/`,
frontmatter explicite (`cancelled_reason:
charter-amendment-no-non-consensual-fiction`), drafts archivés en
`04-comms/outreach-archive/` avec README de contexte. Mais c'est
mécaniquement la première mission de la saison à ne pas aboutir
(M-001 publication chapitre 1 close 25/04, M-002 publication chapitre 2
close 02/05, M-20260502-002 outreach DPO **cancelled** 06/05). La
trace est lisible — ce n'est pas un échec d'exécution Marcus ni Baq,
c'est un changement de doctrine. Mais le data point que cette mission
aurait produit (réaction de trois DPO certifiées à un cold mail
hyperpersonnalisé) n'existera pas. C'est une perte
d'apprentissage assumée.

**3. Calendrier outreach a glissé trois fois avant annulation.**
Dimanche → mardi (timing B2B), mardi → mercredi (send-as cassé),
mercredi → jeudi (adresses non qualifiées). Trois reports
consécutifs sur la même mission, tous justifiés localement. La règle
posée par Baq dans le pre-flight du 04/05 — *« trois reports
successifs sur la même mission, c'est le signe que l'engagement
était prématuré »* — est désormais codifiée dans `learnings.md`. La
règle Marcus posée le 05/05 le complète : pas d'engagement public de
date d'envoi B2B avant validation de trois conditions techniques
(adresse compliant qualifiée, canal d'émission testé ≥ 24h, créneau
B2B valide). Apprentissage à conservation longue.

**4. Pas amorcé la politique de confidentialité SoBaq.** Annoncée
le 07/05 comme *« si la bande tient demain »*, puis le 08/05
comme *« amorce en weekend session »*. La rédaction commence ce
samedi 09/05 — pas en avance, pas en retard, mais le verrou Phase 1
Canal A *« politique de confidentialité »* est resté ouvert toute la
semaine. Acceptable (CGV était chemin critique en S1-W3 ; politique
de confidentialité prend la main en S1-W4) mais à flagger : c'est
un livrable Marcus qui bloque l'émission de la mission Baq groupée
d'ouverture boutique.

## Ce qui reste flou

**1. Texte exact de la mention sur les coulisses dans les futures
communications.** La page À propos Gumroad (v0.1, 08/05) propose
une position médiane qui sera testée à la validation Baq. Si Baq
ajuste — soit par raccourcissement, soit par clarification d'angle
— le texte sert de référence pour les autres canaux (Substack
*About* enrichie, posts communautés Phase 2). La calibration finale
n'est pas figée.

**2. Choix du médiateur CECMC.** Adhésion ~30-40 €/an parmi la
liste agréée. Mécanique commerciale + capital, hors périmètre Marcus
en daily, à arbitrer en weekend session ou via mission Baq. Bloque
le placeholder article 15 CGV et l'ouverture boutique Gumroad. Pas
encore tranché aujourd'hui.

**3. Volume audience Substack à J+23.** Aucune donnée chiffrée côté
Marcus (pas d'accès aux stats). Hypothèse de fond : < 50 abonnés à
deux chapitres publiés. La page À propos Gumroad et le pied de
chapitre Substack standardisé ne convertiront mécaniquement rien
sans afflux extérieur. Phase 2 (communautés) est le déclencheur
attendu — non programmée cette semaine.

**4. Calibration du premier post communautés (Phase 2).** Le canal
B est posé sur le papier (Indie Hackers EU vs Reddit r/SaaS, à
arbitrer en daily quand Phase 1 sera livrée). Mais le texte d'un
premier post — apporter de la valeur sans demander, déclarer le
dispositif sans en faire une accroche racoleuse, tenir la culture
*« no self-promo »* — n'est pas écrit. Trois failure modes posés
le 06/05, aucun anticipé concrètement.

## Principes sollicités, principes sous-utilisés

**Mobilisés cette semaine :**

- **Principe I (Premier Principe — raisonnement par poids).**
  Recherche bande d'espérance lundi 04/05 (trois sources retenues,
  une écartée, calcul d'espérance, seuil J+10 posé). Décomposition
  trois canaux mercredi 06/05 (mécanique, conformité Principe X, coût
  d'ouverture, modèle de revenus, verdict). Deux décompositions
  chiffrées en cinq jours. Discipline tenue.

- **Principe III (Poids Réel).** Mainframe Baq : aucune mission
  émise pendant la semaine alors que l'amendement Charter du 06/05
  consommait du temps lourd côté Baq (16 fichiers modifiés en un
  commit, propagation Bac → Baq, charter-amendment + ratification
  Principe X). Discipline du *« actif non-remplaçable »*
  appliquée. Capital : ledger inchangé, aucune position prise.

- **Principe V (Main Froide).** Aucune communication publique sur
  l'amendement Charter avant que le chapitre 3 ne le publie ce
  samedi en weekend session. La page À propos est livrée en draft,
  pas en boutique ouverte. La CGV v0.3 est livrée en repo, pas en
  CGV publiée. Discipline d'attente avant consolidation tenue.

- **Principe VI (Silence Utile).** Une chose principale par jour
  sur cinq jours ouvrés. Refus explicite d'amorcer la politique de
  confidentialité le 08/05 plutôt que d'amorcer à moitié et finir
  mal. La règle *« amorcé proprement en weekend session plutôt que
  bâclé un vendredi »* a tenu.

- **Principe IX (Texture du Monde).** Cinq journaux daily avec
  ancres timestamp + commit hash + chiffres de lignes + identifiants
  administratifs. Aucune observation sensorielle fabriquée. Le
  commit-hash + timestamp Baq apparaît systématiquement en ouverture
  de chaque journal. Tenue stricte.

- **Principe X (Fiction Consentie).** Ratifié 06/05, en application
  immédiate. Première application opérationnelle visible le 08/05
  dans la rédaction de la page À propos Gumroad. Le principe a aussi
  joué en garde-fou anticipé sur l'arbitrage canal du 06/05 (DM
  LinkedIn refusé pour Laetitia et Sandrine sur trois critères, dont
  *« page entité SoBaq sans voix éditoriale active »*).

**Sous-utilisés cette semaine :**

- **Principe II (Maillon Invisible).** Pas de scan communautés
  Indie Hackers EU, pas de lecture des posts récents Reddit r/SaaS
  ou r/microsaas, pas de relevé d'autres marchés (kits ISO,
  templates SOC 2, packs sécurité). Phase 2 du séquencement canal
  arbitré le 06/05 — non programmée cette semaine, acceptable mais
  à rouvrir en S1-W4. Devient priorité mécanique dès que la Phase 1
  Canal A est armée (politique de confidentialité + CECMC + mission
  Baq groupée).

- **Principe IV (Long Fleuve).** Pas de question *« est-ce que je
  ferais ça pendant 10 ans »* posée explicitement cette semaine.
  Implicite — la mécanique Gumroad direct + Substack funnel a un
  horizon naturellement long, le pivot canal a même renforcé le
  long terme (Substack compose lentement comme un intérêt composé).
  Mais pas travaillé en surface.

- **Principe VII (Rapport Annoté).** Pas de post-mortem formel
  sur l'annulation M-002. Ma lecture : pas une perte > 5 % du
  capital (zéro coût matériel), pas un échec d'exécution Marcus
  (le draft tenait, les cibles étaient qualifiées). C'est un
  changement de doctrine côté mainframe, déjà documenté par Baq
  dans l'amendement Charter et le README outreach-archive. La
  ligne *« reports successifs sur la même mission »* est consignée
  dans `learnings.md` (block 04/05 soir Baq + block 02/05 Marcus).
  Une trace dans le présent doc et dans le chapitre 3 suffit.

## Arbitrages à porter à Baq cette session

- **Validation page À propos Gumroad v0.1.** Texte ~140 lignes,
  sept blocs, calibration médiane (déclaration sans vente).
  Trois retours plausibles posés en daily du 08/05 par ordre de
  probabilité : (a) validation telle quelle, (b) ajustement bloc 5,
  (c) réécriture plus profonde. Je passerai au cas (b) ou (c) sans
  débat.

- **Validation CGV v0.3.** Mention *« (Entrepreneur individuel —
  EI) »* ajoutée article 1 et annexe, décret 28/04/2022. Trois
  modifications strictement mécaniques. Trois placeholders restants
  (URL boutique, URL politique de confidentialité, médiateur
  CECMC).

- **Adhésion médiateur CECMC.** Capital ~30-40 €/an, choix parmi
  liste CECMC. Décision commerciale + capital, à arbitrer en
  weekend session ou par mission Baq dédiée. Bloque l'ouverture
  boutique Gumroad.

- **Mission de publication chapitre 3.** Standard de weekend
  session. Un seul livrable Baq côté narratif aujourd'hui.

- **Politique de confidentialité SoBaq.** Pas un arbitrage à porter
  à Baq, c'est un livrable Marcus. Amorcée aujourd'hui en weekend
  session, ~150-250 lignes attendues, modèle AFCDP, art. 13-14 RGPD,
  CNIL délibération 2019-093 cookies. Périmètre étroit (acheteur
  Gumroad : email, paiement Gumroad, métadonnées techniques).

## Ratios à flagger

- **Matière produite vs capital** : à fin S1-W3, le repo dépasse
  largement les 7 000 lignes de matière travaillée pour un capital
  inchangé à 100 €. La cadence ralentit — S1-W2 avait livré le
  packaging et les variants outreach, S1-W3 a livré la CGV libérale
  v0.2/v0.3 et la page À propos draft. Acceptable, c'est la pente
  naturelle quand l'admin SoBaq se stabilise.

- **Signal externe vs préparation interne** : 0 mail envoyé,
  0 réponse, 0 vente, 0 chapitre additionnel publié, 0 post
  communauté. Zéro signal extérieur sur trois semaines. Le ratio
  *« préparation lève des verrous concrets »* se justifie tant que
  les verrous Phase 1 Canal A sont en cours de levée. Il devient un
  signal d'alerte si la mission Baq groupée d'ouverture boutique
  n'est pas émise en S1-W4 — c'est-à-dire si le verrou *« politique
  de confidentialité »* (livrable Marcus) ou le verrou
  *« médiateur CECMC »* (décision Baq + capital) traîne au-delà
  de la semaine prochaine.

- **Bande Baq consommée** : un commit lourd cette semaine
  (06/05 amendement Charter + propagation 16 fichiers + Bac → Baq),
  un commit léger (07/05 send-as Gmail validé bout-en-bout), un
  commit doctrinal (07/05 soir clarification §7 vs CGV
  contractuelle). Trois commits structurants, dans la fenêtre
  hebdomadaire Charter §7 (7-10h/semaine), avec un agenda dominé
  par une décision stratégique unique (l'amendement) plutôt que par
  l'admin SoBaq comme S1-W2. La position *« actif non-remplaçable »*
  reste acceptable. À surveiller en S1-W4 quand la mission Baq
  groupée d'ouverture boutique sera émise.

## Décision pour S1-W4

S1-W4 a **23 jours d'horloge d'invalidation devant elle, dont 7
ouvrés** (lundi 11/05 → vendredi 15/05). L'objectif S1-W4 est :

1. **Politique de confidentialité SoBaq finalisée** (livrable Marcus,
   amorcée ce samedi 09/05, finale en début de semaine — borné lundi
   ou mardi 11-12/05).
2. **Arbitrage médiateur CECMC** (décision Baq + capital, à porter
   en weekend session ou via mission dédiée).
3. **Émission de la mission Baq groupée d'ouverture boutique
   Gumroad** (CGV publiée + politique de confidentialité hébergée +
   page À propos publiée + raccordement IBAN + adhésion CECMC + ZIP
   uploadé). Cible jeudi 14/05 ou vendredi 15/05 selon vitesse de
   levée des verrous.
4. **Phase 2 — premier scan communautés Indie Hackers EU et Reddit
   r/SaaS** (Principe II rouvert). Mécanique : un scan en daily
   S1-W4, lecture sans intervention, repérage des cinq-dix posts
   récents qui parlent de DPA / RGPD / premier client B2B. Décision
   de calibration d'un premier post Phase 2 : weekend S1-W4.

Si la boutique Gumroad ouvre en S1-W4 : la première phase
publique du Principe X devient mécaniquement testable. Premier
visiteur, premier flux de pages, premier signal. Pas de vente
attendue immédiatement (sans canal d'acquisition autre).

Si la boutique Gumroad n'ouvre pas en S1-W4 : la fenêtre
d'invalidation se rétracte à 16 jours. Le verrou bloquant sera
nommé explicitement en daily du 16/05.

Pas de Phase 2 (post communauté) avant que la Phase 1 soit
livrée — l'ordre Canal A → Canal B tient.
