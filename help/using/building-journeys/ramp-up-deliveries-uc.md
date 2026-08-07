---
solution: Journey Optimizer
product: journey optimizer
title: 게재 램프 업
description: 게재를 가속화하는 방법에 대해 알아봅니다
feature: Journeys, Use Cases, IP Warmup Plans
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
hide: true
keywords: 전달성, 여정, 사용 사례, 이메일, 신뢰도
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/en0jMw69ddHSQrIH05-9FfGuDwNKb36f5Lp3fLp2oAk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 807
ht-degree: 2%

---

# 사용 사례: 게재 램프 업{#use-case-ramp-up-your-deliveries}

>[!BEGINSHADEBOX]

**이 페이지에서:** 최적화 활동 및 프로필 상한선을 사용하여 전자 메일 게재를 점진적으로 늘려 나가는 여정을 만드는 방법을 알아봅니다. 이를 통해 새 IP 주소를 정리하고 보낸 사람의 신뢰도를 설정할 수 있습니다.

>[!ENDSHADEBOX]

최근 다른 이메일 서비스 공급자, IP 주소, 이메일 도메인 또는 하위 도메인으로 이동한 경우 발신자로서의 신뢰도를 설정해야 합니다. 그렇지 않으면 게재가 차단되거나 수신자 사서함의 스팸 폴더로 이동될 수 있습니다. [게재 가능성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=ko){target="_blank"}에서 IP warming으로 전자 메일 신뢰도를 높이는 방법을 알아봅니다.

IP를 준비하려면 게재 수를 점차적으로 늘릴 수 있습니다. [Journey Optimizer에서 게재 기능 최적화](../reports/deliverability.md)에 대해 자세히 알아보세요.

이 사용 사례의 목적은 이메일 게재를 가속화하는 여정을 만드는 것입니다. 이 여정을 구성하려면 다음 단계를 수행합니다.

1. 여정 만들기 [자세히 보기](journey-gs.md).

1. **[!UICONTROL 최적화]** 활동을 여정에 추가합니다. [자세히 보기](optimize.md).

1. **[!UICONTROL 조건]** 활동 설정에서 게재할 최대 받는 사람 수를 설정하십시오.

   1. **[!UICONTROL 최적화]** 활동 설정에서 **[!UICONTROL 조건]** 메서드를 선택하고 **[!UICONTROL 유형]** 필드를 **[!UICONTROL 프로필 상한]**(으)로 설정하십시오. [자세히 보기](conditions.md#profile_cap).

   1. **[!UICONTROL 제한]** 필드를 이 게재의 최대 받는 사람 수로 설정하십시오.

   ![게재 볼륨을 제어하기 위한 프로필 상한 조건 구성](assets/profile-cap-condition.png)

   이 제한을 총 구독자 수까지 점진적으로 늘릴 수 있습니다.

1. **[!UICONTROL Condition]** 활동 뒤에 **[!UICONTROL Email]** 동작 활동을 명목 경로에 추가합니다.

   ![연속 게재 여정의 전자 메일 메시지 구성](assets/ramp-up-deliveries-message.png)

   여정이 실행되면 지정한 최대 프로필 수까지 입력한 프로필로 메시지가 전송됩니다. 이 한도에 도달하면 입력한 프로필에서 대체 경로를 사용합니다.

1. 선택한 활동으로 여정을 완료합니다.

IP가 예열되면 이 조건을 제거할 수 있습니다.

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

- **TL;DR:** 이 사용 사례에서는 IP 준비 중 보낸 사람의 평판을 보호하기 위해 프로필 상한 조건을 사용하여 이메일 게재 볼륨을 점차적으로 늘리는 Adobe Journey Optimizer 여정을 만드는 방법을 설명합니다.

**의도:**
- IP warming에 대한 이메일 게재 볼륨을 점차적으로 늘리는 여정 구축
- 게재 실행당 수신자 수를 제한하도록 프로필 상한 조건 구성
- 새 이메일 서비스 공급자, IP 주소 또는 도메인으로 전환할 때 발신자의 평판을 보호합니다.
- IP가 완전히 예열되면 볼륨 캡 조건을 제거합니다.

**용어집:**
- **IP 준비 중**: 사서함 공급자 *(제품별)*&#x200B;에서 보낸 사람의 신뢰도를 구축하기 위해 새 IP 주소 또는 도메인에서 전자 메일 전송 볼륨을 점차 늘리는 프로세스입니다.
- **프로필 상한**: 지정된 여정 실행 *(제품별)*&#x200B;에서 메시지를 받는 최대 프로필 수를 제한하는 최적화 활동의 조건 유형입니다.
- **활동 최적화**: 조건, 타깃팅 규칙 또는 실험을 적용하여 여정이 *(제품별)*&#x200B;을(를) 통해 흐르는 방식을 제어하는 데 사용되는 여정 캔버스 활동

**보호 기능:**
- 프로필 상한 조건은 활동의 조건 최적화 방법에서 설정하여 게재 볼륨을 제어해야 합니다.
- 상한을 초과하는 프로필은 여정에 정의된 대체 경로를 사용합니다.
- 프로필 상한 제한은 전체 구독자 수까지 시간이 지남에 따라 점진적으로 증가해야 합니다.

**용어:**
- 정식 이름: 램프 업 게재 — 약어: 없음 — 변형: IP warming, IP warmup, 게재 램프 업
- 동의어: &quot;IP warming&quot; = &quot;IP warmup&quot; = &quot;sender reality building&quot;
- 혼동하지 마십시오. &quot;프로필 상한&quot; ≠ &quot;대상 크기 제한&quot;(프로필 상한은 실행당 게재 제한이며, 대상 크기는 자격을 갖춘 프로필의 총 수입니다.)

**FAQ:**
- **Q: 새 IP 또는 도메인으로 전환할 때 게재를 증가시켜야 하는 이유는 무엇입니까?** — 새 IP 또는 도메인에 전송 기록이 없으므로 점차 증가하는 볼륨을 통해 긍정적인 평판이 확립될 때까지 사서함 제공업체는 폴더 메시지를 차단하거나 스팸 메일로 보낼 수 있습니다.
- **Q: 프로필 상한 조건은 게재 볼륨을 어떻게 제어합니까?** — 단일 여정 실행에서 메시지를 수신할 수 있는 최대 프로필 수를 설정합니다. 이 제한을 초과하는 프로필은 대신 대체 경로를 사용합니다.
- **Q: 프로필 상한 조건은 언제 제거할 수 있습니까?** — IP가 완전히 예열되고 보낸 사람의 신뢰도가 설정되면 여정에서 해당 조건을 제거할 수 있습니다.
- **Q: 시간이 지남에 따라 캡을 점차적으로 늘릴 수 있습니까?** — 예. 프로필 상한 조건의 제한 필드를 업데이트하여 실행당 수신자 수를 전체 가입자 수까지 점진적으로 늘릴 수 있습니다.

+++
