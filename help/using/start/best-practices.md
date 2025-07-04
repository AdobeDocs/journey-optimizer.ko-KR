---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 우수 사례
description: Journey Optimizer 모범 사례에 대해 자세히 알아보기
feature: Get Started
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 271fb85d-5621-4a12-b3d1-65cf6021b174
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '983'
ht-degree: 4%

---

# 모범 사례 {#best-practices}

## 실시간 사용 사례 및 옴니채널 개인화 지침 {#real-time-guidance}

ID 서비스 2.0 업데이트에 따라 실시간 ID 결합이 발전했습니다.

Adobe Journey Optimizer은 ID 서비스를 활용하여 사용자를 위해 프로필을 병합하고 경험을 개인화합니다. 따라서 사용 사례를 구성할 때 서비스에서 알아 두어야 할 몇 가지 중요한 측면이 있습니다. 브랜드는 사람에게 경험을 전달하려고 합니다. ID 그래프를 통해 마케터는 다양한 채널에서 개인이 어떤 장치와 연결되어 있는지 이해할 수 있습니다. 그래프에는 개인(CRMID) 또는 웹 브라우저(ECID)를 나타내는 ID가 포함될 수 있습니다. ID 서비스는 이 정보를 함께 결합하므로 개인 또는 병합된 프로필의 &#39;360도 보기&#39;를 만들 수 있습니다. 즉, 사용자가 사이트를 탐색한 다음 로그인하면 해당 세션의 모든 이전 데이터가 로그인 사용자와 연결될 수 있습니다. 이 작업은 몇 가지 다른 단계에서 수행됩니다.

1. ID의 초기 결합 - 사용자가 로그인하면 로그인 식별자(CRMID)가 웹 브라우저 식별자(웹 또는 모바일 앱 세션)와 연결됩니다.

   * 완료하는 데 30분~4시간 정도 걸릴 수 있습니다.
   * 일반적으로 이 로그인 이벤트는 CRMID를 ECID와 연결하는 ID 그래프를 생성합니다.

1. 초기 결합 후, 두 ID 중 하나로 전송된 모든 데이터는 병합된 프로필에 연결되고 Journey Optimizer에서 실시간으로 개인화할 수 있습니다. 최신 동작 데이터로 프로필 업데이트를 완료하는 데 최대 1분이 걸릴 수 있습니다. 이 [페이지](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=ko)를 참조하세요.

사용 사례를 작성할 때는 다음 사항을 고려하십시오.

1. 브랜드는 중단 후 30분 후에 사이트 방문자를 다시 참여시키려고 합니다(예: 포기한 장바구니 이메일):

   데이터에 ID 사용 - ECID. 지난 30분 내에 이메일 주소/앱 설치를 제공한 방문자의 100%를 캡처하려면 쿠키 기반 ID를 사용하여 이 여정(ECID)를 시작해야 합니다. 이메일 주소 또는 푸시 토큰 또는 경험에 대한 다른 주소가 ECID에 연결되어 있다고 가정합니다.

1. 웹, 이메일, 푸시 등의 옴니채널 참여:

   * 참여 시 프로필에서 사용할 수 있는 통신 주소가 있어야 합니다. 이 작업이 일관되고 적시에 수행되도록 하려면 데이터가 사용하려는 ID에 연결되어 있는지 확인하십시오.
   * 새로 설치된 앱 또는 브라우저 세션에서 알려진 정보나 로그인 정보와 결합하여 정보를 사용해야 하는 경우 이러한 ID가 결합된 후 이 통신을 전송해야 합니다. 이는 고객마다 다를 수 있으며 최대 볼륨의 프로필을 가져오기 위해 최소 30분 이상 기다리는 것이 좋습니다.

## 여정 보호 기능으로 확장 {#scale}

이 섹션에서는 다음 두 가지 제한 사항을 사용하여 크기를 조정하는 방법을 안내합니다.

* Journey Optimizer에는 여정 캔버스에 50개의 활동 보호 기능이 있습니다. 이 가드레일은 가독성, QA 및 문제 해결에 도움이 되도록 설계되었습니다. 여정의 활동 수는 이 제한의 10개 활동 이내에 도달하면 여정 캔버스의 왼쪽 상단 섹션에 표시됩니다.

