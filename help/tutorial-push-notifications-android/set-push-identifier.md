---
title: 'PASSAGGIO 4: impostare l’identificatore push'
description: '**pushIdentifier** è una stringa che contiene il token del dispositivo per le notifiche push. È lo stesso token inviato da Firebase e passato all''SDK utilizzando il metodo MobileCore.setPushIdentifier.'
feature: Push
user: Admin
level: Experienced
jira: KT-4828
doc-type: tutorial
activity: use
team: TM
exl-id: 08387b84-edaa-45ee-ae66-53bcbd5c7c39
source-git-commit: 757afce50981b96b7820c987308d639a73746c0c
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Passaggio 4 - Imposta [!DNL pushidentifier]

**[!DNL pushidentifier]** è una stringa che contiene il token del dispositivo per [!DNL Push] notifiche. È lo stesso token inviato da [!DNL Firebase] e passato all&#39;SDK utilizzando il metodo [!DNL MobileCore.setPushIdentifier].

Apri il progetto in [!DNL Android™] studio. Eliminare l&#39;intero codice in [!DNL MainActivity] **ad eccezione della prima riga, che rappresenta l&#39;istruzione del pacchetto**.

Incolla il seguente codice in [!DNL MainActivity]:

<!--
Removed `{.line-numbers}` below
-->

```java
import androidx.annotation.NonNull;
import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.util.Log;
import android.widget.Toast;

import com.adobe.marketing.mobile.MobileCore;
import com.google.android.gms.tasks.OnCompleteListener;
import com.google.android.gms.tasks.Task;
import com.google.firebase.iid.FirebaseInstanceId;
import com.google.firebase.iid.InstanceIdResult;

public class MainActivity extends AppCompatActivity {

@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);

registerToken();
}

void registerToken() {
FirebaseInstanceId.getInstance().getInstanceId()
    .addOnCompleteListener(new OnCompleteListener<InstanceIdResult>() {
        @Override
        public void onComplete(@NonNull Task<InstanceIdResult> task) {
            if (!task.isSuccessful()) {
                Log.w("Message App", "getInstanceId failed", task.getException());
                return;
            }

// Get new Instance ID token
String token = task.getResult().getToken();

Log.d("Got token", token);

MobileCore.setPushIdentifier(token);
}
});
}

@Override
public void onResume() {
super.onResume();
MobileCore.setApplication(getApplication());
MobileCore.lifecycleStart(null);
}

@Override
public void onPause() {
super.onPause();
MobileCore.lifecyclePause();
}
}
```

## Test dell’app

Ora è il momento giusto per testare l’app, prima di procedere.

* Esegui l&#39;app facendo clic sulla freccia verde o seleziona **[!DNL Run->Run'app']**.
* L&#39;emulatore [!DNL Android™] dovrebbe iniziare e l&#39;app dovrebbe essere in esecuzione con [!DNL "Hello World"] testo.
* Apri la finestra [!DNL logcat]. Cerca &quot;[!DNL Got]&quot;. Dovresti visualizzare il token ricevuto da [!DNL Firebase] scritto nel registro come mostrato di seguito. La stringa lunga dopo &quot;[!DNL Got token]&quot; è [!DNL pushidentifier]inviata ad Adobe Campaign.

![logcat-token](assets/logcat-got-token.PNG)

### Verifica abbonati a applicazioni mobili

Accedi all’istanza di Adobe Campaign Standard.
Passa a **[!UICONTROL Administration->Channels->Mobile App(Experience Platform SDK)]**. Apri l’app mobile appropriata. Selezionare la scheda [!UICONTROL Mobile Application Subscribers]. Dovresti trovare [!UICONTROL registration token] nell&#39;elenco.

![abbonati ad app mobili](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>Se il token di registrazione non è visualizzato nella scheda [!UICONTROL Mobile Application Subscribers], FERMARSI qui prima di procedere.
