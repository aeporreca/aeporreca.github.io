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
