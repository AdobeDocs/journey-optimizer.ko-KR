---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에서 메시지 내보내기
description: 메시지를 내보내는 방법 알아보기
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 내보내기, 메시지, HIPAA, 이메일, SMS, 구성
badge: label="제한된 가용성" type="Informative"
hide: true
hidefromtoc: true
exl-id: 7b50c933-9738-4b1b-acae-08f0a8d41dab
source-git-commit: 8bc0d28ea3e7c26bd8f7a35d00a73e41f35720d0
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 8%

---

# 메시지 콘텐츠 내보내기 {#message-export}

>[!CONTEXTUALHELP]
>id="ajo_admin_msg_export"
>title="전송된 콘텐츠 보존 및 내보내기"
>abstract="이 옵션을 선택하면 이 구성을 사용하여 보낸 이메일이나 SMS 메시지의 내용을 [!DNL Experience Platform]데이터 세트에 쓸 수 있습니다. 레코드는 수집 후 7일 동안 유지되며, 이 기간 동안 자체 스토리지로 내보낼 수 있습니다."

>[!AVAILABILITY]
>
>이 기능은 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.

**메시지 내보내기**&#x200B;를 사용하면 보낸 전자 메일 및 SMS 메시지 콘텐츠를 [!DNL Journey Optimizer]에서 [!DNL Adobe Experience Platform] 대상을 통해 자신의 저장소로 전송하여 [!DNL Experience Platform]의 데이터를 외부 끝점으로 전달할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/destinations/home){target="_blank"}

이 기능을 사용하면 내보내기로 표시된 [!DNL Journey Optimizer]을(를) 통해 보낸 전자 메일 및 SMS 메시지의 콘텐츠가 [!DNL Experience Platform] **AJO 메시지 내보내기 데이터 세트**&#x200B;에 기록됩니다.

그러면 레코드는 수집 후 7일 동안 **AJO 메시지 내보내기 데이터 세트**&#x200B;에 보관되며, 이 기간 동안 선택한 외부 시스템으로 내보낼 수 있습니다.
<!--
## Terminology

* **[!DNL Experience Platform] destinations** - Framework to deliver data out of Experience Platform into external endpoints. [Learn more](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/home){target="_blank"}
* **AJO Message Export Dataset** - An [!DNL Experience Platform] dataset which stores the message content of email and SMS messages sent via [!DNL Journey Optimizer] which have been marked for export.
* **Retention**: Records in the AJO Message Export Dataset are retained for 3 calendar days from ingestion.-->

## 가드레일

* 이 기능은 이메일 및 SMS 채널만 지원합니다.
* AJO 메시지 내보내기 데이터 세트의 레코드는 수집 후 7일 동안 유지됩니다.
* 아래 설명된 대로 메시지 내보내기를 활성화하기 전에 전송된 메시지에 대해서는 채우기 기능이 지원되지 않습니다.

## 메시지 내보내기 활성화 {#enable-message-export}

메시지 내보내기 기능에 대한 온보딩 프로세스는 다음 두 단계로 구성됩니다.

1. [에서 &#x200B;](#set-up-export-dataflow)내보내기 데이터 흐름을 설정[!DNL Experience Platform];
1. [의 채널 구성에서 &#x200B;](#config-message-export)메시지 내보내기 사용[!DNL Journey Optimizer].

>[!WARNING]
>
>내보내기를 활성화하고 메시지를 보낸 후의 새 레코드만 표시됩니다. 내보내기 프로세스를 설정하고 메시지 내보내기 옵션을 활성화하기 전의 콘텐츠 채우기는 지원되지 않습니다.

### 내보내기 데이터 흐름 설정 {#set-up-export-dataflow}

데이터를 내보내려면 먼저 [!DNL Experience Platform] 대상 및 사용할 데이터 집합을 정의하여 내보내기 프로세스를 설정해야 합니다. 아래 단계를 수행합니다.

>[!NOTE]
>
>각 샌드박스에 대해 이 설정을 구성해야 합니다.

1. Experience Platform [대상 유형](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/destination-types){target="_blank"}을(를) 선택하십시오. 데이터를 받을 준비가 된 사용 가능한 대상 플랫폼 목록을 [이 페이지](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/overview){target="_blank"}에서 사용할 수 있습니다.

1. [!DNL Experience Platform]에서 자격 증명, 버킷/컨테이너, 경로 접두사 및 보안 옵션을 정의하여 대상을 구성합니다. [방법 알아보기](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets){target="_blank"}

1. 다음 데이터를 사용하여 데이터 세트 내보내기 플로우를 만듭니다.

   * Source 데이터 세트: **AJO 메시지 내보내기 데이터 세트**&#x200B;를 선택합니다.
   * 파일 포맷: JSON 또는 Parquet 을 선택합니다(다운스트림 도구를 기반으로 한 선택).
   * 일정: 7일 보존 기간 내에 실행되는지 확인합니다.

### 채널 구성에서 메시지 내보내기 활성화 {#config-message-export}

캠페인 및 여정에 메시지 내보내기를 적용하려면 채널 구성 수준에서 전용 옵션을 활성화해야 합니다. 아래 단계를 수행합니다.

1. [!DNL Journey Optimizer]에서 원하는 전자 메일 또는 SMS [채널 구성](channel-surfaces.md#create-channel-surface)을 편집하거나 만듭니다.

1. **[!UICONTROL 메시지 내보내기 사용]** 옵션을 선택하십시오.

   ![](assets/config-message-export.png)

1. 변경 사항을 저장하고 채널 구성을 제출합니다.

이 채널 구성을 사용하여 캠페인이나 여정을 통해 보낸 전자 메일 및 SMS 메시지는 **AJO 메시지 내보내기 데이터 세트**&#x200B;에 기록됩니다. 그런 다음 정의한 내보내기 데이터 흐름에 따라 선택한 스토리지 대상으로 레코드를 내보냅니다.

**[!UICONTROL 메시지 내보내기 사용]** 토글을 사용하지 않도록 설정하면 이 채널 구성에 대한 새 레코드가 데이터 집합에 수집되지 않습니다. 기존 레코드는 보존이 만료될 때까지 유지됩니다.
