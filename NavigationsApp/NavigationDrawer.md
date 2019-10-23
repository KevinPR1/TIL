# Navigation via un menu

1. �norm�ment d'�crans consultables

2. "camoufler" la partie navigation � ses utilisateurs

3. Syst�me de navigation tr�s �volutif 


##Impl�mentation

* Navigation Drawer
* Fragments


### Exemple

dependencies :

```java
dependencies {
    compile 'com.android.support:design:26.1.0'
}
```

#### **Activity Layout** 

* DrawerLayout (utilis� comme layout racine principal)
* Toolbar 
* FrameLayout
* NavigationView
```java
<android.support.design.widget.NavigationView
	.....
	.....
  	app:headerLayout="@layout/activity_main_nav_header"
        app:menu="@menu/activity_main_menu_drawer" />
```
 + Configuration layout "menu" + "header"

> menu.xml

> header.xml


#### Activity

1. Config elements (Toolbar..)

2. Fragments

3. Config each Item Selected
































