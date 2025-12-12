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
source-git-commit: 5dd6ebadd7b8c7490cb10496282697ce32ff3693
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 43%

---

# IP 준비 계획 시작 {#ip-warmup-gs}

[!DNL Journey Optimizer]을(를) 사용하면 최적의 전달성을 위한 모범 사례를 따르는 표준화되고 효율적인 방식으로 사용자 인터페이스에서 직접 IP 워밍업 워크플로우를 쉽게 수행할 수 있습니다. 새로운 플랫폼을 사용하여 이메일이 전송되면 인터넷 서비스 공급자(ISP)는 인식되지 않는 IP 주소를 의심합니다. 대량의 이메일이 갑자기 전송되면 ISP는 해당 이메일을 스팸으로 표시하는 경우가 많습니다.

스팸으로 표시되지 않도록 하기 위해 IP 준비 계획 기능을 사용하여 전송되는 볼륨을 점진적으로 늘릴 수 있습니다. **[!UICONTROL 관리]** 메뉴의 이 새로운 옵션을 사용하면 복잡한 여정 구성 없이도 볼륨 관리를 자동화하고 준비 프로세스를 단순화할 수 있습니다.

>[!NOTE]
>
>IP 웜업 계획을 구현하기 전에 이 [IP 웜업 전달성 안내서](ip-warmup-deliverability-guide.md)에서 전달성 기본 사항, 신뢰도 향상 및 모범 사례에 대해 알아봅니다.

➡️ [이 비디오에서 IP 준비 계획을 만들고 실행하는 방법을 알아봅니다.](#video)

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

>[!VIDEO](https://video.tv.adobe.com/v/3432637/?learn=on)

>[!NOTE]
>
>[게재 가능성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=ko)에서 IP warming으로 전자 메일 평판을 높이는 방법에 대해 자세히 알아보세요.

## 추가 리소스 {#additional-resources}

IP 웜업에 대한 보다 심층적인 지침을 얻으려면 다음과 같은 유용한 블로그 게시물을 살펴보십시오.

* [Adobe Journey Optimizer 전달성 안내서: Zero Reality에서 Inbox Hero까지](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950) - 신뢰도 기본 사항, 준비 달력, 모니터링 및 문제 해결 모범 사례에 대한 포괄적인 안내서입니다.

* [IP 준비 설정 방법 이해](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warmup-understanding-how-to-set-up-the-ip-warmup/ba-p/761949) - 성공적인 구현을 위한 IP 준비 계획 및 모범 사례 설정의 기본 사항에 대해 알아봅니다.

* [IP 준비 계획의 고급 기능](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/advanced-features-in-ajo-ip-warm-up-plans-granular-controls-for/ba-p/761958) - IP 준비 전략을 최적화하기 위한 고급 기능과 세분화된 제어 기능을 살펴보십시오.

* [IP 준비 문제 해결](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warm-up-troubleshooting-audience-delays-and-smart-retry/ba-p/761952) - 대상 지연과 같은 일반적인 문제에 대한 해결 방법을 찾고 스마트 다시 시도 메커니즘에 대해 알아봅니다.
