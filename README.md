# 🐉 DRAGON-NEXUS-ORBIS (Desktop Companion)

**Dragon-Nexus-Orbis** est une application de bureau tout-en-un conçue pour la gestion des systèmes PS4 et PS5, le transfert de payloads, l'optimisation des fichiers et le suivi réseau.

---

## 🚀 Fonctionnalités principales

* **Gestionnaire PS4 & PS5 :** Interface dédiée pour transférer vers la console (`Transférer vers Console`) et vérifier les mises à jour des homebrews indispensables (*Apollo Save Tool, ItemzFlow, Xplorer, FTP Server Pro*, etc.)[cite: 14, 15].
* **Convertisseur & Outils Multi-Formats :** Outil d'analyse et de conversion de fichiers (*Folder Dump, Archives .ZIP/.TAR.GZ, Conteneurs .EXFAT, .FFPFS, ISO, ELF, JSON* et calcul d'empreintes *SHA-256/MD5*)[cite: 16].
* **Explorateur PC ⇄ Console :** Moniteur matériel en temps réel (température CPU/GPU, espace disque), gestion des avatars, thèmes, transferts de sauvegardes/trophées et sécurisation anti-mise à jour (DNS)[cite: 17].
* **Moniteur Système & Réseau :** Scanner réseau automatique, test de liaison par port (`2121`), outil de lecture de fichiers PKG et réveil réseau (*Wake-on-LAN*)[cite: 18].
* **Studio & Bonus :** Outils de sécurité de compte, gestion des sources de patchs externes et personnalisation de l'interface (*Bleu Électrique*, etc.)[cite: 19].

---
## 📋 Fiche technique & architecture — Dragon-Nexus-Orbis v1.0.0

**Auteur & propriétaire :** dragon111 — Tous droits réservés © 2026

### 1. Présentation générale du logiciel
* **Nom de l'application :** DRAGON-NEXUS-ORBIS
* **Version actuelle :** v1.0.0 (Édition Windows 10 / 11 — 64 bits)
* **Type de programme :** Suite logicielle native autonome de gestion, conversion, diagnostic matériel et transfert réseau pour consoles PlayStation 4 et PlayStation 5.
* **Interface graphique :** Développée en Python natif avec le moteur PySide6 (Qt6), garantissant une rapidité d'exécution maximale, aucun fichier HTML/web externe et une intégration parfaite sous Windows.

