Pokémon battle
==============
Le projet Pokémon battle est une adaptation des jeux de programmation comme 
[Core War](http://fr.wikipedia.org/wiki/Core_War) ou [Robocode](http://robowiki.net/). Le but de ces jeux est de 
voir s'affronter des programmes dans une compétition dans un univers aux règles connues de tous.

Dans notre cas l'univers choisi est celui des Pokémons. Les combattants sont des dresseurs qui ont pour objectif de 
faire s'affronter des Pokémons pour remporter la compétition. Au début du jeu les combattants pourront être humains 
mais au fur et à mesure de l'avancée du projet, il faudra les remplacer autant que possible par des intelligences
artificielles.

Il existe plusieurs solutions pour gérer l'univers de notre jeu, partant des plus centralisées avec un serveur
omniscient qui a la responsabilité d'animer les acteurs jusqu'aux plus décentralisées où chaque acteur est un 
programme totalement autonome interagissant directement avec les autres programmes. La solution que nous avons retenue, 
est entre les deux. En effet, en plus des dresseurs et des Pokémons, il existe plusieurs autres types d'acteurs que 
nous appellerons les *médiateurs*. Le but de ces acteurs particuliers est de garantir le bon fonctionnement du jeu. Un 
peu comme les gendarmes et les voleurs, vous devrez améliorer les médiateurs au fur et à mesure que les dresseurs se perfectionneront .

En plus des acteurs il existe un certain nombre de services publics qui permettent de gérer certaines règles de
l'univers. Par exemple, la gestion de tous les échanges financiers sera confiée à la *Pokémon National Bank*(PNB).

* Rôles :
   - Pokémon
   - Dresseurs
   - Arbitre de combat
   - Gérant d'une Arène
   - Organisateur de championnats
   - Espion
* Services :
   - Tableau des scores et classements
   - Annuaire des dresseurs
   - Pokedexia Universalis
   - Tribunal Révolutionaire Pokémon
   - Pokémon National Bank

Description des rôles :
-----------------------
1. Pokémon :  
   ![Pikachu](http://img4.xooimage.com/files/f/6/1/pikachu-110ec1.jpg) Les Pokémons sont des créatures belliqueuses par nature, leur préoccupation principale est de se battre. Pour cela chaque espèce apprend des attaques. La liste des attaques que peut apprendre un Pokémon dépend uniquement de son espèce. Pour chacune d’elles, on souhaite connaître sa description textuelle, sa puissance et la probabilité d’atteindre sa cible. Comme les espèces de Pokémons, les attaques aussi possède un “type”. Une attaque n’a qu’un et un seul type. Un Pokémon d’un type donné ne peut apprendre que des attaques de son type. Au fil des combats, il gagne des points d'expérience qui lui permette de faire évoluer ses caractéristiques. Son parcours initiatique est jalonné en niveau. Le Pokémon peut évoluer. Chaque espèce de Pokémon à des caractéristiques qui lui sont propres. À la naissance, deux Pokémons de la même espèces sont légèrement différents. Ses différences s'expliquent par le caractère propre à chaque individu.
   

2. Dresseurs :  
   ![Sacha](https://twimg0-a.akamaihd.net/profile_images/2711619684/e05382a4d026c7654d7a0cbf21fe64b7.jpeg) Le dresseur est le propriétaire d'un Pokémon. Son but est d'entraîner au mieux ses Pokémons au combat pour obtenir l'équipe capable de remporter tous les championnats. Dans son équipe il ne peut pas avoir plus de 3 Pokémons. Pour obtenir de nouveaux Pokémon il y a 4 possibilités : Les attraper, les gagner au combat, les échanger ou les vendre.

3. Arbitre de combat :  
   L'arbitre de combat est la personne qui a la responsabilité de veiller au respect des règles de combat. C'est lui qui déclare le gagnant et le perdant de chaque combat. Il doit aussi transmettre les fiches de combat au gérant de l'arène qui s'occupera d'établir les classements. Si un dresseur contrevient au règlement, son Pokémon engagé au combat ira au dresseur adverse.

4. Gérant d'une arène :  
   C'est la mémoire d'une arène, les arbitres s'adressent à lui pour organiser les combats. Il s'occupe de la gestion des points ainsi que des classements. Il vérifie la cohérence des informations qui lui sont transmises et établit les différents classements.
   
5. Organisateur de championnats :  
   Régulièrement les arènes organisent des championnats pour déterminer qui est le meilleur dresseur. L'organisateur a 
   la charge de gérer les inscriptions, de planifier les combats, choisir les arbitres et de déclarer le vainqueur de la 
   compétition.

6. Espion :  
   L'espion se fait passer pour un dresseur pour identifier les tricheurs. À chaque tricheur détecté il gagne des points qui lui permettent d'améliorer son classement dans la ligue des espions. Quand il pense avoir détecté une fraude, il la déclare au *Tribunal Révolutionaire Pokémon* qui déterminera grâce aux éléments fournis si la fraude est avérée. Toute fraude détectée rapporte aussi de l'argent.
   
Description des services :
--------------------------

1. Tableau des scores et classements :  
   TODO!
   
2. Annuaire des dresseurs :  
   TODO!
   
3. Pokedexia Universalis :  
   Le pokédex (ou Pokedexia Universalis) est l'encyclopédie des Pokémons, il connaît tout sur toute les espèces. L’un des premiers objectifs du Pokédex est de répertorier toutes les espèces de Pokémons existantes. Pour chacun d’eux le dresseur souhaite connaître toutes les caractéristiques. Une espèce de Pokémon possède un nom qui est unique, une taille, un poids et une couleur. Par exemple l’espèce nommée “Bulbizarre” mesure 0,7m, pèse 6,9kg et est de couleur verte. Pour chaque espèce, on souhaite aussi connaître en quelle espèce elle peut évoluer. Certaines espèces sont au sommet de l’arbre de l’évolution et n’ont donc pas d’évolution possible. 

   Le pokédex est capable de répondre à toutes les questions sur les espèces de Pokémons. Jamais il ne se trompe. Il peut être utilisé pour établir la fraude d'un dresseur. Quand un Pokémon vient au monde, il peut apprendre ses caractéristiques de base en interrogeant le pokédex.

4. Tribunal Révolutionaire Pokémon :  
   C'est le gardien de la loi, c'est lui qui punit le tricheur et qui récompense les espions.

5. Pokémon National Bank :  
   Le monde des Pokémons étant encore soumis à une dictature communiste, il n'y a qu'une seule banque d'état. C'est elle qui effectue la gestion des comptes de chaque dresseur et les flux financiers associés.

Idées pour le protocole:
------------------------
Le protocole de communication de chaque robot sera basé sur un ensembles de hashtag. Les Pokémons sont responsables d'eux mêmes. Mais ils déclarent sur leur timeline chacun de leurs changements. Ainsi un espion pourra toujours vérifier facilement la validité de ses informations.

Chaque robot doit pouvoir être interrogé sur les données qu'il conserve. Selon la nature de ses données, il peut soit les afficher dans sa timeline soit renvoyer vers une URL durable.

L'espèce d'un Pokémon est déterminée par son nom. Par exemple, un Pokémon nommé [@pikachuNyanNyan](http://www.youtube.com/watch?v=VRA-4skclcs) sera de l'espèce pikachu. Son avatar devra correspondre à son espèce. 

Dans les arènes de base, les combats sont 1 contre 1. Le Pokémon est choisi par le dresseur en début de combat. Un combat, sera donc une suite de choix d'attaques qui aura lieu à tour de rôle jusqu'à ce qu'un Pokémon ait épuisé ses points de vie. Si pour une raison ou une autre un Pokémon ne répondait plus pendant un délais trop long, il serait déclaré forfait.

Un arbitre n'acceptera d'effectuer qu'un certain nombre de combats par heure pour ne pas dépasser son quota.

Pour attraper un Pokémon :
```
Dresseur demande propriétaire à Pokémon
Pokémon répond son état à Dresseur (Sauvage ou nom de proprio)
Dresseur envoie Pokeball pour l'attraper
Pokémon répond en disant son nouvel état (Sauvage ou nom de son nouveau proprio)
```
Pour échanger un Pokémon :
```
Dresseur1 demande à dresseur2 echange du Pokémon voulu
```

Trace du travail effectué le 04/03 :
```
Dresseur1: @pikachuNyanNyan #attack #Foudre @bulbizare1 /cc @dresseur2  @arbitre1
Dresseur2: @bulbizare1 #attack #Baston @pikachuNyanNyan /cc @dresseur1  @arbitre1
pikachuNyanNyan : @bulbizare1 #attack #Foudre /cc @arbitre1 @dresseur1  @dresseur2
bulbizare1 : @pikachuNyanNyan #attack #Baston /cc @arbitre1 @dresseur1  @dresseur2
Arbitre1: @pikachuNyanNyan -10pv /cc @dresseur1
Arbitre1: @bulbizare1 -100pv /cc @dresseur2
Dresseur1: @pikachuNyanNyan #attack #Foudre @bulbizare1 /cc @dresseur2  @arbitre1
Dresseur2: @bulbizare1 #attack #Baston @pikachuNyanNyan /cc @dresseur1  @arbitre1
pikachuNyanNyan : #dodo /cc @arbitre1 @dresseur1  @dresseur2
bulbizare1 : @pikachuNyanNyan #attack #Baston /cc @arbitre1 @dresseur1  @dresseur2
Arbitre1: @pikachuNyanNyan -10pv /cc @dresseur1
Arbitre1: @bulbizare1 +0pv /cc @dresseur2
pikachuNyanNyan : #KO /cc @arbitre1 @dresseur1  @dresseur2
Arbitre1: @dresseur2 #Win 
```

- pokemon
  - attrapage
  - combat: attack, dodo, ko

- arbitre
  - donner resultat attacks
  - donner resultat combats
