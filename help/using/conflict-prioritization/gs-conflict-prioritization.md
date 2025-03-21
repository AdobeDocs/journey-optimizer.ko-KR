---
title: 충돌 관리 및 우선 순위 지정
description: Journey Optimizer 충돌 및 우선 순위 지정 도구를 활용하는 방법을 알아봅니다.
role: User
level: Beginner
badge: label="제한 공개"
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: dbe312f332031391c49a973f323994f860e354e3
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 10%

---

# 충돌 관리 및 우선 순위 지정 {#conflict-prioritization}

>[!AVAILABILITY]
>
>충돌 및 우선 순위 지정 기능은 현재 선택한 고객 그룹에 대해 제한된 가용성으로 사용할 수 있습니다. 이 기능은 향후 더 많은 사용자에게 점진적으로 배포될 예정입니다. 이 기능에 대한 대기자 명단에 등록하려면 계정 팀에 문의하십시오.

Journey Optimizer에서 너무 많은 상호 작용으로 고객에게 부담을 주는 상황을 피하려면 캠페인과 여정의 양과 타이밍을 관리하는 것이 필수적입니다. Journey Optimizer은 충돌 관리 및 우선 순위를 위한 여러 도구를 제공합니다.

## 충돌 관리 및 우선 순위 지정 도구 {#tools}

**충돌 검색 도구**&#x200B;를 사용하면 여정 및 캠페인에서 잠재적인 중복을 식별할 수 있습니다. 너무 많은 동시 통신이 고객 피로도를 초래할 수 있으므로 이는 매우 중요합니다. Journey Optimizer을 사용하면 타임라인, 대상 겹침 및 채널 구성과 같은 요소를 모니터링할 수 있습니다. 충돌을 조기에 식별하여 캠페인을 세분화함으로써 동시에 여러 메시지로 고객에게 충격을 주지 않도록 할 수 있습니다. [여정 및 캠페인에서 잠재적인 충돌을 감지하는 방법을 알아보세요](conflicts.md)

또한 **우선 순위 점수**&#x200B;를 통해 고객이 여러 커뮤니케이션에 참가할 수 있는 자격을 얻을 때 우선하는 캠페인이나 여정을 제어할 수 있습니다. 이 기능은 지정된 시간에 하나의 캠페인만 표시할 수 있는 웹 및 모바일과 같은 인바운드 채널에 특히 유용합니다. 각 여정 또는 캠페인에 우선 순위 점수를 할당하면 가장 중요한 메시지가 먼저 게재되도록 할 수 있습니다. [여정 및 캠페인에 우선 순위 점수를 할당하는 방법을 알아보세요](priority-scores.md)

**여정 제한 및 중재**&#x200B;를 통해 특정 기간 내에 고객이 입력할 수 있는 여정 수와 빈도를 제한할 수 있습니다. 프로필에 대한 여정 항목 수를 제한하거나 고객이 동시에 등록할 수 있는 여정 수를 제한하는 규칙을 설정할 수 있습니다. 또한 중재 설정을 사용하여 고객이 여러 여정에 적합한 경우 입력해야 하는 여정을 결정할 수 있으며, 우선순위 점수를 사용하여 가장 적합한 항목을 결정할 수 있습니다. [여정 한도 및 중재 작업 방법 알아보기](journey-capping.md)

마지막으로, 규칙 세트를 사용하여 **통신 유형별 빈도 제한**(예: 판매, 프로모션)을 설정하여 유사한 메시지가 있는 고객을 오버로드할 수 있습니다. 여러 채널에서 빈도를 제어할 수 있으며, 과도하게 요청된 프로필을 자동으로 제외하여 고객 경험을 개선할 수 있습니다. [규칙 집합 작업 방법 알아보기](../configuration/rule-sets.md)</li></ul>

이러한 기능을 활용하면 더욱 원활하고 타기팅된 마케팅을 수행할 수 있으므로 충돌과 과부하를 방지하면서 적시에 적절한 메시지를 전달할 수 있습니다.

## 가드레일 및 제한 사항

**빈도 제한 및 일괄 대상자**

빈도 제한, 채널 또는 여정 모두에서 사용되는 대상자가 배치 대상자인 경우 여정 입력 시 참조되는 프로필 카운터 값 또는 채널 통신을 위한 메시지 런타임은 수행되는 일별 스냅샷에서 가져옵니다.

고객이 다른 여정에 입력했거나 일별 스냅숏 시간과 여정이 입력된 시간(또는 배달되는 메시지) 사이에 다른 커뮤니케이션을 받은 경우 빈도 제한 제한을 초과할 수 있으므로 문제가 발생할 수 있습니다.

**빈도 제한 및 스트리밍 대상**

스트리밍 대상의 경우 시스템에서 업데이트된 카운터 값을 인식하는 데 최대 2시간이 걸릴 수 있으므로, 이러한 위험을 완화하려면 가능한 한 최소 2시간 간격으로 통신 및 여정을 구분하는 것이 좋습니다.

**여정 시작 시간**

충돌 관리 및 우선 순위 지정 기능이 올바르게 작동하도록 하려면 시스템이 카운터를 적절하게 업데이트할 수 있도록 여정의 시작 시간을 적어도 10분 후로 설정하는 것이 좋습니다.

고객이 여정을 입력할 때 이미 한도에 도달한 경우에도 입력이 허용되지 않지만 한도에 도달하지 않은 경우 입력 카운터가 증가하지 않습니다.

**여정 중재**

지금은 여정 중재에 대해 읽기 대상 여정 만 지원됩니다. 중재 설정은 단일 또는 대상 자격 여정에 활용할 수 없습니다.