* 여정을 게시하면 Journey Optimizer이 자동으로 확장 및 조정되어 최대 처리량과 안정성을 보장합니다. 샌드박스에서 한 번에 100개의 라이브 여정의 이정표에 가까워지면 주황색 오버레이가 표시되고 이 도전 과제의 인터페이스에 경고 기호가 나타납니다. 이 알림을 받았는데 실시간 여정을 100개 넘게 실행하도록 현재 여정의 수를 확장해야 하는 경우, 고객 지원 센터에 보내는 티켓을 개설해 주시면 Adobe가 목표 달성을 도와 드리겠습니다.

<!--DOCAC-10977

* As you publish journeys, Journey Optimizer automatically scales and adjusts to ensure maximum throughput and stability. As you near the milestone of 500 live journeys at one time in a sandbox, you will see an orange overlay and warning sign appear in the interface on this achievement. If you see this notification and have a need to extend your journeys beyond 500 live journeys at a time, please create a ticket for customer care and we will help you reach your goals.-->


여러 가지 모범 사례를 채택하여 보호 기능 내에서 유지하고 시스템을 효율적으로 사용하는 데 도움이 됩니다.

* 라이브 여정 한도에 가까워지면 **여정**&#x200B;의 **개요** 탭으로 이동하여 최근 24시간 동안 활성화된 프로필이 있는 여정 내에 활성화된 여정 수를 확인하는 것이 첫 번째 단계입니다. 이 섹션에서 여정을 시작 및 종료하는 프로필 수를 확인하여 확인할 수 있습니다.

  ![](assets/journey-guardrails2.png)

* 다음으로, 여정 인벤토리 섹션에서 상태 = &quot;라이브&quot; 및 유형 = &quot;대상 읽기&quot;로 모든 여정을 필터링할 수 있습니다. 그런 다음 발행 날짜별로 정렬합니다(가장 오래된 날짜부터 가장 최근 날짜까지). 여정을 클릭하고 일정으로 이동합니다. **한 번** 또는 **가능한 한 빨리**&#x200B;를 실행하도록 예약되어 있고 하루 이상 실행 중인 작업 하나만 있는 모든 라이브 여정을 중지합니다.

  ![](assets/journey-guardrails1.png)

* **대상자 읽기** 여정에 대기/결정 또는 전송 시간 최적화가 없는 한 가지 작업만 있는 경우 Journey Optimizer 캠페인으로 이동하는 것이 좋습니다. 캠페인은 단일 단계 참여에 더 적합합니다. Campaign과 여정 간의 주요 차이점 중 하나는 사용자 참여를 적극적으로 수신하여 다음 단계를 결정하고 다른 작업에 참여하는 것이 중요하다고 느끼는지 여부입니다.
* 여정 내의 활동 수를 줄이려면 조건 단계를 확인하십시오. 조건을 세그먼트 정의 또는 대상 구성으로 이동할 수 있는 인스턴스가 여러 개 있을 것입니다.
* 여러 여정(동의 확인, 제외)에 걸쳐 동일한 조건이 반복되는 경우 세그먼트 정의의 일부로 이동하는 것이 좋습니다. 예를 들어 여러 여정에서 &quot;이메일 주소가 비어 있지 않습니다&quot;를 확인하는 조건이 있는 경우 해당 조건을 세그먼트 정의의 일부로 포함시킵니다.
* 여정에 각 단계의 숫자를 보기 위해 대상을 분할하는 여러 조건이 있는 경우 분석에 더 적합한 Customer Journey Analytics 또는 기타 보고 솔루션을 사용하는 것이 좋습니다.
* 캔버스에서 노드 제한에 근접하고 있다면 동적 매개 변수 또는 명시적 노드 대신 올바른 컨텐츠를 제공하는 컨텐츠와 작업을 통합하는 것이 좋습니다.

* 일괄 처리 세그먼트(A)가 있는 **대상 읽기** 여정이 있고 여정 inAudience 스트리밍 세그먼트(B) 내에서 를 사용하여 를 제외(즉, A-B 수행)하는 경우 해당 논리를 세그멘테이션 논리로 이동하고 제외를 세그멘테이션 논리의 일부로 사용하십시오.