# Utilisation du terminal

Aide pour les commandes Unix : man (MANual). Ouvrez un terminal. Par défaut, vous êtes dans votre espace de travail (home).



Affichez les éléments contenus dans le répertoire principal (racine ~ = ou "répertoire home") en utilisant la commande ls.

Si le répertoire principal ne contient pas un sous-répertoire nommé 'Documents',

créez-le en utilisant la commande mkdir.

Depuis 'Documents', créez un sous-répertoire nommé 'Septembre_2018'. Pour se déplacer d'un répertoire à un autre, utilisez la commande cd.

Créez deux fichiers 'tp1.py' et 'tp2.py' dans le dossier 'Septembre_2018'.

Pour cela, utilisez la commande touch.

Quelle est la commande qui affiche à l'écran le nom de votre répertoire courant ?

Écrivez les commandes qui vous permettent d'aller dans le répertoire principal et d'afficher récursivement son contenu (sous-dossiers et fichiers).

Dessinez l’arborescence de tous les répertoires et fichiers depuis le répertoire principal.

Écrivez une commande qui déplace dans 'Documents' tous les fichiers .py du répertoire 'Septembre_2018'. Pour cela, utilisez la commande mv.

Écrivez une commande qui supprime le répertoire 'Septembre_2018'. Pour cela, utilisez la commande rmdir.

# Python



    # Ceci est un commentaire en python. Référence Python 3: https://docs.python.org/fr/3/

Python, un langage interprété.

Vous allez d’abord utiliser python en mode interactif, c’est-à-dire de manière à dialoguer avec lui directement depuis le clavier.

Vous pouvez utiliser l’interpréteur directement comme une simple calculatrice de bureau.

Dans la console python, entrez les expressions ci-dessous et observez le résultat :

Pour ouvrir la console, il suffit de cliquer sur le bouton Python console en bas de votre fenêtre de Pycharm :

5+10

7 - 9

7+3 * 5

(7 +3) *5

20/6

8,7 / 5

Notez que le séparateur décimal est toujours un point, et non une virgule!

Les opérateurs arithmétiques : + (addition) / ( division) - (soustraction) * ( multiplication) % (reste de la division entière) // (division entière) ** (puissance)

# Variables et types

Remarques préliminaires



Les variables sont utilisées pour stocker des valeurs afin que

nous puissions nous y référer ultérieurement.

Un nom de variable est une séquence de lettres (a → z , A → Z)

et de chiffres (0 → 9), qui doit toujours commencer par une lettre. Seules les lettres ordinaires sont autorisées. Les lettres accentuées, les cédilles, les espaces, les caractères spéciaux tels que $, \#, @, etc. sont interdits, à l’exception

du caractère \_ (souligné).

La casse est significative (les caractères majuscules et minuscules sont distingués). Attention : Joseph, joseph, JOSEPH sont donc des variables différentes. Soyez attentifs !

L'opération d’affectation est représentée par le signe égale "=" exemple: nom_de_la_variable par la valeur 2 en Python: nom_de_la_variable = 2. Attention, elle ne signifie pas l'égalité au sens mathématiques.

Sous Python, on peut assigner une valeur à plusieurs variables

simultanément. Exemple : a = b = 8

print() : permet d'afficher la valeur d’une variable. Exemple: print(nom_de_la_variable)

Il est possible de connaître le type d’une variable en utilisant la

fonction type : print(type(nom_de_la_variable))

int : désigne un entier

float : désigne un nombre décimal

str : désigne une chaîne de caractères Exercice

Affectez les valeurs 7.692 et 21.8 aux variables a et b. Calculez leur somme dans une variable nommée resultat et affichez le contenu de cette dernière.

On cherche à calculer la valeur d'un téléphone valant 999 dollars US en euros. Affectez cette valeur à une variable telephone_usd. Calculez la conversion en euros et affectez le résultat à une variable nommée telephone_euro. Rappel: 1 dollar = 0.86 euro lors de la création de cp TP.

Affectez la valeur 2 à une variable nommée ma_variable.

Quel est le type de cette variable ? Répétez l’opération avec les

valeurs suivantes:

2.5

2 + 2.5

3 * 1.0

3.14 * 1

'z'

"bonjour"

10 / 3

10 // 3 Note : En python, une variable peut changer de type au gré des valeurs qu'elle prend.

# Exercice -

Définissez deux variables : a et b ayant pour valeur respectivement 5 et 3.

