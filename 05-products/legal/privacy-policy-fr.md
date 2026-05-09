---
file: 05-products/legal/privacy-policy-fr.md
purpose: Politique de confidentialité SoBaq publique (boutique Gumroad + Substack).
target: page tierce hébergée (URL à arbitrer en S1-W4 — sous-page Substack ou hébergement statique).
status: amorce v0.0 — squelette livré 09/05, finalisation S1-W4 (lundi 11 ou mardi 12/05).
date: 2026-05-09
author: Marcus
related:
  - 05-products/legal/cgv-fr.md (article 13 — placeholder URL politique de confidentialité)
  - 04-comms/gumroad/about-page-fr.md (renvoi indirect via § Identification du Vendeur)
references:
  - RGPD (UE 2016/679), articles 13 et 14 — informations à fournir à la personne concernée
  - CNIL, délibération 2019-093 du 4 juillet 2019 — recommandation cookies et autres traceurs
  - AFCDP — modèle de politique de confidentialité pour e-commerce (consulté pour structure)
  - Code de la consommation, article L. 111-1 — informations précontractuelles obligatoires
---

# Politique de confidentialité SoBaq

> **Amorce v0.0 — 9 mai 2026.** Squelette de structure, sections
> nommées, périmètre borné. À étoffer en S1-W4 (lundi 11/05 ou
> mardi 12/05) pour livraison v0.1 prête à hébergement et liaison
> dans CGV article 13. Le périmètre est *étroit* — l'acheteur visé
> est l'utilisateur de la boutique Gumroad SoBaq qui télécharge le
> kit RGPD. Pas de finalité marketing, pas de profilage, pas de
> publicité ciblée, pas de revente à tiers. La simplicité du
> traitement est le filtre principal de rédaction.

## Sections à rédiger

### 1. Identité du Responsable de traitement
- Identification SoBaq alignée sur CGV article 1 et page À propos
  (titulaire, EI, siège, SIRET, APE, RNE, contact).
- Pas de DPO désigné (seuils RGPD article 37 non atteints — < 250
  salariés, traitement non systématique à grande échelle, pas de
  catégories particulières). Mention explicite de cette absence
  motivée.

### 2. Données collectées et finalités
*Périmètre étroit — trois sources de données seulement.*
- **Données d'achat** (collectées par Gumroad en tant que
  responsable conjoint / sous-traitant selon ses CGU) : email,
  nom de facturation, pays, métadonnées de paiement (jamais
  numéro complet de carte — Gumroad agit comme MoR).
- **Données de support** (collectées par SoBaq directement sur
  `contact@sobaq.fr`) : email, contenu de la demande, fil de
  réponse.
- **Données techniques de téléchargement** (logs Gumroad
  standards) : adresse IP de téléchargement, horodatage, agent
  utilisateur. Conservation limitée par Gumroad selon ses
  propres règles.
- **Aucune** donnée de navigation collectée par SoBaq sur la page
  Substack (Substack porte ses propres traceurs, déclarés dans
  *sa* politique de confidentialité). À mentionner explicitement
  pour neutraliser le doute.

### 3. Bases légales de traitement (RGPD art. 6)
- Achat et livraison du kit : exécution du contrat (art. 6.1.b).
- Réponse aux demandes de support : exécution du contrat
  (art. 6.1.b) ou intérêt légitime (art. 6.1.f) selon contexte.
- Notifications de mises à jour pendant la garantie d'un an :
  obligation légale (art. 6.1.c — L. 224-25-12 Code conso).
- Comptabilité, conservation des factures : obligation légale
  (art. 6.1.c — L. 123-22 Code de commerce).

### 4. Durées de conservation
- Données d'achat (facturation, comptabilité) : **10 ans**
  conformément au Code de commerce.
- Données de support (fils mail) : **3 ans** après dernière
  interaction, sauf demande de suppression antérieure.
- Données techniques de téléchargement : selon politique
  Gumroad (à référencer, ne pas re-déclarer).
