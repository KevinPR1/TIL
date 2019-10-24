# 2 d�marches pour g�rer un click 

* Button
* ImageView
* .....



## D�marches

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

> via le layout : android:onClick="NomDeLaM�thode"



```java

BindView(R.id.identifiant) TextView tv ;
OR
TextView tv ; 
......
tv = (TextView) findViewById(R.id.identifiant)
..
Then
......
pv NomDeLaM�thode(View view) {

tv.setText("Answer")

}

```
