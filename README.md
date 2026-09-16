# NEXUS Engineering — Enterprise Network Infrastructure Project

Projet réseau fil rouge : conception, déploiement, sécurisation, supervision et
diagnostic d'une infrastructure réseau d'entreprise évolutive — du niveau
CCNA-1 jusqu'aux technologies avancées (OSPF, ACL, supervision, automatisation).

## Le scénario

**NEXUS Engineering** est une entreprise fictive de conseil et d'ingénierie
industrielle (~140 employés, 3 sites : Casablanca, Rabat, Tanger). Le réseau
actuel est plat, sans segmentation, sans sécurité ni supervision. Ce projet
construit progressivement l'infrastructure qui résout ces problèmes,
département par département, version par version.

## Où en est le projet

| Version | Contenu | Statut |
|---|---|---|
| V1 | VLAN, trunking, routage inter-VLAN, DHCP (site HQ) | 🟡 En cours |
| V2 | OSPF, interconnexion multi-site (Rabat, Tanger) | ⚪ À venir |
| V3 | Services réseau (DNS, DHCP centralisé, NTP, web) | ⚪ À venir |
| V4 | Sécurité (ACL, SSH, Port Security) | ⚪ À venir |
| V5 | Supervision (SNMP, Zabbix/Grafana) | ⚪ À venir |
| V6 | Diagnostic d'incidents | ⚪ À venir |
| V7-V9 | Linux avancé, automatisation, extensions | ⚪ À venir |

## Architecture V1 (en construction)

- 1 routeur (R-HQ) en router-on-a-stick
- 1 switch cœur (SW-CORE) + 5 switches d'accès (un par département + invités)
- 2 PC par VLAN, pour tester à la fois le switching intra-VLAN et le routage inter-VLAN
- Les schémas de topologie seront ajoutés dans `topology/` une fois finalisés

## Plan d'adressage

Voir [`addressing/v1-hq.csv`](addressing/v1-hq.csv) pour le détail complet
(VLAN, réseaux, masques, passerelles).

## Documentation

- [Cahier des charges](documentation/cahier-de-charges.md)

## Structure du dépôt

```text
nexus-enterprise-network/
├── documentation/       # Cahier des charges, feuilles de route
├── topology/            # Schémas réseau (technique + vue entreprise)
├── addressing/          # Plans d'adressage IPv4 par version
├── configurations/      # Configurations texte des équipements, par version
├── services/            # DNS, DHCP, NTP, serveur web (V3+)
├── security/            # ACL, durcissement, SSH (V4+)
├── monitoring/          # Supervision SNMP/Zabbix (V5+)
├── automation/          # Scripts Python/Ansible (V8+)
├── incidents/           # Fiches de diagnostic (V6+)
├── tests/               # Résultats de validation par version
└── screenshots/         # Captures d'écran des tests
```

## Compétences travaillées dans ce projet

VLAN, trunking 802.1Q, inter-VLAN routing, DHCP, OSPF, ACL, SSH, Port Security,
SNMP, administration Linux, Python/Netmiko *(mises à jour au fil des versions,
uniquement une fois réellement implémentées et testées)*.