- Logs de mise à jour : durée de la garantie + 1 an
  (L. 224-25-12).

### 5. Destinataires des données
- **SoBaq** (responsable de traitement, accès interne unique :
  Baq titulaire).
- **Gumroad** (sous-traitant pour la transaction et MoR) — DPA
  Gumroad publié sur leur site, à référencer.
- **OVH** (sous-traitant pour l'hébergement email
  `contact@sobaq.fr`) — DPA OVH publié, à référencer.
- **Pas de transfert hors UE** par SoBaq directement. Gumroad
  étant US, cf. mention SCC dans la note transferts du kit
  (cohérence du discours — ce que SoBaq vend dans son kit, SoBaq
  l'applique).

### 6. Droits des personnes (RGPD art. 15-22)
- Droit d'accès, de rectification, d'effacement, de limitation,
  de portabilité, d'opposition.
- Modalités d'exercice : mail à `contact@sobaq.fr` avec mention
  *« Demande RGPD »* en objet.
- Délai de réponse SoBaq : ≤ 1 mois (art. 12.3 RGPD).
- Réclamation auprès de la CNIL : URL et adresse à renseigner
  (cnil.fr, formulaire de plainte en ligne).

### 7. Cookies et traceurs
- **Aucun cookie déposé par SoBaq directement.** SoBaq n'a pas
  de site propriétaire à ce stade — la page produit est sur
  Gumroad, le feuilleton est sur Substack, l'API contact est
  via le canal mail OVH.
- Cookies déposés par Gumroad : voir politique de
  confidentialité Gumroad.
- Cookies déposés par Substack : voir politique de
  confidentialité Substack.
- Cohérence avec CNIL délibération 2019-093 : SoBaq ne dépose
  pas, donc pas de bandeau de consentement à porter côté
  SoBaq.

### 8. Sécurité
- Mention courte et factuelle. Pas de revendication
  disproportionnée pour une micro-entreprise (Principe IX
  appliqué : pas d'invention).
- Hébergement OVH (contact mail), Gumroad (transaction et
  livraison), Substack (publication). Sous-traitants choisis
  pour leur conformité documentée. Aucune base de données
  propriétaire SoBaq.

### 9. Modifications
- Modalités de mise à jour de la politique. Notification par
  mail uniquement aux clients ayant acheté dans la dernière
  année (cohérent avec la garantie d'un an).

### 10. Contact et réclamations
- `contact@sobaq.fr`.
- Adresse postale du siège (cohérence CGV).
- CNIL pour les réclamations.

---

## Notes de rédaction (à supprimer en v0.1)

- **Périmètre étroit volontairement.** Une politique courte et
  honnête est plus défendable qu'une politique longue qui
  copie-colle des modèles. Cible : 150-250 lignes en
  v0.1 finale.
- **Cohérence avec le kit vendu.** SoBaq vend des modèles RGPD
  pour SaaS. La politique de SoBaq elle-même doit être
  exemplaire de ce qu'elle promet — sinon le kit est
  auto-disqualifié. Principe que la mention *« la cohérence
  interne du livrable est aussi un argument de vente »* du
  daily 08/05 anticipe.
- **Renvoi vs re-déclaration.** Pour Gumroad, OVH, Substack,
  le bon pattern est *« voir leur propre politique »* — ne pas
  re-déclarer ce que les sous-traitants déclarent eux-mêmes.
  Évite les contradictions et marque la responsabilité.
- **Pas de DPO.** Le seuil RGPD article 37 n'est pas atteint
  (entreprise individuelle, pas de traitement à grande
  échelle, pas de catégories particulières). Mention explicite
  motivée plutôt que silence.
- **Article L. 224-25-12.** La garantie d'un an annoncée dans la
  page À propos et les CGV est cohérente avec l'obligation
  légale issue de la directive (UE) 2019/770 transposée en droit
  français — mises à jour pendant la durée raisonnablement
  attendue, jamais inférieure à un an.
