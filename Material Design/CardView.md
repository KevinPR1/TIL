# CardView

![D�composition CardView](https://user-images.githubusercontent.com/54910238/67548753-e83fc780-f702-11e9-89e8-ea4598774262.png)

![Multicards](https://user-images.githubusercontent.com/54910238/67548859-440a5080-f703-11e9-8cc4-eae52d4cbe41.png)

**build.gradle**

```java
dependencies {
    ...
    // CARD VIEW
    implementation 'com.android.support:cardview-v7:version
}

```



## Exemple 


> <android.support.v7.widget.CardView 

> </android.support.v7.widget.CardView>

```java

<?xml version="1.0" encoding="utf-8"?>
<android.support.v7.widget.CardView 

xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_margin="5dp"
 
    app:cardBackgroundColor="@android:color/white"
    app:cardCornerRadius="2dp"
    app:cardElevation="2dp">
 
    <!-- Les CardView poss�dent des attributs suppl�mentaires dont
         - cardBackgroundColor
         - cardElevation pour l'�l�vation (donc aussi l'ombre)
         - cardCornerRadius pour arrondir les angles
     -->
 
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical">
 
        <!-- Les CardView agissent comme des FrameLayout,
         pour avoir une organisation verticale nous devons
         donc rajouter un LinearLayout -->
 
        <ImageView
            android:id="@+id/image"
            android:layout_width="match_parent"
            android:layout_height="200dp"
            android:scaleType="centerCrop"
            tools:src="@drawable/parisguidetower" />
 
        <TextView
            android:id="@+id/text"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:background="?android:selectableItemBackground"
            android:padding="20dp"
            tools:text="Paris"
            android:textColor="#333"
            android:textSize="18sp" />
    </LinearLayout>
 
</android.support.v7.widget.CardView>

```

>  Les CardView poss�dent des attributs suppl�mentaires dont
         - cardBackgroundColor
         - cardElevation pour l'�l�vation (donc aussi l'ombre)
         - cardCornerRadius pour arrondir les angles
     

>   (exemple) Les CardView agissent comme des FrameLayout,
         pour avoir une organisation verticale nous devons
         donc rajouter un LinearLayout 



















