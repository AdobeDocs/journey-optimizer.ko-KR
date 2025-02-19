---
solution: Journey Optimizer
product: journey optimizer
title: 사용자 지정 작업 문제 해결
description: 사용자 지정 작업 문제를 해결하는 방법 알아보기
badge: label="제한 공개"
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 작업, 서드파티, 사용자 지정, 여정, API
source-git-commit: d6501c8cc7e3293bd6a057d8e74654bced7dae75
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 2%

---


# 사용자 지정 작업 문제 해결 {#troubleshoot-a-custom-action}

>[!AVAILABILITY]
>
>이 기능은 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.
>

Journey Optimizer 사용자 인터페이스의 관리 섹션에서 API 호출을 전송하여 사용자 지정 작업을 테스트할 수 있습니다. 이 기능은 여정에서 사용자 지정 작업을 사용하기 전이나 후에 문제를 해결하는 데 도움이 됩니다.

관리자는 **[!UICONTROL 테스트 요청 보내기]** 기능을 사용하여 Adobe Journey Optimizer에서 직접 실제 API를 호출하여 사용자 지정 작업 구성의 유효성을 검사합니다. 이 기능을 사용하면 여정에서 사용하기 전에 요청 구조, 헤더, 인증 및 페이로드의 형식이 올바르게 지정됩니다.

![](assets/send-test-request.png){width="70%" align="left"}

이 기능을 사용하면 테스트 및 유효성 검사 프로세스를 간소화하여 사용자 지정 작업이 라이브 여정에서 올바르게 작동하도록 할 수 있습니다.

## 전제 조건 {#troubleshoot-custom-action-prereq}

**[!UICONTROL 테스트 요청 보내기]** 기능을 사용하려면 **사용자 지정 작업**&#x200B;을(를) URL, 헤더 및 인증 설정으로 미리 구성해야 합니다.

관리자가 이 기능을 사용하려면 다음 권한이 필요합니다.

* 사용자에게 **[!DNL Manage journeys events, data sources and actions]** 권한이 있어야 합니다.
* 이 권한은 *여정 관리자* 역할에 포함되어 있습니다.
* **[!DNL View journeys events]** 권한만으로는 충분하지 않습니다.

[이 섹션](../administration/high-low-permissions.md#journey-capability)에서 여정 권한에 대해 자세히 알아보세요.

## 테스트 요청 보내기 기능을 사용하는 방법 {#troubleshoot-custom-action-use}

사용자 지정 작업을 테스트하려면 다음 단계를 수행합니다.

1. **작업** 구성 화면으로 이동하여 사용자 지정 작업을 선택합니다.
1. 작업 구성 화면 하단의 **[!UICONTROL 테스트 요청 보내기]** 단추를 클릭합니다.
   ![작업 구성 패널의 테스트 요청 보내기 단추](assets/test-request.png){width="70%" align="left"}
1. 팝업 창에서 요청 매개 변수를 지정할 수 있습니다.

   * **사용자 지정 작업 메서드가 GET**&#x200B;인 경우 페이로드가 필요하지 않습니다.
   * **사용자 지정 작업 메서드가 POST**&#x200B;인 경우 JSON 페이로드를 제공해야 합니다.

     >[!NOTE]
     >
     >Adobe Journey Optimizer은 이 JSON의 구조가 잘못된 경우 오류를 발생시키지만 데이터 유형과 불일치하는 경우 오류를 발생시키지 않습니다. 예를 들어 문자열이어야 하는 항목에 정수 매개 변수를 사용하는 경우 오류가 발생하지 않습니다.

   * 인증이 정의된 경우 인증 세부 정보를 입력하라는 메시지가 표시됩니다.

1. 요청을 실행하려면 **보내기**&#x200B;를 클릭하세요.
1. 헤더 및 상태 코드를 포함한 API의 응답이 인터페이스에 표시됩니다.

## 인증 처리 {#troubleshoot-custom-action-auth}

사용자 지정 작업에 인증이 포함되어 있는 경우 Adobe Journey Optimizer에서는 사용자가 각 테스트 요청에 대한 인증 세부 정보를 입력해야 합니다.

* **기본 인증:** 사용자가 *암호*&#x200B;를 제공해야 합니다.
* **API 키 인증:** 사용자가 API 키 *값*&#x200B;을(를) 입력해야 합니다.
* **사용자 지정 인증:** 사용자는 요청 *bodyParam*&#x200B;에 인증 매개 변수를 제공해야 합니다. 이 경우 완료할 두 개의 섹션이 추가됩니다. **인증 요청** 및 **인증 응답**.

## 주요 이점 {#troubleshoot-custom-action-benefits}

Journey Optimizer 관리자는 외부 도구(예: Postman)를 사용하여 사용자 지정 작업을 테스트할 수도 있습니다. 외부 테스트와 비교하여 제품 내 문제 해결 기능이 제공하는 주요 이점은 다음과 같습니다.

* 테스트 요청은 **AJO 여정**&#x200B;에 의해 실행됩니다. 즉, 다음을 의미합니다.

   * 정확한 요청 구조(Adobe Journey Optimizer 관련 헤더 포함)가 사용됩니다.
   * 소스 IP 및 헤더가 라이브 여정에 사용된 헤더와 일치합니다.

* 사용자 지정 작업이 이미 배포되었으므로 **[!UICONTROL 테스트 요청 보내기]** 기능을 **실시간 여정** 문제 해결에 사용할 수 있습니다.

* 이 제품 내 테스트 기능을 사용하면 도구 간에 구성 세부 정보를 수동으로 복사할 필요가 없으므로 오류 위험이 줄어듭니다.

## 문제 해결 {#troubleshoot-custom-action-check}

요청이 실패하는 경우 다음을 확인할 수 있습니다.

* 테스트에 입력한 인증 자격 증명입니다.
* 요청 메서드(GET 및 POST) 및 해당 페이로드.
* 사용자 지정 작업에 정의된 API 끝점 및 헤더입니다.
* 응답 데이터를 사용하여 잠재적인 구성 오류를 식별합니다.

