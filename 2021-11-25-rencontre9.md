# InfoSansOrdi 25 novembre 2021





Présent·e·s : Jean-Marc Vincent, Nina Gasking, Martin Quinson, Gilles Muller, Natacha Portier, Raphaël Bleuse, Nathalie Revol, Benjamin Wack, Anne Rasse, Aline Parreau, Éric Duchêne, Emmanuel Beffara, Yves Bertrand, Sylvie Alayrangues, Marie Duflot-Kremer, Gaëlle Walgenwitz, Daniela Guiol, Guillaume Claus, Timothée Pécatte

Programme du jour : 
déjeuner à 11h30
12h30 : café expo IA
Marie : "grande muraille d'Égypte" sur le parallélisme - une activité d'Emmanuelle Saillard
Nina : atelier MMI sur l'apprentissage supervisé
Martin : j'peux pas j'ai informatique
Benjamin : origami et réseaux
Raphaël : musique

Points à discuter : 
- site
- petits débrouillards
- ANR
- CS unplugged
- École de médiation
- étudiants dans les classes.

Happening de début de journée : Martin distribue des sacs "j'peux pas j'ai informatique". Il fallait être là :o)

## [Marie] grande muraille d'Égypte

Marie : "grande muraille d'Égypte" sur le parallélisme - une activité d'Emmanuelle Saillard (CR à Bordeaux)

30aine de briques légo de 2 couleurs différentes

https://emmanuellesaillard.fr/mediation/

suggestions
:  - plastifier les supports pour permettre de noter les briques qui déclenchent une pénalité.
   - travailler à plat et retourner les briques (celles qui correspondent à une pénalité) : mais c'est pas drôle car on n'assemble pas les briques pour construire une pyramide
   - planches plus simples pour expliquer le problème → 1er problème sans pénalités

questions ouvertes
:  - lien avec ordo sur 2 machines → quelle est la complexité du problème ?
   - existe-t-il un algo poly «simple» à expliquer ?
   - glouton pas forcément optimal ?
   - GPU : ne sait faire que des calculs très réguliers, donc ne peut pas poser 2 briques à 2 endroits différents, il peut mettre une grande brique ou une petite brique
   - cas avec GPU : préciser le calcul de pénalité : +1 uniquement quand on va chercher des briques - celui qui a 2 briques peut-il poser une brique, laisser jouer l'autre et poser la 2e pendant  que l'autre va chercher une brique
   - quand on a un GPU, doit-il poser 2 briques côte à côte ou peut-il en poser une brique à un bout du mur et l'autre bout du mur ? (en contradiction avec point précédent avec des rectangles)

Une autre activité en ordonnancement : cf. Julien Narboux (Strasbourg) :  https://github.com/InfoSansOrdi/InfoSansOrdi/blob/master/20190614-rencontre7.md#ordonnancement-julien
 https://github.com/jnarboux/MediationInfoStrasbourg/tree/master/ordonnancement


## [Gilles Muller] Petits débrouillards

regroupement associations éducation populaires
rq : départ en mi-temps dans des associations (avant départ en retraite) → Orange peut déduire la moitié de son salaire comme "don à des associations"

Se fait en extra-scolaire, public jeune (mais pas que).

exemples ateliers
:  - animations sur Thymio (petit robot open-source + prog. scratch) / Arduino / 
   - bio-diversité / energie renouvelables
   - vivre ensemble
   - coding goûter

Principe fondateur : manipulation (exemple : fusée à eau)
Apprentissage par renforcement : Exapion : style nim, avec 6 pions sur un échiquier (cf. machine qui apprend avec des gobelets)

Jeu sur le son, avec des Arduino, réf. : John Cage
Jeu style "1000 bornes" : il faut ramasser le plus de données personnelles, panne = "datacenter en panne"

Lien : Wikipedia "Petits débrouillards" : https://fr.wikipedia.org/wiki/Les_Petits_Débrouillards , Facebook des petits débrouillards d'Auvergne.

