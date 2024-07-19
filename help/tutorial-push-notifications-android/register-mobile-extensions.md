---
title: 'Passaggio 3: registrare le estensioni con la tua app mobile'
description: In questa parte viene aggiunto il codice per registrare le estensioni UserProfile, Identity, Lifecycle e Signal.
feature: Push
user: Admin
level: Experienced
jira: KT-4827
doc-type: tutorial
activity: use
team: TM
exl-id: d8c0d8c6-2e04-4c27-b27a-d0de79dd953b
source-git-commit: 9be31e056800b806c49a2c5ffbf9f9f42b001d4c
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 14%

---

# Passaggio 3: registrare le estensioni con la tua app mobile

In questa parte viene aggiunto il codice per registrare le estensioni Profilo utente, Identità, Ciclo di vita e Segnale. Dobbiamo anche registrare l’estensione Adobe Campaign Standard come mostrato nel codice seguente.

Apri il progetto in [!DNL Android] studio. Eliminare l&#39;intero codice in MainApp **ad eccezione della prima riga, che rappresenta l&#39;istruzione del pacchetto**.

Incolla il seguente codice in MainApp

<!--
Removed `{.line-numbers}` below
-->

```java
import [!DNL android].app.Application;
import android.util.Log;

import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.Campaign;
import com.adobe.marketing.mobile.Identity;
import com.adobe.marketing.mobile.InvalidInitException;
import com.adobe.marketing.mobile.Lifecycle;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;
import com.adobe.marketing.mobile.Signal;
import com.adobe.marketing.mobile.UserProfile;

public class MainApp extends Application {

@Override
public void onCreate() {
super.onCreate();

MobileCore.setApplication(this);
MobileCore.setLogLevel(LoggingMode.DEBUG);

try{
    Campaign.registerExtension();
    UserProfile.registerExtension();
    Identity.registerExtension();
    Lifecycle.registerExtension();
    Signal.registerExtension();
    MobileCore.start(new AdobeCallback () {
        @Override
        public void call(Object o) {
            MobileCore.configureWithAppID("copy your launch property id here");
        }
    });
} catch (InvalidInitException e) {
    Log.d("ACS Exception", "exception");
}
}
}
```

Riga 32 è necessario fornire l&#39;ID del file di ambiente della proprietà [!UICONTROL  Launch]. È possibile accedervi dal [!UICONTROL environment tab] della proprietà [!UICONTROL Launch].

![launch-id](assets/launch-id-property.PNG)
