---
title: Comprendere il connettore dati di Adobe Experience Platform
description: Il connettore dati di Adobe Experience Platform aiuta i clienti esistenti a rendere i propri dati disponibili su Adobe Experience Platform mappando i dati XTK (dati acquisiti in Campaign) su Experience Data Model (XDM) in Adobe Experience Platform.
feature: People Core Service Integration
jira: KT-2826
thumbnail: 27304.jpg
role: User
level: Experienced
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: 943599bd7ce139ef846f093ebda9084a91550aca
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 5%

---

# Comprendere Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>Questa funzionalità è disponibile in versione beta e soggetta a frequenti aggiornamenti e modifiche senza preavviso.
>
>Rivolgiti a [!UICONTROL Adobe Customer Support] se intendi implementare questa funzionalità.

## Panoramica

Adobe Experience Platform [!UICONTROL Data Connector] aiuta i clienti esistenti a rendere i propri dati disponibili su Adobe Experience Platform mappando i dati XTK (dati acquisiti in Adobe Campaign) su [!DNL Experience Data Model] (XDM) dati su Adobe Experience Platform.

Il connettore è unidirezionale e invia i dati da Adobe Campaign Standard a Adobe Experience Platform. I dati non vengono mai inviati da Adobe Experience Platform ad Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] è destinato ai data engineer che conoscono Adobe Campaign Standard [!UICONTROL custom resources] e che hanno una conoscenza di come lo schema generale dei dati del cliente dovrebbe essere all&#39;interno di Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/328612?learn=on&captions=ita){transcript=true}

*Questo video offre una panoramica sul Adobe Experience Platform [!UICONTROL Data Connector] (09:35 min)*

>[!NOTE]
>
>Il trasferimento predefinito di [!UICONTROL subscription events] non è supportato. Per trasferire [!UICONTROL subscription events], puoi creare il set di dati e XDM corrispondenti in Adobe Experience Platform, quindi configurare una mappatura dati personalizzata per questi dati.
>
>Impossibile acquisire in Adobe Experience Platform [!UICONTROL experience events] esistente, ma [!UICONTROL experience events] generato in corso viene inviato in streaming a Adobe Experience Platform.

## Passaggi chiave per eseguire una mappatura dei dati

I seguenti tutorial descrivono i passaggi chiave per eseguire una mappatura dei dati tra Campaign Standard e Adobe Experience Platform:

1. [Mappatura di risorse personalizzate](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Mappatura di eventi Experience](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mappatura dei dati della tabella dei valori iniziali](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modifica del mapping dei dati](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Verificare lo stato di un processo di acquisizione dati](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

