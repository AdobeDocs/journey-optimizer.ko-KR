---
title: Journey Optimizer에서 ID 시작
description: Adobe Journey Optimizer에서 ID를 관리하는 방법 알아보기
feature: 프로필
role: User
level: Beginner
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 6%

---

# ID 시작 {#identities-gs}

ID는 엔티티에 고유한 데이터(일반적으로 개별 개인)입니다. 로그인 ID, ECID 또는 충성도 ID와 같은 ID를 알려진 ID라고 합니다.

이메일 주소 및 전화 번호와 같은 PII(개인 식별 정보)는 고객을 직접 식별하는 데 사용됩니다. 따라서 PII는 여러 시스템에서 고객의 여러 ID를 일치시키는 데 사용됩니다.

[!DNL Adobe Journey Optimizer], **Identities**&#x200B;가 장치 및 채널에서 소비자를 연결하는 경우 결과는 [identity graph](#id-graph)입니다. 연결된 ID 그래프는 모든 비즈니스 터치포인트에서 상호 작용을 기반으로 경험을 개인화하는 데 사용됩니다.

![](assets/identities-home.png)

[이 설명서](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html){target=&quot;_blank&quot;}의 **ID 서비스**&#x200B;에 대해 자세히 알아보십시오.

## ID 네임스페이스

**** ID 네임스페이스는 ID 서비스의 구성 요소이며 ID가 연관되는 컨텍스트의 지표 역할을 합니다. 예를 들어 `name@email.com` 값을 이메일 주소로 구분하거나 `443522` 값을 숫자 CRM ID로 구분합니다. ID 네임스페이스로 작업하려면 관련된 다양한 Adobe Experience Platform 서비스를 이해해야 합니다. 네임스페이스로 작업을 시작하기 전에 다음 서비스에 대한 설명서를 검토하십시오.

[이 설명서](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html){target=&quot;_blank&quot;}의 **ID 네임스페이스**&#x200B;에 대해 자세히 알아보십시오.

## ID 그래프{#id-graph}

**Identity Graph**&#x200B;는 특정 고객을 위한 서로 다른 ID 간의 관계 맵으로서, 고객이 다른 채널에서 브랜드와 상호 작용하는 방식을 시각적으로 보여줍니다. 모든 고객 ID 그래프는 고객 활동에 대한 응답으로 거의 실시간으로 Adobe Experience Platform Identity Service에서 통합 관리 및 업데이트됩니다.

[!DNL Adobe Journey Optimizer] 사용자 인터페이스의 ID 그래프 뷰어를 사용하면 함께 결합되는 고객 ID와 결합되는 항목을 시각화하고 더 잘 이해할 수 있습니다. 뷰어를 사용하면 그래프의 다른 부분과 드래그 및 상호 작용할 수 있으므로 복잡한 ID 관계를 살펴보고 보다 효율적으로 디버깅할 수 있으며 정보 활용 방식의 투명성 증대를 얻을 수 있습니다.

[이 설명서](https://experienceleague.adobe.com/docs/experience-platform/identity/ui/identity-graph-viewer.html){target=&quot;_blank&quot;}의 **ID 그래프**&#x200B;에 대해 자세히 알아보십시오.

