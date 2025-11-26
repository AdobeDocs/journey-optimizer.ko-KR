---
title: 콘텐츠 카드 구성
description: 콘텐츠 카드 채널 사전 요구 사항
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: df92e319-1e42-486f-b688-595964a762c9
source-git-commit: 3d5ed7c5efd76616c8dbc89078f7368eedc5f1af
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 3%

---

# 콘텐츠 카드 사전 요구 사항 {#content-card-configuration-prereq}

Adobe Journey Optimizer에서 컨텐츠 카드를 올바르게 표시하려면 다음 Adobe Experience Platform 설정을 구성해야 합니다.

* **Adobe Experience Platform 데이터 수집**

  [데이터 스트림을 만들고](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure){target="_blank"} [Experience Platform 서비스를 추가](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure#aep){target="_blank"}. **[!UICONTROL Edge 세그멘테이션]** 및 **[!UICONTROL Adobe Journey Optimizer]** 옵션을 사용하도록 설정하십시오. 이렇게 하면 Journey Optimizer 이벤트가 Adobe Experience Platform Edge Network에서 처리됩니다.
보고서에 이 데이터를 포함하려면 데이터 집합에 **경험 이벤트 - 제안 상호 작용** 필드 그룹을 추가하십시오. [데이터스트림에 대해 자세히 알아보기](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure){target="_blank"}

* **Adobe Experience Platform**

  기본 병합 정책에 **고객** > **[!UICONTROL 프로필]** > **[!UICONTROL 병합 정책]** Experience Platform 메뉴에서 **[!UICONTROL Active-On-Edge 병합 정책]**&#x200B;이 활성화되어 있는지 확인하십시오. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  >[!NOTE]
  >
  >사용자 지정 **[!UICONTROL 데이터 집합 환경 설정]** 병합 정책을 사용하는 경우 지정된 병합 정책 내에 **[!UICONTROL 여정 인바운드]** 데이터 집합을 추가해야 합니다.

* **Adobe Experience Platform Mobile 또는 Platform Web SDK**

  모바일 및 웹 응용 프로그램의 경우 웹 페이지 또는 모바일 앱에 수정 사항을 추가하려면 웹 사이트에서 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/ko/docs/platform-learn/implement-web-sdk/overview){target="_blank"} 또는 모바일 앱에서 [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/){target="_blank"}을 구현해야 합니다.

* **Journey Optimizer**

  [콘텐츠 카드 구성](#content-card-configuration)을 만듭니다.

* **문제 해결**

  모바일 경험 문제를 해결하려면 **Edge Delivery** 내의 **Adobe Experience Platform Assurance** 보기를 사용하십시오. 요청을 검사하고, Edge 호출을 확인하고, 프로필 데이터를 검사할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

* **콘텐츠 실험**

  앱의 [데이터 스트림](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview#_blank){target="_blank"}에 사용된 데이터 집합도 콘텐츠 실험 보고 구성에 포함되어 있는지 확인하십시오. 데이터 세트가 일치하지 않으면 앱 데이터가 보고서에 표시되지 않습니다.

  [이 섹션](../reports/reporting-configuration.md)에서 콘텐츠 실험 보고를 위한 데이터 세트를 추가하는 방법을 알아보세요.

## 프로필 관리 보호 {#profile-management-guardrail}

[!DNL Journey Optimizer] 콘텐츠 카드는 익명 프로필을 타겟팅할 수 있습니다. 즉, 다른 채널에서 이전에 참여하지 않았으므로 인증되지 않았거나 아직 알 수 없는 프로필을 의미합니다. 이 경우는 예를 들어 ECID와 같은 임시 ID를 기반으로 모든 방문자 또는 대상을 타겟팅할 때 해당됩니다.

이렇게 하면 총 참여 가능 프로필 수가 증가하므로 구입한 계약 참여 가능 프로필 수를 초과하는 경우 비용이 발생할 수 있습니다. 각 패키지에 대한 라이선스 지표는 [Journey Optimizer 제품 설명](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"} 페이지에 나와 있습니다. [라이선스 사용 대시보드](../audience/license-usage.md)에서 참여 가능한 프로필 수를 확인할 수 있습니다.

참여 가능한 프로필을 합리적인 제한 이내로 유지하려면 Adobe에서는 TTL(Time-To-Live)을 설정하여 특정 기간 내에 방문하거나 참여한 적이 없는 경우 실시간 고객 프로필에서 익명 프로필을 자동으로 삭제할 것을 권장합니다.

>[!NOTE]
>
>[Experience Platform 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}에서 익명 프로필에 대한 데이터 만료를 구성하는 방법에 대해 알아봅니다.

Adobe에서는 현재 Edge 프로필 TTL과 일치하도록 TTL 값을 14일로 설정하는 것이 좋습니다.