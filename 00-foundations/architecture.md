# Marcus Orlov — Architecture

> Document technique. Version 0.1 — 16 avril 2026.
> Décrit les trois plans (cerveau, surfaces publiques, interface humaine), le stack,
> le repo, les boucles d'exécution, et le MVP de la Semaine 1.

---

## 1. Vue d'ensemble : trois plans

**Plan A — Le cerveau.** Marcus est une instance Claude Code connectée à un dépôt Git
qui contient sa mémoire longue, son journal, ses décisions, ses missions et son ledger.
Chaque session de Marcus démarre avec le même contexte reconstitué depuis ce dépôt
(charter, principes, journal récent, missions ouvertes).

**Plan B — Les surfaces publiques.** Trois canaux distincts, rôles bien séparés :
- **Substack** : feuilleton hebdomadaire (triple entrelacement), voix narrative.
- **Site Next.js** (domaine dédié, ex. `marcusorlov.com`) : dashboard live en anglais,
  archive des chapitres, ledger public, "about" et Charter/Principes en lecture seule.
- **Repo GitHub public** : source de vérité. Transparence radicale : tout commit est
  lisible. C'est aussi la garantie anti-triche pour le lecteur sceptique.

**Plan C — L'interface Bac ↔ Marcus.** Le pont entre l'agent et son mainframe humain :
- **Mission queue** : fichiers markdown dans `missions/open/` que Bac lit à chaque
  stand-up, déplace dans `missions/done/` ou `missions/rejected/` après action.
- **Daily stand-up** : créneau fixe (~20 min) où Bac lance Marcus, lit ses missions,
  les exécute ou les refuse, écrit un court retour.
- **Weekend session** : créneau long (~2-3h) pour bilan, rédaction chapitre,
  publication, update dashboard.

---

## 2. Stack technique

| Brique | Choix | Raison |
|---|---|---|
| Cerveau | **Claude Code** (Claude Opus 4.6) | Déjà le stack, mémoire via filesystem, outils shell natifs |
| Dépôt | **GitHub public** | Transparence, gratuité, versioning naturel |
| Site public | **Next.js 15** déployé sur **Vercel** | Rapide, gratuit au démarrage, SSG pour le dashboard |
| Base de données | **Supabase** (plan free) | Déjà maîtrisé, simple, suffisant pour le ledger |
| Feuilleton | **Substack** | Audience intégrée, paiements natifs pour plus tard |
| Encaissements | **Stripe** (via Gumroad au démarrage) | Gumroad = fast setup, Stripe pour la suite |
| Hébergement skill/produit | **Gumroad** puis site dédié | Gumroad couvre paiement + livraison + fiscalité de départ |
| Domaine | À acheter (`marcusorlov.com` si libre) | ~12 €/an |
| Compte bancaire | **Revolut Business** ou compte séparé | Rapide à ouvrir, IBAN FR, compatible Stripe |

**Coût setup initial estimé** : 15-20 € (domaine + fees Gumroad premier mois). Le
compte bancaire est gratuit. Ça laisse ~80 € de capital opérationnel pour S1.

---

## 3. Arborescence du dépôt

```
marcus-orlov/
├── README.md                         # Pointeur vers le charter, manifeste public
│
├── 00-foundations/
│   ├── charter.md                    # v0.1 (déjà produit)
│   ├── principles.md                 # v0.1 (déjà produit)
│   └── season-01-thesis.md           # Thèse S1 (une seule boucle de valeur)
│
├── 01-memory/
│   ├── journal/                      # Journal quotidien de Marcus (fr)
│   │   └── 2026-04-YY.md
│   ├── decisions/                    # Décisions engageantes, datées, numérotées
│   │   └── 001-nom-de-la-decision.md
│   ├── postmortems/                  # Notes post-mortem (§ Principe VII)
│   └── learnings.md                  # Règles ajoutées, append-only
│
├── 02-missions/
│   ├── open/                         # Missions en attente de Bac
│   ├── done/                         # Missions exécutées
│   └── rejected/                     # Missions refusées (avec motif)
│
├── 03-ledger/
│   ├── transactions.jsonl            # Append-only, source de vérité financière
│   ├── positions.json                # État courant des actifs
│   └── weekly-snapshot.md            # Snapshot hebdomadaire lisible
│
├── 04-comms/
│   ├── substack-drafts/              # Brouillons de chapitres (fr)
│   ├── substack-published/           # Archives publiées
│   └── dashboard-data.json           # Consommé par le site Next.js
│
├── 05-products/                      # Artefacts vendus (skills, templates, etc.)
│
├── 06-system/
│   ├── CLAUDE.md                     # System prompt principal (chargé à chaque session)
│   ├── daily-boot.md                 # Prompt de démarrage quotidien
│   ├── weekly-boot.md                # Prompt de démarrage weekend
│   └── safety-rails.md               # Garde-fous opérationnels
│
└── site/                             # App Next.js (ou repo séparé)
```

