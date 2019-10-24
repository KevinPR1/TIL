# 2 démarches pour gérer un click 

* Button
* ImageView
* .....



## Démarches

> via un View.OnClickListener

```java

Button bt ; 
......
Then
......
private void MyMethod(){
      
       imageViewOC =(ImageView) findViewById(R.id.imageView) ;
       
        imageViewOC.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
 
            }
        });
}


```

> via le layout : android:onClick="NomDeLaMéthode"



```java

BindView(R.id.identifiant) TextView tv ;
OR
TextView tv ; 
......
tv = (TextView) findViewById(R.id.identifiant)
..
Then
......
pv NomDeLaMéthode(View view) {

tv.setText("Answer")

}

```
