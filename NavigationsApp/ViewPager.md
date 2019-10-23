# Navigation par Onglets

1. Cmpte un écran principal (Fil d'actualité), et quelques écrans secondaires

2. Une quantité de données relativement importante

3. **La navigation par onglets peut être combinée avec d'autres systèmes de navigation**


##Implémentation

* ViewPager 
* Fragments 


### Exemple

```java
dependencies {
    compile 'com.android.support:appcompat-v7:26.1.0'
}
```

* **Ajout de l'élément ViewPager dans le layout de l'Activité concernée**

1. **Adapter** 

> Extend FragmentStatePagerAdapter (Cet adapter ne va PAS garder en mémoire toutes les pages affichées (fragments) après leur création.)

> Extend FragmentPagerAdapter (Cet adapter va garder en mémoire toutes les pages affichées (fragments) après leur création.)

	* Constructeur
	* getCount()
	* getItem()


2. **Attacher l'adapter au ViewPager**
	* Activity



3. **Ajoutez des onglets**

```java
dependencies {
    compile 'com.android.support:design:26.1.0'
}
```
> LinearLayout
* Ajouter la vue TabLayout au-dessus de notre ViewPager 

* Ajouter getPageTitle(int position) dans l'Adapter afin de retourner le titre de chacune des pages d'un ViewPager
	> Overwride
* Attacher le TabLayout au ViewPager 
	> Activity
	

		
	






























