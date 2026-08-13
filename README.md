
# 🛡️ IR-Portfolio — Karen Jessley Desiresse

**Incident Response Analyst | Blue Team SOC | IFAPME Charleroi**

Étudiante en 1ère année de formation Incident Response Analyst à l'IFAPME 
Charleroi (alternance). Ce portfolio documente mes investigations réelles, 
mes rapports d'incidents et mes labs de cybersécurité défensive.

---

## 🔍 Investigations PCAP réelles

| # | Malware | Technique | Hôte infecté | C2 identifié |
|---|---------|-----------|--------------|--------------|
| 1 | NetSupport Manager RAT | Analyse Kerberos AS-REQ · Wireshark | DESKTOP-TEYQ2NR (10.2.28.88) | 45.131.214.85:443 |
| 2 | Lumma Stealer | Analyse HTTP · DNS · Kerberos | DESKTOP-ES9F3ML (10.1.21.58) | whitepepper.su (153.92.1.49:80) |

📁 Rapports complets : voir dossier [investigations/](./investigations/)

---

## 🧰 Compétences techniques

**Analyse réseau & forensics**
- Wireshark — filtres avancés TCP/IP, DNS, HTTP, SMB, Kerberos, LDAP
- Identification IOCs, trafic C2, beaconing, DNS tunneling
- Analyse PCAP réels (malware-traffic-analysis.net)

**Frameworks IR**
- MITRE ATT&CK — cartographie TTPs, tactiques et techniques
- NIST SP 800-61 — cycle de vie officiel IR
- SANS PICERL — communication opérationnelle SOC
- Rédaction rapports d'incident (technique + exécutif)

**Systèmes & artefacts forensiques**
- Windows : Event IDs (4624, 4625, 4688, 4698, 7045), Prefetch, Registry Run keys, Scheduled Tasks
- Linux : auth.log, auditd, cron, /tmp, bash_history
- Active Directory : Kerberos AS-REQ, LDAP, attribution utilisateur

**SIEM & outils SOC**
- Wazuh (déploiement en cours — VM Ubuntu + agent Windows)
- Règles de détection custom
- TheHive (notions)

**Réglementation**
- Directive NIS2 (Belgique, 2024)
- RGPD · ISO 27001 (notions)

---

## 📋 Rapports d'incidents

- [Investigation NetSupport RAT — 2026-07-12](./investigations/rapport-netsupport-rat.md)
- [Investigation Lumma Stealer — 2026-07-12](./investigations/rapport-lumma-stealer.md)

---

## 🎓 Formation & certifications

| Certification | Statut | Organisme |
|---------------|--------|-----------|
| Incident Response Analyst (PQ) | En cours 2025–2027 | IFAPME Charleroi |
| TryHackMe SOC Level 1 | En cours | TryHackMe |
| MOOC SecNumAcadémie | À compléter | ANSSI |
| BTL1 — Blue Team Labs | En préparation | Security Blue Team |

---

## 📬 Contact

- 📧 karenjessley1@gmail.com
- 💼 [linkedin.com/in/votre-profil]
- 📍 tamines
