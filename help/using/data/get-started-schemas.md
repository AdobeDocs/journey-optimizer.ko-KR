---
solution: Journey Optimizer
product: journey optimizer
title: 스키마 시작
description: Adobe Journey Optimizer에서 Adobe Experience Platform 스키마를 사용하는 방법 알아보기
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: 스키마, 플랫폼, 데이터, 구조
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
TQID: https://experienceleague.adobe.com/fWsW9Rvyd8L4nphczzc7GF1rbO7HuYsjqDBBpy3uoGU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: a1cdc218-59b7-4eef-b5cf-2a7ad74b3371
  - id: d6e5c7fd-c1d6-4137-98cd-138ccde6752f
  - id: cf3fbcd7-c075-4ae4-8de5-96e736ab2ea3
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 79b0c44fffb4297a9a5675200f086c5de544ec88
workflow-type: tm+mt
source-wordcount: 609
ht-degree: 78%

---

# 스키마 시작 {#schemas-gs}

>[!BEGINSHADEBOX]

**이 페이지의 내용:** Adobe Experience Platform 표준 및 관계형 스키마가 데이터 구조를 정의하는 방식을 이해하여 Adobe Journey Optimizer에서 개인화 및 오케스트레이션된 캠페인을 위한 프로필, 행동 이벤트 및 관계형 엔티티를 모델링합니다.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer]에서는 데이터의 구조를 일관되고 재사용 가능한 방식으로 서술하기 위해 **Adobe Experience Platform 스키마**&#x200B;를 사용합니다. 스키마는 실제 오브젝트(예: 사람)에 대한 추상적인 정의를 제공하고, 해당 오브젝트의 각 인스턴스에 포함되어야 하는 데이터(예: 이름, 성, 생일 등)에 대한 개요를 제공합니다. 데이터가 Experience Platform에 수집되면 항상 **XDM 스키마**&#x200B;에 따라 구조화됩니다.

## 표준 및 관계형 스키마

Adobe Experience Platform에는 두 가지 유형의 스키마가 있습니다.

* **표준 스키마**&#x200B;는 클래스 및 필드 그룹을 사용하여 레코드 또는 시계열 데이터를 캡처하는 계층 스키마입니다.

  표준 스키마는 다음 요소로 구성됩니다.

   * 데이터 동작(레코드 또는 시계열)을 정의하는 **클래스**.
   * 스키마에 특정 필드를 추가하는 하나 이상의 **필드 그룹**.

  Journey Optimizer에서 표준 스키마는 일반적으로 **개별 사용자와 그 속성**&#x200B;을 나타내고, 클릭이나 구매 또는 로그인과 같은 **시계열 상호 작용**&#x200B;을 캡처하고, 세분화 및 개인화를 위해 **실시간 고객 프로필**&#x200B;을 제공하는 데 사용됩니다.

  ➡️ [이 비디오에서 표준 스키마를 만들고 구성하는 방법 알아보기](#video-schema)(비디오)

* **관계형 스키마**&#x200B;는 클래스나 필드 그룹을 사용하지 않는 단층적인 비계층 스키마입니다. 관계형 엔티티의 레코드 데이터를 캡처하는 데 사용되며 주로 [!DNL Journey Optimizer] **오케스트레이션된 캠페인**&#x200B;에서 사용됩니다.

  관계형 엔티티의 예는 다음과 같습니다.
   * 예약, 계약 또는 구독
   * 제품 또는 카탈로그
   * 매장, 위치 또는 파트너

  관계형 스키마를 사용하면 엔티티당(예: 예약당, 구독당) 하나씩 메시지를 보내고, 엔티티 속성(예: 제품 카테고리, 매장 위치)을 기반으로 세그먼트를 만들고, 엔티티에 연결된 모든 연락처에 도달하여 도달성을 향상시킬 수 있습니다.

  관계형 스키마의 작동 방식:

   1. **수동으로 스키마를 만들거나 DDL을 통해 가져옴**
   1. **스키마를 연결**&#x200B;하여 엔티티와 사람 간의 관계를 정의합니다(예: 충성도 트랜잭션과 구성원 연결, 보상과 브랜드 연결).
   1. 지원되는 소스에서 데이터 세트로 **데이터를 수집**&#x200B;합니다.

  ➡️ [관계형 스키마와 데이터 세트를 관리하는 방법 알아보기](../orchestrated/gs-schemas.md)
➡️ [오케스트레이션된 캠페인 시작](../orchestrated/gs-schemas.md)

>[!IMPORTANT]
>
>실시간 고객 프로필에 대한 스키마 활성화는 영구적인 결정입니다. 활성화하면 스키마를 비활성화하거나 삭제할 수 없습니다. 해당 스키마를 기반으로 구축된 데이터 세트는 별도로 비활성화하거나 삭제할 수 있지만 이렇게 하면 관련 프로필 레코드가 제거되고 세그멘테이션 및 활성화 워크플로에 영향을 줄 수 있습니다. 활성화하기 전에 ID 구성 및 필드 그룹 선택을 완료합니다. 자세한 지침은 Adobe Experience Platform 설명서에서 [프로필 활성화 계획](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/schema/profile-enablement-planning){target="_blank"} 및 [프로필 사용 스키마 관리](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/schema/best-practices#managing-profile-enabled-schemas){target="_blank"}를 참조하십시오.

## 사용 방법 비디오{#video-schema}

표준 스키마를 만들고, 필드 그룹을 추가하고, 사용자 정의 필드 그룹을 만들고 구성하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3416872?captions=kor&quality=12)

>[!MORELIKETHIS]
>
>* [Journey Optimizer에서 데이터 관리 시작](gs-data.md)
>* [Journey Optimizer에서 스키마와 데이터 세트를 만들고 데이터를 수집하여 테스트 프로필 추가](../audience/creating-test-profiles.md)
>* [XDM 시스템 개요](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"}
>* [데이터 모델링 모범 사례](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=ko){target="_blank"}
>* [프로필 활성화 계획](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/schema/profile-enablement-planning){target="_blank"}
>* [프로필 사용 스키마 관리](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/schema/best-practices#managing-profile-enabled-schemas){target="_blank"}
>* [Schema Registry API를 사용하여 스키마 만들기](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=ko){target="_blank"}
>* [스키마 편집기로 두 스키마의 관계 정의](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=ko){target="_blank"}
