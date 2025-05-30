---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 보고서
description: Campaign 보고서에서 이메일 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: d11dd1cb-041b-48cd-b1fc-bcbe12338a07
source-git-commit: cc435a133f5fe24bff0f6ec9ec135941cf0bab99
workflow-type: tm+mt
source-wordcount: '2181'
ht-degree: 1%

---

# 이메일 캠페인 보고서 {#campaign-global-report-cja-email}

>[!INFO]
>
>Apple에서 메일 개인 정보 보호 기능을 포함하여 기본 메일 앱에 새로운 개인 정보 보호 기능을 도입했기 때문에, 발신자는 더 이상 Apple의 메일 개인 정보 보호를 사용하도록 설정한 프로필의 데이터를 수집하기 위해 추적 픽셀을 사용할 수 없습니다. 따라서 추적 픽셀을 사용하여 이메일 열기를 추적하는 Adobe Journey Optimizer 기능에 영향을 줄 수 있습니다.
> [Apple iOS 개인 정보 보호 변경이 이메일 마케팅에 미치는 영향에 대해 자세히 알아보세요](https://experienceleaguecommunities.adobe.com/t5/adobe-campaign-classic-blogs/the-impact-of-apple-ios-privacy-changes-on-email-marketing-and/ba-p/699780?profile.language=ko).
> 
> 보다 정확한 통찰력을 위해 오픈율 대신 클릭 및 전환 지표에 집중하는 것이 좋습니다.


>[!BEGINSHADEBOX]

캠페인에서 **[!UICONTROL 보고서]** 버튼을 클릭한 다음 **[!UICONTROL 모든 시간 보고서 보기]**&#x200B;를 선택하여 이메일 캠페인 보고서에 액세스할 수 있습니다. [자세히 알아보기](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## 이메일 KPI

![](assets/cja-email-kpis-unique.png)

**[!UICONTROL 이메일]** 주요 성과 지표(KPI)는 이메일 캠페인의 성과 및 참여 수준을 반영하는 고유한 집계된 지표로 구성된 집중 대시보드를 제공합니다.

+++ 이메일 KPI 지표에 대해 자세히 알아보기

* **[!UICONTROL 고유 클릭스루 비율]**: 배달된 고유 이메일 수와 비교하여 전자 메일에서 하나 이상의 링크를 클릭한 고유 프로필의 비율입니다.

* **[!UICONTROL 열람율(CTOR)]**: 메시지와 상호 작용한 프로필의 비율입니다.

* **[!UICONTROL 고유 열람율]**: 배달된 고유 이메일 수와 비교하여 이메일을 한 번 이상 연 고유 프로필의 비율입니다.

* **[!UICONTROL 고유 바운스 비율]**: 총 고유 전송 수를 기준으로 한 번 이상 반송된 고유 프로필의 비율입니다.

* **[!UICONTROL 배달됨]**: 보낸 총 메시지 수와 관련하여 보낸 전자 메일 수입니다.

* **[!UICONTROL 배달된 고유]**: 하나 이상의 메시지를 성공적으로 받은 고유 프로필 수입니다.

* **[!UICONTROL 예상 열기 수]**: 프로필의 직접 열기 수와 메일 서버에서 트리거된 자동 열기 수를 모두 설명하는 총 전자 메일 열기 수를 예측합니다. 이 지표는 전자 메일을 수동으로 연 수신자로부터 계산된 열기 비율을 메일 서버에서만 연 수신자에게 적용하여 개인 정보 보호 또는 보안 검색을 위해 메일 서버에서 트리거된 열기에 대해 조정합니다.

* **[!UICONTROL 고유 예상 열람수]**: 이메일을 열람했을 수 있는 고유 이메일 수신자 수를 예상합니다. 이 지표는 전자 메일을 수동으로 연 고유 프로필에서 계산된 고유 열람률을 메일 서버에서만 연 고유 프로필에 적용하여 개인 정보 보호 또는 보안 검색을 위해 메일 서버에서 트리거되는 개별 참여의 보다 정확한 수를 제공하는 것을 목표로 합니다.

* **[!UICONTROL 클릭 수]**: 동일한 프로필에서 여러 번의 클릭을 포함하여 메시지의 총 링크 클릭 횟수입니다.

* **[!UICONTROL 고유 클릭 수]**: 메시지에서 콘텐츠를 클릭한 고유 프로필 수입니다.

+++


## 고유 클릭 단계

![](assets/cja-email-click-funnel.png)

**[!UICONTROL 클릭 단계]** 그래프는 프로필이 이메일 콘텐츠와 어떻게 참여했는지 자세히 분석하여 게재에서 클릭에 이르기까지 상호 작용의 각 단계에 대한 중요한 통찰력을 제공하여 메시지가 사용자 참여를 얼마나 효과적으로 유도하는지 이해하는 데 도움이 됩니다.

+++ 클릭 단계 지표에 대해 자세히 알아보기

* **[!UICONTROL 고유 타깃팅]**: 전송 프로세스 중에 타깃팅된 고유 프로필 수입니다.

* **[!UICONTROL 고유 전송 수]**: 하나 이상의 전자 메일을 전송하려고 시도한 고유 프로필 수입니다.

* **[!UICONTROL 배달된 고유]**: 하나 이상의 메시지를 성공적으로 받은 고유 프로필 수입니다.

* **[!UICONTROL 고유 예상 열람 수]**: 이메일을 열람했을 수 있는 고유 이메일 수신자 수를 예상합니다. 이 지표는 전자 메일을 수동으로 연 고유 프로필에서 계산된 고유 열람률을 메일 서버에서만 연 고유 프로필에 적용하여 개인 정보 보호 또는 보안 검색을 위해 메일 서버에서 트리거되는 개별 참여의 보다 정확한 수를 제공하는 것을 목표로 합니다.

* **[!UICONTROL 고유 클릭 수]**: 메시지에서 콘텐츠를 클릭한 고유 프로필 수입니다.

+++

## 고유 게재 상태

![](assets/cja-email-delivery-status.png)

**[!UICONTROL 게재 상태]** 그래프는 캠페인에서 보낸 전자 메일과 관련된 데이터를 종합적으로 볼 수 있도록 해주며 게재 및 바운스 수와 같은 주요 지표에 대한 통찰력을 제공합니다. 이를 통해 이메일 전송 프로세스를 세부적으로 분석하여 캠페인의 효율성과 성능에 대한 중요한 정보를 제공할 수 있습니다.

+++ 게재 상태 지표에 대해 자세히 알아보기

* **[!UICONTROL 고유 전송 오류]**: 아웃바운드 프로세스 중에 하나 이상의 전송 오류가 발생한 고유 프로필 수입니다.

* **[!UICONTROL 배달된 고유]**: 하나 이상의 메시지를 성공적으로 받은 고유 프로필 수입니다.

* **[!UICONTROL 고유 송신 제외]**: 사전 정의된 규칙 또는 대상 기준으로 인해 메시지 수신에서 제외된 고유 프로필 수입니다.

* **[!UICONTROL 고유 바운스 수]**: 보내는 동안 하나 이상의 메시지가 반송된 고유 프로필 수입니다.

+++

## 게재됨 및 클릭 트렌드 {#delivered-click}

![](assets/cja-email-delivered-click.png)

**[!UICONTROL 게재됨 및 클릭 트렌드]** 그래프는 프로필과 전자 메일의 참여를 자세히 분석하여 프로필이 콘텐츠와 상호 작용하는 방법에 대한 중요한 통찰력을 제공합니다. 그래프는 두 축을 사용하여 전달된 이메일과 클릭을 나란히 표시하므로 전송된 이메일 수에 비해 비정상적인 패턴이나 참여 변화를 쉽게 발견할 수 있습니다.

+++ 게재됨 및 클릭 트렌드 지표에 대해 자세히 알아보기

* **[!UICONTROL 배달됨]**: 보낸 총 전자 메일 수와 관련하여 보낸 전자 메일 수입니다.

* **[!UICONTROL 클릭 수]**: 전자 메일에서 콘텐츠를 클릭한 횟수입니다.

+++

## 고유 전송 통계 {#unique-sending-statistics-email}

![](assets/cja-unique-email-sending-stat.png)

**[!UICONTROL 고유 전송 통계]** 표에는 캠페인의 고유한 전자 메일 성능 지표에 대한 자세한 개요가 나와 있습니다. 이메일이 대상자에게 도달하고 유도하는 방법에 대한 심층적인 통찰력을 제공하여 고유하게 타겟팅되거나, 전달되거나, 반송되거나, 제외되는 프로필과 같은 개별 프로필에 중점을 둡니다.

+++ 고유 전송 통계 지표에 대해 자세히 알아보기

* **[!UICONTROL 고유 타깃팅]**: 전송 프로세스 중에 타깃팅된 고유 프로필 수입니다.

* **[!UICONTROL 고유 전송 수]**: 하나 이상의 전자 메일을 전송하려고 시도한 고유 프로필 수입니다.

* **[!UICONTROL 배달된 고유 프로필]**: 하나 이상의 전자 메일을 성공적으로 받은 고유 프로필 수입니다.

* **[!UICONTROL 고유 바운스 수]**: 하나 이상의 전자 메일이 바운스로 연결된 고유 프로필 수입니다.

* **[!UICONTROL 고유 바운스 비율]**: 총 고유 전송 수를 기준으로 한 번 이상 반송된 고유 프로필의 비율입니다.

* **[!UICONTROL 고유 전송 오류]**: 아웃바운드 프로세스 중에 하나 이상의 전송 오류가 발생한 고유 프로필 수입니다.

* **[!UICONTROL 고유 송신 제외]**: 자격 규칙, 대상자 세분화 또는 프로필 상태로 인해 메시지 수신에서 제외된 고유 프로필 수입니다.

+++

## 고유한 추적 통계 {#unique-tracking-statistics-email}

![](assets/cja-unique-email-track-stat.png)

**[!UICONTROL 고유 추적 통계]** 표는 캠페인의 전자 메일에 대한 프로필 수준 참여를 중점적으로 볼 수 있습니다. 주요 참여 단계에서 개별 프로필이 이메일 콘텐츠와 상호 작용하는 방법에 대한 중요한 통찰력을 제공하는 고유한 지표를 강조 표시합니다.

+++ 추적 통계 지표에 대해 자세히 알아보기

* **[!UICONTROL 고유 클릭스루 비율(CTR)]**: 배달된 고유 전자 메일 수와 비교하여 전자 메일에서 하나 이상의 링크를 클릭한 고유 프로필의 비율입니다.

* **[!UICONTROL 고유 클릭스루 열람율(CTOR)]**: 고유 열람 수를 기준으로 이메일을 연 후 링크를 클릭한 고유 프로필의 비율입니다.

* **[!UICONTROL 고유 열람율]**: 배달된 고유 전자 메일 수와 비교하여 전자 메일을 한 번 이상 연 고유 프로필의 비율입니다.

* **[!UICONTROL 고유 클릭 수]**: 전자 메일에서 하나 이상의 콘텐츠를 클릭한 고유 프로필 수입니다.

* **[!UICONTROL 고유 예상 이메일 열람수]**: 이메일을 열람했을 수 있는 고유 이메일 수신자 수를 예상합니다. 이 지표는 전자 메일을 수동으로 연 고유 프로필에서 계산된 고유 열람률을 메일 서버에서만 연 고유 프로필에 적용하여 개인 정보 보호 또는 보안 검색을 위해 메일 서버에서 트리거되는 개별 참여의 보다 정확한 수를 제공하는 것을 목표로 합니다.

* **[!UICONTROL 고유 이메일 구독 취소]**: 이메일 또는 연결된 랜딩 페이지에서 구독 취소 링크를 클릭한 고유 프로필 수입니다.

+++

## 전송 통계 {#sending-statistics-email}

![](assets/cja-email-sending-stat.png)

**[!UICONTROL 전송 통계]** 표는 캠페인의 전자 메일에 대한 필수 데이터에 대한 포괄적인 요약을 제공합니다. 이메일과의 상호 작용 및 성공적으로 게재된 이메일 수와 같은 주요 지표를 자세히 설명하므로 이메일 및 캠페인의 효율성과 도달에 대한 중요한 통찰력을 제공합니다.

+++ 전송 통계 지표에 대해 자세히 알아보기

* **[!UICONTROL 타깃팅]**: 전송 프로세스 중에 처리된 총 전자 메일 수입니다.

* **[!UICONTROL 전송]**: 전자 메일의 총 전송 수입니다.

* **[!UICONTROL 배달됨]**: 보낸 총 메시지 수와 관련하여 성공적으로 보낸 총 전자 메일 수입니다.

* **[!UICONTROL 바운스 수]**: 보낸 총 메시지 수와 관련하여 보내는 프로세스 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL 바운스 비율]**: 총 보낸 전자 메일 수에 대한 바운스 결과를 가져온 전자 메일의 비율입니다.

