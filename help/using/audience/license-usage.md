---
solution: Journey Optimizer
product: journey optimizer
title: 라이선스 사용 대시보드
description: Journey Optimizer 라이선스 사용 대시보드에 대해 알아보기
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 7e91face-c8f4-4e70-9123-9e36bae7e67e
source-git-commit: db1e4ee5b2b4bb3a3d7d9e86aded14ad3c613765
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 1%

---

# 라이선스 사용 대시보드 {#license-usage}

[!DNL Adobe Journey Optimizer] [사용자 인터페이스](../start/user-interface.md)는 일일 스냅숏 중에 캡처한 대로 조직의 라이선스 사용에 대한 중요한 정보를 표시하는 대시보드를 제공합니다.

이 대시보드에 액세스하려면 **[!UICONTROL 관리]** > **[!UICONTROL 라이선스 사용량]**(으)로 이동하십시오. 대시보드를 표시하는 **[!UICONTROL 개요]** 탭이 열립니다.

![라이선스 사용 대시보드 개요](assets/license-usage-dashboard.png)

>[!NOTE]
>
>* 대시보드를 보려면 [라이선스 사용량 대시보드 보기](https://experienceleague.adobe.com/docs/experience-platform/dashboards/permissions.html?lang=ko#available-permissions){target="_blank"} 권한이 있어야 합니다.
>
>* 할당량 열에 `N/A`로 표시된 대로 특정 지표(예: 계산 시간, 이메일)는 개발 샌드박스에 표시되지 않습니다. 대시보드에는 null이 아닌 값만 표시됩니다. 지표가 0이거나 0에 가까우면 값이 채워지지 않습니다.


[!DNL Adobe Journey Optimizer]의 경우 대시보드에서 **참여 가능한 프로필**&#x200B;의 수를 확인할 수 있습니다.

## 참여 가능한 프로필이란? {#what-is-engageable-profile}

**참여 가능 프로필**&#x200B;은(는) 프로필 서비스에 저장되어 있으며 여정 또는 캠페인에 참여한 개인을 나타내는 정보 레코드입니다.

참여 가능한 프로필의 주요 특징:

* **12개월 순환 기간**: 참여 가능한 프로필은 지난 12개월 동안의 참여를 기준으로 계산됩니다. 이 지표는 Journey Optimizer의 작성, 의사 결정, 게재, 실험 또는 오케스트레이션 기능을 사용하여 관여하려고 한 고유한 프로필 수를 보여줍니다.

* **샌드박스당 고유 개수**: 프로필이 샌드박스 내에 여러 개의 여정 또는 캠페인을 입력하는 경우 해당 샌드박스에 대한 단일 참여 가능 프로필로 한 번만 계산됩니다.

* **대응 가능 대상 기반**: 참여 가능 프로필은 대응 가능 대상에서 계산됩니다. 총 대응 가능 대상 중 Journey Optimizer의 기능을 사용하여 지난 12개월 동안 관여한 대상을 나타내는 수입니다.

* **지표 동작**: 참여 가능한 프로필 수:
   * 여정 또는 캠페인을 통해 새 프로필이 참여하면 증가할 수 있습니다
   * 12개월 이상 특정 프로필에 참여하지 않는 한 줄일 수 없습니다
   * 익명 프로필이 알려진 프로필에 결합되는 경우 감소할 수 있음

>[!NOTE]
>
>참여 가능 프로필 수가 갑자기 급증한 경우 아래의 [문제 해결 섹션](#troubleshooting-engageable-profiles)에서 문제를 이해하고 해결하는 방법에 대한 자세한 지침을 참조하십시오.

## 문제 해결: 참여 가능한 프로필 수가 크게 증가했습니다 {#troubleshooting-engageable-profiles}

참여 가능 프로필 수가 갑자기 급증하는 경우(예: 하루에 수십만 개에서 수백만 개로 증가하는 프로필) 이 섹션에서는 문제를 이해하고 해결하기 위한 지침을 제공합니다.

### 증가 이해

참여 가능 프로필 지표는 지난 12개월 동안 여정 또는 캠페인에 참여한 고유 프로필 수를 반영합니다. 갑작스러운 증가는 다음 원인으로 인해 발생할 수 있습니다.

* 새로운 여정 또는 캠페인의 타겟이 되는 대규모 대상자
* 프로필 서비스에 대해 활성화된 데이터 세트 변경
* 최근에 참여하지 않은 대상의 일괄 처리

### 해결 단계

이 문제를 해결하려면 다음 단계를 수행합니다.

1. **프로필 계산 논리 이해:**

   * 참여 가능 프로필은 지난 12개월 동안 여정 또는 캠페인에 의해 참여된 고유 프로필을 기반으로 계산됩니다.
   * 프로필이 여러 여정을 입력하면 해당 샌드박스에 대한 하나의 참여 가능 프로필로 계산됩니다.
   * 12개월 이상 특정 프로필에 대한 참여가 없거나 익명 프로필이 알려진 프로필에 결합된 경우가 아니면 지표를 줄일 수 없습니다.
   * 참여 가능 프로필은 고객의 대응 가능 대상 을 사용하여 계산됩니다.
   * 지난 12개월 동안 Journey Optimizer의 기능을 사용하여 참여한 대상은 총 대응 가능 대상 중에서 참여 가능한 프로필의 수를 결정합니다.

2. **대규모 대상을 타겟팅하는 여정, 캠페인 및 의사 결정 조사:**

   * [참여 가능한 프로필 쿼리](../reports/query-examples.md#engageable-profiles-queries) 또는 [쿼리 서비스](https://experienceleague.adobe.com/ko/docs/experience-platform/query/home){target="_blank"}를 사용하여 많은 프로필을 타겟팅하는 최근 여정 및 캠페인을 검토하십시오.
   * 프로필 수가 급증하는 데 기여한 특정 여정 버전을 식별합니다.
   * 새 프로필과 관련된 여정, 캠페인 및 의사 결정은 여정 데이터 세트의 이벤트 수를 증가시켜 참여 가능한 프로필 수 증가에 기여할 수 있습니다.

3. **여정 및 캠페인 수준에서 대상자 필터링:**

   * 여정 또는 캠페인을 시작하기 전에 대상 수준에서 필터를 적용하여 참여 가능한 프로필이 불필요하게 증가하지 않도록 합니다.
   * 참여 중에 적절한 대상만 타깃팅되는지 확인하십시오.

4. **주소 지정 가능한 대상 크기 줄이기:**

   * 필요한 경우 익명 프로필을 삭제합니다. 이 작업은 Journey Optimizer 및 Real-Time Customer Data Platform 모두에 영향을 줍니다.
   * 실시간 고객 프로필 안내서에서 [익명 프로필 데이터 만료](https://experienceleague.adobe.com/ko/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}에 대해 자세히 알아보십시오.
   * **참고:** Platform UI 또는 API를 통해 익명 프로필 데이터 만료를 구성할 수 없습니다. 이 기능을 활성화하려면 지원팀에 문의해야 합니다.

5. **데이터 세트 변경 모니터링:**

   * 프로파일링을 위해 활성화된 데이터 세트를 확인하고 과도한 ECID(Experience Cloud ID)가 포함되어 있지 않은지 확인하십시오.
   * 필요한 경우 ECID 수가 많은 데이터 세트를 삭제하고 감소된 레코드로 다시 만듭니다.

6. **장기 감소 전략 개발:**

   * 특정 프로필이 12개월 이상 동안 미참여 상태로 유지되면 참여 가능 프로필 수가 자연스럽게 줄어듭니다.

**참고 항목:**

* [참여 가능한 프로필 쿼리 예제](../reports/query-examples.md#engageable-profiles-queries) - 참여 가능한 프로필을 모니터링하고 분석하는 샘플 쿼리
* [Adobe Experience Platform 쿼리 서비스 개요](https://experienceleague.adobe.com/ko/docs/experience-platform/query/home){target="_blank"}

## 관련 설명서 {#related-documentation}

Adobe Experience Platform 설명서에서 자세히 알아보십시오.

* [라이선스 사용 대시보드 개요](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html?lang=ko){target="_blank"}
* [라이선스 사용 대시보드 살펴보기](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html?lang=ko#exploring-the-license-usage-dashboard){target="_blank"}
* [사용 가능한 지표](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html?lang=ko#available-metrics){target="_blank"}
* [익명 프로필 데이터 만료](https://experienceleague.adobe.com/docs/experience-platform/profile/pseudonymous-profiles.html?lang=ko){target="_blank"}
