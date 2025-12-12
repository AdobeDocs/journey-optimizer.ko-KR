---
solution: Journey Optimizer
product: journey optimizer
title: IP 웜업 전달성 안내서
description: 게재 기능의 기본 사항과 IP 웜업에 대한 모범 사례에 대해 알아봅니다.
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, 전달성, 신뢰도, ISP, 참여
source-git-commit: 07896931a7c06e1b712f3b65e1dcf939b521ba83
workflow-type: tm+mt
source-wordcount: '1088'
ht-degree: 6%

---

# IP 웜업 전달성 안내서 {#ip-warmup-deliverability-guide}

Adobe Journey Optimizer에서 새로운 IP 주소 또는 도메인으로 이메일 캠페인을 시작할 때 강력한 발신자 평판을 구축하려면 게재 기능의 기본 사항을 이해하는 것이 중요합니다. 이 안내서에서는 평판이 0에서 성공적인 받은 편지함 배치로 전환하는 데 도움이 되는 주요 개념, 준비 단계 및 모범 사례를 다룹니다.

➡️ [IP 웜업 전달성 기본 사항에 대해 알아보려면 이 비디오를 시청하십시오](#video)

>[!NOTE]
>
>Adobe Journey Optimizer에서 IP 준비 계획을 구현하는 방법에 대한 단계별 지침은 [IP 준비 계획 시작](ip-warmup-gs.md)을 참조하세요.

## IP 및 도메인 신뢰도가 중요한 이유 {#reputation-matters}

사서함 공급자(Gmail, Yahoo, Microsoft, Apple Mail 등)는 네 가지 주요 요소를 기반으로 모든 보낸 사람을 평가합니다.

* **컴플레인**: 받는 사람이 메시지를 스팸으로 표시했습니까?
* **참여**: 수신자가 이메일을 열고, 클릭하거나, 회신합니까?
* **인프라**: 전송 인프라가 인증되고 안정적이며 신뢰할 수 있습니까?
* **콘텐츠**: 메시지 콘텐츠가 합법적이고 가치 있게 표시됩니까?

IP 웜업은 주로 전체 전송 볼륨으로 확장하기 전에 사서함 공급자에게 새 인프라가 합법적이며 필요함을 점진적으로 보여줌으로써 처음 세 가지 문제를 해결합니다.

## 사전 검사 목록 {#pre-flight-checklist}

IP 주소를 준비하기 전에 모든 기본 요소가 제대로 되어 있는지 확인하십시오. 아래 표는 IP 준비 계획을 시작하기 전에 완료해야 하는 필수 작업을 간략하게 설명합니다.

| 작업 | 이것이 중요한 이유 | 수행 방법 |
|------|----------------|-------------------|
| AJO에서 고정 IP 및 위임 하위 도메인 예약 | 미래의 모든 평판은 이러한 인프라 요소에 연결됩니다 | **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL 전자 메일 설정]** > **[!UICONTROL 하위 도메인]**&#x200B;으로 이동합니다. [자세히 알아보기](delegate-subdomain.md) |
| SPF 및 DKIM 구성 | 전송 서버가 합법적이며 권한이 있는지 확인합니다. | 하위 도메인 위임 및 채널 구성 생성 후 Adobe에서 자동으로 처리됩니다. [자세히 알아보기](delegate-subdomain.md) |
| DMARC 레코드 설정 | 이메일 인증 보고 및 향후 적용 정책 활성화 | 하위 도메인 위임 및 채널 구성 생성 후 Adobe에서 자동으로 처리됩니다. [자세히 알아보기](dmarc-record.md) |
| 시드 목록 모니터링 구성 | 준비 프로세스 초기에 받은 편지함 배치 문제 감지 | 채널 구성을 만들 때 시드 주소를 추가합니다. [자세히 알아보기](seed-lists.md) |
| 1단계 높은 참여도 대상 구축 | 가장 활동적인 수신자와 함께 조기 참여 지표 강화 | 지난 30일 동안 열거나 클릭한 5,000명 미만의 대화 상대에 대한 대상 만들기 |

>[!CAUTION]
>
>볼륨 램핑을 통해 인증 문제(SPF, DKIM, DMARC)를 해결할 수 없습니다. 전송을 시작하기 전에 이러한 항목이 올바르게 구성되었는지 확인하십시오.