* **[!UICONTROL 전송 오류]**: 전송 프로세스 중에 발생한 총 오류 수로 인해 프로필로 전송되지 않았습니다.

* **[!UICONTROL 제외 보내기]**: Adobe Journey Optimizer에서 제외된 총 프로필 수입니다.

+++

## 추적 통계 {#tracking-statistics-email}

![](assets/cja-email-track-stat.png)

**[!UICONTROL 전자 메일 - 추적 통계]** 표에는 캠페인에 포함된 전자 메일과 관련된 프로필 활동에 대한 자세한 계정이 있습니다. 여기에는 열람, 클릭 수 및 기타 관련 참여 지표에 대한 지표가 포함되며 프로필이 이메일 콘텐츠와 상호 작용하는 방식에 대한 포괄적인 보기를 제공합니다.

+++ 추적 통계 지표에 대해 자세히 알아보기

* **[!UICONTROL 클릭스루 비율(CTR)]**: 전자 메일과 상호 작용한 사용자의 비율입니다.

* **[!UICONTROL 클릭스루 열람율(CTOR)]**: 이메일을 연 횟수입니다.

* **[!UICONTROL 예상되는 전자 메일 열기 수]**: 프로필에 의한 직접 열기 수와 메일 서버에 의해 트리거된 자동 열기 수를 모두 계산하는 총 전자 메일 열기 수를 예측합니다. 이 지표는 전자 메일을 수동으로 연 수신자로부터 계산된 열기 비율을 메일 서버에서만 연 수신자에게 적용하여 개인 정보 보호 또는 보안 검색을 위해 메일 서버에서 트리거된 열기에 대해 조정합니다.

