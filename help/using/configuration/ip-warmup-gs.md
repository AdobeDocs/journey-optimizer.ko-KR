---
solution: Journey Optimizer
product: journey optimizer
title: IP 준비 계획 시작
description: IP 준비 계획을 구현하는 방법 알아보기
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, 전달성
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
source-git-commit: 5e0d683bf52df4992773c6147b9e418241777e5d
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 73%

---

# IP 준비 계획 시작 {#ip-warmup-gs}

[!DNL Journey Optimizer]을(를) 사용하면 최적의 전달성을 위한 모범 사례를 따르는 표준화되고 효율적인 방식으로 사용자 인터페이스에서 직접 IP 워밍업 워크플로우를 쉽게 수행할 수 있습니다. 새로운 플랫폼을 사용하여 이메일이 전송되면 인터넷 서비스 공급자(ISP)는 인식되지 않는 IP 주소를 의심합니다. 대량의 이메일이 갑자기 전송되면 ISP는 해당 이메일을 스팸으로 표시하는 경우가 많습니다.

스팸으로 표시되지 않도록 하기 위해 IP 준비 계획 기능을 사용하여 전송되는 볼륨을 점진적으로 늘릴 수 있습니다. **[!UICONTROL 관리]** 메뉴의 이 새로운 옵션을 사용하면 복잡한 일일 여정을 만드는 대신 통합된 방식으로 더 쉽게 작업을 수행할 수 있습니다.

➡️[이 비디오에서 IP 준비 계획을 만들고 실행하는 방법을 알아봅니다](#video)

>[!AVAILABILITY]
>
>이 기능은 프로덕션 유형 샌드박스에서만 활성화할 수 있습니다.

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

IP 준비 계획을 구현하는 주요 단계는 다음과 같습니다.

1. 먼저 IP 준비 옵션이 활성화된 캠페인을 하나 이상 만들어야 합니다. [자세히 알아보기](ip-warmup-campaign.md)

1. [!DNL Journey Optimizer]에서 IP 준비 계획을 만들고 전달성 컨설턴트의 도움을 받아 준비된 Excel 시트를 업로드합니다. [자세히 알아보기](ip-warmup-plan.md)

1. 계획의 각 단계에 대한 캠페인을 선택하고 해당 실행을 활성화합니다. [자세히 알아보기](ip-warmup-execution.md)

## 방법 비디오 {#video}

IP 준비 계획을 만들고 실행하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3453847/?learn=on&captions=kor)

>[!NOTE]
>
>[게재 가능성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=ko)에서 IP warming으로 전자 메일 평판을 높이는 방법에 대해 자세히 알아보세요.
