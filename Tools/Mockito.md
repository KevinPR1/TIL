#Mockito 


Mockito est un framework qui permet de bouchonner certaines parties de code.
Il permet de simuler l'appel à certaines méthodes, et de décider à l'avance de la valeur retournée.

##Exemple

> Tester l'intéraction avec un bouton (objet)

* Le problème, c'est qu'il est désormais nécessaire de lancer l'application et d'intervenir manuellement 
pour gérer cette action. Et c'est là que Mockito intervient : il va nous permettre de simuler cette partie, 
et nous renvoyer directement le résultat. Et le tout localement, savoir avoir à lancer l'émulateur.


```java

dependencies { testCompile "org.mockito:mockito-core:2.+" }


```