---
title: 콘텐츠 카드 구성
description: 콘텐츠 카드 채널 사전 요구 사항
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="제한된 가용성" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: 8a902298bbbac5689b4f84266dd9c9027e45fad5
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 7%

---

# 콘텐츠 카드 사전 요구 사항 {#content-card-configuration-prereq}

>[!BEGINSHADEBOX]

**목차**

* [콘텐츠 카드 시작](get-started-content-card.md)
* **콘텐츠 카드 필수 구성 요소**
* [Journey Optimizer에서 컨텐츠 카드 채널 구성](content-card-configuration.md)
* [콘텐츠 카드 만들기](create-content-card.md)
* [콘텐츠 카드 디자인](design-content-card.md)
* [컨텐츠 카드 보고서](content-card-report.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>콘텐츠 카드는 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.

Adobe Journey Optimizer에서 컨텐츠 카드를 올바르게 표시하려면 다음 Adobe Experience Platform 설정을 구성해야 합니다.

* **Adobe Experience Platform 데이터 수집**

  [데이터 스트림을 만들고](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) [Experience Platform 서비스를 추가](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure#aep)합니다. **[!UICONTROL Edge 세그멘테이션]** 및 **[!UICONTROL Adobe Journey Optimizer]** 옵션을 사용하도록 설정하십시오. 이렇게 하면 Journey Optimizer 이벤트가 Adobe Experience Platform Edge Network에서 처리됩니다. 데이터 스트림을 구성하는 방법에 대한 자세한 내용은 [데이터 스트림 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)를 참조하십시오.

* **Adobe Experience Platform**

  기본 병합 정책에 **[!UICONTROL 고객]** > **[!UICONTROL 프로필]** > **[!UICONTROL 병합 정책]** Experience Platform 메뉴에서 **Active-On-Edge 병합 정책**&#x200B;이 활성화되어 있는지 확인하십시오. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  >[!NOTE]
  >
  >사용자 지정 **[!UICONTROL 데이터 집합 환경 설정]** 병합 정책을 사용하는 경우 지정된 병합 정책 내에 **[!UICONTROL 여정 인바운드]** 데이터 집합을 추가해야 합니다.

* **Adobe Experience Platform Mobile 또는 Platform Web SDK**

  모바일 및 웹 애플리케이션의 경우 웹 페이지 또는 모바일 앱에 수정 사항을 추가하려면 웹 사이트에서 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/ko/docs/platform-learn/implement-web-sdk/overview) 또는 모바일 앱에서 [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/)를 구현해야 합니다.

* **Journey Optimizer**

  [콘텐츠 카드 구성](#content-card-configuration)을 만듭니다.

* **문제 해결**

  모바일 경험의 문제를 해결하려면 **Edge Delivery 보증** 내의 **Adobe Experience Platform** 보기를 사용하십시오. 요청을 검사하고, Edge 호출을 확인하고, 프로필 데이터를 검사할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/assurance/view/edge-delivery)

* **콘텐츠 실험**

  앱의 [데이터 스트림](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview#_blank)에 사용된 데이터 집합도 콘텐츠 실험 보고 구성에 포함되어 있는지 확인하십시오. 데이터 세트가 일치하지 않으면 앱 데이터가 보고서에 표시되지 않습니다.

  [이 섹션](../content-management/reporting-configuration.md)에서 콘텐츠 실험 보고를 위한 데이터 세트를 추가하는 방법을 알아보세요.
