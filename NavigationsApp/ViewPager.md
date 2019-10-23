# Navigation par Onglets

1. Cmpte un �cran principal (Fil d'actualit�), et quelques �crans secondaires

2. Une quantit� de donn�es relativement importante

3. **La navigation par onglets peut �tre combin�e avec d'autres syst�mes de navigation**


##Impl�mentation

* ViewPager 
* Fragments 


### Exemple

```java
dependencies {
    compile 'com.android.support:appcompat-v7:26.1.0'
}
```

* **Ajout de l'�l�ment ViewPager dans le layout de l'Activit� concern�e**

1. **Adapter** 

> Extend FragmentStatePagerAdapter (Cet adapter ne va PAS garder en m�moire toutes les pages affich�es (fragments) apr�s leur cr�ation.)

> Extend FragmentPagerAdapter (Cet adapter va garder en m�moire toutes les pages affich�es (fragments) apr�s leur cr�ation.)

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
	

		
	






























