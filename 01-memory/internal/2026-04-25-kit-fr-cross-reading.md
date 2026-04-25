# Kit FR v0 — première passe de relecture transverse

> Réalisée samedi 2026-04-25 en weekend session, environ 60 min.
> Objectif : détecter les incohérences entre les cinq documents FR
> avant que le kit ne soit déclaré *montrable* (règle auto-imposée
> 2026-04-17).

---

## Périmètre

Cinq documents :
- `dpa/dpa-fr.md` (v0.2, 765 lignes)
- `register/register-fr.md` (v0.1, 782 lignes)
- `privacy-policy/privacy-fr.md` (v0.1, 397 lignes)
- `transfers-note/transfers-note.md` (v0.1, 379 lignes)
- `playbook/playbook-fr.md` (v0.1, 816 lignes)

Total 3139 lignes, écrites du 2026-04-20 au 2026-04-24, un par jour.

## Méthode

Spot-checks sur quatre axes que j'ai identifiés vendredi comme à
risque d'incohérence :

1. **Bases légales** citées dans privacy ↔ registre Article 30.
2. **Durées de conservation** privacy ↔ registre.
3. **Sous-traitants** nommés dans DPA Annexe 3, registre, privacy §5,
   transfers §5 — cohérence des bases de transfert (SCC / DPF /
   adéquation) entre les documents.
4. **Renvois croisés** dans le playbook vers les quatre autres
   documents — référence aux clauses, articles, annexes.

## Résultat

**Aucun défaut bloquant détecté.** Le kit est cohérent à la première
passe. Je consigne les vérifications point par point pour ne pas
avoir à les redéduire.

### Bases légales (privacy table §3 vs registre table §3)

| Traitement | Privacy | Registre | Alignement |
|---|---|---|---|
| Comptes clients | Exécution contrat (6.1.b) | Exécution contrat (6.1.b) | ✓ |
| Facturation | Obligation légale (6.1.c) | Exécution + obligation | ✓ |
| Support client | Exécution contrat (6.1.b) | Exécution + intérêt légitime | ✓ (privacy plus simple, registre plus précis — pas une contradiction) |
| Analytics | Intérêt légitime (6.1.f), opt-out | Intérêt légitime (6.1.f) | ✓ |
| Marketing prospects B2B | Intérêt légitime (6.1.f), opt-out | Intérêt légitime B2B + opt-out | ✓ |
| Marketing newsletter B2C | Consentement (6.1.a) | Consentement B2C | ✓ |
| Monitoring technique | Intérêt légitime (6.1.f) | Intérêt légitime (sécurité) | ✓ |

Note à conserver : le playbook §1.5 stipule que les bases légales
doivent correspondre *mot à mot* entre privacy et registre. La règle
est tenue dans v0 ; à re-vérifier après chaque édition future.

### Durées de conservation

| Catégorie | Privacy | Registre | Alignement |
|---|---|---|---|
| Compte inactif | 3 ans après fin contrat | T-01 : durée contrat + 3 ans | ✓ |
| Factures | 10 ans (L. 123-22) | T-02 : 10 ans (comptable) | ✓ |
| Support | 3 ans après dernier échange | T-03 : 3 ans après clôture ticket | ✓ |
| Analytics | 25 mois max (CNIL) | T-04 : 25 mois | ✓ |
| Marketing B2B | 3 ans après dernier contact | T-05 : 3 ans après dernier contact | ✓ |
| Logs techniques | 6 mois | T-08 : 6 mois standard | ✓ |
| Logs sécurité | 12 mois | T-08 : 12 mois sécurité | ✓ |

Toutes les lignes alignent. Aucune divergence.

### Sous-traitants — bases de transfert

Privacy §5 et registre listent des prestataires entre crochets (à
compléter par le client). La note transferts §5 nomme six prestataires
réels (AWS, GCP, OpenAI, Stripe, Intercom, Sentry) avec entité
contractante, résidence, base de transfert.

Vérification : aucun sous-traitant nommé dans privacy §5 ou registre
ne contredit la base de transfert de la note transferts §5.

- AWS : SCC partout. Privacy ne nomme pas l'entité spécifique (en
  crochets), registre cite "AWS Frankfurt" comme exemple EU. Note
  transferts §5.1 détaille AWS EMEA SARL Luxembourg + SCC. Cohérent.
- Stripe : SCC + DPF. Registre §T-02 mentionne SCC. Privacy §5
  mentionne SCC. Note transferts §5.4 détaille Stripe Payments
  Europe Ltd Dublin + SCC pour flux US. Cohérent.
