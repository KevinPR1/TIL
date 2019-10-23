# Navigation via un menu

1. énormément d'écrans consultables

2. "camoufler" la partie navigation à ses utilisateurs

3. Système de navigation très évolutif 


##Implémentation

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

* DrawerLayout (utilisé comme layout racine principal)
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
