* **[!UICONTROL 클릭 수]**: 전자 메일에서 콘텐츠를 클릭한 횟수입니다.

* **[!UICONTROL 스팸 고객 불만]**: 메시지가 스팸 또는 정크로 선언된 횟수입니다.

* **[!UICONTROL 구독 취소]**: 구독 취소 링크 또는 연결된 랜딩 페이지의 클릭 수입니다.

+++

## 이메일 도메인 {#email-domains}

![](assets/cja-email-email-domains.png)

**[!UICONTROL 이메일 도메인]** 표에는 도메인별로 분류된 이메일에 대한 심층적인 분류가 있어 이메일 캠페인의 성능 지표에 대한 광범위한 통찰력을 제공합니다. 이 포괄적인 분석을 통해 이메일 콘텐츠에 대한 응답으로 다양한 도메인의 동작을 이해할 수 있습니다.

+++ 이메일 도메인 지표에 대해 자세히 알아보기

* **[!UICONTROL 배달된 고유 프로필]**: 하나 이상의 전자 메일을 성공적으로 받은 고유 프로필 수입니다.

* **[!UICONTROL 예상되는 전자 메일 열기 수]**: 프로필에 의한 직접 열기 수와 메일 서버에 의해 트리거된 자동 열기 수를 모두 계산하는 총 전자 메일 열기 수를 예측합니다. 이 지표는 전자 메일을 수동으로 연 수신자로부터 계산된 열기 비율을 메일 서버에서만 연 수신자에게 적용하여 개인 정보 보호 또는 보안 검색을 위해 메일 서버에서 트리거된 열기에 대해 조정합니다.

