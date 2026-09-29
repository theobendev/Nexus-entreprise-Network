# Cahier des charges — NEXUS Engineering

## Entreprise

**NEXUS Engineering** est un bureau d'études en ingénierie industrielle
(mécanique, électronique, logiciel embarqué), basé sur **un site unique**
à Casablanca. L'entreprise compte environ **140 employés**, répartis dans
plusieurs départements, avec une clientèle qui nécessite un support
technique réactif.

## Organisation interne (départements)

| Département | Effectif approx. | Rôle |
|---|---|---|
| Direction | ~10 | Pilotage stratégique |
| RH | ~10 | Gestion du personnel |
| Finance | ~10 | Comptabilité, paie, facturation |
| R&D / Ingénierie | ~50 | Conception, CAO, développement |
| Commercial | ~20 | Vente, relation client |
| Support Technique | ~15 | Maintenance, SAV, assistance client |
| Invités | variable | Visiteurs, partenaires, clients en réunion |

## Problématique

Le réseau actuel est plat, sans segmentation par département, sans plan
d'adressage structuré, sans sécurité ni supervision. Avec la croissance
de l'entreprise et la diversité des services (données confidentielles en
R&D, données sensibles en Finance/RH, accès visiteurs fréquents), cette
situation devient un risque opérationnel et sécuritaire.

## Exigences fonctionnelles

- Segmentation logique par département (VLAN)
- Communication inter-département contrôlée
- Accès Internet pour l'ensemble du site
- Attribution automatique des adresses IP (DHCP)
- Accès invité isolé du reste du réseau
- Prise en charge d'équipements variés (postes fixes, laptops,
  imprimantes, point d'accès Wi-Fi)
- Architecture organisée en zones logiques (administrative / technique)
  pour refléter l'organisation réelle de l'entreprise

## Exigences techniques

- Adressage IPv4 structuré et évolutif (VLSM)
- Architecture réseau hiérarchique à 3 couches : **Core**, **Distribution**,
  **Access** — pour une infrastructure robuste et évolutive
- Redondance et évolutivité pour accompagner la croissance de l'entreprise
  (ouverture possible d'un second site à moyen terme)
- Sécurité par couches (ACL, SSH, Port Security) — *prévu en V4*
- Supervision centralisée avec alerting — *prévu en V5*
- Documentation complète et reproductible

## Évolutions futures envisagées

NEXUS prévoit une possible ouverture d'un second site dans les 12 à 18
mois. L'architecture actuelle est conçue pour permettre l'ajout ultérieur
d'une interconnexion multi-site (routage dynamique OSPF), sans remise en
cause de l'organisation actuelle.