---
solution: Journey Optimizer
product: journey optimizer
title: 여정에서 경험 이벤트 조회
description: 여정에서 경험 이벤트 조회를 사용하는 방법 알아보기
exl-id: 35e2e347-0669-44a3-92ba-aee52e54c219
source-git-commit: a587b8754e94781b7735f3d7d5abb9b9767a74a5
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 5%

---

# 여정에서 경험 이벤트 조회 {#ee-journeys}

>[!CAUTION]
>
>2025년 7월 8일부터 새로운 고객 조직에서는 경험 이벤트를 사용하여 표현식을 만드는 것이 여정 조건에 사용되는 표현식 편집기에서 더 이상 지원되지 않습니다. 따라서 표현식을 만드는 데 [Experience Platform 데이터 소스](../datasource/adobe-experience-platform-data-source.md)의 경험 이벤트를 사용할 수 없습니다. 경험 이벤트를 사용하여 표현식/논리를 생성하기 위한 대체 접근 방식 및 모범 사례가 아래에 참조됩니다.
>
>세부 정보가 필요하십니까? [FAQ 읽기](#faq-ee).

이 페이지에서는 Adobe Journey Optimizer의 경험 이벤트를 최대한 활용할 수 있는 일반적인 패턴 및 확장 가능한 접근 방식에 대해 설명합니다. 이러한 사용 사례는 옵트아웃 관리, 메시지 빈도 제어, 사용자 행동을 기반으로 콘텐츠 개인화, 실시간 신호 반응과 같은 자주 발생하는 문제를 해결하는 데 도움이 되도록 설계되었습니다.

이러한 전략을 활용함으로써 행동 데이터를 트리거하는 이벤트 또는 전달하는 속성에 따라 프로필을 억제, 자격 부여 또는 제외하는 의미 있는 작업으로 만들 수 있습니다. 구매 임계값, 포기 트리거 또는 바운스 처리에 대한 논리를 작성하는 경우 이러한 예제는 요구 사항에 맞게 조정할 수 있는 실용적인 지침을 제공합니다.

가장 적합한 접근 방식을 평가할 때 사용 사례의 지연 요구 사항을 고려하여 여정이 반응적이고 효과적으로 유지될 수 있도록 하십시오.

## 옵트아웃 비표시

마케팅 커뮤니케이션을 옵트아웃한 프로필을 표시하지 않으려면 기본 제공 동의 관리를 사용합니다. 옵트아웃 환경 설정은 프로필의 동의 필드에 자동으로 캡처됩니다. 여정 조건에서 직접 참조할 수 있으며 메시지 게재 중에 Journey Optimizer에 의해 자동으로 적용됩니다.

자세히 알아보기:

* [동의 관리](../privacy/opt-out.md)
* [이메일 옵트아웃 관리](../email/email-opt-out.md)
* [텍스트 메시지에 대한 옵트아웃 관리](../sms/sms-opt-out.md)


## 바운스 기반 제외

이메일 반송이 발생한 프로필을 제외하려면 반송된 주소에 대한 Adobe Journey Optimizer의 자동 제외 목록을 활용하십시오. 이 기본 제공 메커니즘은 사용자 지정 논리 없이 잘못되었거나 연결할 수 없는 이메일이 향후 전송에서 제외되도록 합니다.

자세히 알아보기:

* [금지 목록 관리](../configuration/manage-suppression-list.md)


## 일반 제외

특정 동작을 보여 준 프로필을 표시하지 않으려면 이벤트 기반 논리가 있는 배치 대상을 사용하여 제외 기준을 충족하는 프로필을 캡처합니다. 여정 조건에서 이 대상자를 참조합니다.

자세히 알아보기:

* Adobe Experience Platform [세그먼트 빌더 - 이벤트](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [세그먼트 빌더 - 시간 제한](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [조건에서 대상 사용](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [inAudience() 함수](../building-journeys/functions/functioninaudience.md)


## 커뮤니케이션 수신 제외

최근 기간 내에 어떤 연락이든 받은 프로필에 메시지를 보내지 못하게 하려면

* 시간 기반 기준으로 배치 대상자를 사용하고 여정 조건에서 참조합니다.
* 빈도 제한 비즈니스 규칙을 적용하여 일별 또는 주별 메시지 제한을 적용합니다.


대상 을 사용하여 자세히 알아보기:

* Adobe Experience Platform [세그먼트 빌더 - 이벤트](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [세그먼트 빌더 - 시간 제한](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [조건에서 대상 사용](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [inAudience() 함수](../building-journeys/functions/functioninaudience.md)


다음도 참조하십시오.

* [채널 및 커뮤니케이션 유형별 빈도 캡핑](../conflict-prioritization/channel-capping.md)



## 메시지별 포함/제외

특정 메시지를 수신했는지 여부에 따라 프로필을 포함하거나 제외하려면 이 논리를 캡슐화하고 여정 조건에서 참조하는 일괄 대상을 만듭니다.


자세히 알아보기:

* Adobe Experience Platform [세그먼트 빌더 - 이벤트](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [세그먼트 빌더 - 시간 제한](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [조건에서 대상 사용](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [inAudience() 함수](../building-journeys/functions/functioninaudience.md)

## 장바구니 또는 찾아보기 포기 개인화

최신 장바구니를 기반으로 커뮤니케이션을 개인화하거나 여러 장바구니 유형 또는 제품 보기에서 이벤트를 찾아보려면 다음과 같이 하십시오.

* [Adobe Experience Platform Data Distiller](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/overview){target="_blank"}에 대한 액세스 권한이 있는 경우 자동화된 쿼리를 구성하여 이벤트에서 필요한 데이터를 추출하고 사용 사례에 맞게 조작한 다음 활성화를 위해 프로필 사용 데이터 집합에 다시 씁니다.
* 중단 데이터를 스칼라 속성으로 프로필에 모델링할 수 있는 경우 계산된 속성을 사용하여 최신 정보를 캡처한 다음 여정에서 이러한 속성을 참조하여 커뮤니케이션을 구성하는 것이 좋습니다. [Adobe Experience Platform 설명서에서 자세히 알아보기](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}


## 동작 기반 여정 종료

프로필이 특정 동작을 나타낼 때 여정에서 프로필을 제거하려면 종료 기준을 활용하여 특정 이벤트가 수신되거나 프로필이 특정 대상에 적합할 때 여정에서 프로필을 종료합니다.

자세히 알아보기:

* [여정 속성 설정 - 종료 기준](journey-properties.md#exit-criteria)

## 가치 임계값이 있는 구매 기반 검증

구매를 기반으로 여정을 트리거하고 값이 임계값 초과/미만인 경우 억제하려면 계산된 속성을 정의하여 특정 기간 동안의 구매를 합계합니다. 지출액이 특정 기준을 충족하는 프로필을 포함하는 대상자를 만듭니다.

자세히 알아보기:

* Adobe Experience Platform [계산된 특성 개요](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}



## 자주 묻는 질문 {#faq-ee}

여정 표현식/조건에서는 경험 이벤트 사용이 더 이상 지원되지 않습니다. 영향은 아래 FAQ에 나열되어 있습니다.

+++어떤 특정 기능이 영향을 받습니까?

표현식 편집기의 경험 이벤트 조회만 영향을 받습니다. 다음 기능은 영향을 받지 **않고** 그대로 유지됩니다.

* 프로필 UI에서 특정 프로필과 연결된 경험 이벤트 관찰

* 계산된 속성 규칙에서 경험 이벤트 사용 및 여정의 계산된 속성 액세스

* 단일 또는 비즈니스 이벤트로 여정 트리거

* 표현식 및 개인화 편집기에서 여정을 트리거하는 이벤트의 여정 컨텍스트 데이터 사용

* 여정 내 이벤트 수신

* 여정을 트리거하기 위한 이벤트 구성

* 마케팅 커뮤니케이션에 대한 최종 사용자 반응 이벤트 감지(예: 이메일 열기)

+++

+++기존 Adobe 조직이 이 업데이트의 영향을 받습니까?

Adobe 조직은 경험 이벤트 조회를 아직 사용하지 않은 경우에만 영향을 받습니다. [Experience Platform 데이터 소스](../datasource/adobe-experience-platform-data-source.md)에서 이미 경험 이벤트를 사용하고 있는 경우 Adobe 조직에서는 경험 이벤트 조회를 계속 지원합니다.

+++

+++새로운 Adobe 조직이 있습니다. 경험 이벤트 데이터가 필요한 사용 사례를 해결하려면 어떻게 합니까?

경험 이벤트와 관련된 대체 접근 방식 및 모범 사례는 원하는 사용 사례를 달성하기 위해 위에서 사용할 수 있습니다.

+++

+++ 대체 접근 방식이 내 사용 사례에 작동하지 않는 경우 어떻게 합니까?

위에 나열된 대체 접근 방식 중 하나를 사용하여 사용 사례를 해결할 수 없는 경우 Adobe 담당자에게 문의하십시오.

+++
