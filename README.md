# Le Knowledge Base (alias LKB)

## Présentation

Le Knowledge Base, ou LKB, est une application **portable** de prise et de recherche de notes, faite avec amour (et sueur !).  
Depuis très longtemps jusqu'à 2021, j'ai tâtonné, tâtonné et tâtonné jusqu'à enfin arriver à une méthode de gestion de la connaissance qui me satisfasse vraiment. Cette méthode manquait de l'outil parfaitement adéquat, et c'est ce qui a donné naissance à LKB.  
J'espère que vous en trouverez bon usage à votre tour, peut-être même au point de l'intégrer entièrement à vos flux de travail personnels et/ou professionnels.  

## Installation

Je rappelle que l'application est portable donc c'est plus un démarrage qu'une installation ;).
- Récupérez le dossier qui correspond à votre machine, entre `Windows_x64_Self-Contained` ou `Linux_x64_Self-Contained`, et mettez-le où bon vous semble.
- Démarrez `LeKnowledgeBase_CrossPlatform` (sur Linux il faudra peut-être faire un `chmod u+x LeKnowledgeBase_CrossPlatform` avant), qui est le fichier avec le petit logo.
- Vous pouvez l'utiliser immédiatement, ou bien modifier le fichier de configuration `LeKnowledgeBase_CrossPlatform.dll.config` pour par exemple faire pointer l'appli vers un autre dossier de notes (plus d'explications dans la suite de ce document).

## Mise à jour

Remplacez tous les fichiers du dossier des exécutables par ceux du dossier de la dernière version que vous aurez téléchargée, tout en conservant :
- Votre dossier de notes
- `LeKnowledgeBase_CrossPlatform.dll.config` actuel (pour ne pas avoir à recommencer la config)

## Aspects techniques à comprendre

- Une note textuelle <=> un fichier Markdown (.md) à la racine du dossier. Un fichier .md est fondamentalement un fichier texte. En savoir plus sur le Markdown peut permettre d'optimiser votre expérience, mais n'est pas indispensable.
- L'application n'est qu'une interface qui permet d'interagir avec vos notes qui sont donc de simples fichiers texte. Si l'appli casse ou disparaît, vous ne devriez pas perdre vos notes.
- Ces fichiers textes sont sur votre ordi et l'appli ne les enverra jamais à l'extérieur.

## Suggestions d'utilisation

- Ayez votre dossier de notes **à l'extérieur** du dossier contenant les exécutables.
- Nommez vos notes en vous demandant par quels termes vous la chercherez lorsque vous en aurez besoin dans 1 an.
- "Backuppez" vos notes par un moyen extérieur, par une solution de type cloud par exemple. Personnellement j'utilise git et gitlab.
- Si vous n'avez pas le temps de bien choisir vos mots au moment de la prise de note, ajoutez au nom de la note un tag (par ex "[mal nommé]), et vous la renommerez plus tard pour bien choisir vos mots.
- Informez-vous sur le Markdown et essayez de l'utiliser dans votre vie bureautique dès que c'est pertinent.

## Questions et réponses

***Le dossier peut-il contenir d'autres choses que des notes ?***  
=> Oui, si vous le voulez, notamment c'est utile pour contenir un dossier .git ;)

## Toutes les fonctionnalités

### Recherche rapide
- `Ctrl`+`F` : Met la focalisation sur la barre de filtre (et préselectionne tout le texte)
- `Alt`+`F` : Idem 

### Copie rapide
- Faire clic-droit sur une cellule copie son contenu dans le presse-papier  
- `Alt`+`J` : Copie le contenu de la première note de la grille dans le presse-papier  
- `Alt`+`K` : Copie le contenu de la deuxième note de la grille dans le presse-papier  
- `Alt`+`L` : Copie le contenu de la troisième note de la grille dans le presse-papier  
- `Alt`+`M` : Copie le contenu de la quatrième note de la grille dans le presse-papier  

### Édition rapide
- `Ctrl`+`J` : Démarre l'édition de la première note de la grille  
- `Ctrl`+`K` : Démarre l'édition de la deuxième note de la grille  
- `Ctrl`+`L` : Démarre l'édition de la troisième note de la grille  
- `Ctrl`+`M` : Démarre l'édition de la quatrième note de la grille  
- `Ctrl`+`Maj`+`J` : Démarre le renommage de la première note de la grille  
- `Ctrl`+`Maj`+`K` : Démarre le renommage de la deuxième note de la grille  
- `Ctrl`+`Maj`+`L` : Démarre le renommage de la troisième note de la grille  
- `Ctrl`+`Maj`+`M` : Démarre le renommage de la quatrième note de la grille  
- `Ctrl`+`S` : Enregistre l'édition en cours sans perdre la main sur l'édition (pour le Contenu seulement ; pour les mots-clés il y a perte de la main pour - rester cohérent avec le cas où la note doit disparaître de la grille suite au renommage)  
- `Ctrl`+`T` (pendant l'édition d'une case contenu) : supprime l'espace blanc en début de ligne commun à toutes les lignes  
- `Ctrl`+`Entrée` : Enregistre l'édition en cours en quittant l'édition  
- `Ctrl`+`Entrée` : Crée la note en cours de création  
- `Alt`+`Haut` : Échange la ligne courante avec la ligne au-dessus  
- `Alt`+`Down` : Échange la ligne courante avec la ligne en-dessous  

### Configuration
- Le seul et unique fichier de configuration est `LeKnowledgeBase_CrossPlatform.dll.config`, qui est à côté de `LeKnowledgeBase_CrossPlatform.exe`. Vous pouvez y changer les valeurs de certaines clés décrites ci-après.
- `pathRootFolderNotes` : indique le chemin (relatif ou absolu) du dossier comprenant toutes vos notes. L'application en créera un par défaut mais vous pouvez le changer.
- `windowTitle` : Définit le titre de la fenêtre dans la barre de titre et la barre des tâches.
- `synonymsFilePath` : indique le chemin du fichier qui définit vos synonymes (voir la section sur la fonctionnalité de synonymie). L'application en fixe (un chemin et un fichier) par défaut mais vous pouvez les changer.
- `keyWords_FontSize` : taille de police de la colonne `Mots-Clés` de la grille (supprimez la clé entièrement pour laisser l'application (re)mettre la valeur par défaut)
- `content_FontSize` : taille de police de la colonne `Contenu` de la grille (supprimez la clé entièrement pour laisser l'application (re)mettre la valeur par défaut)
- `encodingWanted` : Si par malheur vous devez utiliser des notes encodées en Windows 1252, indiquez "windows 1252".
- `executeFile_OpenNoteWithDefaultApp`, `executeFile_Arguments`, `executeFile_UseShellExecute`, `executeFile_FileName` : cf. chapitre dédié "Boutons personnalisables"

### Boutons de tout en haut
- Engrenage : Ouvre le fichier de configuration `LeKnowledgeBase_CrossPlatform.dll.config` (sélectionner un éditeur de texte au besoin)  
- Dossier : Ouvre le dossier contenant les notes  
- I : Ouvre le README.md
- Point de géolocalisation : Ouvre le dossier contenant les exécutables de l'application

### Synonymie (à la recherche)
Vous pouvez configurer une liste de groupes de synonymes dans un fichier texte. Cela permet de chercher un terme avec un de ses synonymes à la place.  
Le chemin du fichier text est défini dans la valeur de `synonymsFilePath` dans le fichier de configuration  
Normalement, les modifications faites au fichier de synonymes sont immédiatement prises en compte.

### Cacher des notes dans la grille
Ajouter `[hidden]` dans le nom d'une note la rend invisible dans la grille sauf si vous entrez entièrement `[hidden]` dans la barre de filtre  

### Notes sous forme d'image
Les notes sous forme d'image (png, jpg, bmp) peuvent être affichées et renommées, mais ne peuvente être ajoutées par LKB, elles doivent être ajoutées au dossier des notes par d'autres moyens.  

### Les boutons personnalisables (éclair et œil)

Par défaut, ces boutons ouvrent la note sous forme de fichier avec l'application par défaut configurée dans votre système d'exploitation.  

#### Le bouton "éclair" jaune

***Tableau des valeurs des clés de configuration :***

| Mode voulu du bouton :arrow_right: <br/> × <br/>Nom de la clé  :arrow_down: | Le bouton ouvre la note avec l'application par défaut¹ | Le bouton exécute l'équivalent de `monApp.exe nom_de_la_note.md` | Le bouton exécute l'équivalent de `monApp.exe --option1 nom_de_la_note.md` | Le bouton exécute l'équivalent de `monScript.sh nom_de_la_note.md` où `monScript.sh` est lui-même exécuté par l'application par défaut¹ | Le bouton exécute l'équivalent de `monScript.sh --option1 nom_de_la_note.md` où `monScript.sh` est lui-même exécuté par l'application par défaut¹ |
|---|---|---|---|---|---|
| `executeFile_OpenNoteWithDefaultApp` | `"True"` | `"False"` | `"False"`| `"False"`| `"False"` |
| `executeFile_FileName` |*Ignoré, peut même être supprimé* | `"chemin/vers/monApp.exe"` | `"chemin/vers/monApp.exe"` | `"chemin/vers/monScript.sh"` |  `"chemin/vers/monScript.sh"` |
| `executeFile_UseShellExecute` | *Ignoré, peut même être supprimé*  | `"False"` | `"False"` | `"True"` | `"True"` |
| `executeFile_Arguments` |*Ignoré, peut même être supprimé* | `""` | `"--option1"` | "" | `"--option1"` |

¹ : *par défaut définie au niveau du système d'exploitation (c'est-à-dire celle utilisée lorsque vous double-cliquez la note dans l'explorateur de fichiers)*

#### Le bouton "œil" bleu

Idem avec le suffixe `2` (`executeFile_OpenNoteWithDefaultApp2`, `executeFile_FileName2`, `executeFile_UseShellExecute2`, `executeFile_Arguments2`)

----------

## Patch updates

v2.5.1   (2023-02-17) : Acrylic Background : visual noise in the background is added ; this grainy look looks prettier to me and possibly easier on the eyes. Linux user still don't have the transparent blur, but they do get the noise which is pretty nice. // now a selected note has a big cell height, not only a scrollable cell  
v2.5.0   (2023-01-28) : Filter TextBox : ctrl+s saves // [FileWatcher] adding a hopefully fully functional file watcher // decrease top margin of filterbar // Background is dimgray if the acrylic blur doesn't work (enables contrasts when there were actual black background), typically on Ubuntu. // [Visual improvements] optimizing icons centering and replacing the book icon by the infolargeoutline icon because the book one is ugly  
v2.4.4   (2023-01-28) : [Keybindings][Quick Edit] Ctrl+shift+J/K/L/M gives focus to the 1st/2nd/3rd/4th keywords cell of the grid  
v2.4.3   (2023-01-27) : [Top Buttons] Added an "Open README" button, and optimizing button appearance // [Editor improvements] Ctrl+t now removes leading whitespace offset (useful for pasting code with useless indentation) // [Keybindings] Ctrl+s now works on the filter bar too // Removing the .config in the source files to lessen the risk of overriding the user's when updating LKB manually (which is currently the only way to do it).  
v2.4.2   (2023-01-25) : [Configuration] Fontsizes in the grid is now configurable // [Filter Bar] adding a grid splitter // [TextBox edition] You can swap a line with the above/below one with alt+up/down. The command is ignored if there is a selection active. // [Top buttons] There is one more button, the open config file (Cog button ; the open binary folder is now the one with the "location" icon) // [Visuals] Grey border all around the window, slimmer left col, slimmer minimal row height.  
~~v2.5.0   (?) : [Feature : file watcher] A watcher listens for changes in the notes directory. If a file is renamed, deleted, created, or changed, the changes are reflected in the grid. If there are pending changes, they are kept. // [TextBox edition] You can swap a line with the above/below one with alt+up/down. The command is ignored if there is a selection active. // [Top buttons] There is one more button, the open config file (Cog button ; the open binary folder is now the one with the "location" icon) // [Visuals] Grey border all around the window, slimmer left col, slimmer minimal row height.~~  
v2.4.1   (2023-01-19) : initial fetch of notes orders them in linguistic order // minimize row height difference between pure read state and selected state // bugfix : windowTitle was not updating on the UI after hitting the refresh button  
v2.4.0   (2023-01-08) : [feature: custom buttons] two custom buttons (yellow lightning and blue eye) are now usable. See documentation below. // [new shortcut: ctrl+s and ctrl+enter] Ctrl+S commit changes without losing focus (only on "Content" cells), ctrl+enter commits changes and stops editing. // Cog and Folder button should now work on Linux too // The filtering string is updated to its trimmed version after successful note creation // The "new content" textbox uses my corrected key handling // [visual] add corner radius to the focus border // new tutorial notes  
**Custom buttons**  
***Tableau des valeurs des clés de configuration pour le bouton "éclair" jaune:***  

| Mode voulu du bouton :arrow_right: <br/> × <br/>Nom de la clé  :arrow_down: | Le bouton ouvre la note avec l'application par défaut¹ | Le bouton exécute l'équivalent de `monApp.exe nom_de_la_note.md` | Le bouton exécute l'équivalent de `monApp.exe --option1 nom_de_la_note.md` | Le bouton exécute l'équivalent de `monScript.sh nom_de_la_note.md` où `monScript.sh` est lui-même exécuté par l'application par défaut¹ | Le bouton exécute l'équivalent de `monScript.sh --option1 nom_de_la_note.md` où `monScript.sh` est lui-même exécuté par l'application par défaut¹ |
|---|---|---|---|---|---|
| `executeFile_OpenNoteWithDefaultApp` | `"True"` | `"False"` | `"False"`| `"False"`| `"False"` |
| `executeFile_FileName` |*Ignoré, peut même être supprimé* | `"chemin/vers/monApp.exe"` | `"chemin/vers/monApp.exe"` | `"chemin/vers/monScript.sh"` |  `"chemin/vers/monScript.sh"` |
| `executeFile_UseShellExecute` | *Ignoré, peut même être supprimé*  | `"False"` | `"False"` | `"True"` | `"True"` |
| `executeFile_Arguments` |*Ignoré, peut même être supprimé* | `""` | `"--option1"` | "" | `"--option1"` |

¹ : *par défaut définie au niveau du système d'exploitation (c'est-à-dire celle utilisée lorsque vous double-cliquez la note dans l'explorateur de fichiers)*  

Bouton œil bleu : Idem avec le suffixe `2` (`executeFile_OpenNoteWithDefaultApp2`, `executeFile_FileName2`, `executeFile_UseShellExecute2`, `executeFile_Arguments2`)  

v2.3.5   (2023-01-08) : Synonyms file: can now contain emptylines // Synonyms: a term A can be in groups A,B and A,C ; A will search for A,B,C, while B will still search for A,B and C for A,C // Visuals : cells in column other than Mots-Clés and Content won't turn background to black // Add Button : turns to grey when a note was just added  
v2.3.4   (2023-01-08) : default notes folder is now a sibling of the app folder, not a child  
v2.3.3   (2023-01-08) : **Bugs corrections :** TextBox improvements : First/last line detection is now detected also when there is only one line // A note newly added wouldn't update its display on the view //  
All text of FilterBox is selected when accessed with ctrl/alt+f  
**Visual improvements** : Focus happens just for one cell, not the whole line. Ugly focus white border is GONE (FINALLY). Hello pretty border. Hello coloured carets. Hello nice selection colours. Fixed paddings  
v2.3.0   (2023-01-07) : **Features** : when user is a first-time user, tutorial and mock notes are inserted to his initial database // **TextBox improvements** : when last line is an empty line and that caret was on the line before it, going down would do nothing. now it actually moves to the last line. // **Bugs corrections :** Correcting tooltip conflict, and buffer behaviour when trimming is applied  
v2.2.5   (2023-01-05) :  
**Features**  
- right clicking on a cell copies its content.
- content cell is scrollable when row is selected
- On edit, content cell gets bigger but smaller than the grid. Is scrollable. Solves the problem of the view not following the caret when typing (this issue is absent in wpf).
- vertical scrollbar for fine-positioning

**Visual improvements**:
- Datagrid headers

**TextBox improvements (or rather corrections, Avalonia's current textbox sucks…)**
- going right when being one position before the end of the line gets you to the end of the line instead of the beginning of next line
- going up when on first line or going down when on last line wont get you out of the textbox anymore

**Bugs correction**
- refresh button wasnt reinitializing synonyms

v2.2.0   (2023-01-04) : Quick copy feature (Press alt + j/k/l/m to copy the 1st/2nd/3rd/4th content. Works for bépo users with corresponding keys i.e. t/s/r/n). // read and edit content : font size bumped up from 10 to 11. // small visual tweaks and trying the acrylic border  
v2.1.1   (2023-01-03) : Embed Jetbrains Mono // Window title in also in taskbar // Adding the bird icon for the assembly  
v2.1.0   (2023-01-03) : a note that has pending notifications (=dirty) on keywords (or content) shows with blue background and a tooltip // Note images are now displayed and can be renamed, but not added or modified  
v2.0.2   (2023-01-03) : failing keyword updating through interface : user cant create note if the note name is empty or the one of an existing one // Error messages talk about empty keywords // Tooltip on add button // Correct bug on modifying a note  
v2.0.0   (2023-01-03) : Following features work :  

**Quick Edit**  
Ctrl+J : Triggers editing the content of the first note of the grid  
Ctrl+K : Triggers editing the content of the second note of the grid  
Ctrl+L : Triggers editing the content of the third note of the grid  
Ctrl+M : Triggers editing the content of the fourth note of the grid  

**Configuration**  
pathRootFolderNotes : it understands environment variables so typically "%userprofile%\Documents\KnowledgeDatabase_Dev\" would work  

**Top Buttons**  
Cogs   : opens the folder containing the app [2022-11-28]  
Folder : opens the folder containing the notes [2022-11-28]  

**Synonyms feature (at search)**  
You can configure a set of (strict) synonym groups in a text file. You can search for a term with one of its synonyms instead.  
The text file path is in synonymsFilePath 's value in the config file.  
Hit refresh button to refresh the synonyms from your list.  
***Advice*** : the feature was built with *strict* synonymy in mind.  

**"Hidden" feature**  
Adding `[hidden]` to a note's title makes it invisible on the grid unless you explicitely and entirely type [hidden] in the filter box  
