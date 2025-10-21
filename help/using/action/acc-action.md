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
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 12%

---

# Adobe Campaign v7/v8과 통합 {#integrating-with-adobe-campaign-v7-v8}

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

## 전제 조건 {#prerequisites}

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
1. **작업 유형** 필드에서 **Adobe Campaign Classic**을(를) 선택합니다.
   ![](assets/accintegration1.png)
1. **페이로드** 필드를 클릭하고 캠페인 메시지에 해당하는 JSON 페이로드의 예제를 붙여 넣습니다. 이 페이로드를 가져오려면 Adobe에 문의하십시오.
1. 여정 캔버스에서 매핑할지 여부를 기준으로 각 필드를 정적 또는 변수로 설정합니다. 예를 들어 전자 메일 채널 매개 변수 및 개인화 필드(`ctx`)와 같은 필드는 일반적으로 여정 내에서 동적으로 조정할 수 있도록 변수로 설정해야 합니다.
1. **저장**&#x200B;을 클릭합니다.

