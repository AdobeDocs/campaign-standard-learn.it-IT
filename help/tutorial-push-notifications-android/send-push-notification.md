---
title: Parte 6 - Inviare una notifica push per testare il lavoro
description: Parte 6 - Inviare una notifica push per testare il lavoro
feature: Push
jira: KT-4830
user: Admin
level: Experienced
doc-type: tutorial
activity: use
team: TM
exl-id: 10218e1f-6e85-490a-84d9-c5d42bd2321d
TQID: 'https://experienceleague.adobe.com/NrQc40vzqTy0fNfVT6fN0IjMKuXjilt6eZV-lgZpAcQ'
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
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: 508c3590ce956401ccfba3a256000cbc5849a684
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%
---
# Parte 6 - Invia [!UICONTROL Push Notification] per testare il tuo lavoro

È ora necessario creare e inviare un [!UICONTROL Push Notification] tramite Adobe Campaign. Per creare una semplice notifica push a scopo di test, segui la procedura riportata di seguito.

* Accedi all’istanza di Adobe Campaign Standard
* Fare clic su **[!UICONTROL Marketing Activities]->[!UICONTROL Create]->[!UICONTROL Push Notification]**
* Seleziona **[!UICONTROL Send push to app subscribers(mobileApp)]** e fai clic su Avanti
* Selezionare l&#39;app mobile appropriata dall&#39;elenco a discesa **[!UICONTROL Associate a Mobile App to a delivery]** e fare clic su **[!UICONTROL Next]**
* Fai clic sull’etichetta del conteggio per restituire un valore maggiore di 0. Fai clic su **[!UICONTROL Next]**
* Specificare [!UICONTROL Message title] e [!UICONTROL Message body] significativi e fare clic su **[!UICONTROL Create]**.
* Fai clic su **[!UICONTROL Prepare]**. Una volta completata la preparazione, fare clic su **[!UICONTROL Confirm]** per inviare il messaggio.

Se tutto va bene, dovresti vedere la notifica nell’app Android™ in esecuzione nell’emulatore

## Risorse aggiuntive

* [Documentazione dettagliata sulle notifiche push](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/push-notifications/about-push-notifications.html?lang=en)
* [Creazione di una notifica push (video)](/help/communication-channels/mobile/push-notifications/creating-a-push-notification.md)