### 2. Architecture modulaire du programme
Le logiciel repose sur une architecture découpée en 10 modules indépendants compilés en un seul exécutable autonome (`Dragon-Nexus-Orbis.exe`) :
* `main.py` : Noyau principal qui coordonne l'interface, l'horloge temps réel, la sauvegarde automatique des préférences (`config.json`) et le lancement sécurisé.
* `login_screen.py` : Module de verrouillage au démarrage gérant la clé maître créateur (`dragon111`), l'inscription par code unique et la connexion chiffrée en SHA-256 (`user_account.json`).
* `themes.py` : Moteur graphique sombre avec 5 thèmes néon haute visibilité (Bleu Électrique, Rouge Électrique, Jaune Fluo, Vert Fluo, Orange Fluo).
* `languages.py` : Dictionnaire de traduction dynamique en temps réel (Français, Anglais, Espagnol, Allemand).
* `network_module.py` : Moteur réseau multi-thread (scan automatique d'IP locale, test de connexion, explorateur de fichiers double panneau PC ↔ Console, barre de progression et notifications sonores).
* `consoles_module.py` : Catalogues dédiés aux utilitaires PS4 et PS5.
* `tools_module.py` : Moteur de traitement de fichiers multi-format (12 formats supportés) et calculateur d'empreintes cryptographiques SHA-256 et MD5.
* `system_module.py` : Module de télémétrie matérielle (capteurs thermiques, espace disque libre, gestion des avatars/thèmes, sauvegardes/trophées et protection DNS anti-mise à jour).
* `bonus_module.py` : Intègre le PKG Tool (lecture binaire des en-têtes CUSA / PPSA), le gestionnaire multi-consoles (`consoles_profiles.json`), le studio de redimensionnement d'images (440x440 et 3840x2160) et le réveil réseau Wake-on-LAN.
* `updater_module.py` : Système silencieux de vérification et d'installation des futures mises à jour du logiciel.

### 3. Sécurité & protection des données
* **Contrôle d'accès strict :** Aucune fonctionnalité n'est accessible tant que l'utilisateur n'a pas validé son compte ou entré la clé créateur.
* **Confidentialité totale :** Les mots de passe sont hachés localement en SHA-256 avant d'être enregistrés. Aucune donnée personnelle ni aucun identifiant d'envoi d'e-mail n'est exposé dans le code.
* **Intégrité réseau :** L'installateur configure automatiquement une règle dédiée dans le Pare-feu Windows Defender pour autoriser uniquement les échanges locaux entre le PC et la console.

### 4. Déploiement & installation Windows
* **Compilation autonome :** Empaqueté via PyInstaller avec l'icône personnalisée `dragon.ico` et les ressources intégrées (`assets`).
* **Installateur professionnel :** Généré avec Inno Setup Compiler (`Setup_Dragon_Nexus_Orbis_v1.0.exe`).
* **Emplacement sur le disque dur :** `C:\Program Files\Dragon-Nexus-Orbis` (avec droits complets accordés au dossier pour la sauvegarde des paramètres utilisateurs).
* **Intégration système :** Création automatique du raccourci sur le Bureau Windows, dans le Menu Démarrer et ajout d'un désinstalleur officiel dans les paramètres Windows.

---
*Créé par **dragon111** — Tous droits réservés © 2026*[cite: 19]

## 📥 Téléchargement

Téléchargez la dernière version de l'installateur officiel pour Windows :
👉 **[Télécharger Dragon-Nexus-Orbis v1.0 (Setup.exe)](https://github.com/wolf-mika/Dragon-Nexus-Orbis-App/releases/latest)**

---

## 🖼️ Aperçu de l'interface

<p align="center">
  <img width="453" height="471" alt="Aperçu Dragon-Nexus-Orbis" src="https://github.com/user-attachments/assets/83ab8ea5-7229-4594-b465-29dc732f8808" />
</p>
## 📥 Téléchargement

Téléchargez la dernière version de l'installateur officiel pour Windows :
👉 **[Télécharger Dragon-Nexus-Orbis v1.0 (Setup.exe)](https://github.com/wolf-mika/Dragon-Nexus-Orbis-App/releases/latest)**

---

## 🖼️ Aperçu de l'interface


<img width="1150" height="772" alt="Capture d&#39;écran 2026-11-19 010504" src="https://github.com/user-attachments/assets/800db64a-b01b-4956-9ab7-208e5e4fc745" />
<img width="1136" height="778" alt="Capture d&#39;écran 2026-11-19 010639" src="https://github.com/user-attachments/assets/ba84bbd3-c5b0-468b-a67c-d27f30008cc4" />
<img width="1142" height="768" alt="Capture d&#39;écran 2026-11-19 010621" src="https://github.com/user-attachments/assets/3ab87dba-be69-4cb1-ae15-ae5e843778f3" />
<img width="1156" height="782" alt="Capture d&#39;écran 2026-11-19 010559" src="https://github.com/user-attachments/assets/7d8fa6b2-074d-47ba-a6fa-f0950aed8ee5" />
<img width="1140" height="778" alt="Capture d&#39;écran 2026-11-19 010542" src="https://github.com/user-attachments/assets/90513cf4-5194-4da3-b81c-2566f0a1a7af" />
<img width="1152" height="785" alt="Capture d&#39;écran 2026-11-19 010523" src="https://github.com/user-attachments/assets/a4c909bf-00ff-4029-b992-85d7f92fa61c" />

