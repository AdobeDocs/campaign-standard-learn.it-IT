---
title: 'Passaggio 1: creazione dell’app Android e configurazione per l’utilizzo della messaggistica Firebase Cloud'
description: In questa parte verrà creata l' [!DNL Android] app per ricevere [!UICONTROL Push notifications] inviata da Adobe Campaign Standard. Per ricevere le notifiche push, l'app deve essere registrata con Google [!DNL Firebase Cloud Service].
feature: Push
user: Admin
level: Experienced
jira: KT-4825
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: f087d9f2-cce9-4903-977f-3c5b47522c06
source-git-commit: 0ad82fb0533ed8fc2a85c2a32c7e54deef14d05a
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Passaggio 1: creazione dell&#39;app [!DNL Android] e configurazione per l&#39;utilizzo di [!DNL Firebase Cloud Messaging]

In questa parte verrà creata l&#39;app [!DNL Android] per ricevere [!UICONTROL Push notifications] inviato da Adobe Campaign Standard. Per ricevere le notifiche push, l&#39;app deve essere registrata con Google [!DNL Firebase Cloud Service].

1. Accedi al tuo account [!DNL Firebase].

   [!DNL Firebase] è la piattaforma mobile di Google che consente di sviluppare rapidamente app di alta qualità. Se non hai un account [!DNL Firebase], creane uno [da qui](https://firebase.google.com).

2. Avvia [!DNL Android Studio]
3. Fare clic su **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Selezionare **[!UICONTROL Empty Activity]** e fare clic su **[!UICONTROL Next].**

   ![progetto android](assets/android-project.PNG)

5. Specifica un nome significativo per il progetto.

   Ai fini di questa demo abbiamo denominato il nostro progetto come *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Accettare i nomi dei pacchetti predefiniti e fare clic su **[!DNL Finish]** per creare il progetto.
7. La struttura del progetto deve essere simile alla schermata seguente

   ![android-project-structure](assets/android-project-structure.PNG)

8. Fare clic su **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** (aggiunge il progetto a [!DNL Firebase])
9. Fare clic su **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![configurare firebase](assets/android-project-firebase-messaging.PNG)

10. Fare clic su **[!UICONTROL Connect to Firebase].**
11. Dopo aver connesso l&#39;app a Firebase, fai clic su **[!UICONTROL Add FCM to your app].**
12. Fare clic su **[!UICONTROL Accept Changes].**

   Quando aggiungi FCM all’app, la procedura guidata richiede l’autorizzazione per apportare alcune modifiche al progetto.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Una volta completata l’integrazione dell’app con Firebase, dovresti ricevere un messaggio simile a quello mostrato di seguito:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Verifica che il progetto sia elencato in [!DNL Firebase &#x200B;]console](https://console.firebase.google.com/)

## Configura impostazioni [!UICONTROL Push Channel]

1. Accedi alla console [!DNL Firebase]
2. Apri il progetto **[!UICONTROL ACSPushTutorial]**.
3. Fai clic sull&#39;**icona ingranaggio** e apri le impostazioni del progetto

   ![impostazioni-progetto](assets/firebase-project-settings.PNG)

4. Selezionare la scheda **[!UICONTROL Cloud Messaging]**.
5. Copia la chiave del server

   ![chiave server](assets/firebase-server-key.PNG)

6. Accedi all’istanza di Adobe Campaign Standard
7. Fare clic su **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Seleziona **[!UICONTROL Mobile Application Property].** appropriato
9. Fare clic sull&#39;icona **[!DNL Android]** nella sezione **[!UICONTROL Push Channel settings]**.
10. Incolla la chiave del server nel campo chiave del server.

Se tutto va bene, dovresti visualizzare un messaggio di SUCCESSO.

![impostazioni-canale-push](assets/push-channel-settings.PNG)

In sintesi, è stato creato un [!DNL Android App] e l&#39;utente [!DNL Android App] è stato connesso con [!DNL Firebase]. Abbiamo quindi connesso l&#39;app mobile in Adobe Campaign con [!DNL Android App] incollando la chiave del server dell&#39;app [!DNL Android] nell&#39;app mobile in Adobe Campaign Standard.
