---
title: Adobe Campaign v7/v8과 통합
description: Adobe Campaign v7/v8과 통합하는 방법을 알아봅니다
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: 51c63b196b11905289c3c0c450c1976eb551bbc8
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 4%

---

# Adobe Campaign v7/v8과 통합 {#integrating-with-adobe-campaign-classic}

이 통합은 21.1 릴리스부터 Adobe Campaign Classic v7 및 Adobe Campaign v8에서 사용할 수 있습니다. Adobe Campaign 트랜잭션 메시지 기능을 사용하여 이메일, 푸시 알림 및 SMS를 전송할 수 있습니다.

Journey Optimizer 인스턴스와 Campaign 인스턴스 간의 연결은 프로비저닝 시 Adobe에 의해 설정됩니다.

여기에는 종단 간 사용 사례가 나와 있습니다 [섹션](../building-journeys/campaign-classic-use-case.md).

구성된 각 작업에 대해 여정 디자이너 팔레트에서 작업 활동을 사용할 수 있습니다. 다음을 참조하십시오 [섹션](../building-journeys/using-adobe-campaign-classic.md).

## 중요 정보 {#important-notes}

* 메시지 제한이 없습니다. 시스템은 현재 Campaign SLA를 기반으로 하여 5분마다 4000으로 전송할 수 있는 메시지 수를 제한합니다. 이러한 이유로 Journey Optimizer은 단일 사용 사례(세그먼트가 아닌 개별 이벤트)에서만 사용해야 합니다.

* 사용하려는 템플릿당 캔버스에서 한 개의 작업을 구성해야 합니다. Adobe Campaign에서 사용할 각 템플릿에 대해 Journey Optimizer에서 하나의 작업을 구성해야 합니다.

* 진행 중인 다른 Campaign 작업에 영향을 주지 않도록 이 통합을 위해 호스팅되는 전용 메시지 센터 인스턴스를 사용하는 것이 좋습니다. 마케팅 서버는 호스팅 또는 온프레미스할 수 있습니다. 필요한 빌드는 21.1 릴리스 후보 이상입니다.

* 페이로드 또는 Campaign 메시지가 올바른지 확인하지 않습니다.

* 세그먼트 자격 이벤트에서 캠페인 작업을 사용할 수 없습니다.

## 전제 조건 {#prerequisites}

Campaign에서는 트랜잭션 메시지와 관련 이벤트를 만들고 게시해야 합니다. 자세한 내용은 [Adobe Campaign 설명서](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target=&quot;_blank&quot;}.

아래 패턴에 따라 각 메시지에 해당하는 JSON 페이로드를 작성할 수 있습니다. 그런 다음 Journey Orchestration에서 작업을 구성할 때 이 페이로드를 붙여 넣습니다(아래 참조)

다음은 한 예입니다.

```
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **channel**: 캠페인 트랜잭션 템플릿에 대해 정의된 채널
* **eventType**: Campaign 이벤트의 내부 이름
* **ctx**: 변수에 설정된 값은 메시지에 포함된 개인화를 기반으로 합니다.

## 작업 구성 {#configure-action}

Journey Optimizer에서는 트랜잭션 메시지당 하나의 작업을 구성해야 합니다. 다음 단계를 수행합니다.

1. 새 작업을 만듭니다. 다음을 참조하십시오 [섹션](../action/action.md).
1. 이름과 설명을 입력합니다.
1. 에서 **작업 유형** 필드, 선택 **Adobe Campaign Classic**.
1. 을(를) 클릭합니다. **페이로드** 필드를 만들어 Campaign 메시지에 해당하는 JSON 페이로드의 예제를 붙여넣습니다. 이 페이로드를 가져오려면 Adobe에 문의하십시오.
1. 여정 캔버스에 매핑할지 여부에 따라 다른 필드를 정적 또는 변수로 조정합니다. 전자 메일 주소 및 개인화 필드(ctx)에 대한 채널 매개 변수와 같은 특정 필드는 여정 컨텍스트에서 매핑을 위한 변수로 정의할 수 있습니다.
1. **저장**&#x200B;을 클릭합니다.

![](assets/accintegration1.png)
