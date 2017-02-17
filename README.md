# HiBoP

Ce wiki est destiné à la configuration du module 3D d'HiBoP.

## Depuis Unity3D

### Utiliser l'API:

La scène **LastMain** contient le GameObject **HiBoP 3DModule API**, il définit tout ce qui est nécessaire pour utiliser le module 3D:
 * évènements (acessibles depuis l'inspector ou directement dans le code)
 * camera principale du module
 * fonctions de commande

Il est inutile d'essayer d'utiliser d'autres GameObjects que celui-ci, la structure du programme s'en trouverait endommagée.

### Accéder aux fonctionnalités debug du module 3D:

Deux programmes de debug sont disponible depuis le dossier où se trouve l'éxécutable d'HiBoP:

  * **HiBoP_debug_launcher** permet de parser la BDD Epilepsy et d'afficher rapidement une scène SP ou MP dans HiBoP avec des données géométriques réelles et des données iEEG simulées. Ce programme va se charger lui-même de lancer HiBoP et de le quitter, il en sera ainsi à chaque chargement d'une nouvelle scène.
  Très utile pour tester rapidement une scène avec un nouveau build.
  * **HiBoP_debug_launcher_editor** fonctionne de la même façon sauf qu'il ne lancera pas HiBoP de lui même, il se contente d'écrire un fichier de configuration contenant les chemiens vers Epilepsy. Pour charger la scène définie dans ce fichier il faudra utilier le menu personnalisé "Debug test" dans l'éditeur et choisir "Load patient from debug launcher".







Rendu à la fin de mon contrat:
------------------------------

Hierachie du dossier
* HiBoP_dd_mm_yyyy
  * HiBoP
    * build_linux
    * build_windows
    * editor
    * export
      * hbp_export
      * Data
        * debug
          * dummy_icones
            * car.png
            * computer.png
            * house.png
          * IRM
            * chr256.nii
          * MarsAtlas
            * broadman_areas.txt
            * mars_atlas_index.csv
          
      
  * HiBoP_DB_manager
    * build_linux
    * build_windows








