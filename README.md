# 🛡️ Lab Wazuh / AD

## 📌 Présentation

Projet de mise en place d’un SIEM (Wazuh) pour centraliser et analyser les logs d’une infrastructure composée d’un Active Directory et de machines Windows/Linux.

## 🎯 Objectifs

- Centraliser les logs système et sécurité
- Détecter des événements suspects (authentification, brute force)
- Améliorer la visibilité des actions sur les machines
- Simuler des scénarios d’attaque en environnement contrôlé

## 🏗️ Architecture

- Hôte Windows 11 (hyperviseur / machine locale)
- VPS Ubuntu (Wazuh – SIEM)
- VM Domain Controller (Active Directory)
- VM Windows 10 (Client du domaine)
 ```
                 🖥️ Hôte Windows 11
                 (Hyperviseur local)
                        │
        ┌───────────────┴───────────────┐
        ▼                               ▼
🌐 VPS Ubuntu (Internet)         🧪 Environnement Virtualisé
   Wazuh SIEM                    ┌──────────────────────────┐
                                 │ 🧠 DC Active Directory   │
                                 │ 💻 Windows 10 Client     │
                                 └──────────────────────────┘
 ```   

## ⚙️ Fonctionnalités mises en place

- Collecte des logs Windows et Linux
- Détection d’échecs / succès de connexion
- Surveillance des tentatives de brute force SSH
- Amélioration de la télémétrie Windows avec Sysmon
- Durcissement du serveur (SSH + Fail2ban)

## 📊 Résultat

- SIEM fonctionnel et centralisé
- Visibilité sur les événements de sécurité
- Détection de comportements suspects
- Supervision SOC

## 🚀 Conclusion

Projet de mise en place d’un SIEM permettant la centralisation des logs et l’analyse d’événements de sécurité dans un environnement Windows / Active Directory.
L’ensemble permet de comprendre la chaîne complète de détection : génération des logs → collecte → analyse → visualisation.

## ⏭️ Suite logique

Évolution vers des scénarios Active Directory plus avancés, incluant mouvement latéral et enrichissement des sources de logs dans une logique SOC.