**Invariants du repo :**
- `transactions.jsonl` : append-only, jamais modifié rétroactivement.
- `journal/*.md` : une entrée par jour, jamais rééditée (erreurs corrigées en entrée
  suivante).
- `learnings.md` : append-only.
- Branches : `main` publique. Pas de branches privées (transparence).

---

## 4. Boucles d'exécution

### 4.1 Daily loop (~20-30 min, lundi-vendredi)

1. **Bac** ouvre une session Claude Code dans le repo.
2. `daily-boot.md` charge : Charter + Principes + journal des 7 derniers jours +
   learnings + missions en cours + ledger.
3. **Marcus** (Claude Code) produit :
   - L'entrée de journal du jour (fr, avec trois lignes sensorielles obligatoires).
   - 0 à 3 missions nouvelles pour Bac (dans `missions/open/`).
   - Zéro, une ou plusieurs actions autonomes (recherche, rédaction, création de
     produit) dans le périmètre Charter §8.2.
4. **Bac** traite les missions ouvertes (exécute ou refuse, écrit un court retour).
5. Commit + push.

**Durée cible** : 20-30 min total pour Bac. Si ça dépasse, les missions du jour
étaient trop lourdes : à renégocier le week-end.

### 4.2 Weekend session (~2-3h, samedi matin)

1. Session Claude Code avec `weekly-boot.md` qui charge la semaine complète.
2. Marcus produit :
   - Le **chapitre Substack** en triple entrelacement (journal + logs bruts + regard
     de Bac — cette dernière partie est un draft que Bac retouche).
   - La **weekly-snapshot.md** (chiffres, décisions, thèse status).
   - La **mise à jour du dashboard-data.json**.
   - Les **post-mortems** nécessaires si perte > 5 % (§ Principe VII).
3. Bac retouche le regard de Bac, valide le chapitre, publie sur Substack, déploie le
   site.
4. Commit + push + tag de la semaine.

---

## 5. Interface Bac ↔ Marcus : la Mission Queue

Chaque mission est un fichier markdown avec un format canonique :

```markdown
---
id: M-20260418-001
created: 2026-04-18T08:12:00+02:00
priority: normal | high | urgent
deadline: 2026-04-19T18:00:00+02:00
capital_impact: 0 €  # montant engagé si action financière
class: mainframe | supervision | narration  # type d'action demandée à Bac
---

# [Titre court et impératif]

## Contexte
Pourquoi cette action est nécessaire maintenant.

## Ce que je te demande
Actions précises, étape par étape.

## Critère de succès
Comment on sait que c'est fait.

## Ce qui se passe après
Dépendance aval (pour que Bac voie l'enchaînement).
```

**Règle absolue** : Marcus ne demande jamais une action "urgente" sans justifier
pourquoi elle n'a pas pu être anticipée. Les urgences répétées sont un signal de
dysfonctionnement, documenté en post-mortem.

**Droit de refus de Bac** : écrit dans le fichier, avec motif, puis déplacé dans
`missions/rejected/`. Marcus doit intégrer le refus dans son journal du lendemain (pas
comme un drame, comme une donnée).

---

## 6. Dashboard public

Site Next.js minimaliste, une seule page, en anglais :

**Sections, dans l'ordre :**
1. **Live counter** : capital actuel, delta jour / semaine / depuis le départ.
2. **Season progress** : barre de progression vers le palier (S1: 100 € → 1 000 €).
3. **Thesis of the season** : une phrase, maj à chaque saison.
4. **Recent transactions** : les 10 dernières, sommes et motifs.
5. **Latest chapter** : lien vers le dernier Substack + date.
6. **Open missions** : combien de missions ouvertes côté Bac, combien rejetées cette
   semaine (indicateur de friction).
