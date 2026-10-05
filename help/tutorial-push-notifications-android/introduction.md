---
title: Guida introduttiva alle notifiche push con app Android™
description: Il presente tutorial illustra i passaggi necessari per l’invio di notifiche push da Adobe Campaign e la ricezione di tali notifiche all’interno dell’app Android™.
feature: Push
jira: KT-3846
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: 8dd772b2-b082-4e1e-842d-c5d6bcec564c
TQID: 'https://experienceleague.adobe.com/Ov4KKtdN-uhIr-TGldJCXw3GYFNUjap-SBE227dImfw'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
  - id: f5407121-8933-4ac3-8e06-a9b692a4e88a
    internal-label: Campaign Standard
feature_v2:
  - id: a4671286-a59f-47e3-b97b-90627a1977d5
    internal-label: Communication channels
subfeature_v2:
  - id: a4657621-810c-498b-8a27-7ced9c176dda
    internal-label: Push notifications
source-git-commit: 508c3590ce956401ccfba3a256000cbc5849a684
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 100%
---
# Guida introduttiva alle notifiche push con app Android™

Adobe Campaign ti consente di inviare notifiche push personalizzate e segmentate ai dispositivi mobili iOS e Android™.
Questi messaggi vengono ricevuti nelle app mobili che configuri in Adobe Campaign mediante Experience Cloud Mobile SDK V4 o Experience Platform SDK.
Il presente tutorial illustra i passaggi necessari per l’invio di notifiche push da Adobe Campaign e la ricezione di tali notifiche all’interno dell’app Android™.

## Prerequisiti

* Devi configurare la proprietà di Platform Launch con Adobe Campaign Standard Extension. Segui la guida online elencata di seguito.
  * [Tutorial video](https://video.tv.adobe.com/v/26224?learn=on){transcript=true}
  * [Documentazione](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.html?lang=it)

* Assicurati che lo stato della proprietà corrispondente in Adobe Campaign Standard sia impostato su configurato.
* [Disporre di un account Google Firebase attivo](https://firebase.google.com)
* [Versione più recente di Android™ Studio installata](https://developer.android.com/studio)

## Passaggi del tutorial

* [Passaggio 1 - Creare un’app Android™](/help/tutorial-push-notifications-android/create-android-app.md)
* [Passaggio 2: integrare l’SDK per dispositivi mobili](/help/tutorial-push-notifications-android/integrating-with-mobile-sdk.md)
* [Passaggio 3: registrare le estensioni con la tua app mobile](/help/tutorial-push-notifications-android/register-mobile-extensions.md)
* [Passaggio 4: impostare l’identificatore push](/help/tutorial-push-notifications-android/set-push-identifier.md)
* [Passaggio 5: propagare le notifiche](/help/tutorial-push-notifications-android/propagate-notification.md)
* [Passaggio 6: inviare le notifiche push](/help/tutorial-push-notifications-android/send-push-notification.md)
