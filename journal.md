# Journal de bord du projet encadré
## Semaine 1

On a commencé par une présentation du cours, et notamment du projet titulaire, qui consistera en l’étude d’un mot et des ses variations en plusieurs langues sur le web, le tout en groupe de 3, groupe idéalement constitué d’un élève pour chaque université.

On a ensuite introduit le concept de *pipelines* unix, l’enchaînement de petits outils en ligne de commande, chacun faisant une tâche simple et précise, afin de réaliser au final des tâches plus complexes. Le tout avec une mise en avant ici du traitement de données textuelles (e.g., recherche avec `grep`, tri avec `sort`, mesure de longueur (lignes/mots/octets) avec `wc`).

Après cette petit mise on bouche, on a été introduit à la philosophie Unix, système où tout est fichier, même les périphériques. L’occasion ainsi de faire un petit tour de présentation des concepts généraux permettant de travailler avec des fichiers, notamment en ligne de commande, via les notions de chemin et d’arborescence. En particuliers, la différence entre un chemin absolu (qui part de la racine de l’arborescence, `/`, e.g., `/home/niluje/Documents`) et un chemin relatif (chemin relatif au dossier courant, aussi appelé dossier de travail, e.g., `./Documents` pointera au même endroit que l’exemple précédent si je me trouve dans mon dossier utilisateur). On peut aussi utiliser `.`pour référer de manière explicite au dossier actuel (e.g., `./Documents/./PPE/.` serait une manière extrêmement explicite de simplement dire `Documents/PPE`), et `..`pour référer au parent d’un dossier (e.g., depuis mon dossier utilisateur, `../../../../../home/niluje/Documents` pointe tout simplement vers `Documents`).

On enchaîne ensuite sur le shell Unix, qui est notre interface pour interagir avec tous ces fichiers depuis la ligne de commande. On commence à tester en particulier le concept de `globbing` du shell, qui permet d’utiliser des *wildcards* pour faire des remplacements automatiques. On note ainsi la possibilité d’utiliser des classes de caractères comme `[a-z]`pour remplacer une occurence de n’importe quel caractère alphabétique minuscule, ou le `?`, qui remplace une seule occurence de n’importe quel caractère, ou le `*`, qui remplace de 0 à une infinité de caractères.

On enchaîne ensuite sur la présentation de quelques commandes, ainsi que du concept d’arguments, et d’un type particulier d’arguments, les options, qui nous permettent de configurer la manière dont certains outils fonctionnent (dans la limite des possibilités offertes par le programme en question ;)).
On peut citer en particulier la commande `man`, l’autre meilleur ami de l’homme, car elle nous permet d’accéder aux manuels d’utilisation d’une myriade de choses, que ce soit des outils en ligne de commande, ou des fonctions C pour interagir avec le système.

Puis vient le moment fatidique de la mise en pratique, nous invitant à manipuler diverses commandes afin de trier proprement une liste de fichiers en vrac. On observe le fouillis initial avec `ls -lash`, on crée notre arborescence avec `mkdir -p`, on déplace les fichiers au bon endroit en jouant avec `mv` et des *wildcards*, puis on vérifie le résultat avec `tree`, qui nous offre une vision claire d’une arborescence de fichier.

## Semaine 2

Initiation à git & GitHub pour tout le monde. Bonne chance à ceux qui ne l'utilisent pas depuis presque 15 ans ;p.

Introduction rapide de git en tant que VCS décentralisé, puis création d’une paire de clés SSH et intégration avec GitHub pour sécuriser les transactions.
Petit tour des sous-commande de base de git, `clone`pour copier un dépôt distant, `fetch` pour réceptionner les méta-données distantes, `pull` pour mettre à jour une branche locale, `add` pour ajouter des modifications locales au suivi, `rm`  pour retirer du suivi, `commit`pour valider les modifications des fichiers suivis, `push`pour envoyer nos modifications locales validées vers le dépôt distant, `status` pour faire le point sur les changements locaux et les différences avec le dépôt distant, `log` pour afficher le journal des changements, `tag` pour gérer les étiquettes.

Mise en pratique avec un mix de travail via l'interface web GH et la CLI (i.e., ce dépôt). Création du dépôt via l’interface web, clone local du nouveau dépôt, ajout du journal au dépôt via l’interface web, mise à jour du journal en local, puis création d’un `.gitgnore` avant de commit & tag le tout.
