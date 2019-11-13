# EventBus

> Librairie permettant de communiquer entre Fragment et activit�, passer une information entre diff�rents fragments ou diff�rentes classes/activit�s.

## EventBus fonctionne de la mani�re suivante, si nous voulons envoyer un message de la classe A vers la classe B :

1. B s�enregistre en tant que receveur aupr�s d�EventBus
2. A envoie le message � EventBus
3. EventBus le transmet � B

> buidl.gradle
```java
dependencies {
 // EVENT BUS
    implementation 'org.greenrobot:eventbus:3.1.1'
}
```

## **D�clarer un �v�nement**

> le nom de la classe d�signe uniquement le sens de l'information

> Exemple

```java
public class DeleteCurrentMeeting{
}
```

# Lancer un �v�nement

```java
EventBus.getDefault().post(new PleaseRefreshEvent());
```

Recevoir un �v�nement

> Exemple ---- register and unregister

```java
public class MyFragment extends Fragment{
 
    @Override
    public void onStart() {
        super.onStart();
        EventBus.getDefault().register(this);
    }
    @Override
    public void onStop() {
        super.onStop();
        EventBus.getDefault().unregister(this);
    }
}
```
> + la m�thode void onEvent pour d�crire son action

* Exemple (on change le nom pour le sens)

```java
 public void onDeleteCurrentMeetingEvent(DeleteCurrentMeetingEvent event){
        mMeetingApiService.deleteToMeetingList(event.mMeeting);
    }
```
> � ajouter dans la classe receveur

```java
    @Override
    protected void configureOnStart() {
        EventBus.getDefault().register(this);
    }

    @Override
    protected void configureOnStop() {
        EventBus.getDefault().unregister(this);
    }
    public void onDeleteCurrentMeetingEvent(DeleteCurrentMeetingEvent event){
        mMeetingApiService.deleteToMeetingList(event.mMeeting);
    }
```

