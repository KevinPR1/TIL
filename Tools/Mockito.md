#Mockito 


Mockito est un framework qui permet de bouchonner certaines parties de code.
Il permet de simuler l'appel � certaines m�thodes, et de d�cider � l'avance de la valeur retourn�e.

##Exemple

> Tester l'int�raction avec un bouton (objet)

* Le probl�me, c'est qu'il est d�sormais n�cessaire de lancer l'application et d'intervenir manuellement 
pour g�rer cette action. Et c'est l� que Mockito intervient : il va nous permettre de simuler cette partie, 
et nous renvoyer directement le r�sultat. Et le tout localement, savoir avoir � lancer l'�mulateur.


```java

dependencies { testCompile "org.mockito:mockito-core:2.+" }


```