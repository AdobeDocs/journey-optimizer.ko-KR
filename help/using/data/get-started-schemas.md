---
solution: Journey Optimizer
product: journey optimizer
title: 스키마 시작
description: Adobe Journey Optimizer에서 Adobe Experience Platform 스키마를 사용하는 방법 알아보기
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 스키마, 플랫폼, 데이터, 구조
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
source-git-commit: 70f647cf4e95c1152a5c16395b88b11a6b72865c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 스키마 시작 {#schemas-gs}

[!DNL Adobe Journey Optimizer]은(는) **Adobe Experience Platform 스키마**&#x200B;를 사용하여 데이터의 구조를 일관되고 재사용 가능한 방식으로 설명합니다. 스키마는 실제 객체(예: 사람)에 대한 추상적인 정의를 제공하고, 해당 객체의 각 인스턴스에 포함되어야 하는 데이터(예: 이름, 생일 등)에 대한 개요를 제공합니다. 데이터가 Experience Platform에 수집되면 항상 **XDM 스키마**&#x200B;에 따라 구조화됩니다.

## 표준 및 관계형 스키마

Adobe Experience Platform에는 두 가지 유형의 스키마가 있습니다.

* **표준 스키마**&#x200B;는 클래스 및 필드 그룹을 사용하여 레코드 또는 시계열 데이터를 캡처하는 계층 구조 스키마입니다.

  표준 스키마는 다음으로 구성됩니다.

   * 데이터 동작(레코드 또는 시계열)을 정의하는 **class**.
   * 하나 이상의 **필드 그룹**(스키마에 특정 필드 추가).

  Journey Optimizer에서 표준 스키마는 일반적으로 **개별 사용자 및 해당 특성**&#x200B;을 나타내고, 클릭, 구매 또는 로그인과 같은 **시계열 상호 작용**&#x200B;을 캡처하고, 세분화 및 개인화를 위해 **실시간 고객 프로필**&#x200B;을 제공하는 데 사용됩니다.

  ➡️ [이 비디오에서 표준 스키마를 만들고 구성하는 방법을 알아보세요](#video-schema)(비디오)

* **관계형 스키마**&#x200B;는 클래스나 필드 그룹을 사용하지 않는 비계층 스키마입니다. 관계형 엔터티의 레코드 데이터를 캡처하는 데 사용되며 주로 [!DNL Journey Optimizer] **오케스트레이션된 캠페인**&#x200B;에서 사용됩니다.

  관계형 엔티티의 예는 다음과 같습니다.
   * 예약, 계약 또는 구독
   * 제품 또는 카탈로그
   * 스토어, 위치 또는 파트너

  관계형 스키마를 사용하면 엔티티당(예: 예약당, 구독당) 하나의 메시지를 보내고, 엔티티 속성(예: 제품 카테고리, 스토어 위치)을 기반으로 세그먼트를 만들고, 엔티티에 연결된 모든 연락처에 도달하여 주소 기능을 향상시킬 수 있습니다.

  관계형 스키마 작동 방식:

   1. **수동으로 스키마를 만들거나 DDL을 통해 가져오기**
   1. **스키마를 연결**&#x200B;하여 엔터티와 사람 간의 관계(예: 구성원에 연결된 충성도 거래, 브랜드에 연결된 보상)를 정의합니다.
   1. **지원되는 소스에서 데이터 집합에 데이터 수집**.

  ➡️ [관계형 스키마 및 데이터 세트를 관리하는 방법을 알아봅니다](../orchestrated/gs-schemas.md)
➡️ [오케스트레이션된 캠페인 시작](../orchestrated/gs-schemas.md)

## 사용 방법 비디오{#video-schema}

표준 스키마를 만들고, 필드 그룹을 추가하고, 사용자 지정 필드 그룹을 만들고 구성하는 방법에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334461?quality=12)

>[!MORELIKETHIS]
>
>* [Journey Optimizer에서 스키마와 데이터 세트를 만들고 데이터를 수집하여 테스트 프로필 추가](../audience/creating-test-profiles.md)
>* [XDM 시스템 개요](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"}
>* [데이터 모델링 모범 사례](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=ko){target="_blank"}
>* [Schema Registry API를 사용하여 스키마 만들기](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=ko){target="_blank"}
>* [스키마 편집기로 두 스키마의 관계 정의](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=ko){target="_blank"}