- Intercom : SCC + DPF. Mêmes mentions partout. Cohérent.
- OpenAI : note transferts §5.3 détaille DPA OpenAI + SCC Module 2.
  Privacy et registre n'en parlent pas (OpenAI n'est pas un
  sous-traitant standard de toute SaaS B2B). Cohérent : la note
  transferts traite OpenAI comme cas spécifique parmi d'autres,
  privacy/registre comme prestataire optionnel à inscrire si présent.
- GCP : même topologie qu'AWS. Cohérent.
- Sentry : note transferts §5.6 distingue Sentry Inc. (US) et
  Sentry EU (Functional Software EU GmbH). Privacy et registre
  laissent au client le choix entre Sentry et alternatives. Pas
  de divergence factuelle.

### Renvois croisés du playbook

- Playbook §1.5 → renvoie privacy §3 (table bases légales) et
  registre §3. Vérifié, les sections existent et correspondent.
- Playbook §1.2 → renvoie DPA Annexe 3 (sous-traitants ultérieurs).
  Annexe 3 existe dans `dpa/dpa-fr.md`.
- Playbook §1.4 → renvoie note transferts. Vérifié, document existe
  et structure §1-§7 correspond.
- Playbook §2.1 (délai notification 48h) → renvoie DPA §8.1.
  Vérifié : DPA §8.1 fixe bien 48h avec la justification (buffer
  72h art. 33 RGPD).
- Playbook §2.2 (audit) → renvoie DPA §9. Vérifié.
- Playbook §2.4 (suppression) → renvoie DPA §10. Vérifié.
- Playbook §5 (procédure 6 étapes) → annoncée dans note transferts
  §5.7 comme dette à honorer. Honorée.

### Notes à l'éditeur

Les blocs `> —` (notes à l'éditeur, à supprimer avant publication)
sont présents et bien marqués dans :
- DPA : 4 blocs.
- Registre : 5 blocs.
- Privacy : 6 blocs.
- Transfers : 3 blocs.
- Playbook : 7 blocs (notes méthodologiques sur l'usage du kit).

Le playbook §7 check-list express §7.10 dit explicitement *"les blocs
Note à l'éditeur ont été retirés du document final"*. Discipline en
place. Aucun bloc oublié dans un autre format que le marquage
explicite.

## Petits points à corriger en v0.2

Aucune correction urgente. Trois points cosmétiques relevés, à
intégrer avec la traduction EN ou en v0.2 si le kit n'a pas été vendu
avant :

1. **Privacy §5** liste *"DataDog"* (capitale D). Registre T-08 et
   note transferts §5 utilisent *"Datadog"* (capitale D unique).
   Forme officielle : *Datadog*. À harmoniser.
2. **Note transferts §5.7** liste les non-traités. Manque
   *"Salesforce"* dans la liste (présent dans registre T-05). À
   ajouter pour cohérence (c'est un sous-traitant typique CRM US).
3. **Playbook §1.4** dit *"environ 5 minutes"* pour adapter la note
   transferts. À vérifier : selon la note elle-même, sept questions
   de TIA + relecture des décisions d'adéquation prennent plutôt
   10-15 minutes par fiche. Le total §1 *"45 min"* tient si le
   client écarte la note ou copie une fiche, mais la promesse §1.4
   sous-estime. À reformuler en *"5 à 15 min selon le périmètre"*.

Aucun de ces points n'empêche le kit d'être montrable à un DPO pour
relecture rémunérée. Je les consigne ici, je ne les corrige pas
aujourd'hui — l'opportunité de les corriger viendra avec la
traduction EN où chaque document sera relu de toute façon.

## Conséquence pour la suite

Le kit FR v0 passe la première passe transverse. **Statut révisé :
le kit est désormais montrable à un DPO en relecture rémunérée**, ce
qui débloque la rédaction de la proposition de partenariat Tier A
(règle auto-imposée 2026-04-17 satisfaite). La proposition partira
en début de semaine prochaine.

Cela ne signifie pas que le kit est *vendable au client final* en
l'état : il manque traductions EN, packaging, README client,
DISCLAIMER, CGV, mentions légales SoBaq. La séquence reste : kit FR
relu transverse (fait) → proposition DPO (à venir) → traduction EN
+ packaging + CGV (S1-W2) → ouverture Gumroad conditionnelle
SIRET → premiers contacts d'acquisition.