## 샘플 4주 준비 달력 {#warmup-calendar}

이 샘플 캘린더에서는 최종 일일 볼륨(UDV)의 백분율을 기반으로 하는 점진적 볼륨 램프를 제공합니다. 특정 전송 요구 사항에 맞게 이러한 숫자를 조정하고 전달성 컨설턴트와 협력하여 맞춤화된 계획을 만듭니다.

| 일 | UDV의 % | 타깃 대상자 | 콘텐츠 권장 사항 |
|------|----------|-----------------|------------------------|
| 1-3 | 0.5% | 가장 참여 중인 수신자 | 접힌 부분 위에 명확한 call-to-action을 사용하여 짧고 간단한 텍스트 형식 사용 |
| 4-7 | 1% | 참여 사용자 및 최근 구매자 | 경량 영웅 이미지 추가, 링크 3개 이하로 제한 |
| 8-14 | 5% | 더 광범위한 활성 구독자 목록 | 표준 이메일 템플릿을 소개하되 과도한 홍보 콘텐츠는 피하십시오. |
| 15-21 | 25% | 활성 구독자와 비활성 구독자 | 불만 비율을 면밀히 모니터링하면서 일반적인 마케팅 콘텐츠 사용 |
| 22-28 | 50-100% | 전체 목록(제외 목록 준수) | 고정 상태 전송 케이던스로 전환 |

>[!NOTE]
>
>Adobe Journey Optimizer은 복잡한 여정 구성 없이도 볼륨 관리를 자동화하고 웜업 프로세스를 간소화하는 전용 [IP 웜업 계획 기능](ip-warmup-gs.md)을 제공합니다.

## AJO의 IP 준비 계획 기능 사용 {#ajo-warmup-feature}

Adobe Journey Optimizer에는 복잡한 여정 설정을 통해 수동으로 볼륨을 제한할 필요가 없는 간소화된 IP 웜업 계획 기능이 포함되어 있습니다. 이 기능은 발신자의 신뢰도를 높이는 표준화된 접근 방식을 보장합니다.

### 작동 방식

1. **IP 준비 캠페인 만들기**: **[!UICONTROL IP 준비 계획 활성화]** 옵션을 사용하여 하나 이상의 캠페인을 빌드합니다. [자세히 알아보기](ip-warmup-campaign.md)

1. **플랜 설정**: **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL 전자 메일 설정]** > **[!UICONTROL IP 준비 계획]**&#x200B;에 액세스하고 게재 컨설턴트와 함께 준비한 단계별 준비 템플릿을 업로드합니다. [자세히 알아보기](ip-warmup-plan.md)

1. **단계 실행**: 각 단계에 대한 캠페인을 선택하고 해당 실행을 활성화합니다. 시스템에서는 과대 접촉을 방지하기 위해 이전 실행에서 프로필을 자동으로 제외합니다. [자세히 알아보기](ip-warmup-execution.md)

