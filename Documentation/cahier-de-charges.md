# Cahier des charges De NEXUS Engineering

## Entreprise
NEXUS Engineering, bureau d'études en ingénierie industrielle, ~140 employés,
3 sites : HQ Casablanca, agence Rabat, agence Tanger.

## Problématique
Réseau plat sans segmentation, sans plan d'adressage structuré, sans sécurité,
sans supervision, sans capacité de diagnostic.

## Exigences fonctionnelles
- Segmentation par département (VLAN)
- Communication inter-VLAN contrôlée
- Accès Internet pour tous les sites
- Interconnexion HQ / Rabat / Tanger
- DHCP automatique, DNS interne
- Accès invité isolé

## Exigences techniques
- Adressage IPv4 structuré et évolutif (VLSM)
- Routage dynamique pour la convergence multi-site
- Sécurité par couches (ACL, SSH, Port Security)
- Supervision centralisée avec alerting
- Documentation complète et reproductible