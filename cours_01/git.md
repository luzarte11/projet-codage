## 2. Git et GitHub

### 2.1. Introduction

Ce cours t&#39;introduira � Git et Github, deux fantastiques outils qui permettent de faire des sauvegardes efficaces d&#39;un projet, et de travailler � plusieurs sur le m�me dossier.

Dans cette le�on, nous allons te montrer comment installer Git, comment s&#39;en servir, et comment le faire marcher. Pour ceci, nous allons nous aider de l&#39;excellent [cours](https://openclassrooms.com/courses/gerer-son-code-avec-git-et-github) sur OpenClassrooms de Marc Gauthier, sur Git et GitHub.

#### 2.1.1. Ce que tu vas apprendre dans cette ressource

### 2.2. Historique

Git est un outil de versionning de code, c&#39;est � dire que c&#39;est une commande qui permet de faire des sauvegardes, avec commentaires d&#39;un projet. Ainsi, il est facile de revenir d&#39;une version de sauvegarde � l&#39;autre, et c&#39;est m�me optimis� pour les projets o� tout le monde travaille sur le m�me fichier !

En gros, c&#39;est la m�me chose quand vous fa�tes une grosse pr�sentation PPT. Vous faites tellement de modifications dessus que vous vous retrouvez � la fin avec le nom &quot;VF\_avec\_retours\_Jean01\_final.ppt&quot;. Le versionning vous permet d&#39;avoir toutes les versions sauvegard�es, et de revenir � celles que vous voulez � tout moment, et de nous �viter ces tracas.

Voil� � quoi Git sert : � mieux g�rer ses versions entre les fichiers d&#39;un projet (bonus : Git marche pour tous les fichiers d&#39;un dossier concern�, donc c&#39;est encore plus puissant que CTRL + S). Et GitHub permet de mettre en ligne ton projet, comme �a vous pourrez travailler facilement en �quipe dessus.

Pour information, Git a �t� cr�� en 2005 par Linus Torvald, qui a (entre autres) cr�� le syst�me d&#39;exploitation Linux.

### 2.3. Le cours

#### 2.3.1. Installer Git

Avant de pouvoir se servir de Git, il faut l&#39;installer. Cela tombe bien, il y a un [chapitre �ponyme](https://openclassrooms.com/courses/gerer-son-code-avec-git-et-github/installer-git) dans le cours sur OC.

#### 2.3.2. Premi�re introduction � Git

J&#39;ai fait une petite vid�o d&#39;introduction � Git, que tu pourras retrouver ci-bas :

Ensuite, tu peux suivre le cours de Marc Gauthier jusqu&#39;� la partie [R�cup�rez des modifications](https://openclassrooms.com/courses/gerer-son-code-avec-git-et-github/recuperer-des-modifications). Nous verrons dans la formation THP comment faire les branches et autres joyeuset�s ??

### 2.4. Points importants � retenir

#### 2.4.1. Les commandes pratiques

Voici un r�cap des commandes de base :

- $ git init : il faut TOUJOURS commencer par initialiser git avec cette commande. Avec cette commande, le r�pertoire courant est consid�r� comme un repository git
- $ git add [fichier] : ajoute aux sauvegardes le fichier mentionn�.  **Protip**  : si tu as plusieurs fichiers � ajouter, tu peux utiliser $ git add . qui ajoute au repository tous les fichiers du dossier
- $ git commit -m [commentaire] : cr�� un commit (commit = sauvegarde suivie d&#39;un commentaire).
- $ git status : te dit le status actuel de git.

#### 2.4.2. Lire l&#39;historique

$ git log : permet de voir l&#39;historique et de voir tous les commits. Les commits sont rang�s avec :

- SHA : liste de chiffres et lettres qui indentifient de fa�on unique le commit.
- Auteur
- Date
- Message donn� durant le commit : avec ce message, tu vas comprendre ce que faisait le commit. C&#39;est pour cela qu&#39;il est important d&#39;avoir un bon nom.

Pour quitter le log, il faut appuyer sur Q.

#### 2.4.3. Se positionner sur un commit donn�

Imaginons que veut v�rifier un truc sur un vieux commit. On va utiliser la commande $ git checkout, utilis�e comme ceci :

- $ git checkout 45581cebdd2cae494f80f44010af9e4a86c9b8fa : on dit � git de se positionner sur ce sha pr�cis.
- $ git checkout master : une fois que l&#39;on a fini de se balader, il faut revenir � la version pr�sente de notre repository avec cette commande

##### **??**  **ALERTE ERREUR COMMUNE**

$ git checkout ne marche que si tu n&#39;as pas de modification non sauvegard�e. Si tu es entre deux commits, git checkout ne marchera pas. Du coup il te faudra soit faire une sauvegarde (== faire un commit), soit effacer tout pour revenir au commit d&#39;avant.

$ git checkout n&#39;est pas une commande pour revenir en arri�re et faire des modifications sur les anciens commits. Si tu fais �a, tu vas te retrouver avec une erreur qui a donn� lieu � [l&#39;un des threads](https://stackoverflow.com/questions/5772192/how-can-i-reconcile-detached-head-with-master-origin) les plus c�l�bres de Stack Overflow. Pour tout effacer et revenir en arri�re, le chapitre suivant sera l� pour toi.

#### 2.4.4. Revenir en arri�re

J&#39;ai fait des trucs, mais cela ne me convient pas. Comment revenir sur en arri�re ? (inspir� par [cette excellente](https://stackoverflow.com/questions/4114095/how-to-revert-git-repository-to-a-previous-commit/4114122#4114122) r�ponse de Stack Overflow)

##### 2.4.4.1. Effacer pour revenir au commit d&#39;avant

La fonction $ git reset --hard permet de revenir au commit pr�c�dent, en effa�ant tout. C&#39;est une commande pratique quand on veut essayer de nouvelles choses � la vol�e, puis de revenir en arri�re comme si de rien n&#39;�tait ??

##### 2.4.4.2. Tout effacer et revenir � un ancien commit

On peut faire ceci avec : $ git reset --hard 45581cebdd2cae494f80f44010af9e4a86c9b8fa, avec _45581c_ le SHA sur lequel tu veux revenir.

### 2.5. Pour aller plus loin

Au vu des apologies que l&#39;on lui donne, le [cours de OpenClassrooms](https://openclassrooms.com/courses/gerer-son-code-avec-git-et-github) sur Git est un tr�s bon point pour aller plus loin. Il explique notamment la notion de branches et de fusions.

Aussi, voici [un cours](https://www.vikingcodeschool.com/web-development-basics/getting-to-know-git) sur Git de la Viking Code School. Il explique bien les bases de Git et est une bonne alternative au notre.