# MalTrack - Windows Malware Detection & Removal Tool

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Python](https://img.shields.io/badge/python-3.8%2B-brightgreen)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey)

MalTrack est un outil de détection et de suppression de malware conçu pour Windows, spécialisé dans la détection des RATs (Remote Access Trojans) comme Fynloski/DarkComet.

## 🚨 Avertissement

**IMPORTANT**: Cet outil est créé à des fins éducatives uniquement. Son utilisation doit se faire exclusivement dans un environnement de test contrôlé (machine virtuelle). N'utilisez jamais cet outil sans autorisation explicite sur des systèmes qui ne vous appartiennent pas.

## 🎯 Fonctionnalités

- Détection des processus malveillants
- Identification des connexions réseau suspectes
- Analyse des modifications du registre Windows
- Détection des mécanismes de persistance
- Suppression automatique des malwares détectés
- Identification de l'IP de l'attaquant
- Génération de rapports détaillés

## 📋 Prérequis

- Windows 10/11
- Python 3.8 ou supérieur
- Droits administrateur
- Machine virtuelle (recommandé)

## 🛠️ Installation

1. Clonez le repository :
```bash
git clone https://learn.zone01dakar.sn/git/dgaye/mal-track.git
cd maltrack
```

2. Installez les dépendances :
```bash
pip install -r requirements.txt
```

## 💻 Utilisation

1. Configuration de l'environnement de test (VM recommandée) :
```powershell
# Exécuter en tant qu'administrateur PowerShell
Set-MpPreference -DisableRealtimeMonitoring $true  # Désactiver Windows Defender
```

2. Lancer le scan :
```bash
python malware_hunter.py
```


## 📝 Exemple de Rapport

Le programme génère un rapport détaillé contenant :
- Liste des processus suspects
- Connexions réseau anormales
- Modifications suspectes du registre
- IP de l'attaquant identifiée
- Actions de nettoyage effectuées

## 🔍 Fonctionnement

1. **Phase de Scan**
   - Analyse des processus actifs
   - Vérification des connexions réseau
   - Inspection du registre Windows
   - Recherche de fichiers suspects

2. **Phase de Détection**
   - Identification des signatures malveillantes
   - Détection des mécanismes de persistance
   - Analyse des communications suspectes

3. **Phase de Nettoyage**
   - Arrêt des processus malveillants
   - Suppression des entrées du registre
   - Élimination des fichiers malveillants
   - Blocage des IPs malveillantes

## 🛡️ Mesures de Sécurité

- Utilisez toujours cet outil dans une machine virtuelle
- Isolez la VM du reste du réseau
- Prenez un snapshot avant utilisation
- Ne désactivez pas les protections sur votre machine principale

## 🤝 Contribution

Les contributions sont les bienvenues ! Pour contribuer :
1. Forkez le projet
2. Créez une branche pour votre fonctionnalité
3. Commitez vos changements
4. Poussez vers la branche
5. Ouvrez une Pull Request

## 📜 Licence

Ce projet est sous licence MIT - voir le fichier [LICENSE](LICENSE) pour plus de détails.

## ✍️ Auteur

- Votre Nom - [Votre GitHub](https://github.com/dgthegeek)

## 📚 Ressources

- [Documentation Windows Registry](https://docs.microsoft.com/en-us/windows/win32/sysinfo/registry)
- [Python psutil Documentation](https://psutil.readthedocs.io/)
- [Windows Defender Documentation](https://docs.microsoft.com/en-us/windows/security/threat-protection/)

## 🙏 Remerciements

- Microsoft pour la documentation Windows
- La communauté Python pour les outils et bibliothèques
- La communauté cybersécurité pour le partage de connaissances