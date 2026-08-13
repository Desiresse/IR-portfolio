# Rapport d'incident — Lumma Stealer
**Date :** 2026-07-12
**Analyste :** Karen Jessley Desiresse
**Source :** malware-traffic-analysis.net (exercice 2026-01-31)

---

## Résumé exécutif
Un poste Windows du segment LAN `10.1.21.0/24` a été compromis par Lumma
Stealer, un infostealer capable de voler credentials, cookies de session
et wallets crypto. Le malware communiquait via HTTP en clair avec son C2.
Investigation menée en autonomie complète — 6 questions résolues sur 6.

---

## Contexte SIEM
| Attribut | Valeur |
|----------|--------|
| Signature déclenchée | ET MALWARE Lumma Stealer Victim Fingerprinting Activity |
| IP C2 signalée | `153.92.1.49` |
| Port | `80/TCP` |
| Heure alerte | 2026-01-27 23:05 UTC |

---

## Hôte infecté identifié
| Attribut | Valeur |
|----------|--------|
| Adresse IP | `10.1.21.58` |
| Adresse MAC | `00:04:c1:be:8c:d4` (Xircom) |
| Nom d'hôte | `DESKTOP-ES9F3ML` |
| Compte utilisateur | `gwyatt` |
| Nom complet | Gabriel Wyatt |
| Domaine Active Directory | `WIN11OFFICE` |
| Contrôleur de domaine | `10.1.21.2 — WIN-LU4L24X3UB7` |

---

## Indicateurs de compromission (IOCs)
| Type | Valeur |
|------|--------|
| IP C2 | `153.92.1.49` |
| Port C2 | `80/TCP` |
| Domaine C2 | `whitepepper.su` |
| Famille malware | Lumma Stealer (infostealer) |
| Première activité | 2026-01-27 23:05 UTC |
| Protocole | HTTP en clair |

---

## Méthode d'investigation — étapes détaillées

### Étape 1 — Identification de l'IP infectée
