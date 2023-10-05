---
solution: Journey Optimizer
product: journey optimizer
title: 사용자 지정 작업 구성
description: 사용자 지정 작업을 구성하는 방법 알아보기
feature: Actions
topic: Administration
role: Admin
level: Experienced
keywords: 작업, 서드파티, 사용자 지정, 여정, API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 2874acfda5947bedd6c390468ded294cf07f9383
workflow-type: tm+mt
source-wordcount: '1278'
ht-degree: 12%

---

# 사용자 지정 작업 구성 {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="사용자 정의 작업"
>abstract="서드파티 시스템을 사용하여 메시지를 보내거나 서드파티 시스템으로 API 호출을 보내려는 경우, 사용자 정의 작업을 사용하여 여정에 대한 연결을 구성합니다. 예를 들어 사용자 정의 작업으로 Epsilon, Slack, [Adobe Developer](https://developer.adobe.com), Firebase 등의 시스템에 연결할 수 있습니다."

서드파티 시스템을 사용하여 메시지를 보내거나 서드파티 시스템으로 API 호출을 보내려는 경우, 사용자 정의 작업을 사용하여 여정에 대한 연결을 구성합니다. 예를 들어 사용자 지정 작업으로 Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase 등

사용자 지정 작업은 기술 사용자가 정의하고 마케터가 사용할 수 있는 추가 작업입니다. 구성하고 나면 여정 왼쪽 팔레트의 **[!UICONTROL 작업]** 범주. [이 페이지](../building-journeys/about-journey-activities.md#action-activities)에서 자세히 알아보십시오.

## 제한 사항{#custom-actions-limitations}

사용자 지정 작업은에 나열된 몇 가지 제한 사항이 있습니다. [이 페이지](../start/guardrails.md).

사용자 지정 작업 매개 변수에서 간단한 컬렉션과 개체 컬렉션을 전달할 수 있습니다. 의 컬렉션 제한에 대해 자세히 알아보기 [이 페이지](../building-journeys/collections.md#limitations).

또한 사용자 지정 작업 매개 변수에는 예상 형식(예: 문자열, 십진수 등)이 있습니다. 이러한 예상 형식을 준수하도록 주의해야 합니다. 자세히 알아보기 [사용 사례](../building-journeys/collections.md).

## 모범 사례{#custom-action-enhancements-best-practices}

모든 사용자 지정 작업에 대해 30초 동안 150,000개의 호출 제한 이 정의됩니다. 이 제한은 사용자 지정 작업으로 타깃팅된 외부 끝점을 보호하기 위해 고객의 사용을 기반으로 설정되었습니다. 적절한 읽기 비율(사용자 지정 작업 사용 시 5000개 프로필/초)을 정의하여 대상 기반 여정에서 이를 고려해야 합니다. 필요한 경우 최대 가용량/최대 가용량 API를 통해 더 큰 최대 가용량 또는 최대 가용량 제한을 정의하여 이 설정을 재정의할 수 있습니다. [이 페이지](../configuration/external-systems.md)를 참조하십시오.

다음과 같은 다양한 이유로 사용자 지정 작업으로 공개 끝점을 타깃팅해서는 안 됩니다.

* 적절한 제한 또는 제한이 없으면 이러한 볼륨을 지원하지 않을 수 있는 공개 끝점에 너무 많은 호출을 보낼 위험이 있습니다.
* 프로필 데이터는 사용자 지정 작업을 통해 전송될 수 있으므로 공개 엔드포인트를 타겟팅하면 의도치 않게 외부적으로 개인 정보를 공유할 수 있습니다.
* 공개 끝점에서 반환되는 데이터에 대해 제어할 수 없습니다. 엔드포인트가 API를 변경하거나 잘못된 정보를 보내기 시작하는 경우 전송된 통신에서 사용할 수 있게 되고 부정적인 영향이 발생할 수 있습니다.

## 동의 및 데이터 거버넌스 {#privacy}

Journey Optimizer에서는 데이터 거버넌스 및 동의 정책을 사용자 지정 작업에 적용하여 특정 필드가 서드파티 시스템으로 내보내지지 않도록 하거나 이메일, 푸시 또는 SMS 통신 수신에 동의하지 않은 고객을 제외할 수 있습니다. 자세한 내용은 다음 페이지를 참조하십시오.

* [데이터 거버넌스](../action/action-privacy.md).
* [동의](../action/action-privacy.md).


## 구성 단계 {#configuration-steps}

사용자 지정 작업을 구성하는 데 필요한 주요 단계는 다음과 같습니다.

1. 관리 메뉴 섹션에서 다음을 선택합니다. **[!UICONTROL 구성]**. 다음에서  **[!UICONTROL 작업]** 섹션, 클릭 **[!UICONTROL 관리]**. 클릭 **[!UICONTROL 작업 만들기]** 새 작업을 만듭니다. 작업 구성 창이 화면 오른쪽에 열립니다.

   ![](assets/custom2.png)

1. 작업 이름을 입력합니다.

   >[!NOTE]
   >
   >공백이나 특수 문자는 사용하지 마십시오. 이름은 30자까지만 입력하십시오.

1. 작업에 설명을 추가합니다. 데이터 소스에 이벤트에 설명을 추가합니다.
1. 이 작업을 사용하는 여정 수는 **[!UICONTROL 다음에서 사용됨]** 필드. 다음을 클릭할 수 있습니다 **[!UICONTROL 여정 보기]** 단추를 클릭하여 이 작업을 사용하는 여정 목록을 표시합니다.
1. 다른 항목 정의 **[!UICONTROL URL 구성]** 매개 변수. [이 페이지](../action/about-custom-action-configuration.md#url-configuration)를 참조하십시오.
1. 구성 **[!UICONTROL 인증]** 섹션. 이 구성은 데이터 소스의 경우와 동일합니다.  [이 섹션](../datasource/external-data-sources.md#custom-authentication-mode)을 참조하십시오.
1. 다음을 정의합니다. **[!UICONTROL 작업 매개 변수]**. [이 페이지](../action/about-custom-action-configuration.md#define-the-message-parameters)를 참조하십시오.
1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   이제 사용자 지정 작업이 구성되었으며 여정에서 사용할 준비가 되었습니다. [이 페이지](../building-journeys/about-journey-activities.md#action-activities)를 참조하십시오.

   >[!NOTE]
   >
   >여정에서 사용자 지정 작업을 사용하는 경우 대부분의 매개 변수는 읽기 전용입니다. 다음 작업만 수정할 수 있습니다. **[!UICONTROL 이름]**, **[!UICONTROL 설명]**, **[!UICONTROL URL]** 필드 및 **[!UICONTROL 인증]** 섹션.

## 끝점 구성 {#url-configuration}

사용자 지정 작업을 구성할 때 다음을 정의해야 합니다 **[!UICONTROL 끝점 구성]** 매개 변수:

![](assets/action-response1bis.png){width="70%" align="left"}

1. 다음에서 **[!UICONTROL URL]** 필드에 외부 서비스의 URL을 지정합니다.

   * URL이 정적인 경우 이 필드에 URL을 입력합니다.

   * URL에 동적 경로가 포함된 경우 URL의 정적 부분, 즉 체계, 호스트, 포트 및 경로의 정적 부분(선택 사항)만 입력합니다.

     예: `https://xxx.yyy.com/somethingstatic/`

     사용자 지정 작업을 여정에 추가할 때 URL의 동적 경로를 지정합니다. [자세히 알아보기](../building-journeys/using-custom-actions.md).

   >[!NOTE]
   >
   >보안상의 이유로 URL에 HTTPS 스키마를 사용하는 것이 좋습니다. 공개되지 않은 Adobe 주소 및 IP 주소의 사용은 허용되지 않습니다.
   >
   >사용자 지정 작업을 정의할 때 기본 포트만 허용됩니다. http의 경우 80, https의 경우 443.

1. 호출 선택 **[!UICONTROL 방법]**: 다음 중 하나일 수 있습니다. **[!UICONTROL POST]**, **[!UICONTROL GET]** 또는 **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > 다음 **DELETE** 메서드가 지원되지 않습니다. 기존 리소스를 업데이트해야 하는 경우 **PUT** 메서드를 사용합니다.

1. 헤더 및 쿼리 매개 변수를 정의합니다.

   * 다음에서 **[!UICONTROL 헤더]** 섹션, 클릭 **[!UICONTROL 헤더 필드 추가]** 외부 서비스로 보낼 요청 메시지의 HTTP 헤더를 정의합니다. 다음 **[!UICONTROL Content-Type]** 및 **[!UICONTROL Charset]** 헤더 필드는 기본적으로 설정됩니다. 이러한 필드는 수정하거나 삭제할 수 없습니다.

   * 다음에서 **[!UICONTROL 쿼리 매개 변수]** 섹션, 클릭 **[!UICONTROL 쿼리 매개 변수 필드 추가]** 를 사용하여 URL에 추가할 매개 변수를 정의할 수 있습니다.

   ![](assets/journeyurlconfiguration2bis.png)

1. 필드의 레이블 또는 이름을 입력합니다.

1. 유형을 선택합니다. **[!UICONTROL 상수]** 또는 **[!UICONTROL 변수]**. 을(를) 선택한 경우 **[!UICONTROL 상수]**&#x200B;을(를) 만든 다음 **[!UICONTROL 값]** 필드. 을(를) 선택한 경우 **[!UICONTROL 변수]**&#x200B;를 설치한 다음 여정에 사용자 지정 작업을 추가할 때 이 변수를 지정합니다. [자세히 알아보기](../building-journeys/using-custom-actions.md).

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >여정에 사용자 지정 작업을 추가한 후에도 여정이 초안 상태인 경우 헤더 또는 쿼리 매개 변수 필드를 추가할 수 있습니다. 여정이 구성 변경의 영향을 받지 않도록 하려면 사용자 지정 작업을 복제하고 필드를 새 사용자 지정 작업에 추가합니다.
   >
   >헤더는 필드 구문 분석 규칙에 따라 유효성이 검사됩니다. 다음에서 자세히 알아보기 [이 설명서](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## 페이로드 매개 변수 정의 {#define-the-message-parameters}

1. 다음에서 **[!UICONTROL 요청]** 섹션에 외부 서비스로 전송할 JSON 페이로드의 예제를 붙여 넣습니다. 이 필드는 선택 사항이며 POST 및 PUT 호출 메서드에만 사용할 수 있습니다.

1. 다음에서 **[!UICONTROL 응답]** 섹션에 호출에서 반환된 페이로드의 예제를 붙여 넣습니다. 이 필드는 선택 사항이며 모든 호출 방법에서 사용할 수 있습니다. 사용자 지정 작업에서 API 호출 응답을 활용하는 방법에 대한 자세한 내용은 다음을 참조하십시오. [이 페이지](../action/action-response.md).

>[!NOTE]
>
>응답 기능은 현재 Beta 버전으로 제공됩니다.

![](assets/action-response2bis.png){width="70%" align="left"}

>[!NOTE]
>
>페이로드 예는 null 값을 포함할 수 없습니다. 페이로드의 필드 이름에는 &quot;.&quot;를 사용할 수 없습니다. 문자. &quot;$&quot; 문자로 시작할 수 없습니다.

매개 변수 유형(예: 문자열, 정수 등)을 정의할 수 있습니다.

매개 변수가 상수인지 변수인지 지정할 것인지 선택할 수도 있습니다.

* **상수** 는 매개 변수 값이 기술 담당자에 의해 작업 구성 창에서 정의됨을 의미합니다. 값은 여정 간에 항상 동일합니다. 여정에서 사용자 지정 작업을 사용할 때 변경되지 않으며 마케터가 표시되지 않습니다. 예를 들어 서드파티 시스템에서 예상하는 ID일 수 있습니다. 이 경우 상수/변수 전환 오른쪽에 있는 필드가 전달된 값입니다.
* **변수** 는 매개 변수의 값이 달라짐을 의미합니다. 여정에서 이 사용자 지정 작업을 사용하는 마케터는 원하는 값을 전달하거나 이 매개 변수에 대한 값을 검색할 위치를 지정할 수 있습니다(예: 이벤트, Adobe Experience Platform 등). 이 경우 전환 상수/변수 오른쪽의 필드는 마케터가 여정에서 이 매개 변수의 이름을 지정하는 레이블입니다.

![](assets/customactionpayloadmessage2.png)