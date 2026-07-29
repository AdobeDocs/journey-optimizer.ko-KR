---
solution: Journey Optimizer
product: journey optimizer
title: 여정 문제 해결
description: 여정 문제 해결 방법 알아보기
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: 문제 해결, 문제 해결, 여정, 확인, 오류
exl-id: d255e9e4-301a-444a-86d3-97e0df4d3a49
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/2DTpTGcdmuFoajmHTUKGLK8zN2nfQp98tTc3FWtfI80
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: fa683eda-48de-4558-af32-2673edcd44fe
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 255
ht-degree: 38%

---

# 여정 문제 해결 {#troubleshooting}

>[!BEGINSHADEBOX]

**이 페이지에서:** 여정 오류, 실행 불일치, 인바운드 동작 문제 및 사용자 지정 동작 문제를 진단하고 해결하는 데 도움이 되는 일반적인 문제 영역별로 구성된 문제 해결 리소스를 찾으십시오.

>[!ENDSHADEBOX]

고객 여정이 예상대로 진행되지 않을 경우, 근본 원인을 파악하는 것이 어려울 수 있습니다. 문제를 효율적으로 해결하기 위해 아래에서 가장 일반적인 문제 영역별로 문제 해결 리소스를 찾을 수 있습니다. 여정 실패, 실행 불일치 또는 작업 수준의 문제가 표시되는 경우 각 섹션에서는 이러한 문제를 조사하고 해결하기 위한 구체적인 지침을 제공합니다.

특정 문제 해결 주제를 자세히 살펴보려면 아래 페이지를 탐색하십시오.



<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
    <a href="../building-journeys/troubleshooting.md"><img src="../assets/do-not-localize/troubleshooting.jpeg"></a>
    <div><strong>여정 오류 문제 해결</strong><br/> 테스트 또는 게시 전에 활동 또는 여정 오류를 식별하고 해결하는 방법과 여정 활동에 오류가 있는 경우 대체 동작을 정의하는 방법에 대해 알아봅니다.</div>
    </td>
    <td>
    <a href="../building-journeys/troubleshooting-execution.md"><img src="../assets/do-not-localize/ao-audiences.jpeg"></a>
    <div><strong>여정 실행 문제 해결</strong><br/> 여정 이벤트의 문제 해결 방법, 프로필이 여정에 입력되었는지 여부, 프로필의 탐색 방법, 메시지가 전송되었는지 여부를 확인합니다.</div>
    </td>
    <td>
    <a href="../building-journeys/troubleshooting-inbound.md" "><img src="../assets/do-not-localize/in-app.jpg"></a>
    <div><strong>인바운드 동작 문제 해결</strong><br/>여정에서 인바운드 동작과 관련된 문제를 디버깅하여 스스로 문제를 식별하고 해결하는 방법에 대해 알아봅니다.</div>
    </td>
    <td>
    <a href="../action/troubleshoot-custom-action.md"><img src="../assets/do-not-localize/lp-list.jpg"></a>
    <div><strong>사용자 지정 작업 문제 해결</strong><br/>Journey Optimizer 사용자 인터페이스의 관리 섹션에서 API 호출을 전송하여 사용자 지정 작업을 테스트하는 방법을 알아봅니다.</div>
    </td>
  </tr>
  <tr style="border: 0;">
    <td align="center"><a href="../building-journeys/troubleshooting.md"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="../building-journeys/troubleshooting-execution.md"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="../building-journeys/troubleshooting-inbound.md"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="../action/troubleshoot-custom-action.md"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    </tr>
</table>


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div>
    <a href="https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884">
    <img alt="일반적인 오류 코드 이해" src="../assets/do-not-localize/icon-quick-start.svg" /></a> 
    <br>또한 <strong>일반적인 오류 코드</strong>와 이를 효과적으로 해결하는 방법에 대해 자세히 설명하는 <a href="https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884" target="_blank">이 Adobe 커뮤니티 블로그 게시물</a>을 확인하십시오.
    </div>
  </td>
</tr>
</table>
