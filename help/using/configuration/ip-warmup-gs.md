---
solution: Journey Optimizer
product: journey optimizer
title: IP 준비 계획 시작
description: IP 웜업 계획을 구현하는 방법 알아보기
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, 전달성
hide: true
hidefromtoc: true
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 8%

---

# IP 준비 계획 시작 {#ip-warmup-gs}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!BEGINSHADEBOX]

이 설명서의 내용:

* **[IP 준비 시작](ip-warmup-gs.md)**
* [IP 워밍업 캠페인 만들기](ip-warmup-campaign.md)
* [IP 준비 계획 만들기](ip-warmup-plan.md)
* [IP 준비 계획 실행](ip-warmup-execution.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>IP 웜업 기능은 현재 사용자를 선택하는 베타 버전으로만 사용할 수 있습니다. Beta 프로그램에 참여하려면 Adobe 고객 지원 센터에 문의해 주십시오.

포함 [!DNL Journey Optimizer]를 사용하면 최적의 전달성을 위한 모범 사례를 따르는 표준화되고 효율적인 방식으로 사용자 인터페이스에서 직접 IP 웜업 워크플로우를 쉽게 수행할 수 있습니다.

>[!CAUTION]
>
>이 기능은 이메일 채널에만 적용됩니다.

새로운 플랫폼을 사용해 이메일을 보낼 때 인터넷 서비스 제공자(ISP)는 인지되지 않은 IP 주소를 의심하게 된다. 대량의 이메일이 갑자기 전송되면 ISP는 해당 이메일을 스팸으로 표시하는 경우가 많습니다.

스팸으로 표시되지 않도록 하기 위해 IP 준비 계획 기능을 사용하여 전송되는 볼륨을 점진적으로 늘릴 수 있습니다. 의 이 새로운 옵션 **[!UICONTROL 관리]** 메뉴를 사용하면 복잡한 일별 여정을 만드는 대신 통합 방식으로 보다 쉽게 수행할 수 있습니다. 이를 통해 시작 단계를 원활하게 발전시키고 잘못된 주소의 전체 비율을 줄일 수 있습니다.

>[!NOTE]
>
>에서 IP warming을 사용하여 이메일 평판을 높이는 방법에 대해 자세히 알아보십시오. [전달성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html).

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

IP 준비 계획을 구현하는 주요 단계는 다음과 같습니다.

1. 먼저 IP 웜업 옵션이 활성화된 캠페인을 하나 이상 만들어야 합니다. [자세히 알아보기](ip-warmup-campaign.md)

1. 에서 IP 준비 계획 만들기 [!DNL Journey Optimizer] 및 게재 컨설턴트의 도움을 받아 준비한 Excel 시트를 업로드합니다. [자세히 알아보기](ip-warmup-plan.md)

1. 플랜의 각 단계에 대한 캠페인을 선택하고 해당 실행을 활성화합니다. [자세히 알아보기](ip-warmup-execution.md)
