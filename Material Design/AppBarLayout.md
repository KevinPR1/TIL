# AppBarLayout


> AppBarLayout is a vertical LinearLayout which implements many of the features of material designs app bar concept, namely scrolling gestures. 

> Children should provide their desired scrolling behavior through setScrollFlags(int) and the associated layout xml attribute: app:layout_scrollFlags. 

> This view depends heavily on being used as a direct child within a **CoordinatorLayout**. If you use AppBarLayout within a different ViewGroup, most of it's functionality will not work. 

> AppBarLayout also requires a separate scrolling sibling in order to know when to scroll. 

> The binding is done through the AppBarLayout.ScrollingViewBehavior behavior class, meaning that you should set your scrolling view's behavior to be an instance of AppBarLayout.

> ScrollingViewBehavior. A string resource containing the full class name is available. 


## Exemple (xml)

```java
<android.support.design.widget.CoordinatorLayout
...
>
     <android.support.design.widget.AppBarLayout
             android:layout_height="wrap_content"
             android:layout_width="match_parent">

         <android.support.v7.widget.Toolbar

                 ...
                 app:layout_scrollFlags="scroll|enterAlways"/>

         <android.support.design.widget.TabLayout
                 ...
                 app:layout_scrollFlags="scroll|enterAlways"/>

     </android.support.design.widget.AppBarLayout>


</android.support.design.widget.CoordinatorLayout>

```