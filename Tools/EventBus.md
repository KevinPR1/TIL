# EventBus

> Librairie permettant de communiquer entre Fragment et activité, passer une information entre différents fragments ou différentes classes/activités.

## EventBus fonctionne de la manière suivante, si nous voulons envoyer un message de la classe A vers la classe B :

1. B s’enregistre en tant que receveur auprès d’EventBus
2. A envoie le message à EventBus
3. EventBus le transmet à B

> buidl.gradle
```java
dependencies {
 // EVENT BUS
    implementation 'org.greenrobot:eventbus:3.1.1'
}
```

## **Déclarer un événement**

> le nom de la classe désigne uniquement le sens de l'information

> Exemple

```java
public class DeleteCurrentMeeting{
}
```

# Lancer un événement

```java
EventBus.getDefault().post(new PleaseRefreshEvent());
```

Recevoir un évènement

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
> + la méthode void onEvent pour décrire son action

* Exemple (on change le nom pour le sens)

```java
 public void onDeleteCurrentMeetingEvent(DeleteCurrentMeetingEvent event){
        mMeetingApiService.deleteToMeetingList(event.mMeeting);
    }
```
> À ajouter dans la classe receveur

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

