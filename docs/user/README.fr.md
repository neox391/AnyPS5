[English](../../README.md) | [Português (Brasil)](README.pt-BR.md) | [Español](README.es.md) | [Català](README.ca.md) | [Italiano](README.it.md) | **Français** | [简体中文](README.zh-CN.md) | [Русский](README.ru.md) | [Bahasa Indonesia](README.id.md) | [Polski](README.pl.md) | [日本語](README.ja.md) | [العربية](README.ar.md)

# Présentation

Outil de portage automatique d'exécutables vers Linux et Windows.

La compilation du relinker seul fonctionne également sur macOS, y compris sur les Mac équipés d'une puce Apple Silicon.

[**Convertisseur web**](https://boykopovar.github.io/AnyPS5/) — les fichiers restent sur votre appareil.

![anyps5_collage1](https://github.com/user-attachments/assets/ed2f0b2d-33d3-46d7-ab88-767ca872fc99)

Le projet comprend un [relinker](../../core/relinker) qui convertit les exécutables au format natif du système cible, ainsi que des implémentations des [bibliothèques système PRX](../../core/libs/prx) compatibles avec l'édition de liens dynamique. Il ne repose ni sur l'émulation ni sur un processus d'exécution distinct.

[**Discord**](https://discord.gg/x9naWVzC6A), [Utilisation](USAGE.md), [Instructions de compilation](../dev/BUILD.md), [Architecture](../dev/ARCHITECTURE.md), [Dette technique du projet](../dev/TechnicalDebt.md), [Conventions de code](../dev/CONVENTIONS.md), [Contribution](../../CONTRIBUTING.md)

## État d'avancement

[![libraries](https://boykopovar.github.io/AnyPS5/badge-libraries.svg)](https://boykopovar.github.io/AnyPS5/progress.html) [![RDNA2 reference shader forms decoded](https://boykopovar.github.io/AnyPS5/badge-shaders.svg)](https://boykopovar.github.io/AnyPS5/progress.html) [![gfx1013 reference shader forms decoded](https://boykopovar.github.io/AnyPS5/badge-shaders-gfx1013.svg)](https://boykopovar.github.io/AnyPS5/progress.html) [![implemented in 7 days](https://boykopovar.github.io/AnyPS5/badge-week.svg)](https://boykopovar.github.io/AnyPS5/history.html)

[![progress map](https://boykopovar.github.io/AnyPS5/progress.svg)](https://boykopovar.github.io/AnyPS5/progress.html)

[Historique de l'avancement](https://boykopovar.github.io/AnyPS5/history.html)

<sub>* Bibliothèques système : pourcentage des fonctions connues du projet à ce jour (déclarées dans [core/libs/prx](../../core/libs/prx)), et non de l'ensemble des fonctions système de la PS5. Ce total augmente à mesure que de nouvelles fonctions sont déclarées.</sub>

Les états non pris en charge ou inattendus déclenchent une exception C++, généralement `std::runtime_error`. Si elle n'est pas interceptée, son message `what()` est affiché sur la sortie d'erreur standard et le processus se termine.

Le [recompilateur de shaders](../../core/shader/recompiler/Recompiler.cpp) produit du SPIR-V avec succès (validé par [SPIRV-Tools](../../3rdparty/SPIRV-Tools) lorsque le projet est compilé avec `ANYPS5_ENABLE_SPIRV_TOOLS`).

## Compatibilité

L'état de compatibilité et les rapports de test de chaque jeu figurent dans les discussions [Game bring-up](https://github.com/boykopovar/AnyPS5/discussions/categories/game-bring-up), avec une discussion par titre.

## Configuration des commandes

Les manettes reconnues par SDL sont prises en charge, notamment les sticks analogiques et les gâchettes. Le clavier et la souris peuvent être configurés au moyen d'un fichier `anyps5-input.ini`. Consultez la [documentation sur les commandes](INPUT_MAPPING.md) pour connaître les périphériques pris en charge et le format de configuration.

## Avertissement

Ce projet est destiné à l'interopérabilité, à la recherche, à la préservation et à la compatibilité. Il n'inclut, ne distribue et ne nécessite aucun logiciel, micrologiciel, clé cryptographique ou bibliothèque propriétaire protégé par le droit d'auteur. Il appartient aux utilisateurs de s'assurer que les fichiers binaires employés avec ce projet ont été obtenus et sont utilisés conformément aux lois applicables et aux conditions de leurs licences respectives.

AnyPS5 est un projet indépendant, sans affiliation avec Sony Interactive Entertainment, et n'est ni autorisé ni approuvé par cette société. « PlayStation » et « PS5 » sont des marques de Sony Interactive Entertainment Inc.

## Licence

Ce projet est distribué sous licence GNU General Public License, version 2 uniquement.
