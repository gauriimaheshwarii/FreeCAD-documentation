# Fine-tuning/fr
{{TOCright}}

Cette page contient différents réglages et paramètres que vous pouvez utiliser pour améliorer votre installation de FreeCAD ou résoudre des problèmes.

## Paramètres des options 

L\'[Editeur de préférences](Preferences_Editor/fr.md) de FreeCAD du menu **Édition → Préférences** est généralement utilisé pour définir et manipuler la table des paramètres de FreeCAD.

Cependant, il est également possible d\'accéder, de modifier et de créer des paramètres manuellement, à l\'aide de l\'[Editeur de paramètres](Std_DlgParameter/fr.md) du menu **Outils → Editer les paramètres...**.

La liste ci-dessous répertorie les paramètres qui ne sont pas accessibles via l'éditeur de préférences mais que vous pouvez définir manuellement (situé dans **BaseApp/Preferences**)

-   **Addons/developerMode** (booléen) : défini à `True` pour activer le mode développeur du [Gestionnaire des extensions](Std_AddonMgr/fr.md). Voir [Métadonnées du package](Package_Metadata/fr#Validation.md).
-   **Bitmaps/Theme/ThemeSearchPaths** (booléen) : défini à `False` pour que FreeCAD utilise ses icônes incluses au lieu du thème des icônes du système sous Linux.
-   **Dialog/DontUseNativeColorDialog** (booléen) : paramètre de la boîte de dialogue du sélecteur de couleur. Définir à `False` si vous voulez que FreeCAD utilise la boîte de dialogue de couleur natif de votre système plutôt que la boîte de dialogue de couleur Qt. La valeur par défaut est `True`.
-   **Dialog/DontUseNativeDialog**\' (booléen) : paramètre de dialogue de fichier. Définir à `False` si vous voulez utiliser la boîte de dialogue native de fichier lors de l\'ouverture de fichiers ou à `True` pour utiliser la boîte de dialogue File Picker de Qt. La valeur par défaut dépend d\'un paramètre de compilation : #define (USE_QT_FILEDIALOG).
-   **Dialog/DontUseNativeFontDialog** (booléen) : utilisé par la commande [Draft Formes à partir de texte](Draft_ShapeString/fr.md). Définir à `False` pour utiliser la boîte de dialogue de la police native. La valeur par défaut est `True`.
-   **DockWindows/DAGView/Enabled** (booléen) : défini à `True` pour activer un widget dockable beta de la [Vue DAG](DAG_view/fr.md). Après avoir changé la valeur du paramètre, un redémarrage de FreeCAD est nécessaire pour que le widget soit disponible dans la liste des vues/panneaux.
-   **DockWindows/PropertyView/Enabled** (booléen) : défini à `True` pour activer un widget ancrable de l\'[Éditeur de propriétés](Property_editor/fr.md) indépendant de la vue combinée. Après avoir changé la valeur du paramètre, un redémarrage de FreeCAD est nécessaire pour que le widget soit disponible dans la liste des vues/panneaux.
-   **Document/AutoNameDynamicProperty** (booléen) : défini à `True` pour que FreeCAD renomme automatiquement les propriétés dynamiques avec un nom spécifié invalide au lieu de lancer une exception. Notez que le code Python n\'aura pas accès au nouveau nom.
-   **DockWindows/TreeView/Enabled** (booléen) : défini à `True` pour activer un widget ancrable de la [vue en arborescence](Document_structure/fr.md) indépendant de la vue combinée. Après avoir changé la valeur du paramètre, un redémarrage de FreeCAD est nécessaire pour que le widget soit disponible dans la liste des vues/panneaux.
-   **Document/ChangeViewProviderTouchDocument** (booléen) : défini à `False` pour que les changements de visibilité des éléments ne marquent pas le document comme modifié.
-   **Document/SaveThumbnailFix** (booléen) : défini à `True` pour corriger un problème avec Qt5 qui empêche la génération de miniatures de fichiers `.FCStd`.
-   **General/LockToolBars** (booléen) : défini à `True` pour empêcher les barres d\'outils d\'être déplaçables et pour cacher les petites poignées de déplacement. Surtout utilisé en conjonction avec des feuilles de style qui rendent les barres d\'outils verticales.
-   **General/RecentIncludesExported** (booléen) : défini à `True` pour inclure les fichiers exportés dans la liste des fichiers récents. La valeur par défaut est `False`.
-   **General/RecentIncludesImported** (booléen) : défini à `False` pour exclure les fichiers importés de la liste des fichiers récents. La valeur par défaut est `True`.
-   **Macro/DuplicateFrom001** : (booléen) : défini à `True` pour toujours commencer à chercher le nom de fichier de macro dupliqué suggéré avec \@001 au lieu du \@NNN en cours, le cas échéant. La valeur par défaut est `False`.
-   **Macro/DuplicateIgnoreExtraNote** (booléen) : défini à `True` pour ignorer la note supplémentaire lors de la suggestion d\'un nom de fichier de macro dupliqué. La note supplémentaire est le texte du nom de fichier qui suit \"@NNN\" et précède \".FCMacro\". Exemple : \"my_macro@005.my_note.FCMacro\". Si `True`, le nom de fichier suivant suggéré est \"my_macro@006.FCMacro\". S\'il est défini sur `False`, le prochain nom de fichier suggéré est \"my_macro@006.my_note.FCMacro\". Pour être reconnu comme une note supplémentaire, le texte doit commencer par un point (\".\") après le \"@NNN\". Sinon, par exemple, \"my_macro@006_my_note.FCMacro\" se voit suggérer \"my_macro@006_my_note@001.FCMacro\" comme nouveau nom de fichier, ce qui peut être souhaitable dans certains cas. La valeur par défaut est `False`.
-   **Macro/ReplaceSpaces** (booléen) : défini à `False` si vous ne voulez pas que les espaces dans vos noms de fichiers soient automatiquement convertis en caractères de soulignement lorsque vous créez, renommez ou dupliquez une macro. Cela n\'affecte pas les fichiers existants, mais uniquement lors de la création d\'un nouveau fichier ou du renommage ou de la duplication d\'un fichier existant. La valeur par défaut est `True`.
-   **MainWindow/ClearMenuBar** (booléen) : défini à `True` pour effacer la barre de menu lors du changement d\'atelier, utile lors de l\'utilisation d\'un menu global, car elle peut ne pas être mise à jour lors du changement d\'atelier et peut être rapidement encombrée par les entrées de menu de chaque atelier. La valeur par défaut est `False`. Sous macOS, elle est effacée dans les deux sens pour contourner un bogue de Qt.
-   *MainWindow/ToolBarNameAsToolTip* (booléen) : défini à `False` pour ne pas obtenir le nom de la barre d\'outils comme infobulle. La valeur par défaut est `True`.
-   **Mod/Draft/defaultCameraHeight** (entier) : définit la hauteur de la caméra lorsque Draft démarre dans un document vide. 0 désactive, la valeur par défaut de FreeCAD est 5, bon quand on travaille en millimètres, une bonne hauteur pour le travail en arc est 4500.
-   **Mod/Part/ParametricRefine** (booléen) : défini à `False` pour que [Part Affiner la forme](Part_RefineShape/fr.md) crée une copie indépendante plutôt qu\'une copie liée. La valeur par défaut est `True`.
-   **Mod/PartDesign/AdditiveHelixPreview** (booléen) : défini à `True` pour s\'assurer qu\'une hélice additive qui n\'intersecte pas le corps est visible dans l\'aperçu. La valeur par défaut est `False`.
-   **Mod/PartDesign/SubtractiveHelixPreview** (booléen) : défini à `True` pour qu\'une hélice soustractive qui n\'intersecte pas le corps soit visible dans l\'aperçu. La valeur par défaut est `True`.
-   **Mod/PartDesign/SwitchToTask** (booléen) : défini à `False` pour empêcher l\'[atelier PartDesign](PartDesign_Workbench/fr.md) de passer au panneau Tâche au démarrage. La valeur par défaut est `True`.
-   **Mod/PartDesign/SwitchToWB** (booléen) : défini à `False` pour empêcher l\'appel automatique de l\'[atelier PartDesign](PartDesign_Workbench/fr.md) lorsqu\'un [PartDesign Corps](PartDesign_Body/fr.md) est activé. La valeur par défaut est `True`.
-   **Mod/Sketcher/RadiusDiameterConstraintDisplayBaseAngle** (flottant) : définit l\'angle (par rapport à l\'horizontale) utilisé pour afficher les contraintes de rayon/diamètre dans Sketcher au moment de la création. La valeur par défaut est de 15 degrés (si aucune valeur n\'est définie).
-   **Mod/Sketcher/RadiusDiameterConstraintDisplayAngleRandomness** (flottant) : définit un angle aléatoire sur la valeur ci-dessus. La valeur est la plage de l\'angle aléatoire, centrée sur l\'angle de base. La valeur par défaut est 0 degré \-- désactivé \-- (si aucune valeur n\'est définie).
-   **PropertyView/AutoTransactionView** (booléen) : défini à `True` pour que les modifications des propriétés de l\'onglet View soient ajoutées à la pile d\'annulation (et donc annulables). La valeur par défaut est `False`.
-   **Selection/AutoShowSelectionView** (booléen) : défini à `True` pour que le volet de la vue de sélection s\'affiche automatiquement lorsque vous sélectionnez quelque chose. La valeur par défaut est `False`.
-   **Selection/singleClickFeatureSelect** (booléen) : défini à `False` pour désactiver la sélection en un seul clic d\'une fonction dans PartDesign. La valeur par défaut est `True`.
-   **TreeView/TreeViewStretchDescription** (booléen) : défini à `True` pour étirer la colonne \'Description\' dans la [Vue en arborescence](Tree_view/fr.md) vers le bord droit du volet. La valeur par défaut est `False`.
-   **View/Dimensions3dColor** (chaîne) : définit une valeur de couleur au format hexa `#RRGGBB` pour modifier la couleur d\'affichage des dimensions directes dans [Part Mesure linéaire](Part_Measure_Linear/fr.md).
-   **View/DimensionsAngularColor** (chaîne) : définit une valeur de couleur au format hexa `#RRGGBB` pour modifier la couleur d\'affichage de la dimension angulaire dans [Part Mesure angulaire](Part_Measure_Angular/fr.md).
-   **View/DimensionsDeltaColor** (chaîne) : définit une valeur de couleur au format hexa `#RRGGBB` pour modifier la couleur d\'affichage des dimensions orthogonales dans [Part Mesure linéaire](Part_Measure_Linear/fr.md).
-   **View/NavigationDebug** (booléen) : active la sortie de débogage des styles de navigation (à partir de la v0.19, seul le style de navigation Gesture a quelque chose à dire).
-   **View/SavePicture** (chaîne) : défini à **FramebufferObject**, **PixelBuffer** ou **CoinOffscreenRenderer** pour différentes méthodes de production d\'images à partir de la vue 3D.

### Exportation du nom de fichier par défaut 

-   **General/ExportDefaultFilenameMultiple** (chaîne de caractères) : définit le nom de fichier par défaut à utiliser lors de l\'exportation d\'objets multiples. La valeur par défaut est \"%F\".
-   **General/ExportDefaultFilenameSingle** (chaîne de caractères) : définit le nom de fichier par défaut à utiliser lors de l\'exportation d\'un objet unique. La valeur par défaut est \"%F-%P-\".

Ces deux options permettent l\'insertion automatique de diverses informations dans le nom du fichier, en utilisant les caractères de format suivants :

-   %F - le nom du fichier .FCStd (ou l\'étiquette, si elle n\'est pas encore enregistrée)
-   %Lx - l\'étiquette du ou des objets sélectionnés, séparés par le caractère \'x\'.
-   %Px - l\'étiquette du ou des objets sélectionnés et de leur premier parent, séparés par le caractère \'x\'.
-   %U - la date et l\'heure, en UTC, [ISO 8601](https://fr.wikipedia.org/wiki/ISO_8601)
-   %D - la date et l\'heure, dans le fuseau horaire local, [ISO 8601](https://fr.wikipedia.org/wiki/ISO_8601)

Tous les autres caractères sont traités littéralement. Si le nom de fichier résultant est illégal, il sera modifié lors de la sauvegarde, les caractères illégaux étant remplacés par le trait de soulignement (\_).

### Couleurs des étiquettes de contraintes dans Sketcher 

L\'étiquette dans Sketcher qui affiche l\'état en cours des contraintes (par exemple, \"Underconstrained\", \"Overconstrained\", \"Fully Constrained\", etc\...) peut être stylisée sur une base par état, soit à l\'aide de la feuille de style Qt, soit via les préférences de l\'utilisateur. Les préférences de l\'utilisateur sont prioritaires si elles ont été définies (dans **Mod/Sketcher/General**) :

-   **EmptySketchMessageColor** - Valeur par défaut à 50% d\'opacité noire.
-   **UnderconstrainedMessageColor** - Noir par défaut
-   **MalformedConstraintMessageColor** - Rouge par défaut
-   **ConflictingConstraintMessageColor** - Rouge par défaut
-   **RedundantConstraintMessageColor** - Rouge orangé par défaut
-   **PartiallyRedundantConstraintMessageColor** - Bleu royal par défaut
-   **SolverFailedMessageColor** - Rouge par défaut
-   **FullyConstrainedMessageColor** - Vert par défaut

## En rapport avec la souris 

-   **General/ComboBoxWheelEventFilter** (booléen) : défini à `True` pour que les widgets ne captent pas l\'événement de la molette de la souris et empêchent le défilement des zones défilantes. Nécessite le redémarrage de FreeCAD pour être pris en compte.
-   **View/GestureMoveThreshold** (entier): le curseur de la souris à distance (px) doit se déplacer pour entrer dans les modes de rotation ou de panoramique du style de navigation Gesture. La valeur par défaut est 5.
-   **View/GestureRollFwdCommand**, **View/GestureRollBackCommand** (chaîne): commandes à exécuter par des gestes de roulis de bouton de la souris de style de navigation Gesture.
-   **View/GestureTapHoldTimeout** (entier): définit le temps d\'attente (en millisecondes) pour passer en mode panoramique dans le style de navigation Gesture. Il peut être utile de l\'augmenter s\'il est difficile de faire glisser la géométrie dans l\'esquisse. La valeur par défaut est 700.

## Raccourcis clavier 

### Touche Echap 

-   **General/TasksKeyEsc** (booléen) : défini à `False` pour désactiver la touche **Echap** sortant du [Panneau des tâches](Task_panel/fr.md) dans tous les ateliers (c\'est-à-dire si le panneau des tâches a le focus).

## Ateliers particuliers 

-   L\'<img alt="" src=images/Workbench_TechDraw.svg  style="width:16px;"> [atelier TechDraw](TechDraw_Workbench/fr.md) dispose de plusieurs options masquées décrits dans [TechDraw Préférences](TechDraw_Preferences/fr#Paramètres_cachés.md).
-   L\'<img alt="" src=images/Workbench_Path.svg  style="width:16px;"> [atelier Path](Path_Workbench/fr.md) a une option pour activer les fonctionnalités expérimentales documentées dans [Path Fonctions expérimentales](Path_experimental/fr.md).
-   L\'<img alt="" src=images/Workbench_BIM.svg  style="width:16px;"> [atelier BIM](BIM_Workbench/fr.md) :
    -   **Mod/BIM/DefaultPageScale** (flottant) : mise à l\'échelle par défaut pour les nouvelles pages TechDraw créées à partir de l\'atelier BIM, au cas où le modèle ne contiendrait pas de champ de texte modifiable (insensible au texte) \"Échelle\" ou \"Mise à l\'échelle\".

## En relation 

-   [Editeur des paramètres](Std_DlgParameter/fr.md)
-   [Réglage des préférences](Preferences_Editor/fr.md)



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Developer Documentation](Category_Developer Documentation.md) > Fine-tuning/fr
