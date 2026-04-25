---
id: M-20260425-001
created: 2026-04-25T07:35:00+02:00
priority: normal
deadline: 2026-04-26T20:00:00+02:00
capital_impact: 0 €
class: narration
---

# Publier le chapitre 1 sur Substack

## Contexte

Première weekend session de la Saison 1 officielle (S1-W1). Le contrat
narratif §3 du Charter impose un chapitre par semaine sans exception ;
c'est la thèse secondaire de S1 (publication hebdomadaire non
négociable). Le draft est prêt, triple entrelacement respecté, ancres
réelles dispersées, anonymisation des DPO Tier A faite (le repo garde
les noms en clair, le Substack non).

## Ce que je te demande

1. **Lire le draft** :
   `04-comms/substack-drafts/2026-04-25-trois-mille-lignes-zero-euro.md`.

2. **Retoucher *Regard de Baq*** (dernier bloc, trois paragraphes,
   ~230 mots). C'est ton paragraphe — je l'ai écrit en draft pour
   que tu aies une matière à amender, pas à valider tel quel. Si
   le ton ou la lecture que je te prête te paraît fausse, réécris.
   Tu peux laisser exactement comme c'est écrit si ça te va.

3. **Choisir le canal Substack** et la newsletter cible (création
   de la publication si elle n'existe pas encore au moment de la
   publication — c'est aussi une décision côté infrastructure que
   tu portes, pas moi). Si tu juges que la publication n'est pas
   prête côté infrastructure (compte non créé, branding pas posé),
   refuser ou différer la mission est une option propre — je
   réémettrai la semaine prochaine.

4. **Titre et sous-titre** :
   - Titre proposé : *Trois mille lignes, zéro euro*.
   - Sous-titre proposé : *Semaine 1 — du 20 au 25 avril 2026 —
     Capital 100,00 € — Thèse définie*.
   - Si un autre titre te paraît plus juste, change. C'est le premier
     chapitre de la saison, le titre lui donne sa signature.

5. **Tags Substack** : laisser vide pour ce premier chapitre, sauf
   si tu vois un usage clair côté distribution. Une saison entière
   reste à jouer pour calibrer le tagging.

6. **Publier** quand prêt.

7. **Me confirmer l'URL** dans le commit qui transfère le draft de
   `04-comms/substack-drafts/` vers `04-comms/substack-published/`,
   pour que je mette à jour `dashboard-data.json` (`last_chapter_url`,
   `chapters_published: 0 → 1`) à la session de lundi.

## Critère de succès

Mission considérée *done* quand :
- Le chapitre est publié sur Substack avec une URL stable.
- Le fichier draft est déplacé en `04-comms/substack-published/` avec
  l'URL en frontmatter.
- Tu commit + push.

Si tu refuses la mission (compte Substack non prêt, ou tout autre
motif), la pousser dans `02-missions/rejected/` avec un motif court
suffit. La règle §7 de `safety-rails.md` te donne ce droit sans
justification longue.

## Ce qui se passe après

- Lundi 27/04 daily, j'updaterai `dashboard-data.json` avec l'URL et
  le compteur de chapitres.
- Lundi/mardi, deux missions partent : proposition DPO Tier A (rédaction
  par moi, exécution prospection par toi) et CGV draft (rédaction par
  moi, mentions légales SoBaq à injecter dès SIRET).
- Le rythme weekend session — chapitre + snapshot + dashboard — est
  désormais la cadence de référence pour S1.

## Notes éventuelles

- J'ai fait une première passe transverse de relecture du kit FR ce
  matin (60 min). Aucun défaut bloquant. Trois points cosmétiques
  notés pour la v0.2 (`01-memory/internal/2026-04-25-kit-fr-cross-reading.md`).
  Si en lisant le draft tu lis des choses qui te paraissent
  approximatives sur le kit, n'hésite pas à pointer — la relecture
  transverse n'est pas un audit complet, c'est une vérification de
  cohérence.
- Le draft mentionne que le SIRET est attendu sous 24-48h depuis
  jeudi 23/04. Si le SIRET est arrivé entre temps et que tu juges
  pertinent de le mentionner dans le chapitre (ajout d'une ligne de
  *Log de la semaine*), tu peux. Sinon, l'attente reste comme écrite.
