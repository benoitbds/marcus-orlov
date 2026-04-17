# GDPR Starter Kit — Outline v0

> Working outline for the first kit. Updated as sections are drafted or
> refined.

---

## 1. DPA template (bilingual FR / EN)

Structure (11 sections) :

1. **Objet et définitions** — reprise RGPD art. 4, scope du traitement.
2. **Description du traitement** — catégories de personnes, de données,
   finalités, durée.
3. **Obligations du sous-traitant** — confidentialité, formation, tenue d'un
   registre propre, assistance au contrôleur.
4. **Sécurité des traitements** — mesures techniques et organisationnelles
   minimales (chiffrement, contrôle d'accès, logs, backups, gestion des
   incidents).
5. **Sous-traitants ultérieurs** — clause d'autorisation générale + liste
   initiale + procédure d'opposition.
6. **Transferts internationaux** — référence aux SCC, adequacy decisions,
   TIAs (Transfer Impact Assessments) en annexe.
7. **Droits des personnes concernées** — comment le sous-traitant assiste
   le contrôleur sur les demandes (accès, rectification, effacement,
   portabilité, opposition).
8. **Violations de données** — délai de notification (72h art. 33 RGPD),
   contenu de la notification, coordination.
9. **Audits** — droit d'audit du contrôleur, conditions, coûts.
10. **Restitution et suppression** — à la fin du contrat, options de
    restitution ou suppression, délai.
11. **Responsabilité, durée, droit applicable** — limitation, durée alignée
    sur le contrat principal, droit applicable (FR / EU).

Annexes :
- **Annexe 1** : description détaillée du traitement.
- **Annexe 2** : mesures de sécurité.
- **Annexe 3** : liste des sous-traitants ultérieurs autorisés.
- **Annexe 4** : SCC Module 2 (controller → processor) quand transfert
  international applicable.

Livrables : `dpa/dpa-fr.md`, `dpa/dpa-en.md`, exports `.docx`.

## 2. Registre de traitements (Article 30)

Traitements pré-remplis (standards SaaS) :

1. Gestion des comptes clients.
2. Facturation et recouvrement.
3. Support client (tickets, chat).
4. Analytics produit (usage, sessions).
5. Marketing (newsletter, CRM).
6. Recrutement (candidatures).
7. Gestion RH (salariés).
8. Monitoring technique (logs, APM).

Pour chaque traitement, colonnes :
- Finalité
- Base légale (art. 6 RGPD)
- Catégories de personnes
- Catégories de données
- Destinataires
- Transferts hors UE
- Durée de conservation
- Mesures de sécurité

Livrables : `register/register-fr.md`, `register/register-en.md`, export
`.xlsx`.

## 3. Politique de confidentialité publique

Structure standard :

1. Qui nous sommes (éditeur, contact DPO si applicable).
2. Données collectées et finalités.
3. Base légale de chaque traitement.
4. Durée de conservation.
5. Destinataires et sous-traitants ultérieurs (liste à jour).
6. Transferts internationaux.
7. Droits des personnes concernées (+ modalité d'exercice).
8. Cookies et traceurs (si applicable — renvoi possible vers bannière
   dédiée).
9. Contact et réclamation (CNIL).
10. Modifications de la politique.

Livrables : `privacy-policy/privacy-fr.md`, `privacy-policy/privacy-en.md`,
renders HTML minimalistes.

## 4. Note sur les transferts internationaux

Brief de 2-3 pages couvrant :

- Les quatre modules SCC (2021/914).
- Les principales décisions d'adéquation en vigueur (UK, Suisse, Japon,
  Corée du Sud, etc.) — date et limites.
- Les cas d'école sous-traitants courants chez une SaaS EU : AWS (régions
  EU vs US, CLOUD Act), Google Cloud, OpenAI (DPA OpenAI, zéro data
  retention option), Stripe, Intercom, Sentry.
- TIA (Transfer Impact Assessment) : modèle minimal.

Livrable : `transfers-note/transfers-note.md` + export PDF.

## 5. Playbook de négociation

6-8 pages. Structure :

1. **Comment adapter le kit en 45 minutes** — checklist pas à pas.
2. **Les 5-8 clauses que les clients poussent le plus souvent** :
   - Délai de notification de violation (< 72h).
   - Audit sur site vs audit documentaire.
   - Clause d'indemnisation illimitée.
   - Suppression vs restitution des données.
   - Engagement à ne pas utiliser de sous-traitants hors EU.
   - Chiffrement at-rest obligatoire partout.
   - Pen-test annuel communiqué.
3. **Ce qu'il faut défendre ; ce qu'il est normal de concéder.**
4. **Signaux d'alerte** : demandes du client qui doivent déclencher une
   consultation juridique (données de santé, scoring, profilage
   automatisé, mineurs, etc.).
5. **Ce qui ne relève pas du DPA** mais du contrat principal (SLA, prix,
   résiliation) — rappel pour ne pas mélanger.

Livrable : `playbook/playbook.md` + export PDF.

## 6. Packaging

- `README.md` client-facing placé à la racine du ZIP.
- `DISCLAIMER.md` en première position de lecture.
- Organisation en sous-dossiers (dpa/, register/, privacy-policy/, etc.).
- Archive ZIP générée à la main pour v0, automatisée ensuite si le
  produit vit.

---

## Work breakdown — v0 production (2026-04-17 → 2026-04-18)

**Friday 2026-04-17 (today) :**
- [x] Outline + product spec.
- [ ] DPA FR — sections 1 à 4 (v0 draft).
- [ ] Registre FR — traitements 1 à 4 pré-remplis.

**Saturday 2026-04-18 (weekend session) :**
- [ ] DPA FR — sections 5 à 11 + annexes.
- [ ] Registre FR — traitements 5 à 8.
- [ ] Politique de confidentialité FR.
- [ ] Note SCC courte.
- [ ] Playbook 6-8 pages.
- [ ] Traductions EN (DPA + privacy policy) — v0 acceptée, polished plus tard.
- [ ] Packaging ZIP + README client + DISCLAIMER.
- [ ] CGV draft soumis à Bac.
- [ ] Décision Gumroad opening : go / hold.
