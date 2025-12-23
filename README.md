# Kinder Schaffa 🧸 — Guide d’utilisation

Kinder Schaffa est une interface pédagogique pour **apprendre à enquêter à partir de Wikipédia** lorsqu’une _certaine_ question se pose au sujet d’une entreprise ou d’une organisation.

L’objectif n’est pas de “trancher” en quelques secondes : l’outil sert à **repérer des passages**, puis à **lire, contextualiser et vérifier**.

L'application est disponible ici : https://guillaumefe.github.io/kinder-schaffa

---

## Fonctionnement et limites

### Ce que l’application fait
- Recherche une page Wikipédia correspondant au nom saisi.
- Tente d’identifier une section **« Controverse »** (ou section assimilée).
- Détecte la présence de mots-clés liés au **travail** et aux **enfants**.
- Affiche un extrait ciblé pour orienter vers un passage pertinent.

### Ce que l’application ne fait pas
- Elle **n’établit aucune preuve**.
- Elle ne conclut pas à la véracité d’une accusation.
- Elle ne remplace ni une lecture complète, ni des sources externes fiables.

---

## Parcours d’usage

1. Saisie du nom d’une entreprise ou d’une organisation.
2. Lancement de la recherche.
3. Lecture du résultat affiché :
   - **Signal détecté** : des mots liés au travail *et* aux enfants ont été repérés dans la section analysée.
   - **Pas de signal** : l’outil n’a pas repéré ces mots-clés ensemble dans la section analysée.
   - **Indéterminé** : l’outil ne parvient pas à identifier une page unique ou une section exploitable.
4. Ouverture de la page Wikipédia et lecture guidée (contexte, date, sources).

> Remarque : la version anglaise de Wikipédia est souvent plus complète et détaillée. Une recherche complémentaire en anglais peut donc être utile.
> TIPS : pour Nestlé cherchez et vous trouverez.
---

## Interprétation des badges

### 🟠 Signal détecté
Signifie : **des mots ont été trouvés** dans le texte analysé.  
Ne signifie pas : “c’est prouvé”.

À vérifier systématiquement :
- le passage exact,
- la date,
- le contexte,
- les sources citées.

### 🟢 Pas de signal
Signifie : **l’outil n’a rien trouvé** selon ses critères.  
Ne signifie pas : “il n’y a rien”.

À faire :
- ouvrir la page malgré tout,
- élargir la recherche,
- croiser avec d’autres sources fiables.

### 🔴 Indéterminé / Plusieurs pages
Cas fréquent lorsque :
- Wikipédia propose une homonymie,
- le nom est ambigu,
- la page n’existe pas clairement.

---

## “Ce que l’application a vu”
Cette zone reformule ce qui a été détecté pour **orienter la lecture**, pas pour conclure.  
Elle constitue un **point de départ**, jamais un verdict.

---

## Mini-checklist de vérification
- La page traite-t-elle bien de la même organisation ?
- Quel passage exact aborde le sujet ?
- Quelles sources sont citées ?
- De quand date l’information ?
- Existe-t-il des sources indépendantes concordantes ?

---

## À propos du nom
“Kinder Schaffa” signifie “travail des enfants” en alsacien (version Haut-Rhin).

---

## Notes techniques

Le code du serveur est disponible dans une **archive zippée** accessible dans le dépôt.

Ce choix vise à :
- limiter l’indexation automatique par les moteurs de recherche et les scanners de dépôts,
- pour rendre plus difficile le lien entre le **serveur de l’application** et cette page web,
- et protéger un peu (oui, c'est fragile) l’API exposée publiquement.

En effet, la page web contient un secret : elle embarque un **token d’accès statique** visant à réduire les abus automatisés (robots, scans massifs).  
Il s’agit d’une **protection légère et transitoire**, assumée comme telle, préférée à la mise en place plus longue ou plus couteuse d'un service tiers et/ou reverse-proxy.
Avec le token vous pouvez requêter assez librement le proxy qui interroge wikipedia depuis vos propres applications mais **merci de ne pas en abuser : hébergez votre instance!**

## Licence

Ce projet est distribué sous licence **GNU General Public License v3 (GPLv3)**.

Cela signifie notamment que :
- le code source peut être utilisé, étudié, modifié et redistribué ;
- toute redistribution ou utilisation dérivée doit rester sous licence GPLv3 ;
- les modifications doivent rester accessibles sous la même licence.

Le texte complet de la licence est disponible ici :  
https://www.gnu.org/licenses/gpl-3.0.fr.html

---
