# HiBoP

Ce wiki est destiné à la configuration du module 3D d'HiBoP.

## Depuis Unity3D

### Utiliser l'API:

La scène **LastMain** contient le GameObject **HiBoP 3DModule API**, il définit tout ce qui est nécessaire pour utiliser le module 3D:
 * évènements (acessibles depuis l'inspector ou directement dans le code)
 * camera principale du module
 * fonctions de commande

Il est inutile d'essayer d'utiliser d'autres GameObjects que celui-ci, la structure du programme s'en trouverait endommagée.

L'utilisation de la GUI Qt a été modifiée et les fonctions sont désormais statiques:
**HBP.VISU3D.DLL.QtGUI.get_existing_directory_name(string message = "Select a directory", string defaultDir = "")**

### Accéder aux fonctionnalités debug du module 3D:

Deux programmes de debug sont disponible depuis le dossier où se trouve l'éxécutable d'HiBoP:

  * **HiBoP_debug_launcher** permet de parser la BDD Epilepsy et d'afficher rapidement une scène SP ou MP dans HiBoP avec des données géométriques réelles et des données iEEG simulées. Ce programme va se charger lui-même de lancer HiBoP et de le quitter, il en sera ainsi à chaque chargement d'une nouvelle scène.
  Très utile pour tester rapidement une scène avec un nouveau build.
  * **HiBoP_debug_launcher_editor** fonctionne de la même façon sauf qu'il ne lancera pas HiBoP de lui même, il se contente d'écrire un fichier de configuration contenant les chemiens vers Epilepsy. Pour charger la scène définie dans ce fichier il faudra utilier le menu personnalisé "Debug test" dans l'éditeur et choisir "Load patient from debug launcher".

### Dossier Data

Pour que le module marche, ce dossier doit-être présent dans le dossier **Assets** pour l'éditeur et à la racine de l'éxécutable pour une version build.

Unity_scenes
 * HiBoP
  * hibop_Data
  * Assets
   * Data

Unity_builds
 * HiBoP_dd_mm_yyyy
   * hibop.exe
   * hibop_Data
   * Data

Détails du dossier:

Data
 * debug
   * dummy_icones (dossier d'icônes utilisées quand une scène est chargée par "HiBoP_debug_launcher"
     * car.png
     * computer.png
     * house.png
   * IRM
     * chr256.nii (IRM utilisée pour les scènes MNI)
   * MarsAtlas
     * broadman_areas.txt (noms des aires de broadman, utilisées avec mars atlas)
     * mars_atlas_index.csv (zones de mars atlas)
   * Meshes
     * MNI_single_hight_Bhemi.obj (le maillage MNI contenant les 2 hemisphères avec la matière grise)
     * MNI_single_hight_Lhemi.obj (le maillage MNI contenant l'hemisphère gauche avec la matière grise)
     * MNI_single_hight_Rhemi.obj (le maillage MNI contenant l'hemisphère droit avec la matière grise)
     * MNI_single_hight_Bwhite.obj (le maillage MNI contenant les 2 hemisphères avec la matière blanche)
     * MNI_single_hight_Lwhite.obj (le maillage MNI contenant l'hemisphère gauche avec la matière blanche)
     * MNI_single_hight_Rwhite.obj (le maillage MNI contenant l'hemisphère droit avec la matière blanche)
     * MNI_single_hight_Bwhite_inflated.obj (le maillage MNI contenant les 2 hemisphères avec la matière blanche) en version gonflée
     * MNI_single_hight_Lwhite_inflated.obj le maillage MNI contenant l'hemisphère gauche avec la matière blanche en version gonflée)
     * MNI_single_hight_Rwhite_inflated.obj (le maillage MNI contenant l'hemisphère droit avec la matière blanche en version gonflée)




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

          
      
  * HiBoP_DB_manager
    * build_linux
    * build_windows








