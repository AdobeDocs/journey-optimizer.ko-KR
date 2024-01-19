---
solution: Journey Optimizer
product: journey optimizer
title: 레코드
description: Journey Optimizer에서 DMARC 레코드를 설정하는 방법 알아보기
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 하위 도메인, 도메인, 메일, 도메인, 레코드
hide: true
hidefromtoc: true
source-git-commit: 5565c98e41e0abc9ae93f85cb12679e372e6d36f
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# DMARC 레코드 중요 업데이트{#dmarc-record}


>[!CAUTION]
>
>대량 발신자에 대한 최근 Gmail 및 Yahoo 공지에 이어 이제 Journey Optimizer에서 DMARC 인증 기술을 지원합니다.

시행 업계 모범 사례의 일부로서, Google과 Yahoo는 모두 이메일을 보내는 데 사용하는 모든 도메인에 대한 DMARC 레코드를 보유해야 합니다. 이 새 요구 사항은에 시작됩니다. **2024년 2월 1일**.

에서 DMARC 기록을 위한 Google 및 Yahoo의 요구 사항에 대해 자세히 알아보십시오. [이 섹션](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Google 및 Yahoo에서 발표된 변경 사항에 대해 자세히 알아보십시오. [이 페이지](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

다음 작업 또는 섹션을 위한 다음 단계에 대해 설명합니다.

모든 하위 도메인에 대해 설정해야 합니다.
* 도메인을 당사에 완전히 위임한 경우 두 가지 옵션이 있습니다
   * 호스팅 솔루션에서 위임된 도메인의 상위 도메인에 DMARC를 설정하거나
   * 호스팅 솔루션에 대한 추가 작업 없이 관리 UI에서 예정된 기능을 사용하여 위임된 도메인에 대한 DMARC를 설정합니다
* 전송 도메인에 대해 CNAME을 설정한 경우 두 가지 옵션이 있습니다
   * 호스팅 솔루션에서 하위 도메인 또는 하위 도메인의 상위 도메인에 DMARC를 설정하거나
   * 관리자 UI의 예정된 기능을 사용하여 DMARC를 설정합니다. 그러나 UI뿐만 아니라 호스팅 솔루션에 입력해야 합니다.

예정된 기능에 대한 자세한 내용이 곧 제공됩니다.

또한 아래 섹션(위 링크에서 복사됨)에서 DMARC와 관련된 섹션을 복사하여 설정하지 않은 경우 영향을 포함할 수 있습니다. 이제 DMARC와 관련된 것들을 빼든지 또는 여기에서 DMARC와 원클릭 미확인자를 위한 발표임을 교육할 수 있으며, 두 기능에 대한 최신 타임라인을 소개합니다.

10월에 처음 발표된 이후 타임라인에 대한 업데이트가 예정되어 있습니다.

가장 최근 타임라인은 다음과 같습니다.

Gmail:

* 2024년 2월 - 미준수 경고를 제공하기 위해 설계된 임시 바운스가 시작됩니다. 아직 규정을 준수하지 않는 경우 짧은 지연 후에도 이메일은 정상적으로 배달됩니다. 당신이 완전히 규정을 준수한다면, 일시적인 반등은 없을 것이고 당신은 아무것도 알아차리지 못할 것이다.
* 2024년 4월 - 목록 구독 취소 1-클릭을 제외한 모든 사항을 준수하지 않는 발신자에 대해 차단이 시작됩니다. 호환되지 않는 이메일은 일부만 차단되며 차단되는 비율은 시간이 지남에 따라 증가합니다.
* 2024년 6월 1일 - List-Unsubscribe 1-Click을 포함하여 완전히 준수하지 않은 보낸 사람은 차단됩니다.

Yahoo:

는 정확한 날짜는 밝히지 않았지만 &quot;2024년 2월부터 시행이 시작될 것&quot;이라고 말했다. 시행은 점진적으로 이루어질 것이다.&quot;
