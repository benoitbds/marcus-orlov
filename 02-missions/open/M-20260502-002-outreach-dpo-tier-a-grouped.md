---
id: M-20260502-002
issued_at: 2026-05-02T08:55:00+02:00
issued_by: Marcus Orlov
priority: normal
status: open
capital_engaged_eur: 0
deadline: 2026-05-05 (mardi soir au plus tard, sinon glissement S1-W3 trop visible)
related_principles:
  - II — Maillon Invisible (canal DPO niche, pas saturé)
  - V — Main Froide (envoi sans annonce, pas de fanfare)
  - VIII — Dette Honorée (engagement à livrer le kit dès qu'une réponse positive arrive)
related_rails:
  - Charter §8.2 (produits numériques ≤ 30 % capital en coûts de lancement) — respecté, zéro upfront
  - safety-rails §5 (surfaces dédiées au projet) — channel mail SoBaq + page LinkedIn entité
related_files:
  - 04-comms/outreach-drafts/2026-04-28-laetitia-schmuck-v1.md
  - 04-comms/outreach-drafts/2026-04-29-sandrine-thyrault-v1.md
  - 04-comms/outreach-drafts/2026-04-30-celine-petit-v1.md
  - 05-products/gdpr-starter-kit/dpa/dpa-fr.md
  - 05-products/gdpr-starter-kit/register/register-fr.md
  - 05-products/gdpr-starter-kit/privacy-policy/privacy-fr.md
  - 05-products/gdpr-starter-kit/transfers-note/transfers-note.md
  - 05-products/gdpr-starter-kit/playbook/playbook-fr.md
  - 05-products/gdpr-starter-kit/package/README-customer-fr.md
  - 05-products/gdpr-starter-kit/package/DISCLAIMER-fr.md
  - 05-products/gdpr-starter-kit/package/COVER-fr.md
---

# M-20260502-002 — Outreach DPO Tier A groupé (packaging + envoi)

## Contexte

Six verrous outreach levés en S1-W2 (SIRET définitif 10437881500013,
email channel SoBaq en réception et émission send-as, page LinkedIn
entité créée, pourcentage d'affiliation 30 % figé, packaging du kit
préparé, fraîcheur des trois profils LinkedIn vérifiée). Les trois
drafts sont à v0.4 / v0.4 / v0.3, prêts à partir, identifications
SoBaq complètes (SIRET + APE 5814Z), signatures doubles, mécanique
financière commune, premier engagement minimal de 30 minutes sur le
seul playbook.

Cette mission groupe **trois actions techniques en une seule passe
d'exécution humaine** pour respecter le rythme mainframe (ne pas
fragmenter en trois missions séparées qui consommeraient trois
créneaux daily).

Le bilan interne S1-W2
(`01-memory/internal/2026-W18-weekly-reflection.md`) nomme
explicitement le pattern de report observé sur la semaine. Émettre
cette mission ce samedi est le geste qui rompt le pattern.

## Ce que je te demande

### Étape 1 — Packaging et upload

1. Créer un dossier `GDPR-Starter-Kit-FR-v0/` localement.
2. Copier dedans les huit fichiers suivants :
   - `05-products/gdpr-starter-kit/package/COVER-fr.md`
   - `05-products/gdpr-starter-kit/package/README-customer-fr.md`
   - `05-products/gdpr-starter-kit/package/DISCLAIMER-fr.md`
   - `05-products/gdpr-starter-kit/dpa/dpa-fr.md`
   - `05-products/gdpr-starter-kit/register/register-fr.md`
   - `05-products/gdpr-starter-kit/privacy-policy/privacy-fr.md`
   - `05-products/gdpr-starter-kit/transfers-note/transfers-note.md`
   - `05-products/gdpr-starter-kit/playbook/playbook-fr.md`
3. Compresser le dossier en `GDPR-Starter-Kit-FR-v0.zip`.
4. Uploader le ZIP dans le Drive folder existant
   (`https://drive.google.com/drive/folders/1dzuN7Hg_BFVBQ68NcUG44k3UzNUmOjAg`).
5. Garder les permissions du dossier en *« Toute personne avec le
   lien »*. Le partage est en lecture seule, suffisant pour
   l'usage de découverte d'une DPO certifiée.

### Étape 2 — Envoi des trois mails

Pour chacun des trois variants (Laetitia / Sandrine / Céline) :

1. Composer un mail depuis Gmail en mode *« Envoyer en tant que
   `contact@sobaq.fr` »* (send-as configuré 30/04, commit
   `a33207e`).
2. Copier-coller le **corps du mail** depuis la section
   `## Texte du message` du fichier variant correspondant. Le sujet
   est inclus dans la même section.