* **[!UICONTROL 고유 클릭 수]**: 전자 메일에서 하나 이상의 콘텐츠를 클릭한 고유 프로필 수입니다.

* **[!UICONTROL 고유 바운스 수]**: 하나 이상의 전자 메일이 바운스로 연결된 고유 프로필 수입니다.

* **[!UICONTROL 고유 전송 오류]**: 아웃바운드 프로세스 중에 하나 이상의 전송 오류가 발생한 고유 프로필 수입니다.

* **[!UICONTROL 고유 송신 제외]**: 자격 규칙, 대상자 세분화 또는 프로필 상태로 인해 메시지 수신에서 제외된 고유 프로필 수입니다.

+++

## 추적된 링크 레이블 {#track-link-label}

![](assets/cja-email-tracked-link.png)

**[!UICONTROL 추적된 링크 레이블]** 테이블은 이메일 내의 링크 레이블에 대한 포괄적인 개요를 제공하며 가장 높은 방문자 트래픽을 생성하는 레이블을 강조 표시합니다. 이 기능을 사용하면 가장 인기 있는 링크를 식별하고 우선 순위를 지정할 수 있습니다.

+++ 추적된 링크 레이블 지표에 대해 자세히 알아보기

* **[!UICONTROL 고유 클릭 수]**: 전자 메일의 콘텐츠를 클릭한 프로필 수입니다.

