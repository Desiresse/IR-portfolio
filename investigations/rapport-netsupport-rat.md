# Rapport d'incident — NetSupport Manager RAT
**Date :** 2026-07-12  
**Analyste :** Karen Jessley Desiresse  
**Source :** malware-traffic-analysis.net (exercice 2026-02-28)

---

## Résumé exécutif
Un poste Windows du segment LAN `10.2.28.0/24` a été compromis par un 
NetSupport Manager RAT communiquant avec un serveur C2 sur le port TCP 443. 
L'activité a débuté le 2026-02-28 à 19:55 UTC.

## Hôte infecté
| Attribut | Valeur |
|----------|--------|
| Adresse IP | `10.2.28.88` |
| Adresse MAC | `00:19:d1:b2:4d:ad` |
| Nom d'hôte | `DESKTOP-TEYQ2NR` |
| Compte utilisateur | `brolf` |
| Nom complet | Becka Rolf |
| Domaine AD | `EASYAS123.TECH` |

## Indicateurs de compromission (IOCs)
| Type | Valeur |
|------|--------|
| IP C2 | `45.131.214.85` |
| Port | `443/TCP` |
| Famille malware | NetSupport Manager RAT |
| Première activité | 2026-02-28 19:55 UTC |

## Méthode d'investigation
1. Filtre Wireshark `ip.addr == 45.131.214.85` → identification IP infectée
2. Analyse Ethernet II → extraction adresse MAC
3. Filtre `kerberos` → AS-REQ → hostname et compte AD
4. Corrélation avec contexte SIEM (alerte signature)

## Actions recommandées
- Isoler immédiatement `10.2.28.88` du réseau
- Réinitialiser les credentials de `brolf`
- Bloquer `45.131.214.85` au firewall et proxy
- Analyser les autres postes du segment pour propagation
- Vérifier les Scheduled Tasks et Registry Run keys sur l'hôte

## Outils utilisés
`Wireshark` · `MITRE ATT&CK` · `NIST SP 800-61` · `SANS PICERL`