https://www.lespetitsdebrouillards.org/

## [Nina Gasking] IA : apprentissage supervisé

> Entrez dans la tête d'une IA

atelier à destination de lycéens (voire fin de collège) en 1/2 classe (l'autre 1/2 classe visite l'expo)

L'objet de l'atelier est l'apprentissage supervisé.

Principe : 5 sets de 12 images avec leurs étiquettes (et au préalable la liste des étiquettes possibles. Pour chaque set, il faut "deviner", apprendre la règle qui permet d'attribuer l'étiquette. Ensuite, pour chaque set / règle : on présente quelques images pour appliquer la règle déduite : phase de test.
Quelques commentaires : quand plusieurs règles sont possibles, comment savoir laquelle est la bonne (explicabilité) ? que faire quand aucune règle ne s'applique (il faut toujours répondre) ? problème de sur-apprentissage quand il y a quelques images mal annotées : on crée une règle trop compliquée pour bien couvrir tous les cas même les mal annotées - problème de données d'entraînement biaisé : il manque des données représentatives de tous les cas possibles (on peut élargir à des exemples de la vie réelle).
Conseil pratique : ajouter un 6e set bien compliqué, parce qu'il y a toujours un groupe qui va beaucoup plus vite que les autres et qu'il faut l'occuper.

Pour aller plus loin, conseil de lecture de Jean-Marc et Raphaël sur l'induction naïve : 

Ca fait aussi penser au jeu Zendo, basé sur l'induction. Un maître de jeu tire une carte qui donne une règle comme "la figure contient deux pièces vertes", et les joueurs construisent des ptites figures. Le maître répond oui/non si la figure construite respecte la règle secrète, et les joueurs essaient d'induire la règle en le moins de coups possibles.
- http://www.koryheath.com/zendo/ <-- site d'origine
- https://www.boardgamegeek.com/boardgame/6830/zendo <-- review, avec des photos du matériel

Deuxième partie sur le classifieur : chaque participant·e dessine un 6 et un 9 avec un gros feutre sur une grille 10x10, puis compte pour chaque chiffre combien de pixels sont traversés par le tracé dans la moitié gauche et pour la moitié haute : chaque dessin est alors résumé par 2 entiers. On utilise Géogebra : pour chaque "6" dessiné dans la salle (sauf ceux et celles sur la dernìère rangée), on met un point rouge de coordonnées ces 2 entieres, pour chaque "9" un point bleu. On "voit" bien que les points sont regroupés, on trace une droite qui sépare les 2 paquets. Ensuite on demande aux personnes de la dernière rangée de donner une paire de coordonnées et on devine, en regardant de quel côté de la droite on se trouve, si c'était un 6 ou un 9.
En pratique : avoir au moins 3 ou 4 pour tester, si on en a trop peu et que les dessins sont mal faits, cela échoue. Mais si on en a trop, le public se lasse de tester trop de valeurs. Et avoir une dizaine de valeurs pour l'apprentissage (à la MMI on le fait en demi-classe).

Idée d'extension possible : aide à l'animation sous forme d'une appli téléphone qui compte les carrés d'un flash, pour les groupes qui ont du mal à compter.

## Journée IA à Grenoble
Su une journée, présentation d'activités sans ordi et IA, on envisage 6 ateliers l'objectif serait d'aboutir ultérieurement a des jeux d'activités en IA/infosans ordi et de les diffuser
Période envisagée février/mars/avril 

Donc appel à activités, on fera une sélection pour équilibrer thèmes, équipes, + annexes s'il y a trop de demandes, 

## Journées médiation SIF - mars 2022

1/2 journée en distanciel (webinaire en décembre), 3 journées en présentiel sur Paris (8-9-10 mars). Environ 60 places.
Ateliers : Audrey Mickaëlian sur la vidéo, Cécile Michaut sur l'écriture d'un article, Jean-Marc et Marie sur l'informatique sans ordi...

## Étudiants dans les classes - Strasbourg

- Pour info: création de l'option "Partenaire Scientifique pour la Classe" en L3 Informatique à Strasbourg: formation à l'informatique débranchée + formation générale sur le dispositif et l'enseignement des sciences en primaire par la conseillère pédagogique Sciences, 4 étudiant.e.s la première année, 12 la seconde. Bon accueil par les profs des écoles.
- Autre moyen de mettre des étudiants dans les classes (collège/lycée): "Cordée de la réussite, Décodeuses d'informatique", thème égalité filles-garçons en informatique https://mathinfo.unistra.fr/admission/lyceen/decodeuses-dinformatique/. Si quelqu'un à des questions contacter Julien Narboux.

## J'peux pas j'ai informatique
Martin présente les actions d'Anne-Cécile Orgerie et al. pour lutter contre les stéréotypes de genre en informatique. 
Pendant quelques années : 5 classes par an, activités branchées. Mais c'est compliqué d'accueillir 5 classes dans un labo.
En 2021 : version pour les profs, prévue pour 30, finalement 55 personnes présentes. Objectif : que les profs passent d'une position qui -- inconsciemment -- perpétue les stéréotypes à une position consciemment neutre voire encourageante.
Attention quand on fait ce genre d'exposé à ne pas accuser l'auditoire, à ne pas se poser en être supérieur et pur, mais à bien faire comprendre que chacun·e est empreint de stéréotypes, en est victime autant que vecteur de propagation. Par exemple essayez de faire ce test d'association implicite : https://implicit.harvard.edu/implicit/takeatest.html (on a beau être bien sensibilisé·e, le résultat fait mal). Que répondre à ceux et celles qui disent "moi je ne suis pas comme ça" : insister sur l'importance d'être proactive et pas seulement neutre.()

Tout le matériel présenté aux profs: https://gitlab.inria.fr/orgerie/jppjai-profs/

Martin nous montre le quiz (les quiz) pour casser les préjugés.

BD Les décodeuses https://www.cnrseditions.fr/catalogue/societe/les-decodeuses-du-numerique/
https://www.ins2i.cnrs.fr/fr/les-decodeuses-du-numerique

Exposé Isabelle Collet "Réintégrer les femmes dans les métiers du numérique : études de pratiques inclusives" https://videos-rennes.inria.fr/video/auC5Nyqp5

## Retour sur expérience Rennes - dialogue avec Grenoble
Rennes 
élèves ENS/L3 - L3 à Grenoble https://github.com/InfoSansOrdi/pedago-rennes/blob/trunk/sommaire.md
-> cycle 3
4x par semestre 2x en observateur

Grenoble https://iso.gricad-pages.univ-grenoble-alpes.fr/sim/
environ 20 étudiants  de L3
cycle 3 par binome
réseau de classes

On leur fournit un catalogue d'activités clé en main, mais les binômes se servent souvent de ressources supplémentaires.
Discussion sur le "bon" nombre d'étudiant·e·s à envoyer : à 4, c'est trop. À Rennes, 1 binôme actif et 2 binômes en observation (pour les premières séances).
Fête de la Science : envoyer des étudiant·e·s animer un stand avec une personne plus aguerrie pas trop loin, c'est une bonne idée.

Rennes toujours : en M1, philo des sciences, cours fait par un prof de philo. En binôme avec un prof d'info qui intervient de temps en temps pour raccrocher à des concepts d'informatique.
En M2, module "pédago 2" : créer des activités débranchées en lien avec leur sujet de stage de M1 ou de thèse. Souci : plein d'activités mais dont aucune n'est totalement terminée et fonctionnelle.

Allez voir CSunplugged ! site tout refait, en français, avec l'identification des compétences : https://www.csunplugged.org/fr/computational-thinking/
Pour la MMI et sa future expo "cuisine ": activité "alchimie" (qui peut se transposer en cuisine) et activité "crêpier" ici : cf. https://github.com/InfoSansOrdi/pedago-rennes/

## Chiche ! https://chiche-snt.fr
1 scientifique 1 classe : 1h en classe de 2e, SNT
Parler de recherche en informatique : c'est un peu ambitieux, parler de recherche et parler d'informatique, c'est déjà pas mal. Et humaniser les scientifiques.
ex. de déroulé (Marie) : démarrer par qq chose qui fait interrvenir les élèves : un quiz, expliquer un peu ce qu'est la recherche, faire une activité débranchée (se compter)
ne surtout pas faire un cours magistral sur son sujet de recherche


## ANR déposée sur les activités de médiation en informatique débranchée [Éric Duchêne]
quelles activités
que veut-on faire passer : une notion d'info, l'image de l'informaticien·ne, ?
rebrancher ?
lien entre les activités et l'informatique, épistémologie
concevoir 3-4 activités, les tester en pratique, analyser


## [Benjamin Wack] origami et réseaux

Idée d'activité pas finie. Des enveloppes dans une enveloppe dans une enveloppe pour parler d'encapsulation réseau. Marie propose d'utiliser ça pour expliquer Tor.

## [Jean-Marc Vincent] tri par insertion ou sélection avec des pailles (à boire) et des règles en bois
distinguer la boucle qui parcourt toutes les pailles
de l'opérateur soit de sélection qui repère la plus grande paille restante à trier
ou bien de l'opérateur d'insertion qui range la paille courante parmi les pailles déjà triées

## [Raphaël Bleuse] musique et maths
gamme pythagoricienne
parler de comment se construit une théorie mathématique.
Point de départ : Pythagore et les forgerons qui ont des marteaux de masses différentes : quand les masses ont des rapports simples, c'est harmonieux : différence bruit - note.
Sur une guitare : la note dépend de la corde (de sa masse linéaire), de la tension de la corde et de la  longueur de la corde.

 ressource intéressante sur le sujet https://arxiv.org/abs/1505.05380









----

### Recettes du jour

BROWNIE AUX SMARTIES (de la nièce de Nathalie)
: Préchauffer le four Th 6 (180°).
Faire fondre au micro-ondes dans un petit saladier 135 g de chocolat et 80 g de beurre (demi-sel de préférence).
Dans un autre saladier, mélanger 2 œufs et 165 g de sucre.
Y ajouter le chocolat fondu.
Ajouter ensuite 130 g de farine puis les smarties (100 g).
Cuire entre 22 et 25 mn. (Ne pas faire cuire plus de 30mn : même s'il n'a pas l'air cuit, il l'est. Si on prolonge la cuisson, en refroidissant il devient dur.)
Régalez-vous !
PS : je double les proportions et je cuis le gâteau 28mn.

MERINGUES 
: 65-70g de sucre pour 1 blanc d'oeuf.
Monter les blancs en neige très ferme, puis continuer à battre en incorporant le sucre.
Déposer de petits tas (dee la taille d'une grosse bouchée / 1 petite cuillère à soupe) sur une feuille de papier sulfurisé beurré. Enfourner à 120 degrés pour 30mn, puis baisser à 70 degrés pendant 1h30 (ou toute une nuit).


Gâteau aux noix (de Grenoble, what else)
: Ingrédients (pour 8 personnes) : 
- 200 g de sucre en poudre 
- 150 g de noix moulues 
- 125 g de farine 
- 175 g de beurre
- 4 oeufs 
- 2 cuillères à café de levure chimique 
- 1 cuillère à soupe de rhum (ou plus !!)
Préparation : 
Verser tous les ingrédients dans l'ordre dans une jatte. (Tout dans le mixer, à commencer par les noix, ça marche bien aussi.)
Bien mélanger. 
Verser dans un moule à génoise de 24 cm beurré. Faire cuire au four 35-40 min environ 180° (+ moelleux à 35 min)




























