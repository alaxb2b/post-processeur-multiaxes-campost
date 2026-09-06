# Guide des fichiers et de la reproduction

## Extensions

| Extension | Rôle dans cette archive |
|---|---|
| `.dbf` | Base du post-processeur, à ouvrir avec l'environnement CAM-POST compatible |
| `.lis` | Listing lisible du questionnaire de configuration |
| `.ncl` | Instructions issues de la chaîne FAO |
| `.txt` | Instructions de scénarios d'essai |
| `.tap` | Programme de commande numérique produit |
| `.lst` | Listing associé au traitement |
| `.pdf` | Rapport original |

## Examiner un cas

Choisir un dossier dans [examples](../examples/). Lire d'abord l'entrée, puis retrouver les instructions correspondantes dans le TAP et consulter le LST. Distinguer les messages attendus d'un scénario d'essai des erreurs effectivement observées.

Le cas `fmotsPP-4` teste notamment des instructions interdites ou nécessitant une macro. Les commentaires dans son entrée sont des données du projet, pas la preuve qu'une exigence est satisfaite.

## Régénérer les sorties

1. Disposer d'une installation CAM-POST compatible et des ressources nécessaires à la configuration.
2. Examiner la base [ZERA03.dbf](../postprocessor/ZERA03.dbf) et le [questionnaire archivé](../postprocessor/zera2025%20%285%29.lis).
3. Vérifier la machine, le contrôleur, les unités, les axes et la correspondance entre cette base et le questionnaire.
4. Traiter une copie d'une entrée dans un dossier de travail séparé.
5. Comparer les sorties produites aux TAP/LST historiques, en expliquant les différences.

Aucune commande de génération automatisée n'est fournie : l'archive ne contient pas la configuration complète d'un environnement CAM-POST reproductible. Les noms `ZERA03` et `ZERA2025` ne doivent pas être supposés interchangeables sans vérification.

## Périmètre de vérification

La réorganisation vérifie la conservation des objets Git des fichiers techniques et les liens de la documentation. Elle n'établit ni conformité machine, ni absence de collision, ni validité de tous les cycles.