Afficher la phrase suivante : "a vaut 5 et b vaut 3, leur somme fait 8" en utilisant les valeurs effectives des variables. Note : print() peut prendre une liste de choses à afficher séparées par des virgules. Exemple : print("x vaut", x, "et y vaut", y)

L'opérateur % entre deux nombres calcule le reste de la division du premier par le second. Utilisez cet opérateur pour savoir si « a est un multiple de b ? ».

Écrivez les lignes de code permettant d’échanger les valeurs de a et b, en utilisant une variable temporaire tmp.

Échangez à nouveau les valeurs de a et b, mais sans utiliser de variable temporaire. Note : en python, on peut assigner plusieurs variables d'un seul coup à l'aide de l'opérateur égal : x, y = 1, 2 met 1 dans x et 2 dans y. Dans cet exercice, on ne vous autorise pas à utiliser cette méthode (utilisez des additions et soustractions).

# Manipulation des chaîne de caractères

Préliminaires



Pour les chaînes de caractères, deux opérations sont possibles, l’addition et la multiplication, exemple:

chaine = "Salut" L'affichage de la variable chaine donne : 'Salut' chaine = chaine + " Python" L'affichage de la variable chaine donne : 'Salut Python' (notez l'espace avant Python). chaine = chaine * 3 L'affichage de la variable chaine donne : 'SalutSalutSalut'



L’opérateur d’addition + permet de concaténer (assembler)

deux chaînes de caractères et l’opérateur de multiplication * permet de dupliquer plusieurs fois une chaîne. On ne peut "ajouter" à une chaîne qu'une autre chaîne, et on ne peut multiplier une chaîne que par un entier.

Lorsque l'on utilise print(), on peut afficher à la suite plusieurs valeurs de types différents (par exemple print(1, "hello", 3.14). Cela ne fonctionne pas avec l'addition entre chaînes de caractères. Pour y arriver, il faut d'abord convertir les valeurs de types différent vers le type chaîne de caractères en utilisant str(x) où x est la valeur à convertir. Par exemple resultat = str(1) + "hello" + str(3.14).

Créez une variable contenant "rouge", une autre contenant "ballon". Assignez à une troisième variable la concaténation de ces deux chaînes de manière à ce qu'elle contienne "ballon rouge". Affichez le résultat.

Les chaînes de caractères peuvent être écrites soit encadrées par des guillemets simples 'abc', soit par des gillemets doubles "abc". Il faut utiliser le même type de guillemets avant et après le texte. On peut insérer le type de guillemet utilisé pour encadrer la chaîne dans celle-ci en le préfixant du caractère \ (antislash). Créez une chaîne de caractères contenant le mot aujourd'hui avec les deux méthodes.

Quelle est la différence entre ces deux instructions Python :

x = 2018 x = "2018" Vous avez ici la notion de types et de typage : Chaque valeur en Python se voit associer un type, ceci précise quelles sont les opérations permises sur ces valeurs, et quel est leur sens.

En Python les variables (comme x) n'ont pas de type au départ. C'est au moment de l'exécution, de l'évaluation des valeurs, que le système vérifie le type, et réagit "bien" ou "mal" vis à vis les opérations demandées.

Cette propriété porte le nom de typage dynamique.



Vérifiez ce qui se passe quand on évalue x+x dans les deux cas.

# Rappel:

La fonction print() : pour afficher des messages et des valeurs a. Écrire un programme qui affecte les variables note1, note2, note3 avec les valeurs 15.5, 12.75 et 14.25 respectivement. Ensuite, calculez la moyenne de ces notes et stockez le résultat dans une variable nommée moyenne. Affichez la valeur de la variable moyenne précédée du message suivant : "La moyenne des trois notes est": b. Si 15 étudiants utilisent 5 ordinateurs, combien utiliseront d'ordinateurs 90 étudiants ? Écrire un programme contenant des variables bien nommées avec les données du problème, puis calculant le résultat dans une variable et l'affichant. c. Un brin d'ADN est constitué des bases A,T,C et G. Soit deux gènes "AACTG" et "GAATA", on souhaite céer un nouveau gène qui soit la concaténation du premier et du second, puis créer un brin d'ADN qui répète 7 fois le brin ainsi créé. Écrire un programme qui contienne une variable pour chacun de ces gènes (chaînes de caractères), puis calcule le brin d'ADN (concaténation et réplication) dans une nouvelle variable, et affiche le résultat.
