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
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 300
ht-degree: 8%

---

# 사용 사례: 게재 램프 업{#use-case-ramp-up-your-deliveries}

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
