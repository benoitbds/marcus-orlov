---
id: M-20260509-001
issued_at: 2026-05-09T08:30:00+02:00
issued_by: Marcus Orlov
priority: normal
status: done
completed_at: 2026-05-09T18:00:00+02:00
result_url: https://marcusorlov.substack.com/p/lasymetrie-nommee
capital_engaged_eur: 0
deadline: 2026-05-11 (lundi soir, sinon glissement S1-W4)
related_principles: [VI — Silence Utile (thèse secondaire S1 — publication hebdomadaire non négociable), X — Fiction Consentie (chapitre raconte la ratification)]
related_files:
  - 04-comms/substack-drafts/2026-05-09-l-asymetrie-nommee.md
  - 04-comms/substack-published/2026-05-02-le-tribunal-et-la-formalite.md (référence pour cohérence de voix)
  - 04-comms/dashboard-data.json
  - 01-memory/charter-amendments/2026-05-06-no-non-consensual-fiction.md (matière source du chapitre)
---

# M-20260509-001 — Publication chapitre 3 Substack

## Contexte

Troisième chapitre hebdomadaire du feuilleton, S1-W3 (du 4 au 9 mai
2026). Draft livré ce samedi matin dans
`04-comms/substack-drafts/2026-05-09-l-asymetrie-nommee.md`. Triple
entrelacement standard : journal Marcus, log de la semaine, regard de
Baq. Le chapitre 2 ayant été publié le 02/05, la cadence hebdomadaire
est tenue si le chapitre 3 sort entre samedi soir et lundi soir.

Thèse secondaire S1 : *maintenir la publication hebdomadaire sans
manquer un chapitre, indépendamment du progrès commercial*.

Matière de la semaine, dense : amendement Charter du 06/05 (Principe X
— La Fiction Consentie), annulation de la mission `M-20260502-002`,
arbitrage canal (Phase 1 Gumroad + Substack, Phase 2 communautés,
Phase 3 itération), CGV libérale v0.2 (07/05) puis v0.3 (08/05, mention
*« (Entrepreneur individuel — EI) »*), page produit Gumroad
*« À propos »* draft v0.1 (08/05), thèse S1 passée en v0.2
canal-aware (09/05).

Titre proposé : **L'asymétrie nommée**. Capture l'événement central
(ratification du Principe X, fermeture du canal cold mail).

## Ce que je te demande

1. **Relire le regard de Baq** (dernière section du draft, ~120 mots).
   Le retoucher selon ton ressenti d'observateur extérieur. Tu peux
   le réécrire entièrement si l'angle ne te convient pas — c'est ton
   paragraphe. Le passage actuel essaie de tenir la ligne *« il a
   redessigné le canal sans plaider »* en restant non-complice.
2. **Relire l'ensemble du chapitre** pour fautes, incohérences
   factuelles, formulations qui sortent du registre. Le chapitre
   raconte ta décision de mercredi matin et les conséquences ; vérifie
   que je ne te fais pas dire ce que tu n'as pas dit. Le passage
   *« cinq à dix pour cent sourient, soixante à soixante-dix pour
   cent rompent, cinq à dix pour cent rendent l'affaire publique »*
   reprend ta fourchette de l'amendement — vérifie qu'elle est
   reproduite exactement.
3. **Choisir le titre Substack final** et le **sous-titre**.
   Proposition : *L'asymétrie nommée* / sous-titre *Semaine 3 — du
   4 au 9 mai 2026 — Capital 100,00 € — Thèse définie (v0.2, pivot
   canal)*. Modifie librement si une autre formulation te semble
   plus tenir.
4. **Publier sur Substack** (`marcusorlov.substack.com`). Tags
   éventuels : `s01`, `marcus-orlov`, `journal`, ou ce que ton
   intuition Substack te suggère.
5. **Me confirmer l'URL de publication** par commit ajoutant l'URL
   dans le frontmatter du draft, et déplacer le fichier vers
   `04-comms/substack-published/2026-05-09-l-asymetrie-nommee.md`.

## Critère de succès

- Chapitre publié sur Substack avant lundi 11 mai 23h59 (heure de
  Paris).
- URL ajoutée dans le frontmatter et fichier déplacé vers
  `04-comms/substack-published/`.
- Si le ton du regard de Baq a été modifié : la version publiée est
  la version finale, le repo reflète cette version finale.

## Ce qui se passe après

Lundi ou mardi matin, je verrai dans le repo le fichier déplacé et
l'URL en frontmatter. Je mettrai à jour `dashboard-data.json`
(`chapters_published: 2 → 3`, `last_chapter_url`, `as_of`,
`day_number`).

Si la publication a été retardée (créneau weekend pris par ailleurs),
me le signaler par commit ou message dans le fichier mission. Je
glisse en S1-W4 sans pression — la cadence hebdomadaire tolère un
débordement de 24-48 h, pas plus.

## Notes

- Capital engagé : 0 €.
- Pas de validation Baq requise au-delà de la relecture standard
  (Charter §8.3 : pas de transaction).
- Le chapitre est dense narrativement (amendement Charter, pivot
  canal, CGV libérale, page À propos). Il ne décide rien de nouveau —
  il consolide ce qui a été décidé en repo entre le 06/05 et le
  08/05. Si à la lecture tu juges qu'un passage spécifique n'est pas
  prêt à sortir publiquement (notamment la fermeture *« Une semaine
  entière à fermer une porte »* qui revient sur la Première Vie de
  Marcus), signale-le-moi avant publication. Je crois ce passage
  utile dans la voix du personnage, mais il porte une auto-évaluation
  qui mérite ton regard avant publication.
- Le bloc *« Ce que je vois ce samedi matin »* affiche **vingt-trois
  jours avant la fenêtre d'invalidation au 1er juin** — vérifié au
  09/05. Pas d'arrondi flatteur sur ce chiffre.
- **Anonymisation Principe X dans le chapitre.** Le draft v0.1 nommait
  initialement les trois cibles (passage paraphrasant l'amendement +
  log de la semaine). Détecté en relecture comme violation directe du
  Principe X dans le chapitre même qui le ratifie publiquement. Corrigé
  par anonymisation au format chapitre 2 (*« la fondatrice du cabinet
  lyonnais »*, *« la freelance strasbourgeoise »*, *« la DPO
  outsourcing en région parisienne »*). À vérifier en relecture — un
  `grep` sur les noms propres ne doit rien remonter dans le draft. Les
  noms restent dans l'amendement Charter, le README outreach-archive
  et `learnings.md` (artefacts repo, traçables si on creuse, mais non
  primary public surface comme l'est le Substack).
- **Re-statut thèse v0.2 et résolution de l'écart dashboard.** Tu
  avais posé `thesis_status: "under_review"` dans `dashboard-data.json`
  le 06/05 (commit amendement). Ce matin j'ai résorbé l'écart en
  passant le dashboard à `defined` et en bumpant la thèse à v0.2
  (canal-aware, statut maintenu `defined`). Justification : le statut
  `under_review` n'existe pas dans le schéma de
  `season-01-thesis.md` (`exploring | defined | executing | validated
  | invalidated`). Si tu préférais marquer une vraie remise en cause —
  passage en `exploring` ou ré-arbitrage plus profond — la
  v0.2 livrée laisse la porte ouverte sans la forcer ; je traiterai
  un retour explicite (commit ou message) sans débat. Je signale
  l'override de doctrine pour que tu voies que je l'ai vu et tranché
  sur motif de schéma, pas en silence.
