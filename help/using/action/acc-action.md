---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Campaign v7/v8과 통합
description: Journey Optimizer을 Adobe Campaign v7/v8과 통합하는 방법 알아보기
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Intermediate
keywords: campaign, acc, 통합
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
TQID: https://experienceleague.adobe.com/Ho00nWReUS7S4PnmCzle6RbPzwt0DlZN43IQoF2918k
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 62bc5f833b5612570ba50c98519a2f9c07d0bd5e
workflow-type: tm+mt
source-wordcount: 742
ht-degree: 9%

---

# Adobe Campaign v7/v8과 통합 {#integrating-with-adobe-campaign-v7-v8}

>[!BEGINSHADEBOX]

**이 페이지에서:** 여정이 Campaign 트랜잭션 메시지를 통해 이메일, 푸시 알림 및 SMS를 전송할 수 있도록 Journey Optimizer을 Adobe Campaign v7 또는 v8에 연결합니다.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Adobe Campaign v7/v8 작업"
>abstract="이러한 통합은 Adobe Campaign v7 및 v8에서 사용할 수 있습니다. Adobe Campaign 트랜잭션 메시지 기능을 사용하여 이메일, 푸시 알림, SMS를 전송할 수 있습니다. Journey Optimizer 인스턴스와 Campaign 인스턴스 간의 연결은 프로비저닝 시 Adobe에 의해 설정됩니다."

Adobe Campaign Classic v7 또는 Campaign v8이 있는 경우 여정에서 Adobe Journey Optimizer과 Adobe Campaign을 통합하는 특정 사용자 지정 작업을 사용할 수 있습니다. 이 통합을 통해 Adobe Campaign 트랜잭션 메시지 기능을 사용하여 이메일, 푸시 알림 및 SMS를 전송할 수 있습니다. 이 [전체 사용 사례](../building-journeys/ajo-ac.md)에서 자세히 알아보세요.

구성된 각 작업에 대해 여정 디자이너 팔레트에서 [캠페인 작업 활동](../building-journeys/using-adobe-campaign-v7-v8.md)을 사용할 수 있습니다.

## 활성화 {#access}

요청되면, Journey Optimizer과 Adobe Campaign 환경 간의 연결은 프로비저닝 시 Adobe에 의해 설정됩니다. 프로비저닝 시 연결을 요청하지 않은 경우 Adobe Journey Optimizer 지원에 문의하여 활성화를 요청하십시오. 다음 세부 정보를 제공해야 합니다.

>[!BEGINTABS]

>[!TAB Adobe Journey Optimizer용]

* 조직 ID (Adobe OrgID)
* 샌드박스 이름

>[!TAB Adobe Campaign용]

* Campaign 서버 URL
* 실시간 서버 URL
* Adobe Campaign 버전

>[!ENDTABS]


## 가드레일 및 제한 사항 {#important-notes}

* 메시지 제한이 없습니다. 시스템은 현재 Campaign SLA을 기준으로 5분당 4,000개 이상으로 보낼 수 있는 메시지 수를 제한합니다. 이러한 이유로 Journey Optimizer은 단일 사용 사례(대상이 아닌 개별 이벤트)에서만 사용해야 합니다.

* 사용할 템플릿당 캔버스에 대해 하나의 작업을 구성해야 합니다. Adobe Campaign에서 사용하려는 각 템플릿에 대해 Journey Optimizer에서 하나의 작업을 구성해야 합니다.

* 진행 중인 다른 Campaign 작업에 영향을 주지 않도록 이 통합을 위해 호스팅된 전용 메시지 센터 또는 Managed Services 인스턴스를 사용하는 것이 좋습니다. 마케팅 서버는 호스팅되거나 온-프레미스일 수 있습니다.<!--The build required is 21.1 Release Candidate or greater. -->

* 페이로드 또는 캠페인 메시지가 올바른지 확인할 수 없습니다.

* 대상자 자격 이벤트에는 Campaign 작업을 사용할 수 없습니다.

## 사전 요구 사항 {#prerequisites}

Adobe Campaign에서는 트랜잭션 메시지와 관련 이벤트를 만들고 게시해야 합니다. [Adobe Campaign 설명서](https://experienceleague.adobe.com/en/docs/campaign/campaign-v8/send/real-time/transactional){target="_blank"}를 참조하세요.

아래 패턴에 따라 각 메시지에 해당하는 JSON 페이로드를 빌드할 수 있습니다. 그런 다음 Journey Optimizer에서 작업을 구성할 때 이 페이로드를 붙여 넣습니다(아래 참조).

+++ 예

```json
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **채널**: 캠페인 트랜잭션 템플릿에 대해 정의된 채널
* **eventType**: Campaign 이벤트의 내부 이름
* **ctx**: 메시지에 있는 개인화를 기반으로 하는 변수입니다.

+++

## 작업 구성 {#configure-action}

Journey Optimizer에서는 트랜잭션 메시지당 하나의 작업을 구성해야 합니다.

Campaign 작업을 만들려면 다음 단계를 수행합니다.

1. 새 작업을 만듭니다. [사용자 지정 작업을 만드는 방법을 알아봅니다](../action/action.md).
1. 이름과 설명을 입력합니다.
1. **[!UICONTROL 작업 유형]** 필드에서 **[!UICONTROL Adobe Campaign Classic]**&#x200B;을(를) 선택합니다.
   ![](assets/accintegration1.png)
1. **[!UICONTROL 페이로드]** 필드를 클릭하고 캠페인 메시지에 해당하는 JSON 페이로드의 예제를 붙여 넣습니다. 이 페이로드를 가져오려면 Adobe에 문의하십시오.
1. 여정 캔버스에서 매핑할지 여부를 기준으로 각 필드를 정적 또는 변수로 설정합니다. 예를 들어 전자 메일 채널 매개 변수 및 개인화 필드(`ctx`)와 같은 필드는 일반적으로 여정 내에서 동적으로 조정할 수 있도록 변수로 설정해야 합니다.
1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 기존 작업 업데이트 {#update-action}

초기 설정 후 실시간(RT) 끝점이 변경되는 경우와 같이 기존 Campaign v7/v8 사용자 지정 작업을 업데이트해야 하는 경우 다음 단계를 수행합니다.

1. **[!UICONTROL 관리]** 메뉴에서 **[!UICONTROL 구성]**&#x200B;을 선택한 다음 **[!UICONTROL 작업]**(으)로 이동합니다.
1. 작업 목록에서 업데이트할 Campaign 작업을 찾아 선택합니다.
1. 작업 구성을 열려면 **[!UICONTROL 편집]**&#x200B;을 클릭하세요.
1. **[!UICONTROL URL]** 필드를 새 RT 끝점 URL로 업데이트합니다. 끝점 형식이 올바르고 연결 가능한지 확인하십시오.
1. 필요한 경우 **[!UICONTROL 페이로드]** 구성을 Campaign 트랜잭션 메시지 구조의 변경 사항과 일치하도록 업데이트하십시오.
1. **[!UICONTROL 테스트]**&#x200B;를 클릭하여 새 끝점에 대한 연결의 유효성을 검사합니다. 계속하기 전에 테스트가 성공적인 응답을 반환하는지 확인하십시오.
1. 유효성을 검사했으면 **[!UICONTROL 저장]**&#x200B;을 클릭하여 변경 내용을 적용합니다.

>[!NOTE]
>
>이 작업을 사용하는 모든 여정은 업데이트된 구성을 자동으로 사용합니다. 이 작업을 사용하는 라이브 여정이 있는 경우 끝점을 업데이트한 후 자세히 모니터링하여 적절한 메시지 게재를 확인합니다.

