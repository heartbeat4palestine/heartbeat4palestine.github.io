# heartbeat4palestine

For more information contact ABDELHADI MAHBOUB.

﻿Chapitre 1![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.002.png)![ref2]![ref2]

Représentation des nombres sur ordinateur

ENSAM-Meknès

Université Moulay Ismail - Meknès

28 septembre 2011![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

1  [Introduction](#_page2_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.010.png)![ref2]![ref2]
1  [Représentation des nombres sur ordinateur](#_page13_x353.01_y272.91)![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.011.png)
1  [Arithmétique flottante](#_page33_x353.01_y272.91)![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.012.png)![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

Maths-Info (ENSAM) [CMN](#_page38_x353.01_y272.91) 2 septembre 2011 2 / 42![ref9]![ref9]![ref9]
<a name="_page0_x353.01_y272.91"></a>[Introduction](#_page2_x353.01_y272.91) [Analyse numérique](#_page2_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.014.png)![ref2]![ref2]

L’analyse Numérique est une spécialité récente des mathématiques, elle s’est développée avec l’apparition des ordinateurs.

Son objet essentiel est d’écrire les programmes permettant d’effectuer les opérations nécessaires pour résoudre numériquement un problème donné.

Les méthodes ont un "coût", lié d’une part au temps de calcul, ie au nombre d’opérations élémentaires (additions, soustractions, multiplications et divisions) à faire, et d’autre part à l’espace mémoire nécessaire pour stocker les données et les résultats.

L’ordinateur ne fait pas de calculs exacts (à cause du mode de représentation des nombres). Ceci constitue un inconvénient car cela provoque des erreurs d’arrondis et de troncature.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

Pour un grand nombre de problèmes, le seul moyen de calculer la solution, si elle existe, est de l’approcher numériquement.

Un algorithme c’est

une démarche pour obtenir une solution (impliquant des simplifications, ajout/retrait d’hypothèses sur le modèle, etc)

ET l’implementation sur ordinateur de cette démarche.

Objectifs de l’analyse numérique :

proposer et développer des algorithmes (méthodes d’approximation) pour calculer une solution approchée,

contrôler les diverses sources d’erreurs, propres à l’approximation numérique,

évaluer la pertinence et la valeur de différents algorithmes (estimer leurs performances) pouvant être utilisés pour résoudre le même problème afin de sélectionner les meilleurs .

Quelques problèmes typiques

Interpolation - Extrapolation.

Résolution de systèmes linéaires.

Résolution de systèmes non-linéaires.

Intégration et différentiation numérique.

Résolution de systèmes d’équations différentielles. Résolution de systèmes d’EDP.

Analyse statistique.

Transformée de Fourier.

Diagonalisation.

Calcul de valeurs propres. item Calcul de vecteurs propres. ...![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

Langages de programmation

Fortran : Idéal pour le calcul intensif.

C : le plus proche du "hardware".

IDL : Courant en astrophysique.

Java : Indépendant de la machine (portabilité). Shell : Scripting de base.

Autre : C++, python, Mathematica, etc ....

A choisir en fonction de la tache à réaliser, et non en fonction des habitudes.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

Maths-Info (ENSAM) [CMN](#_page0_x353.01_y272.91) 6 septembre 2011 6 / 42![ref9]![ref9]![ref9]
<a name="_page2_x353.01_y272.91"></a>[Introduction](#_page6_x353.01_y272.91) [Sources d’erreurs](#_page6_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.015.png)![ref2]![ref2]

Qu’est-ce qu’un bon algorithme?

Afin de choisir le meilleur algorithme possible, il faut pouvoir les comparer. Un bon algorithme est :

le moins coûteux possible en place mémoire,

le moins coûteux possible en temps de calcul : c’est-à-dire qui minimise le nombre d’opérations nécessaires. C’est ce qu’on appelle un problème de complexité.

le plus stable possible, ie le moins sensible aux erreurs d’arrondi que nous venons d’évoquer,

le plus précis possible : la solution approchée obtenue est-elle proche ou loin de la solution exacte. C’est ce qu’on appelle l’estimation d’erreur.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

Exemple : Calcul du déterminant d’une matrice *N* × *N*

La méthode mathématique de Cramer nécessite *N* × *N*! opérations élémentaires (*N*! additions et (*N* − 1) × *N*! multiplications).

Prenons N = 50, sachant que 50 × 50! = 15.1055, et qu’un ordinateur peut faire environ 20 GFlops (ie 20 milliards d’opérations à la

seconde), il faudrait quand même environ 1050 ans pour faire ce calcul.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

Les quatre principales sources d’erreurs :

erreurs de modélisation,

erreurs sur les données,

erreurs dues à la représentation des nombres sur ordinateur, erreurs de troncature ou de discrétisation.

Exemple 1

Soit la suite définie par : *xn*+1 = 4*xn*(1 − *xn*) On peut la programmer de deux façons :

*x*1 = 4 ∗*x*1 ∗(1.0 − *x*1) ; *x*2 = 4 ∗*x*2 − 4 ∗*x*2 ∗*x*2 ;

"Normalement", on doit trouver la même chose "mathématiquement", mais les opérations ne sont pas faites dans le même ordre en machine.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

Exemple 2

Soit à résoudre l’équation : *x*2 + 2*bx* − 1 = 0 Où b peut être "très grand". On d√emande de calculer la solution positive :![ref10]

*x*+ = −*b* + *b*2 + 1 Comment faut-il la programmer? La aussi, deux

possibilités :

√ ![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.017.png)

*x* = −*b* + *b* ∗*b* + 1.0;

*x* = √1.0![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.018.png)![ref11]

*b*+ *b*∗*b*+1.

Équivalentes mathématiquement.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

Exemple 3

Soit à calculer, pour n fixé : *S* = *n* 1 Il y a (au moins) deux façons![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.020.png)

*n i*=1 *i*

d’écrire la boucle :

for (i=1; i<=n; i++) x = x + 1.0/i; for (i=n; i>=1; i–) x = x + 1.0/i;

Sans oublier d’initialiser x à 0 évidemment. Ici aussi les mathématiques sont équivalentes.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

Maths-Info (ENSAM) [CMN](#_page0_x353.01_y272.91) 12 septembre 2011 12 / 42![ref9]![ref9]![ref9]

<a name="_page6_x353.01_y272.91"></a>[Introduction](#_page11_x353.01_y272.91) [Erreurs de modélisation](#_page11_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.021.png)![ref2]![ref2]

La modélisation c’est :

L’identification des différents facteurs agissant dans le phénomène (physique, biologique, économique , etc) à l’étude.

L’identification et réprésentation mathématique des relations entre les facteurs : écriture des “formules/équations” représentants ces relations.

Les erreurs de modélisation peuvent provenir de

l’étape de "mathématisation" i.e. simplification ou mauvaise description de la relation entre différents facteurs lors de la mise en équations

pour réduire le degré de complexité d’un phénomème physique, on est souvent amené à simplifier le système d’équations, ce qui revient à négliger certaines composantes de la réalité physique.

Solution : Un choix convenable du modèle mathématique.

Maths-Info (ENSAM) [CMN](#_page0_x353.01_y272.91) 14 septembre 2011 14 / 42![ref9]![ref9]![ref9]

<a name="_page11_x353.01_y272.91"></a>[Introduction](#_page12_x353.01_y272.91) [Erreurs sur les données](#_page12_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.022.png)![ref2]![ref2]

Les erreurs sur les données proviennent généralement de

l’imprécision des mesures physiques qui sont utilisées dans l’algorithme.

Solution : Ces erreurs peuvent généralement être réduites en améliorant la précision des mesures.

Remarque

Il est possible d’étudier l’influence de ces erreurs sur le résultat final, par exemple à l’aide de la notion de conditionnement (sensibilité aux erreurs).

Dans la suite de ce cours, nous ne nous intéresserons pas aux erreurs de modélisation ni à celles sur les données.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

[Représentation des nombres sur ordinateur](#_page13_x353.01_y272.91) [Erreur relative et erreur absolue](#_page13_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.023.png)![ref2]![ref2]

Définition 1

Soit *x* un nombre réel et *x*˜ une approximation de *x*. L’erreur absolue : ∆*x* = |*x* − *x*˜| (mesure de l’erreur)

∆*x*

L’erreur relative : ![ref12] (importance de l’erreur).

|*x*|

Définition 2

Si *m* est le plus petit entier signé tel que ∆*x* ≤ 0.5 × 10*m* alors le chiffre correspondant à la mième puissance de 10 (et tous ceux à sa

gauche jusqu’au dernier non-nul) sont dit significatifs.

Exemple

Si *x* = π et *x*˜ = 3.1428, d’où ∆*x* = 0.12 10−2 < 0.5 10−2. Donc le chiffre des centièmes est significatif, soit le chiffre 4 dans 3.1428 et on a en tout 3 chiffres significatifs (3.14).

[Représentation des nombres sur ordinateur](#_page14_x353.01_y272.91) [Erreurs de représentation des nombres](#_page14_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.025.png)![ref2]![ref2]

L’ordinateur doit représenter les nombres dans un système qui lui permette d’exécuter les opérations souhaitées efficacement.

La structure interne des ordinateurs s’appuie généralement sur le système binaire : représentation des nombres en base 2.

Les calculs sont généralement effectués en base 2, et les interactions avec l’usager affichés en base 10.

Décimal  binaire

(100)10 = 1 × 102 + 0 × 10 + 0 × 100

1

- 1 × 64 + 1 × 32 + 0 × 16 + 0 × 8 + 1 × 4 + 0 × 2 + 0 × 1
- 1 × 26 + 1 × 25 + 0 × 24 + 0 × 23 + 1 × 22 + 0 × 21 + 0 × 20
- (1100100)2

(0.3)10 = (0.010 0110001100 ...)2 ← fraction périodique en binaire!

[Représentation des nombres sur ordinateur](#_page15_x353.01_y272.91) [Longueur de mots : source d’erreur](#_page15_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.026.png)![ref2]![ref2]

Sur un ordinateur l’unité d’information de base ou bit prend la valeur 0 ou 1. On regroupe les bits en mots de longueur variable (8, 16, 32 ou 64 sont les plus courants). Les nombres réels sont représentés à l’aide de ces mots. La capacité mémoire est finie par construction. Il est donc nécessaire de représenter les nombres réels sous forme approchée. Cela entraîne un certain nombre d’erreurs.

Le fait d’utiliser un nombre limité de bits pour représenter un nombre réel a des conséquences importantes. Pour représenter les nombres réels on recourt généralement à

La troncature à *N* chiffres : on retranche les chiffres à partir de la position *N* + 1.

L’arrondi à *N* chiffres : on ajoute 5 au (*N* + 1)ième chiffre de la mantisse avant d’effectuer la troncature.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

[Représentation des nombres sur ordinateur](#_page16_x353.01_y272.91) [Les nombres naturels](#_page16_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.027.png)![ref2]![ref2]

Nombres Entiers

La première codification des nombres consiste à les coder de façon naturelle sur les mots connus au niveau de la machine, 8, 16, 32 ou 64 bits la limitation étant la valeur maximale que l’on peut stocker. On parle alors de représentation en champs fixe.

Par nombre naturel, on entend les nombres entiers, positifs ou nuls

1 octet pourra coder un nombre de (00000000)2 → (11111111)2 (0 → 255)

1 mot de 16 bits : de 0 → 216 − 1 (65535)

1 mot de 32 bits : de 0 → 232 − 1 (4 294 967 295) La limite reste toujours la taille du mot manipulé![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

[Représentation des nombres sur ordinateur](#_page17_x353.01_y272.91) [Les nombres relatifs](#_page17_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.028.png)![ref2]![ref2]

La représentation des nombres négatifs est réalisé grâce au bit de poids fort "bit de gauche". On parle également d’entiers signés.

Nombres positifs → le bit de poids fort est 0 Nombres négatifs → le bit de poids fort est 1

Les autres bits contiennent la valeur absolue du nombre

Exemple sur un octet

![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.029.png)

Inconvénient : Pour réaliser des opérations entre nombres signés, il faut faire un traitement particulier du bit de signe. Le résultat final ne pouvant être obtenu de façon simple (addition ou soustraction des deux nombres).

D’où l’utilisation du complément à 2.

[Représentation des nombres sur ordinateur](#_page18_x353.01_y272.91) [Représentation par le complément à 2](#_page18_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.030.png)![ref2]![ref2]

Représentation par le complément à 1

Le complément à 1 (noté C1) est également appelé complément logique, il consiste à inverser chaque bit (0 → 1 et 1 → 0)

Représentation par le complément à 2

Le complément à 2 (noté C2) est également appelé complément vrai, il consiste à ajouter 1 en binaire au complément à 1.

L’entier positif est représenté en binaire naturel.

L’entier négatif est représenté par le complément à 2 de son opposé.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.031.png)

Maths-Info (ENSAM) [CMN](#_page0_x353.01_y272.91) 22 septembre 2011 22 / 42![ref9]![ref9]![ref9]
<a name="_page12_x353.01_y272.91"></a>[Représentation des nombres sur ordinateur](#_page19_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.032.png)![ref2]![ref2]

Exemple

Une soustraction *a* − *b* devient une addition *a* + (−*b*). (−*b*) étant le complément à 2 de *b*

![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.033.png) ![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.034.png)

Si le bit de poids fort est 0, le résultat est positif, et si le bit de poids fort est 1, le résultat est négatif Pour connaître la valeur absolue du résultat négatif, il suffit de faire le complément à 2 :

![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.035.png)

En effet |5 − 12| = (0000000111)2 = (7)10

Les limites des nombres

Les nombres sont codés de façon fixe, ce qui fait qu’ils ont une limite liée au nombre de bis qui les représentent :

![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.036.png)

En synthèse, si le nombre de bits est *n*, les valeurs vont de −2*n* à 2*n* − 1![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

Maths-Info (ENSAM) [CMN](#_page0_x353.01_y272.91) 24 septembre 2011 24 / 42![ref9]![ref9]![ref9]
<a name="_page19_x353.01_y272.91"></a>[Représentation des nombres sur ordinateur](#_page21_x353.01_y272.91) [Les nombre réels : représentationen virgule flottante](#_page21_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.037.png)![ref2]![ref2]

On se donne un entier *b* ≥ 2 appelé base de numération. On choisit aussi un entier *p* ≥ 2 appelé précision ou nombre de chiffres significatif. On se donne aussi deux entiers *emax* ≥ 2 et *emin* ≤ −2. Un nombre flottant normalisé est alors un nombre de la forme

*x* = (−1)*s* × *m* × *be*

où *s* ∈ {0,1} et (−1)*s* est le signe de *x*. *m* est appelée La mantisse, elle est écrite sous la forme d’un nombre avec virgule fixe et possédant un nombre maximum de *p* chiffres significatifs

*p*

*m* = 0.*d*1*d*2...*dp* = *dk b*−*k*,

*k*=1

avec 1 ≤ *d*1 ≤ *b* − 1 (mantisse normalisée) et 0 ≤ *dk* ≤ *b* − 1. L’entier *e*, appelé exposant , vérifie *emin* ≤ *e* ≤ *emax*.

On vérifie que 1 ≤ *m* ≤ 1 − *b*−*p![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.038.png)*

λ = *bemin*−1 ≤ |*xb*| ≤ µ = (1 − *b*−*p*e)*b*t *emax* . L’ensemble des flottants normalisés est noté *F*(*b*, *p*, *emin*, *emax*)

Par exemple, prenons b = 10, p = 5 et *emax* = −*emin* = 100. Le rationnel 0.000000000000000000000123est dans *F*(10, 5, −100, 100) et s’écrit

*x* = (−1)0 × 1.2300× 10−22

. Notons que 0 n’est pas un entier flottant normalisé.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

On pose  = *b*1−*p* et on vérifie sans peine le lemme suivant.

Lemme 1 Soit *x* > 0 un entier flottant normalisé et *y* le suivant (le plus petit entier flottant normalisé plus grand que *x*) s’il existe. Alors *y* − *x* vérifie

` `|*x*|

![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.039.png) ≤ *y* − *x* ≤ *x*

*b![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]*

Une fois choisis *b*, *p*, *emin* et *emax* on se donne une application d’arrondi

φ : **R** → *F*(*b*, *p*, *emin*, *emax*) {*OVERFLOW*, *UNDERFLOW*}

jouissant des propriétés suivantes :

φ(*x*) = *OVERFLOW* si et seulement si |*x*| > µ ;

φ(*x*) = *UNDERFLOW* si et seulement si |*x*| < λ ;

φ est croissante sur [λ,µ] et sur [−µ, −λ];

La restriction de *phi* à *F*(*b*, *p*, *emin*, *emax*) est l’identité.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8] Le fait d’utiliser un nombre limité de bits pour représenter un nombre réel a des conséquences importantes :

Cette représentation introduit une erreur (troncature ou arrondi) qui peut avoir un impact important sur la précision des résultats.

Quelque soit le nombre de bits utilisés, il existe un plus petit et un plus grand nombre (positif et négatif) représentables . Il existe donc un intervalle fini hors duquel on a un débordement (overflow) ou un sous-dépassement (underflow). Dans ce cas les operations arithmétique n’ont plus de sens.

A l’intérieur de cet intervalle fini, seul un nombre fini de nombres sont représentables exactement.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

La représentation en virgule flottante induit une erreur relative qui dépend du nombre de bits de la mantisse, de l’utilisation de la troncature ou de l’arrondi, ainsi que du nombre *x* à représenter.

Définition

La précision machine est la plus grande erreur relative commise en représentant un nombre réel sur ordinateur :

∆*x* precision machine = maximum![ref12] |*x*|

1−*N*

En utilisant la troncature, on a : ε*m* = *b*

En utilisant l’arrondi, on a : ε = ε*m*/2 = *b*1−*N*/2.

Remarque : En réalité la précision machine est au maximum égale à ε*m* ou ε mais dans la pratique on confond la précision avec cette borne.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

La convention IEEE-754

Norme visant à standardiser la représentation des nombres sur les ordinateurs. En particulier elle impose le nombre de bits pour la mantisse, et l’exposant pour les nombres reels à 32 bits (simple precision) et les reels 64 bits (double precision). Fait en sorte que l’on peut determiner la precision machine ainsi que le plus grand et plus petit reels (simple et double precision) représentable indépendemment de l’ordinateur .

simple precision double precision ε*m* 0.119 × 10−6 0.222 × 10−15 ![ref13]plus petit réel (normalisée) 1.2 × 10−38 2.2 × 10−308 ![ref13]plus petit réel (non-normalisée) 1.4 × 10−45 4.9 × 10−324 ![ref13]plus grand réel 3.4 × 1038 1.8 × 10308![ref13]![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

Maths-Info (ENSAM) [CMN](#_page0_x353.01_y272.91) 30 septembre 2011 30 / 42![ref9]![ref9]![ref9]
<a name="_page21_x353.01_y272.91"></a>[Représentation des nombres sur ordinateur](#_page28_x353.01_y272.91) [IEEE-754](#_page28_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.041.png)![ref2]![ref2]

Décalage de l’exposant

L’exposant étant représenté par un nombre signé (complément à 2), la comparaison entre les nombres flottants devient un peu plus difficile. Pour remedier à ce problème, l’exposant est décalé, afin de le stocker sous forme d’un nombre non signé. Ce décalage est de 2*e*−1 − 1 (*e* représente le nombre de bits de l’exposant); il s’agit donc d’une valeur constante une fois que le nombre de bits *e* est fixé :

*valeur* = *signe* × 1, *mantisse* × 2(*exposant*−*decalage*)![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

Format simple précision (32 bits)

Un nombre flottant simple précision est stocké dans un mot de 32 bit : 1 bit de signe, 8 bits pour l’exposant et 23 pour la mantisse. L’exposant est donc décalé de 28−1 − 1 = 127 dans ce cas. L’exposant -127 (qui est décalé vers la valeur 0) est réservé pour zéro et les nombres dénormalisés, tandis que l’exposant 128 (décalé vers 255) est réservé pour coder les infinis et les NaNs.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.042.png)

Exemple1

Pour 0 01111100 01000000000000000000000,l’exposant est

124 − 127 = −3 et la partie significative est 1,01 soit 1,25 en décimal (1*x*20 + 0*x*2−1 + 1*x*2−2); le nombre représenté est donc +1,25*x*2−3

soit +0, 15625.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

Exemple2

Codons le nombre -118,625 en utilisant IEEE 754.

1  C’est un nombre négatif, le signe est donc "1".
1  Nous écrivons le nombre (sans le signe) en binaire. Nous obtenons 1110110,101.
1  Nous décalons la virgule vers la gauche, de façon à ne laisser qu’un 1 sur sa gauche : 1110110,101 (bin) = 1,110110101 (bin) x

   26. C’est un nombre flottant normalisé : la mantisse est la partie à droite de la virgule, remplie de 0 vers la droite pour obtenir 23 bits. Cela donne 110 1101 0100 0000 0000 0000 (on omet le 1 avant la virgule, qui est implicite).
1  L’exposant est égal à 6, et nous devons le convertir en binaire et le décaler. Pour le format 32-bit IEEE 754, le décalage est

   28−1 − 1 = 127. Donc 6 + 127 = 133 (dec) = 1000 0101 (bin).

-118,625 (dec) = 1100 0010 1110 1101 0100 0000 0000 0000 (bin)

- C2ED4000 (hexa)

Format double précision (64 bits)

Le format double précision est identique au simple précision, mis à part le fait que les champs sont plus grands. En effet, il possède 52 bits de mantisse, et 11 bits d’exposant. La mantisse est très élargie, alors que l’exposant est peu élargi. Ceci est dû au fait que, selon les créateurs du standard, la précision est plus importante que l’amplitude. Les NaNs et les infinis sont représentés en mettant tous les bits de l’exposant à 1 (2047). Pour les nombres normalisés, le décalage de l’exposant est +1023.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.043.png)

Maths-Info (ENSAM) [CMN](#_page0_x353.01_y272.91) 35 septembre 2011 35 / 42![ref9]![ref9]![ref9]

<a name="_page28_x353.01_y272.91"></a>[Arithmétique flottante](#_page33_x353.01_y272.91) [Modèle de l’arithmétique flottante](#_page33_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.044.png)![ref2]![ref2]

Les opérations élémentaires sont effectuées en arithmétique flottante

*x* + *y* −→ *fl*( *fl*(*x*) + *fl*(*y*) )

*x* − *y* −→ *fl*( *fl*(*x*) − *fl*(*y*) )

de la manière suivante : Attention :

*x* ÷ *y* −→ *fl*( *fl*(*x*) ÷ *fl*(*y*) )

*x* × *y* −→ *fl*( *fl*(*x*) × *fl*(*y*) )

plusieurs propriétés de l’arithmétique : associativité, distributivité, etc ne sont plus valides (pas toujours) en arithmétique flottante!![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

Maths-Info (ENSAM) [CMN](#_page0_x353.01_y272.91) 36 septembre 2011 36 / 42![ref9]![ref9]![ref9]

<a name="_page33_x353.01_y272.91"></a>[Arithmétique flottante](#_page34_x353.01_y272.91) [Associativité](#_page34_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.045.png)![ref2]![ref2]

Par exemple : supposons que les réels soient calculés avec *n* = 3 chiffres significatifs et arrondis à la décimale la plus proche. Soient *x* = 8,22, *y* = 0,00317, *z* = 0,00432

(*x* + *y*) + *z* = *x* + (*y* + *z*)![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

[Arithmétique flottante](#_page35_x353.01_y272.91) [Distributivité](#_page35_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.046.png)![ref2]![ref2]

Encore avec n =3

*x* × (*y* + *z*) = *x* × *y* + *x* × *z*

122 × (333 + 695) = *fl*( 0,122 103 × *fl*( 0,333 103 + 0,695 103 ))

- *fl*( 0,122 103 × *fl*( 1,028 103 ))
- *fl*( 0,122 103 × *fl*( 0,103 104 ))
- *fl*( 0,012566 107 ))
- 0,126 106

(122 × 333)+ (122 × 695) = *fl*( *fl*( 0,122 103 × 0,333 103 )

\+ *fl*( 0,122 103 × 0,695 103 ))

- *fl*( *fl*( 0,040626 106 + *fl*( 0,08479 106 )
- *fl*( 0,406 105 + 0,848 105 )
- *fl*( 1,254 105 )
- 0,125 106

Il ya donc une différence entre les deux résultats.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

[Arithmétique flottante](#_page36_x353.01_y272.91) [Attention à l’exposant!!!](#_page36_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.047.png)![ref2]![ref2]

Il faut être prudent avec l’addition et la soustraction. Lorsque les exposants ne sont pas les mêmes il est nécessaire de décaler la mantisse avant d’effectuer l’addition ou la soustraction.

Pour *n* = 4

0,4035 106 + 0,1978 104 = *fl*( 0,4035 106 + 0,1978 104 )

- *fl*( 0,4035 106 + 0,001978 106 )
- *fl*( 0,405478 106 )
- 0,4055 106

et

0,56789 104 − 0,1234321 106 = *fl*( 0,5679 104 − 0,1234 106 )

- *fl*( 0,005679 106 − 0,1234 106 )
- *fl*( −0,11772 106 )
- −0,1177 106![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]

[Arithmétique flottante](#_page37_x353.01_y272.91) [Phénomène de cancellation](#_page37_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.048.png)![ref2]![ref2]

Il existe d’autre part, un certain nombre d’opérations risquées. Soustraire deux nombres presque identiques :

- √ ![ref14]![ref14]

7001 − 7000 = 0,8367 102 − 0,8367 102

- 0,000 100 si *n* = 4
- √ ![ref14]![ref14]

7001 − 7000 = 0,83672 102 − 0,83666 102

- 0,6 10−2 si *n* = 5

Dans ce cas-ci on peut remédier à cette difficulté en évitant la soustraction des racines :

- √ *x* − *y![ref15]![ref15]*

*x* − *y* = √ √ ![ref15]![ref15]![ref16]

*x* + *y*

et on trouve 0,5977 10−2 au lieu de 0 pour *n* = 4.

[Arithmétique flottante](#_page38_x353.01_y272.91) [Conclusion](#_page38_x353.01_y272.91)![ref1]![](Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.052.png)![ref2]![ref2]

L’ordre dans lequel on fait les opérations et le nombre d’opérations ont un impact important sur la précision du résultats. Ainsi on devrait ”toujours“ :

éviter les opérations avec des nombres très différents en ordre de grandeurs,

éviter si possibles les soustractions avec des nombre relativement proche,

on devrait faire les sommes en ordre décroissant.![ref3]![ref4]![ref5]![ref6]![ref7]![ref8]
Maths-Info (ENSAM) [CMN](#_page0_x353.01_y272.91) 42 septembre 2011 42 / 42![ref9]![ref9]![ref9]

[ref1]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.001.png
[ref2]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.003.png
[ref3]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.004.png
[ref4]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.005.png
[ref5]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.006.png
[ref6]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.007.png
[ref7]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.008.png
[ref8]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.009.png
[ref9]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.013.png
[ref10]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.016.png
[ref11]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.019.png
[ref12]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.024.png
[ref13]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.040.png
[ref14]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.049.png
[ref15]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.050.png
[ref16]: Aspose.Words.a547d651-4a3b-46dd-b9fd-abc978e662ee.051.png
