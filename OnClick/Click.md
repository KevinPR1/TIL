# 2 d�marches pour g�rer un click 

* Button
* ImageView
* .....



## D�marches

> via un View.OnClickListener

```java

TextView tv ; 
......
Then
......
private void MyMethod(){
      
       tv = (TextView) findViewById(R.id.TextView) ;
       
        imageViewOC.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {

 		tv.setText("Answer")
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