* **[!UICONTROL 클릭 수]**: 전자 메일에서 콘텐츠를 클릭한 횟수입니다.

+++

## 추적된 링크 URL {#track-link-url}

![](assets/cja-journey-tracked-link-urls.png)

**[!UICONTROL 추적된 링크 URL]** 테이블은 가장 높은 방문자 트래픽을 유도하는 전자 메일 내의 URL에 대한 포괄적인 개요를 제공합니다. 이를 통해 가장 인기 있는 링크를 식별하고 우선 순위를 지정할 수 있으므로 이메일의 특정 콘텐츠와 함께 프로필 참여를 보다 잘 이해할 수 있습니다.

+++ 추적된 링크 URL 지표에 대해 자세히 알아보기

* **[!UICONTROL 고유 클릭 수]**: 전자 메일의 콘텐츠를 클릭한 프로필 수입니다.

* **[!UICONTROL 클릭 수]**: 전자 메일에서 콘텐츠를 클릭한 횟수입니다.

+++

## 이메일 제목 {#email-subjects}

![](assets/cja-email-subject.png)

**[!UICONTROL 전자 메일 제목]** 표에는 가장 높은 방문자 트래픽을 가져온 전자 메일 제목에 대한 전체 개요가 나와 있습니다. 이 리소스는 대상 참여 역학에 대한 중요한 통찰력을 제공합니다.

+++ 이메일 주제 지표에 대해 자세히 알아보기

* **[!UICONTROL 고유 열람율]**: 배달된 고유 전자 메일 수와 비교하여 전자 메일을 한 번 이상 연 고유 프로필의 비율입니다.

* **[!UICONTROL 고유 예상 이메일 열람수]**: 이메일을 열람했을 수 있는 고유 이메일 수신자 수를 예상합니다. 이 지표는 전자 메일을 수동으로 연 고유 프로필에서 계산된 고유 열람률을 메일 서버에서만 연 고유 프로필에 적용하여 개인 정보 보호 또는 보안 검색을 위해 메일 서버에서 트리거되는 개별 참여의 보다 정확한 수를 제공하는 것을 목표로 합니다.

* **[!UICONTROL 열람율]**: 같은 프로필에서 여러 번 열람한 경우를 포함하여 게재된 총 이메일 수에 대한 이메일 열람율.

* **[!UICONTROL 예상되는 전자 메일 열기 수]**: 프로필에 의한 직접 열기 수와 메일 서버에 의해 트리거된 자동 열기 수를 모두 계산하는 총 전자 메일 열기 수를 예측합니다. 이 지표는 전자 메일을 수동으로 연 수신자로부터 계산된 열기 비율을 메일 서버에서만 연 수신자에게 적용하여 개인 정보 보호 또는 보안 검색을 위해 메일 서버에서 트리거된 열기에 대해 조정합니다.

+++

## 제외된 이유 {#excluded-reasons}

![](assets/cja-email-excluded.png)

**[!UICONTROL 제외된 이유]** 표에는 대상 대상에서 사용자 프로필을 제외하여 메시지가 수신되지 않는 다양한 요인에 대한 포괄적인 보기가 표시됩니다.

포괄적인 제외 이유 목록은 [이 페이지](exclusion-list.md)를 참조하세요.

## 바운스 이유 {#bounce-reasons-email}

![](assets/cja-email-bounce-reasons.png)

**[!UICONTROL 반송 이유]** 테이블은 반송된 메시지와 관련된 사용 가능한 데이터를 컴파일하여 이메일 반송 이면의 특정 이유에 대한 자세한 인사이트를 제공합니다.

바운스에 대한 자세한 내용은 [제외 목록](../reports/suppression-list.md) 페이지를 참조하세요.

## 오류 원인 {#error-reasons-email}

![](assets/cja-email-error-reasons.png)

**[!UICONTROL 오류 원인]** 표는 전송 프로세스 중에 발생한 특정 오류에 대한 가시성을 제공하여 오류의 특성 및 발생에 대한 중요한 정보를 제공합니다.
