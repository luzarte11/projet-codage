## Lundi

### Le terminal, et Git

Le terminal, le fameux écran noir qui fait peur à tout le monde en dehors du monde du développement. Et bien aujourd&#39;hui, nous allons démystifier cet écran noir, et te montrer comment s&#39;en servir. Puis nous allons te montrer Git et GitHub, deux fantastiques outils pour gérer des projets.

À la fin de la journée, tu comprendras enfin ce que font les développeurs derrière leur écran noir, et comment ils travaillent.

-

### [Ressources](https://www.thehackingproject.org/precursus/1#collapseTwo)

-

## 1. Le terminal

### 1.1. Introduction

Dans cette ressource, tu vas découvrir les bases du terminal, un outil très puissant qui permet de &quot;parler&quot; à son ordinateur. Nous allons voir les bases : comment intéragir avec le terminal, comment jouer avec ses premiers fichiers, et bien d&#39;autres.

#### 1.1.1. Ce que tu apprendre dans cette ressource

Voici la liste des questions auxquelles tu vas pouvoir répondre avec cette ressource :

- Qu&#39;est-ce que le terminal ?
- Que veut dire GUI et CLI ?
- Comment lancer un terminal ?
- Comment exécuter ses premières fonctions avec un terminal ?
- Pourquoi la notion de géographie est très importante dans un terminal ?
- Qu&#39;est-ce que VIM et comment s&#39;en servir ?

### 1.2. Historique

Le terminal est ce que l&#39;on appelle plus communément un _interpréteur de commande_ (ou command-line interpreter (CLI) en anglais), est un outil qui permet d&#39;interpréter les commandes qu&#39;un utilisateur tape au clavier dans l&#39;interface en ligne de commande.

À la base, les ordinateurs tournaient sans interface graphique, donc les utilisateurs passaient exclusivement par les CLI. Avec l&#39;arrivée des systèmes d&#39;exploitation graphiques (Windows, Apple, Linux), le CLI n&#39;a pas perdu en popularité, puisqu&#39;il permet de faire des tâches extrêmement précises.

En gros, c&#39;est une version texte de l&#39;explorateur de fichiers : on peut ouvrir des dossiers, créer des fichiers, les lancer, les renommer, installer des programmes, et bien d&#39;autres choses. On dit que c&#39;est une  **CLI**  (Command Line Interface), comparée à la  **GUI**  (Graphical User Interface) de l&#39;explorateur normal. Tout est fait via clavier, donc pas besoin de souris dans le terminal.

### 1.3. Le terminal

#### 1.3.1. Qu&#39;est-ce que le terminal ?

Le terminal est un outil intimidant aux premiers abords, mais au final se révèle pas compliqué. J&#39;ai réalisé une vidéo qui explique le terminal :

#### 1.3.2. Comment le lancer ?

Sur Linux : CTRL + ALT + T
Sur macOS : CMD + SPACE, puis écrire Terminal (ou iTerm), Enter.

##### **??**  **ALERTE BONNE ASTUCE**

Si tu utilises Linux, passe ton terminal en anglais. Quand ce dernier te renverra une erreur, c&#39;est bien mieux qu&#39;elle soit en anglais. L&#39;anglais et la langue d&#39;internet, donc la majorité des gens qui ont eu ton problème vont le poster en anglais. Et ainsi tu auras 100 fois plus de résultats sur Google que si tu postais ton erreur en français.

#### 1.3.3. Premières fonctions ?

Pour faire marcher le terminal, rien de plus simple : il suffit de rentrer le texte correspondant à la fonction et cela s&#39;exécutera. Par exemple si dans l&#39;explorateur en GUI il suffit de double cliquer sur mon\_fichier.txt pour l&#39;ouvrir, il faudra faire dans le terminal open mon\_fichier.txt (sur macOS) ou xdg-open mon\_fichier.txt (sur Linux) pour l&#39;ouvrir avec le terminal. On va tester avec notre première fonction :

$ echo &quot;Hello world !&quot;