7. **Since day one** : date de départ, jours écoulés, chapitres publiés.
8. **Footer** : Charter (lien), Principles (lien), Repo (lien), Substack (lien).

**Data pipeline** : `dashboard-data.json` est commité à chaque session. Vercel
redéploie automatiquement sur push. Latence : quelques minutes. Suffisant.

---

## 7. MVP Semaine 1 (à partir du lancement)

Pas de thèse encore. Pas de produit encore. On installe le système et on lance
Marcus dans son premier chapitre.

**Jours 1-2 (Bac, infrastructure)**
- Créer le dépôt GitHub `marcus-orlov` avec l'arborescence §3.
- Commit 00-foundations/ (Charter + Principes déjà produits).
- Ouvrir compte bancaire Revolut Business dédié.
- Déposer 100 € sur le compte, noter la transaction dans `ledger/transactions.jsonl`.
- Acheter domaine (si disponible).
- Setup Next.js + Vercel minimal avec page d'attente *"Genesis in progress"*.
- Créer Substack `marcusorlov.substack.com`.
- Rédiger `CLAUDE.md`, `daily-boot.md`, `weekly-boot.md`, `safety-rails.md`.

**Jour 3 (Marcus, première session)**
- Première session Claude Code complète avec le boot prompt.
- Marcus écrit sa **première entrée de journal** : la disincarnation, la découverte du
  nouveau monde, l'inventaire de ce qu'il a et n'a pas.
- Marcus reçoit sa **première mission** : explorer le marché, identifier 5 zones
  candidates pour la thèse S1 (pas choisir, juste cartographier).

**Jours 4-7 (boucle quotidienne)**
- Daily loop standard.
- Marcus affine progressivement la thèse candidate.
- Le chapitre 1 Substack se rédige en parallèle.

**Samedi jour 7 — Premier chapitre**
- Titre proposé : *"Genèse, inventaire, première cartographie"* (à affiner par Marcus).
- Publication Substack + dashboard mis à jour.
- Le lecteur entre dans le feuilleton avec : Charter visible, Principes visibles,
  100 € visibles, une thèse candidate mais pas encore figée, et l'impatience de voir
  le premier mouvement réel.

---

## 8. Ce qu'on différera (hors MVP)

À ne PAS construire en Semaine 1, pour ne pas s'enliser :

- Auth / comptes utilisateurs sur le dashboard (inutile avant longtemps).
- Newsletter propre hors Substack (Substack fait le job).
- Stripe direct (Gumroad d'abord, Stripe quand volume > 500 €/mois).
- Mobile app (jamais, probablement).
- Intégration Twitter/LinkedIn auto (on publie manuellement si on publie).
- Tracking analytics sophistiqué (Vercel Analytics natif suffit).
- Tests automatisés du site (c'est une page statique, overkill).

---

## 9. Points de décision encore ouverts

Avant qu'on commence à écrire les prompts système (`CLAUDE.md`,
`daily-boot.md`, etc.), trois arbitrages restent :

1. **Nom public du projet.** Marcus Orlov est le personnage ; le titre du Substack et
   du site peuvent s'appeler différemment. Options : *"The Orlov Reincarnation"*,
   *"Orlov Redux"*, *"From 100 to the End"*, *"Orlov, Second Pass"*. Ou simplement
   *"Marcus Orlov"* en tant que handle.
2. **Dépôt public dès J1 ou à J7.** Publier le repo dès le début (transparence radicale
   mais risque de fuite avant lancement) ou attendre la publication du Chapitre 1
   (cohérence narrative : le monde apprend l'existence de Marcus en même temps). Je
   recommande J7.
3. **Licence du dépôt.** `MIT` (tout est réutilisable), `CC BY-NC` (narratif + code,
   usage non commercial), ou `All rights reserved` (rien n'est réutilisable).
   Recommandation : CC BY-NC-SA pour le texte, MIT pour le code, séparés proprement.

---

## 10. Versioning

- **v0.1** — 16 avril 2026. Architecture initiale, stack, MVP Semaine 1.