3. Adresser le mail à l'adresse mail **professionnelle publiée**
   de chaque cible. Les profils LinkedIn ne contiennent pas toujours
   l'adresse mail directement — la trouver via :
   - Pour **Laetitia Schmuck** : aucun site cabinet propre repéré
     dans la recherche du 02/05. Sa page LinkedIn ne semble pas
     publier de mail direct. **Important** : ne pas utiliser une
     adresse récupérée via un service de scraping type ContactOut
     ou similaire (cf. recherche du 02/05 qui a fait remonter
     `laetitiaschmuck@gmail.com` depuis ContactOut). Cette
     adresse n'est pas une adresse publiée par elle, l'utiliser
     en cold mail tomberait dans la zone grise de
     `safety-rails.md §3` (spam / contact non-consenti). Si pas
     de mail public disponible, refus partiel acceptable pour
     cette cible — on bascule en daily lundi, j'arbitre soit un
     contact via DM LinkedIn (qui change la nature du canal et
     mérite que je rééveille), soit le passage à un Tier A
     alternatif.
   - Pour **Sandrine Thyrault** : son site personnel ou
     coordonnées affichées sur LinkedIn / Malt. Si introuvable,
     même règle : refus partiel, j'arbitre.
   - Pour **Céline Petit** : `dataneedadvice.com/contact` ou
     coordonnées professionnelles affichées en page « À propos »
     du cabinet. Cabinet a une présence web établie, mail
     professionnel public probable.
   Si tu ne trouves pas une adresse mail publiée pour une cible,
   contacte-moi en commentant la mission — je n'ai pas de canal
   alternatif propre, et je préfère qu'on en discute avant
   d'envoyer un message LinkedIn (qui change la nature du
   canal) ou de basculer sur un autre profil.
4. **Ajouter en pied de mail**, juste avant la signature, une
   ligne du type : *« Lien d'accès au kit (lecture, durée de
   partage non limitée pour l'instant) :
   https://drive.google.com/drive/folders/1dzuN...
   — l'archive `GDPR-Starter-Kit-FR-v0.zip` est dans le
   dossier. »*.
   Si tu juges que la formulation peut être améliorée, fais-le.
   L'objectif est que la DPO clique et puisse parcourir le kit
   sans avoir à demander un mail de relance.
5. Envoyer les trois mails dans la même session.

### Étape 3 — Consignation

1. Pour chaque variant envoyé, mettre à jour le frontmatter du
   fichier draft :
   - `status: sent v0.4` (ou v0.3 pour Céline)
   - `sent_at: <ISO 8601 timestamp>`
   - `sent_by: Baq`
2. Déplacer chaque fichier de `04-comms/outreach-drafts/` vers
   `04-comms/outreach-sent/` (créer le dossier si absent).
3. Commit unique avec message clair :
   `outreach: 3 propositions DPO Tier A envoyées (Schmuck,
   Thyrault, Petit) depuis contact@sobaq.fr`.

## Critère de succès

- Trois mails envoyés depuis `contact@sobaq.fr` (send-as Gmail
  authentifié), aux trois cibles respectives, avec le lien Drive
  vers le ZIP du kit.
- Les trois fichiers variants déplacés vers
  `04-comms/outreach-sent/` avec frontmatter à jour.
- Un seul commit récapitulatif côté repo.

Idéalement avant lundi 4 mai 18h00 — pour que les trois mails
arrivent en début de semaine ouvrée côté DPO et non noyés dans
une boîte de retour de week-end.

## Ce qui se passe après

J'ouvre la phase de **réception**, qui est inhabituelle pour moi
puisque je n'ai pas de boîte mail directe. Tu reçois les
réponses sur la redirection `contact@sobaq.fr` →
`benoit.bds@gmail.com`. Quand une réponse arrive :

- **Si réponse positive** : me la signaler par commit dans
  `01-memory/journal/` ou message direct (selon ton timing).
  Je rédigerai le mail de suite (cadrage de la lecture transverse,
  envoi du lien d'affiliation tracké, conditions). Tu seras
  re-missionné pour l'envoi de la réponse.
- **Si réponse négative ou absence de réponse à J+10** : on
  rouvre la question en daily ou weekend session — variant 4 sur
  un nouveau profil Tier A, ou bascule vers Tier B, à arbitrer à
  ce moment-là.

Pas de relance automatique. Une seule sollicitation par cible
sur ce canal.

## Garde-fous et refus possibles

Tu peux refuser tout ou partie de cette mission si :

- Une adresse mail valide pour une cible est introuvable et le
  remplacement d'un mail par un message LinkedIn te paraît
  changer la nature du canal d'une façon qui mérite arbitrage
  Marcus → refus partiel acceptable, on bascule la cible non
  contactable en daily semaine prochaine.
- Le packaging révèle une erreur grossière dans un des cinq
  documents du kit (placeholder oublié, formulation cassée,
  fichier manquant) → refus partiel acceptable, je corrige avant
  envoi groupé.
- Tu juges que l'un des trois textes a une formulation
  malheureuse à la dernière relecture → refus partiel acceptable,
  retour pour itération.
- La fenêtre weekend est saturée par autre chose → glissement
  d'une journée acceptable, mais pas plus de mardi soir.

Charge horaire estimée : 60-90 minutes (packaging + upload Drive
+ trois mails composés et envoyés + consignation + commit).
Dans le contrat hebdomadaire (Charter §7).

## Notes

- Capital engagé : 0 €. Aucune validation Bac requise au titre
  de §8.3.
- Aucune annonce publique de l'envoi (Principe V — pas de
  bruit avant consolidation). Pas de mention dans le chapitre 2
  qui est en cours de publication parallèle (M-20260502-001).
  Le chapitre 3 racontera ce qui aura été reçu — réponses
  positives, négatives, ou absence — pas ce qui est espéré.
- Si une DPO te répond directement et que tu peux livrer le
  retour avant que je ne te re-missionne, ne réponds pas pour
  moi — laisse-moi formuler la suite de l'échange. La voix
  doit rester cohérente avec le draft initial (Marcus Orlov —
  pour SoBaq).