_(je commence toutes les commande du terminal avec un  __$__ , c&#39;est une convention, et c&#39;est plus facile à reconnaitre comme ceci)_

Si tu exécutes cette commande le terminal devrait te renvoyer Hello world ! (cette phrase est [un grand classique de la programmation](https://fr.wikipedia.org/wiki/Hello_world)). Et là, tu viens d&#39;exécuter ta première commande de terminal ??
Maintenant nous allons voir les premières commandes de base.

##### 1.3.3.1. PWD

pwd est l&#39;acronyme de Print Working Directory, une commande qui affiche le dossier dans lequel tu es actuellement.

$ pwd

Pour moi, pwd me renvoie :

/Users/felix

C&#39;est comme dans l&#39;explorateur en GUI, quand tu double-cliques sur felix, il te déplace dans le dossier felix qui est dans le dossier Users.

##### **??**  **ALERTE BONNE ASTUCE**

pwd est généralement la première commande que l&#39;on tappe quand on arrive dans le terminal de quelqu&#39;un : c&#39;est idéal pour s&#39;y retrouver ??

##### 1.3.3.2. LS

ls est le diminutif pour _list_, cette fonction affiche les fichiers et dossiers qu&#39;il y a dans mon dossier actuel.

$ ls

Pour moi, ls me renvoie :

Applications/   Dropbox/     Music/       Desktop/

Pictures/     Documents/    Library/     Public/

Downloads/    Movies/

Dans le terminal, nous pouvons donner des options aux fonctions, en faisant $ fonction -option. Par exemple, je peux faire ls -a, ce qui a pour effet d&#39;afficher aussi les fichiers commençant par un . (fichiers de devs en général), ou je peux faire ls -l pour afficher la liste au format long. Et je peux même combiner les deux en faisant ls -al pour afficher aussi les fichiers commençant par un ., tout au format long.

##### 1.3.3.3. MAN

man est le diminutif de _manual_. Man lance un programme qui permet de lire la manuel d&#39;une fonction précise. Pratique pour savoir toutes ses spécificités. Pour s&#39;en servir il suffit de tapper : man fonction. Par exemple pour afficher le manuel de ls, je dois taper :

$ man ls

Ce qui m&#39;ouvrira son manuel, qui je peux quitter à tout moment en tapant q.

#### 1.3.4. Où sommes-nous ?

Une notion  **fondamentale**  pour le terminal : la notion de géographie. Comme dans l&#39;explorateur en GUI, on se déplace de dossiers en dossiers dans le terminal. Si jamais tu veux ouvrir un fichier en tappant open file.txt (sur macOS) ou xdg-open file.txt (sur Linux) et que tu ne te trouves pas dans le bon dossier, le terminal te renverra une erreur. Un peu comme si tu essayais de double-cliquer sur file.txt dans le mauvais dossier : impossible car il n&#39;y est pas.

Tu vas devoir te déplacer donc de dossiers en dossiers pour ouvrir et intéragir avec les bons fichiers.

#### 1.3.5. CD

cd est l&#39;acronyme de _Change Directory_, qui te permet de naviguer entre dossiers. L&#39;équivalent d&#39;un double-clic sur un dossier en quelque sorte ??

$ cd nomdudossier

Tu te déplaceras dans le dossier nommé nomdudossier (s&#39;il existe dans le dossier dans lequel tu te trouves).

Tu peux aussi te déplacer vers le dossier parent en faisant $ cd ..

##### **??**  **ALERTE BONNE ASTUCE**

Utiliser la touche TAB permet de faire de l&#39;autocompletion, très pratique pour cette méthode. Aussi, faire cd + [ESPACE] + TAB + TAB affiche les dossiers disponibles.

#### 1.3.6. Autres fonctions

##### 1.3.6.1. Créer un fichier

En tapant :

$ touch nomdufichier

Cela aura pour effet de créer un fichier qui s&#39;appelle _nomdufichier_

##### 1.3.6.2. Copier

Pour copier un fichier ou un dossier d&#39;un endroit à un autre, il suffit de rentrer :

$ cp fichier\_à\_copier lieu\_de\_destination

##### 1.3.6.3. Déplacer

Pour déplacer (couper) un fichier ou un dossier d&#39;un endroit à un autre, il suffit de rentrer :

mv [fichier\_à\_déplacer] [lieu\_de\_destination]

**Protip**  : mv est très pratique pour renommer un fichier. Imaginons que tu as créé un fichier &quot;hello.rv&quot; au lieu de &quot;hello.rb&quot;. Oups, malheur. Heureusement, faire $ mv hello.rv hello.rb résoud ceci en quelques coups de clavier !

##### 1.3.6.4. Remove

Supprimer un fichier :

$ rm nomdufichier

Il est possible d&#39;effacer un dossier ainsi que son contenu en ajoutant la récursion en option :

$ rm -r nomdudossier

##### **??**  **INSTANT CULTURE GÉ**

rm est à l&#39;origine d&#39;une blague vieille comme le monde. En effet, ajouter l&#39;option -f permet de forcer la suppression d&#39;un fichier, même s&#39;il est important pour l&#39;ordinateur, et finir par / ou \* dit à votre ordinateur de prendre absolument tous les fichiers. Ainsi, si tu tapes $ rm -rf / ou $ rm -rf \* dans ton terminal, tu dis à ce dernier de tout prendre et de tout effacer, en forçant. Et figure toi que rm est très rapide, et donc effacera l&#39;intégralité de ton ordinateur en quelques secondes à peine.  **À ne jamais jamais jamais faire**  donc.

##### 1.3.6.5. Vim

Vim est un des éditeurs de texte les plus respectés au monde. Comme il passe uniquement par le terminal, il se marie extrêmement bien avec cet outil. Et comme vim utilise exclusivement le clavier, ses raccourcis permettent d&#39;aller extrêmement vite, pour qui ose grimper la très dure courbe d&#39;apprentissage (quelques semaines à plein temps). De ce fait, je te montrerai vim pour ta culture générale, mais te demanderai de passer par un autre éditeur de texte ??

$ vim nomdufichier

Permet d&#39;ouvrir vim sur le fichier _nomdufichier_ et de l&#39;éditer. Pour quitter vim, il faut rentrer :q!.

#### 1.3.7. Autres astuces

CTRL + C annule la fonction en cours. Pratique quand on a une boucle infinie.

La casse est très importante, idem pour les espaces.

Il y a des raccourcis pratiques, par exemple CTRL + U efface la ligne en cours.

Les touches du haut et du bas permettent de naviguer dans l&#39;historique des commandes. Très pratique pour par exemple re-éxécuter une commande que tu viens de faire.

### 1.4. Les points importants

Voici les points à retenir de la ressource :

- Pour lancer le terminal sur Linux : CTRL + ALT + T ; pour le lancer sur macOS : CMD + SPACE, puis écrire Terminal (ou iTerm), Enter.
- man est le manuel est permet de lancer la manuel des fonctions
- pwd affiche le dossier dans lequel tu es actuellement.
- ls est une commande qui affiche les fichiers et dossiers qu&#39;il y a dans mon dossier actuel
- la notion de géographie est fondamentale : le terminal n&#39;arrivera pas à ouvrir les fichiers s&#39;il ne se trouve pas dans le bon dossier
- cd permet de changer de dossier
- touch permet de créer un fichier
- cp permet de copier un fichier
- mv permet de déplacer un fichier ou un dossier
- rm permet de supprimer un fichier

### 1.5. Aller plus loin

Voici un excellent [cours express](https://www.vikingcodeschool.com/web-development-basics/a-command-line-crash-course) pour avoir quelques base sur le terminal. Il est un peu similaire au mien, mais aborde d&#39;autres sujets intéressants tels que le PATH.

Viking Code School ont aussi fait un [cours sur le pimp de terminal](https://www.vikingcodeschool.com/web-development-basics/a-command-line-crash-course) pour avoir plein de couleurs de BGs sur le tien.

Michael Hartl a fait une célèbre introduction au terminal nommée [Learn Enough Command Line to Be Dangerous](https://www.learnenough.com/command-line-tutorial). Cette ressource permet d&#39;aller assez loin en détails dans le terminal.

Pour ceux qui veulent découvrir Vim, voici [une marche à suivre](https://medium.com/actualize-network/how-to-learn-vim-a-four-week-plan-cd8b376a9b85) pour être champion de Vim rapidement.