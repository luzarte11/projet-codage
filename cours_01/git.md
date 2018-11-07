## 2. Git et GitHub

### 2.1. Introduction

Ce cours t&#39;introduira à Git et Github, deux fantastiques outils qui permettent de faire des sauvegardes efficaces d&#39;un projet, et de travailler à plusieurs sur le même dossier.

Dans cette leçon, nous allons te montrer comment installer Git, comment s&#39;en servir, et comment le faire marcher. Pour ceci, nous allons nous aider de l&#39;excellent [cours](https://openclassrooms.com/courses/gerer-son-code-avec-git-et-github) sur OpenClassrooms de Marc Gauthier, sur Git et GitHub.

#### 2.1.1. Ce que tu vas apprendre dans cette ressource

### 2.2. Historique

Git est un outil de versionning de code, c&#39;est à dire que c&#39;est une commande qui permet de faire des sauvegardes, avec commentaires d&#39;un projet. Ainsi, il est facile de revenir d&#39;une version de sauvegarde à l&#39;autre, et c&#39;est même optimisé pour les projets où tout le monde travaille sur le même fichier !

En gros, c&#39;est la même chose quand vous faîtes une grosse présentation PPT. Vous faites tellement de modifications dessus que vous vous retrouvez à la fin avec le nom &quot;VF\_avec\_retours\_Jean01\_final.ppt&quot;. Le versionning vous permet d&#39;avoir toutes les versions sauvegardées, et de revenir à celles que vous voulez à tout moment, et de nous éviter ces tracas.

Voilà à quoi Git sert : à mieux gérer ses versions entre les fichiers d&#39;un projet (bonus : Git marche pour tous les fichiers d&#39;un dossier concerné, donc c&#39;est encore plus puissant que CTRL + S). Et GitHub permet de mettre en ligne ton projet, comme ça vous pourrez travailler facilement en équipe dessus.

Pour information, Git a été créé en 2005 par Linus Torvald, qui a (entre autres) créé le système d&#39;exploitation Linux.

### 2.3. Le cours

#### 2.3.1. Installer Git

Avant de pouvoir se servir de Git, il faut l&#39;installer. Cela tombe bien, il y a un [chapitre éponyme](https://openclassrooms.com/courses/gerer-son-code-avec-git-et-github/installer-git) dans le cours sur OC.

#### 2.3.2. Première introduction à Git

J&#39;ai fait une petite vidéo d&#39;introduction à Git, que tu pourras retrouver ci-bas :

Ensuite, tu peux suivre le cours de Marc Gauthier jusqu&#39;à la partie [Récupérez des modifications](https://openclassrooms.com/courses/gerer-son-code-avec-git-et-github/recuperer-des-modifications). Nous verrons dans la formation THP comment faire les branches et autres joyeusetés ??

### 2.4. Points importants à retenir

#### 2.4.1. Les commandes pratiques

Voici un récap des commandes de base :

- $ git init : il faut TOUJOURS commencer par initialiser git avec cette commande. Avec cette commande, le répertoire courant est considéré comme un repository git
- $ git add [fichier] : ajoute aux sauvegardes le fichier mentionné.  **Protip**  : si tu as plusieurs fichiers à ajouter, tu peux utiliser $ git add . qui ajoute au repository tous les fichiers du dossier
- $ git commit -m [commentaire] : créé un commit (commit = sauvegarde suivie d&#39;un commentaire).
- $ git status : te dit le status actuel de git.

#### 2.4.2. Lire l&#39;historique

$ git log : permet de voir l&#39;historique et de voir tous les commits. Les commits sont rangés avec :

- SHA : liste de chiffres et lettres qui indentifient de façon unique le commit.
- Auteur
- Date
- Message donné durant le commit : avec ce message, tu vas comprendre ce que faisait le commit. C&#39;est pour cela qu&#39;il est important d&#39;avoir un bon nom.

Pour quitter le log, il faut appuyer sur Q.

#### 2.4.3. Se positionner sur un commit donné

Imaginons que veut vérifier un truc sur un vieux commit. On va utiliser la commande $ git checkout, utilisée comme ceci :

- $ git checkout 45581cebdd2cae494f80f44010af9e4a86c9b8fa : on dit à git de se positionner sur ce sha précis.
- $ git checkout master : une fois que l&#39;on a fini de se balader, il faut revenir à la version présente de notre repository avec cette commande

##### **??**  **ALERTE ERREUR COMMUNE**

$ git checkout ne marche que si tu n&#39;as pas de modification non sauvegardée. Si tu es entre deux commits, git checkout ne marchera pas. Du coup il te faudra soit faire une sauvegarde (== faire un commit), soit effacer tout pour revenir au commit d&#39;avant.

$ git checkout n&#39;est pas une commande pour revenir en arrière et faire des modifications sur les anciens commits. Si tu fais ça, tu vas te retrouver avec une erreur qui a donné lieu à [l&#39;un des threads](https://stackoverflow.com/questions/5772192/how-can-i-reconcile-detached-head-with-master-origin) les plus célèbres de Stack Overflow. Pour tout effacer et revenir en arrière, le chapitre suivant sera là pour toi.

#### 2.4.4. Revenir en arrière

J&#39;ai fait des trucs, mais cela ne me convient pas. Comment revenir sur en arrière ? (inspiré par [cette excellente](https://stackoverflow.com/questions/4114095/how-to-revert-git-repository-to-a-previous-commit/4114122#4114122) réponse de Stack Overflow)

##### 2.4.4.1. Effacer pour revenir au commit d&#39;avant

La fonction $ git reset --hard permet de revenir au commit précédent, en effaçant tout. C&#39;est une commande pratique quand on veut essayer de nouvelles choses à la volée, puis de revenir en arrière comme si de rien n&#39;était ??

##### 2.4.4.2. Tout effacer et revenir à un ancien commit

On peut faire ceci avec : $ git reset --hard 45581cebdd2cae494f80f44010af9e4a86c9b8fa, avec _45581c_ le SHA sur lequel tu veux revenir.

### 2.5. Pour aller plus loin

Au vu des apologies que l&#39;on lui done, le [cours de OpenClassrooms](https://openclassrooms.com/courses/gerer-son-code-avec-git-et-github) sur Git est un très bon point pour aller plus loin. Il explique notamment la notion de branches et de fusions.

Aussi, voici [un cours](https://www.vikingcodeschool.com/web-development-basics/getting-to-know-git) sur Git de la Viking Code School. Il explique bien les bases de Git et est une bonne alternative au notre.