1. **모니터링 및 조정**: 통합 보고 대시보드를 사용하여 진행 상황을 추적하고, 실행 상태를 모니터링하고, 문제가 발생할 경우 계획을 수정합니다. [자세히 알아보기](ip-warmup-execution.md#monitor-plan)

## 실시간 모니터링 및 주요 지표 {#monitoring}

Adobe Journey Optimizer은 IP 웜업 성능을 추적하는 내장 보고 기능을 제공합니다.

* **실시간 보고서**: **[!UICONTROL 최근 24시간]** 탭에서 캠페인의 실시간 측정 및 시각화에 액세스합니다. [자세히 알아보기](../reports/live-report.md)

* **Customer Journey Analytics 통합**: 더 자세한 통찰력을 얻으려면 Customer Journey Analytics을 활용하여 Adobe Experience Platform에서 데이터를 분석하고 사용자 지정 시각화를 만드십시오. [자세히 알아보기](../reports/report-gs-cja.md)

### Target 지표

준비 기간 동안 다음 주요 성능 지표를 모니터링합니다.

| 지표 | 대상 임계값 | 초과된 경우 작업 |
|--------|-----------------|-------------------|
| 불만 비율 | ≤ 0.1% | 세그먼트 감사 및 만성 컴플레인 억제 |
| 하드 바운스 비율 | ≤ 2% | 목록 품질 및 위생 관행 검토 |
| 열람률 | ≥ 10% | 참여 대상을 타겟팅하고 있는지 확인 |

>[!TIP]
>
>포괄적인 캠페인 분석의 경우 [캠페인 실시간 보고서](../reports/campaign-live-report.md#email-live) 및 [Customer Journey Analytics 보고서](../reports/campaign-global-report-cja-email.md) 기능을 사용하십시오.

## 플레이북 문제 해결 {#troubleshooting}

이 의사 결정 매트릭스를 사용하여 준비 중 발생하는 일반적인 문제를 해결하십시오.

| 증상 | 가능한 원인 | 권장 작업 |
|---------|--------------|-------------------|
| Yahoo 임시 실패(421개 오류) | 볼륨이 너무 빨리 증가함 | 24시간 동안 전송을 일시 중지한 다음 이전 계층에서 다시 시작 |
| 전체 시드 계정의 열람율 2% 미만 | IP 차단 목록에 추가 | [Google Postmaster 도구](https://postmaster.google.com/) 및 [Microsoft SNDS](https://sendersupport.olc.protection.outlook.com/snds/)를 확인하세요. 필요한 경우 게재 가능 티켓을 여세요. |
| 고객 불만율이 0.3%를 초과합니다. | 잘못 타기팅되거나 오래된 대상 | 세그먼트 정의를 감사하고 [비표시 목록](manage-suppression-list.md)에서 만성 컴플레인을 제외합니다. |

>[!IMPORTANT]
>
>나중에 손상된 발신자의 평판을 복구하려고 시도하는 것보다 준비 시간을 늦추는 것이 좋습니다. 항상 적극적인 볼륨 램핑보다 건강한 지표를 유지하는 것을 우선시하십시오.

## 준비 후 우수 사례 {#post-warmup}

준비 계획 및 지표가 안정되면 다음을 수행합니다.

* **일관성 유지**: 일별 볼륨 증가를 매주 30% 미만으로 유지하여 기존 평판을 유지하십시오

* **계속 모니터링**: 분기별 신뢰도 상태 검사를 예약하여 문제를 사전에 식별하고 해결합니다.

* **참여 신호 준수**: 참여 받는 사람의 우선 순위를 계속 지정하고 비활성 구독자에 대한 재참여 캠페인을 구현합니다.

* **현재 인증 유지**: SPF, DKIM 및 DMARC 레코드가 올바르게 구성되어 있는지 정기적으로 확인합니다

## 주요 개선 사항 {#key-takeaways}

* **IP 웜업이 필수임**: 웜업 프로세스를 건너뛰면 이를 올바르게 수행하는 데 필요한 작업보다 시간과 평판이 더 많이 듭니다

* **데이터 기반 결정**: ISP가 귀하를 처벌하기 전에 매일 컴플레인, 바운스 및 참여 비율을 추적하고 전략을 조정합니다

* **먼저 인증하고, 두 번째 볼륨을 인증합니다**: 볼륨을 높이기 전에 모든 SPF, DKIM 및 DMARC 문제를 해결하십시오.

* **일관성 문제**: 사서함 공급자는 예측 가능한 전송 패턴을 선호하므로 갑작스러운 볼륨 스파이크나 불규칙적인 전송 일정을 피하십시오

## 사용 방법 비디오 {#video}

Adobe Journey Optimizer의 IP 웜업에 대한 전달성 기본 사항, 평판 구축 및 모범 사례에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3457695/?learn=on)

<!--
>[!NOTE]
>
>For more guidance, explore the [Adobe Journey Optimizer Deliverability Guide blog post](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950?profile.language=ko).-->

## 관련 항목 {#related-topics}

* [IP 준비 계획 시작](ip-warmup-gs.md)
* [IP 워밍업 캠페인 만들기](ip-warmup-campaign.md)
* [IP 워밍업 플랜 만들기](ip-warmup-plan.md)
* [IP 준비 계획 실행](ip-warmup-execution.md)
* [채널 구성 설정](channel-surfaces.md)
* [하위 도메인 위임](delegate-subdomain.md)
* [금지 목록 관리](manage-suppression-list.md)
* [전달성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=ko)

